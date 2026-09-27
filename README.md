# KAZERA — GitHub Pages Deployment

## Folder structure
```
kazera-website/
├── index.html              ← the whole site (HTML+CSS+JS)
└── assets/
    └── images/
        ├── logo.png         ← your logo (already added)
        └── products/        ← drop product photos here
```

## Deploy in 3 steps
1. Create a new GitHub repository and upload this **entire folder** (keep `index.html` at the repo root, don't rename the `assets` folder).
2. Go to **Settings → Pages**, set Source to the `main` branch, root folder, and save.
3. Your site goes live at `https://<your-username>.github.io/<repo-name>/`.

## Adding images — no code edits, ever
- **Logo / favicon**: replace `assets/images/logo.png` with your own file, keeping the exact same filename.
- **Product photos**: drop a file into `assets/images/products/` (e.g. `tshirt1.jpg`), then in **Admin → Products → Image Path**, type `assets/images/products/tshirt1.jpg`. If a photo is missing, the product card automatically falls back to a placeholder icon instead of breaking.

All paths in the code are **relative** (no leading `/`), so the site works correctly whether it's hosted at the root domain or in a `/repo-name/` subfolder — which is exactly how GitHub Pages serves project sites.

## Notes
- The site's "database" (products, orders, reviews, settings) lives in the visitor's browser local storage. It's fully functional for testing, but admin edits won't sync across different visitors' devices — that requires a real backend.
- Admin panel: open `#/admin` on the live URL. Default password is `kazera123` (change it under Admin → Settings).
