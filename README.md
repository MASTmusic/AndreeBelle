# Andrée Belle — GitHub Pages Website

A complete static website built with HTML, CSS, and JavaScript. No build tools or paid hosting are required.

## Preview it on your computer

Open `index.html` directly in a browser, or run a local server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Sign in to GitHub and create a new **public** repository. A clear name is `andree-belle-website`.
2. Upload everything inside this folder to the repository root. `index.html` must be at the top level, not inside another folder.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then click **Save**.
6. Wait a few minutes. GitHub will show the public `github.io` address on the Pages screen.

## Connect the GoDaddy domain later

Do this only after the GitHub Pages address is working.

1. In GitHub, go to **Settings → Pages → Custom domain** and enter `andreebelle.com`. Save it.
2. In GoDaddy DNS, remove conflicting Wix A and CNAME records.
3. Create four **A** records for host `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Create one **CNAME** record:
   - Host: `www`
   - Value: `YOUR-GITHUB-USERNAME.github.io`
5. Wait for DNS propagation. Return to GitHub Pages and enable **Enforce HTTPS** when it becomes available.

GitHub may automatically create a `CNAME` file after the custom domain is saved. Keep that file in the repository.

## Contact and lesson forms

The lesson intake form currently posts through FormSubmit to `andreebellemusic@gmail.com`. The first real submission triggers a one-time activation email. Open that email and confirm the form before public use.

To use Formspree instead, replace the form `action` in `index.html` with your Formspree endpoint, for example:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## Updating the site

- Text and links: edit `index.html`.
- Colors, spacing, and design: edit `styles.css`.
- Interaction and gallery lightbox: edit `script.js`.
- Images: add optimized JPG, PNG, or WebP files to `assets/images/`, then update the matching image path in `index.html`.

## Before launch

- Test every music, press, and social link.
- Submit the lesson form once and confirm delivery.
- Check the site on a phone and desktop.
- Replace or reorder any photos you prefer.
- Add upcoming dates to the Live section when available.
- Confirm that all images and music artwork are cleared for website use.
