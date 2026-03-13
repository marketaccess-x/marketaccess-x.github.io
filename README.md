Market Access X — GitHub Pages Site
Live at: https://marketaccess-x.com (after DNS update)  
GitHub Pages URL: https://marketaccess-x.github.io
Repository Structure
```
marketaccess-x.github.io/
├── index.html              ← Main landing page (this file)
├── assets/
│   ├── hero.mp4            ← Hero video (add your file here)
│   └── hero-poster.jpg     ← Still frame shown before video loads
├── articles/
│   ├── index.html          ← Articles listing page (create later)
│   └── chokepoint-paradox.html  ← Individual article (create later)
├── reports/
│   └── (PDF files go here)
└── README.md
```
Setup Steps
1. Create the GitHub repository
Go to github.com/marketaccess-x
Create new repo named exactly: `marketaccess-x.github.io`
This triggers GitHub Pages automatically at the root domain
2. Add your files
```bash
git clone https://github.com/marketaccess-x/marketaccess-x.github.io
cd marketaccess-x.github.io
# Copy index.html and assets/ folder here
git add .
git commit -m "Initial site launch"
git push
```
3. Add the hero video
Place your video file at `assets/hero.mp4`
Recommended encoding: H.264, 1280×720 or 1920×1080, ~5–10MB
Create a still frame as `assets/hero-poster.jpg` (shown on mobile/slow connections)
If your video is large, consider hosting on a CDN and updating the `src` attribute
4. Enable GitHub Pages
Repo Settings → Pages → Source: "Deploy from a branch" → Branch: main → / (root)
Site goes live at https://marketaccess-x.github.io within ~2 minutes
5. Point your domain
At WordPress.com DNS (where marketaccess-x.com is registered):
Add A records pointing to GitHub Pages IPs:
```
  185.199.108.153
  185.199.109.153
  185.199.110.153
  185.199.111.153
  ```
Add CNAME record: `www` → `marketaccess-x.github.io`
In GitHub Pages settings, add custom domain: `marketaccess-x.com`
Enable "Enforce HTTPS" once certificate is issued (~10 minutes)
Adding Articles
Create HTML files in `/articles/` following the same color palette.
Link them from the articles grid in index.html by replacing:
```html
<a href="articles/chokepoint-paradox.html" class="article-read-link">Read →</a>
```
Adding PDFs
Place PDF files in `/reports/` and link directly:
```html
<a href="reports/report-name.pdf" target="_blank">Download Report</a>
```
