# Personal Site — GitHub Pages Starter

A minimal, fast static site with an About, Projects, and placeholders for **Resume** and **CV**.

## Quick Start
1. **Create a new repo** on GitHub (e.g., `ethan-website`).
2. Upload all files and commit to `main`.
3. Go to **Settings → Pages**:
   - **Source:** `GitHub Actions` (recommended; workflow provided), or
   - **Deploy from a branch** and pick `main` and `/ (root)`.
4. Visit the Pages URL GitHub shows you.

### Editing
- Update content in `index.html`.
- Tweak styles in `assets/css/styles.css`.
- Add PDFs `assets/resume.pdf` and/or `assets/cv.pdf` and uncomment the `<iframe>` embeds in `index.html`.
- Replace `mailto:you@example.com` in the contact form with your email.

### Local Preview
```bash
python3 -m http.server 8080
```
Open http://localhost:8080
