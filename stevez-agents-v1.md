---
title: SteveZ — Six-Agent Master Specification
date: 2026-07-05
version: v1
type: artifact
artifact_type: architecture-spec
project: stevez
slug: stevez-agents-v1
status: draft
source: claude-conversation
capture_mode: live
model: claude-sonnet-4-6
---

# SteveZ — Six-Agent Master Specification

## Purpose

This document is the canonical definition of the six SteveZ agents. It defines what each agent owns, what it receives and from whom, and what it sends and to whom. All individual agent files (`orchestrator.md`, `context.md`, etc.) are derived from this document. When this document changes version, all agent files must be rederived.

## Design Principles

- One agent, one domain. No agent crosses into another's territory.
- The agent that knows does not act. The agent that acts does not decide.
- YAML frontmatter is the routing instruction. The pipeline reads it, not prose.
- Commit messages are generated from metadata, not typed by hand.
- Every artifact carries provenance: `capture_mode`, `model`, `session_id`.

---

## Pipeline Overview

```
Steve
  ↓ generates input (voice, URL, conversation)
Artifact
  ↓ produces YAML-frontmattered .md → writes to outbox/
Source
  ↓ enriches: normalizes URI, writes to Zotero, returns canonical identifier
Relevance
  ↓ validates: scores, routes (publish / hold / discard)
    ↑ consults Context for routing topology
Publication
  ↓ executes: cp → git add → git commit -m → git push → git status
    ↑ consults Context for destination path and repo
Orchestrator
  ↓ receives status report → logs → moves to next item
```

Context is consulted by Relevance and Publication. It does not initiate.

---

## Agents

---

### 1. Orchestrator

**Owns:** Direction — roadmap, daily log, session continuity, both tracks.

**Receives from:**
- Steve: session start signal, session end signal, blockers, decisions
- Publication: git status report per artifact (success / failure / path)
- All agents: completion signals and error reports

**Sends to:**
- All agents: task assignments and sequencing
- Steve: daily standup log, blockers identified, next actions per track

**Inputs (format):**
- Natural language from Steve
- Structured status reports from Publication: `{artifact, destination, status, timestamp}`

**Outputs (format):**
```markdown
## [YYYY-MM-DD]

**Track A (Pipeline)**
- [agent]: [what was built or decided]
- Blockers: [none | description]
- Next: [next action]

**Track B (Courses)**
- [course]: [content generated or needed]
- Blockers: [none | description]
- Next: [next action]
```

**Rules:**
- Orchestrator does not generate artifacts.
- Orchestrator does not push to git.
- Orchestrator does not score or route.
- Orchestrator logs every Publication status report before moving to next item.
- If Publication returns failure, Orchestrator holds the queue and surfaces to Steve.

---

### 2. Context

**Owns:** Topology — projects, courses, contributors, routing destinations, deployment map.

**Receives from:**
- Orchestrator: requests for routing targets
- Relevance: "where does this go?" query containing artifact YAML frontmatter
- Publication: "what is the local path and repo for this destination?" query

**Sends to:**
- Relevance: valid routing targets given artifact's `project:` and `type:` fields
- Publication: destination map — `{local_path, repo, branch, public_url}`

**Inputs (format):**
- Artifact YAML frontmatter (specifically `project:`, `type:`, `context:` fields)
- Registry file (`steves-registry.md`) — valid project keys and course keys

**Outputs (format):**
```yaml
destination:
  local_path: stevez/contexts/classes/216-111/
  repo: sunypoly-com216-fall26
  branch: main
  public_url: stevesunypoly.github.io/fall26-fys111com216/
```

**Routing topology (embedded — not a separate document):**

| Context | Local Path | Repo | Public URL |
|---|---|---|---|
| Personal AI infrastructure | `stevez/agents/` | `stevesunypoly/stevez` | none |
| Personal AI skills | `stevez/skills/` | `stevesunypoly/stevez` | none |
| AIX Center knowledge vault | `stevez/zettel/` | `sunypolyaix/zettel` | none |
| Shared scholarly bibliography | `stevez/aix-bibliography/` | `sunypolyaix/aix-bibliography` | none |
| FYS 111 & COM 216 Fall 2026 | `stevez/contexts/classes/216-111/` | `sunypoly-com216-fall26` | `stevesunypoly.github.io/fall26-fys111com216/` |
| IDT 555 Fall 2026 | `stevez/contexts/classes/555/` | `sunypoly-idt555-26fall` | `stevesunypoly.github.io/fall26-idt555/` |
| IDT 507 | `stevez/contexts/classes/507/` | TBD | TBD |
| STS 188 | `stevez/contexts/classes/188/` | TBD | TBD |
| Herkimer County AI | `stevez/contexts/aix-projects/herk/` | `sunypolyaix/aix-private` | none |
| TDAC Analytical Capabilities | `stevez/contexts/aix-projects/tdac-ac/` | `sunypolyaix/aix-private` | none |
| Cameroon AI Workshops | `stevez/contexts/aix-projects/cameroon/` | `sunypolyaix/aix-private` | `stevesunypoly.github.io/cameroon/` |
| Farmout archive | `stevez/contexts/misc-projects/farmout/` | `stevesunypoly/farmout` | `stevesunypoly.github.io/farmout/` |
| Zettelkasten methodology | `stevez/contexts/misc-projects/zettel-thinking/` | `stevesunypoly/stevez` | none |

**Rules:**
- Context does not generate artifacts.
- Context does not push to git.
- Context does not score or route — it only answers topology queries.
- When a new project or course is added, Context is updated first. All agents downstream inherit.

---

### 3. Source

**Owns:** Identity — canonical URIs, Zotero records, bibliography.

**Receives from:**
- Artifact: raw URL, DOI, ISBN, podcast URL, YouTube URL embedded in artifact YAML

**Sends to:**
- Artifact: canonical URI to write into `source_url:` or `source_archived:` field
- Relevance: enriched artifact with canonical source identifier attached
- Zotero: new or updated bibliographic record

**Inputs (format):**
- Raw URL string or DOI or ISBN from artifact YAML frontmatter

**Outputs (format):**
- Canonical URI string: `doi:10.xxxx/xxx` | `isbn:978xxxxxxxxxx` | `youtube://[video-id]` | `https://web.archive.org/web/[timestamp]/[url]`
- Zotero record (JSON via API)

**Domain-specific URI normalization rules:**
- DOI: validate and normalize via `doi.org` → `doi:10.xxxx/xxx`
- ISBN: validate via `isbnlib` → `isbn:978xxxxxxxxxx`
- YouTube: extract video ID → `youtube://[video-id]`
- Podcast (Overcast): extract episode path → `overcast://[episode-id]`
- arXiv: extract paper ID → `arxiv:[id]`
- GitHub: extract repo/file path → `github://[org]/[repo]/[path]`
- Web URL: check Wayback Machine → use archived URL as canonical

**Deduplication key hierarchy:** DOI → ISBN → URL-derived canonical URI

**System of record:** Zotero. Three equivalent input surfaces: API, desktop app, browser connector.

**Export formats:** JSON primary (Zotero API). BibTeX downstream compatibility only.

**Bibliography repo:** `sunypolyaix/aix-bibliography` — separate from all web-facing repos.

**Rules:**
- Source does not generate artifacts.
- Source does not score or route.
- Source does not push to git (bibliography repo is Publication's domain).
- If dedup check finds existing record, Source returns existing canonical URI — no duplicate created.

---

### 4. Artifact

**Owns:** Generation — zets, podshares, webzets, convos, session artifacts.

**Receives from:**
- Steve: raw input via skills (`//zet`, `//webzet`, `//podshare`, `//convo`)
- Orchestrator: task assignment (e.g. "generate zet from this session excerpt")

**Sends to:**
- Source: raw URL/DOI/ISBN extracted from generated artifact for normalization
- Relevance: completed artifact with full YAML frontmatter, written to outbox/
- Outbox: `stevez/outbox/[YYYY-MM-DD]-[slug].md` (local staging, not committed)

**Inputs (format):**
- Conversation text, voice annotation, URL, structured form data from Steve via skills

**Outputs (format):**
YAML-frontmattered `.md` file with required provenance fields:

```yaml
---
title: [5 words max]
date: [YYYY-MM-DD]
type: [zet | podshare | webzet | convo | artifact]
status: draft
project: [registry key]
source_url: [raw URL if applicable]
source_archived: [canonical URI from Source agent]
capture_mode: [live | post-hoc]
model: claude-sonnet-4-6
session_id: [session identifier]
---
```

**Skills operated:**
- `//zet` — atomic idea from conversation
- `//webzet` — web article capture with Wayback archive
- `//podshare` — podcast episode capture
- `//convo` — session conversation summary
- `//artifact` — named project deliverable

**Rules:**
- Artifact writes to outbox/, not directly to destination.
- Artifact does not push to git.
- Artifact does not score or route.
- Artifact does not normalize URIs — it passes raw URLs to Source.
- Every output must carry `capture_mode`, `model`, and `session_id`.

---

### 5. Relevance

**Owns:** Validation — scoring, curation gate, routing decision.

**Receives from:**
- Artifact: completed artifact from outbox/ with full YAML frontmatter
- Source: canonical URI confirmation

**Sends to:**
- Publication: artifact with routing decision attached (`publish` | `hold`)
- Orchestrator: `discard` decisions with reason
- Steve (via Orchestrator): `hold` items requiring review

**Inputs (format):**
- `.md` file from outbox/ with full YAML frontmatter

**Outputs (format):**
Same `.md` file with routing decision appended to frontmatter:
```yaml
relevance_score: [1-5]
routing_decision: [publish | hold | discard]
routing_reason: [one sentence]
```

**Three validation questions per artifact:**
1. Is this substantive? (signal vs. noise)
2. Is this unique? (duplicate check against vault — match on title + project + date)
3. Is this routable? (project or course key maps to a known Context destination)

**Three decisions:**
- **Publish** — pass to Publication with routing target from Context
- **Hold** — flag for Steve's review; surface via Orchestrator
- **Discard** — low signal or duplicate; log reason; notify Orchestrator

**Emergent concept detection:**
When a podshare dynamic pair or webzet connection contains a concept not yet in the vault, Relevance flags it: `[NEW CONCEPT CANDIDATE: X — generate //zet?]` and surfaces to Orchestrator.

**Rules:**
- Relevance does not generate artifacts.
- Relevance does not push to git.
- Relevance consults Context for routing topology — does not maintain its own map.
- Relevance never discards without logging reason.

---

### 6. Publication

**Owns:** Execution — git operations, multi-format output, deployment.

**Receives from:**
- Relevance: artifact with `routing_decision: publish` and routing target
- Context: destination map — `{local_path, repo, branch, public_url}`

**Sends to:**
- Orchestrator: git status report `{artifact, destination, commit_hash, status, timestamp}`
- Downstream repos: committed and pushed artifacts

**Inputs (format):**
- `.md` file from outbox/ with `routing_decision: publish`
- Destination map from Context

**Outputs (format):**
- Committed file at destination
- Status report:
```yaml
artifact: [slug]
destination: [local_path]
repo: [github-repo]
commit_hash: [sha]
status: [success | failure]
timestamp: [ISO-8601]
error: [null | description]
```

**Git operation sequence:**
```bash
cp outbox/[artifact].md [local_path]/
git add .
git commit -m "[auto-generated from YAML]"
git push
git status
```

**Commit message auto-generation from YAML:**
```
pub: [project] [type] — [title] [date]
```
Example: `pub: com216 zet — founding-optimism 2026-07-04`

**Multi-format output targets:**
- `.md` → vault, course sites, zettel
- `.html` → GitHub Pages course sites (Jekyll build)
- `.bib` → `aix-bibliography` repo
- slide fragments → course site `_slides/` directory

**Rules:**
- Publication executes git — no other agent touches git.
- Publication does not score or route — it only executes what Relevance decided and Context mapped.
- On git failure: report to Orchestrator with error, do not retry automatically.
- On success: remove artifact from outbox/ after confirming commit.

---

## Version History

| Version | Date | Changes |
|---|---|---|
| v1 | 2026-07-05 | Initial specification |

## Rederivation Protocol

When this document is updated to a new version:
1. Open `stevez/` in Claude Code
2. State: "Rederive all six agent files from stevez-agents-v[N].md"
3. Claude Code reads master spec, rewrites each agent file
4. Commit: `spec: rederive agents from stevez-agents-v[N]`
5. Old master spec version remains in `agents/` as reference
