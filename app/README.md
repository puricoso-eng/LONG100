# LONG100 – Garmin Longevity Score (PWA)

Installable, offline-ready calculator that rolls weekly Garmin metrics into a 0–100 score.

## Deploy on GitHub Pages
1. Create a new public repo (e.g., `LONG100`).
2. Add these files at the repo root: `index.html`, `service-worker.js`, `manifest.webmanifest`, icons, `privacy.html`.
3. Commit + push.
4. In **Settings → Pages**, set Source to **Deploy from a branch**, choose **main** and **/ (root)**.
5. Wait for the green check. Your site will be available at `https://<your-username>.github.io/LONG100/`.

## Make it installable
- HTTPS is required (GitHub Pages provides it).
- The manifest + service worker in this bundle already enable **Add to Home Screen**.

## Add AdSense
1. Create an AdSense account and add your site.
2. After approval, paste your **client ID** into the script tag in `index.html`:
   ```html
   <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
   ```
3. Create an ad unit and replace `data-ad-slot` in the provided ad block. Then remove the HTML comments to activate.
4. Keep a visible **Privacy Policy** (see `privacy.html`) and comply with consent laws (GDPR/CCPA where applicable).

## Customization
- RHR/HRV scoring can use your personal **baselines**.
- Optional **Body Fat %** swaps Body Battery out in the Lifestyle category.
- Edit footer ownership text in `index.html` if needed:
  `© 2025 Gabriel Purice. All rights reserved. LONG100™ is a trademark of Gabriel Purice.`

## Legal
- Copyright for the code and content © 2025 Gabriel Purice. All rights reserved.
- “LONG100” is used here as a brand name. Consider registering it as a **trademark** at the USPTO to protect the name and logo.
- This app provides general wellness insights and is **not medical advice**.

## Local testing
- Open `index.html` directly, or serve with a static server (`python -m http.server`).
- Service worker features (install prompt) work best over HTTPS or `localhost`.

---

Built with vanilla HTML/CSS/JS for simplicity.
