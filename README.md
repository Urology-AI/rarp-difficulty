# RARP Surgical Difficulty Index (RSDI)

Interactive **preoperative assessment tool** for estimating surgical complexity in **robot-assisted radical prostatectomy (RARP)**.

The single-page app lives entirely in the browser – no backend, database, or build step required.

---

## Project structure

- `index.html`  
  Minimal landing page for GitHub Pages that immediately redirects to the main tool.

- `RARP_Difficulty_Index (2).html`  
  The full RSDI interface:
  - Domain-based checklist (anatomy, oncologic, tissue quality, prior procedures, radiation/ablation, bleeding risk)
  - Live total score out of 100, tier classification, and domain breakdown
  - Generated list of anticipated surgical challenges
  - Printable A4 summary report for charting or multidisciplinary review

All styling and logic are inlined; everything runs client-side.

---

## Local development

No tooling is required – you can simply open the HTML file in a browser:

1. Clone the repository.
2. Open `RARP_Difficulty_Index (2).html` directly in a modern browser (Chrome, Edge, Safari, Firefox).

If you prefer a local server (helpful for testing redirects like `index.html`):

```bash
cd rarp-difficulty
python -m http.server 8000
```

Then visit `http://localhost:8000/` in your browser.

---

## Deploying with GitHub Pages

1. **Push to GitHub**
   - Initialize git (if not already), commit `index.html` and `RARP_Difficulty_Index (2).html`, and push to a GitHub repo.

2. **Enable GitHub Pages**
   - In the GitHub repo, go to **Settings → Pages**.
   - Under **Source**, choose:
     - **Branch**: `main` (or your default branch)
     - **Folder**: `/ (root)`
   - Save.

3. **Access the tool**
   - After a short build, GitHub will give you a Pages URL, e.g.  
     `https://<username>.github.io/<repo>/`
   - That URL will load `index.html`, which immediately redirects to the RSDI interface.

---

## Intended use

- Prototype research instrument from the **Tewari Lab, Mount Sinai**.
- For **investigational and planning purposes only**.
- **Not** prospectively validated; **not** for diagnostic use.
- Clinical judgment **always supersedes** any calculated score.

