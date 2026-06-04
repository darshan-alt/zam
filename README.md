# Zamp — landing page

A static, single-page site built around one idea: a finance leader should *understand* Zamp in a sentence, *watch* it do a real job, and *see* the hire it hands back.

No build step, no framework, no dependencies. Just open `index.html`.

## What's interactive
- **The invoice-exception demo** (`#demo`) — auto-plays an end-to-end workflow and **pauses for one human approval click**, dramatising "the only human touch." Replayable.
- **The impact calculator** (`#calc`) — live sliders turn the visitor's volume into dollars, hours, and an FTE-equivalent ("the hires you won't make"), with a one-click **"Copy summary for your CFO."**

## File structure
```
.
├── index.html              # the page
├── assets/
│   ├── css/styles.css      # all styling + design tokens
│   ├── js/main.js          # demo, calculator, scroll reveals
│   └── favicon.svg
├── .nojekyll               # serve files as-is on GitHub Pages
└── README.md
```

## Deploy to GitHub Pages

1. Create a new GitHub repo and push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Zamp landing page"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: **main**, folder: **/ (root)**. Save.
5. Wait ~1 minute. Your site is live at `https://<you>.github.io/<repo>/`.

That's it — paths are all relative, so it works from a project subpath without changes. (For a root domain site, name the repo `<you>.github.io`.)

## Before you ship it for real
- **Swap the byline / claims for verified ones.** Customer names and quotes are taken from Zamp's existing public site; confirm before publishing.
- **Rebuild the calculator on real customer data.** The defaults (≈12 min/exception, 1,800 FTE-hours/yr) are illustrative placeholders — replace with figures you can defend.
- **Wire the CTAs** (`Watch Zamp work`, `Scope your first hire`) to your real demo-booking flow.
- Fonts load from Google Fonts via CDN; self-host them if you need full offline/privacy control.
