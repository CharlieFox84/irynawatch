# Testing Guide - Iryna Watch

Before submitting a pull request from `dev` to `main`, verify the following:

## 🧪 Visual & Functional Checks

- [ ] Timeline cards render correctly across screen sizes
- [ ] Procedural motions are hidden by default; toggle reveals them smoothly
- [ ] Header structure is valid HTML and displays “Last updated” correctly
- [ ] Favicon appears in browser tabs
- [ ] GitHub Pages preview matches expected layout and content
- [ ] No console errors or broken links

## 🧼 Editorial Integrity

- [ ] Medical evaluations and key filings remain visible under `motion`
- [ ] Glossary entries (if present) reflect editorial restraint and clarity
- [ ] README files clearly describe branch roles and deploy logic

---

### 🧼 IrynaWatch CICD Workflow Summary

1. **Development Branch (`dev`)**
   - All updates—editorial, CSS/JS, infrastructure—are made here.
   - GitHub Pages is configured to build from `dev` for live testing.

2. **Testing & Review**
   - Visual and editorial checks are performed via GitHub Pages.
   - Procedural cards and hidden tags allow for quiet iteration.

3. **Merge to Production (`main`)**
   - Once tested, `dev` is merged into `main` with a clean commit history.
   - GitHub syncs the updated `main` branch.

4. **Netlify Auto-Deploy**
   - Netlify is linked to the `main` branch.
   - Every push triggers a fresh build and deploy to https://irynawatch.netlify.app/
   - Public-facing site updates automatically, preserving editorial restraint and technical polish.

---
