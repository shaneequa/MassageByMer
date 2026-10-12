# Massage by Mer — Website

A static HTML/CSS site for Massage by Mer (massagebymer.com), ready to push to GitHub and serve with GitHub Pages.

## Folder structure

```
massage-by-mer/
├── index.html          the whole site (one page, with anchor links)
├── css/
│   └── styles.css       all styling
├── images/
│   └── README-images.txt  notes on which photos to add, and where
└── README.md             this file
```

## Still needs to be filled in

Before this goes live, a few things in `index.html` are placeholders — search the file for these and update them:

- **Contact section** (`#contact`): phone number, email address, hours, and address are marked with `[Add ...]` text. Once you have them, you can also turn the commented-out `tel:` / `mailto:` links (right above the "Book Now" button) into working links, or point the button at your online booking system.
- **Photos**: the About and Parking sections currently show dashed placeholder boxes. Drop your images into the `images/` folder (see `images/README-images.txt` for suggested filenames and sizes), then replace each `<div class="image-placeholder">...</div>` with an `<img>` tag, e.g.:
  ```html
  <img src="images/meredith.jpg" alt="Meredith, massage therapist">
  ```
- **Additional policies**: only the fragrance-free policy was provided, and it's styled front-and-center as requested. If you want to add others (cancellation window, late arrival, intake forms, payment methods), there's a commented-out `.policy-item` template in the Policies section of `index.html` to copy.

## Deploying with GitHub Pages

1. Create a new repository on GitHub (e.g. `massage-by-mer`).
2. Upload the contents of this folder to the repo (drag-and-drop on github.com works fine, or `git init` / `git add .` / `git commit` / `git push` if you're using git locally).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to "Deploy from a branch," choose the `main` branch and the `/ (root)` folder, then save.
5. GitHub will give you a URL like `https://<yourusername>.github.io/massage-by-mer/`.
6. To use `massagebymer.com` instead: in the same **Settings → Pages** screen, add it under "Custom domain," then add a `CNAME` record at your domain registrar pointing to `<yourusername>.github.io` (GitHub's Pages documentation has the exact DNS records if you want to use an apex domain like `massagebymer.com` rather than `www.massagebymer.com`).

## Notes on the design

- Palette and type are earthy/warm on purpose: sage green, clay/terracotta, and cream, with a serif heading font (Cormorant Garamond) paired with a clean sans-serif body font (Nunito Sans) for a calm, professional feel.
- The fragrance-free notice sits in its own banner above the header on every page load, and is repeated in the Policies section, so it can't be missed.
- The page is a single `index.html` with in-page anchors (About / Services / Policies / Parking / Contact) rather than separate pages — simplest to maintain for a one-page business site, and works well with GitHub Pages out of the box.
