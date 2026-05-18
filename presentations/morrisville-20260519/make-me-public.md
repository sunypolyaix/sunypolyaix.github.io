# Make Me Public

Instructions for publishing this folder to the public AIX repository.

This folder lives in `aix-private`. Publishing means copying it into `aix` (the public repo), committing with a publication date, and pushing. That act is the publication event.

---

## Prerequisites

- The public `sunypolyaix/aix` repo exists with GitHub Pages enabled
- `aix/` is cloned locally alongside `aix-private/`
- The `talks-papers/` directory exists in the public repo
- `aix/index.html` lists talks-papers (update it when adding a new entry)

---

## Step 1 — Rename the private repo (once, first time only)

On GitHub: Settings → Repository name → rename `aix` to `aix-private`.

Do this last, after the new public `aix` repo is live, to avoid a gap in the URL.

---

## Step 2 — Prepare this folder for publication

Before copying, verify:

- [ ] `index.html` opens correctly in a browser (reveal.js loads, all tabs work)
- [ ] `README.md` is accurate and complete
- [ ] All source transcripts are in `conversations/`
- [ ] Draft versions are in `drafts/` with feedback in `drafts/feedback/`
- [ ] `query/how-to-query.md` has current starter prompts
- [ ] The closing slide URL in `index.html` points to the correct public GitHub Pages URL
- [ ] No private or sensitive content is present (check `.DS_Store` is in `.gitignore`)

---

## Step 3 — Copy to the public repo

```bash
# From the aix-private root
cp -r "people/steve/talks~papers/2026-05-morrisville-applied-ai-literacy" \
      "../aix/talks-papers/2026-05-morrisville-applied-ai-literacy"
```

Or drag the folder in Finder.

---

## Step 4 — Update the public index

In `aix/index.html`, add an entry to the talks-papers listing:

```html
<div class="artifact-card">
  <div class="artifact-title">
    <a href="talks-papers/2026-05-morrisville-applied-ai-literacy/">
      AI Literacy in Applied Contexts
    </a>
  </div>
  <div class="artifact-description">
    Faculty development talk, SUNY Morrisville, May 19, 2026.
    The compositional/directive distinction in AI literacy pedagogy;
    aviation failure modes mapped to applied programs; the dashboard
    is not the situation.
  </div>
  <div class="artifact-meta">
    <span class="meta-item"><span class="meta-label">Published:</span> [DATE]</span>
    <span class="meta-item"><span class="meta-label">Words:</span> ~900 (talk) / ~45,000 (corpus)</span>
    <span class="meta-item"><span class="meta-label">Type:</span> Talk + repo</span>
  </div>
</div>
```

---

## Step 5 — Commit and push

```bash
cd ../aix
git add talks-papers/2026-05-morrisville-applied-ai-literacy
git add index.html
git commit -m "publish: AI Literacy in Applied Contexts (Morrisville, May 2026)"
git push origin main
```

The commit date is the publication date. It is in the git log permanently.

---

## Step 6 — Verify

- Open `sunypolyaix.github.io/aix/talks-papers/2026-05-morrisville-applied-ai-literacy/`
- Confirm the presentation loads
- Confirm the transcript links resolve
- Update the closing slide URL in `index.html` if needed, recommit

---

## Notes

- Do not publish `conversations/` content that has not been reviewed for privacy
- The `.gitignore` in the root should exclude `.DS_Store`
- The token in `.git/config` should be removed before the private repo is shared with collaborators — use SSH or a credential helper instead
