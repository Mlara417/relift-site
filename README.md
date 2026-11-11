# Relift website

Relift's lightweight, mobile-first coming-soon splash page. Static HTML and CSS only: no JavaScript, package manager, third-party assets, analytics, forms, cookies or build step.

## Contents

- `site/index.html`: page content, semantic HTML, metadata, and an **illustrative** workout concept (not a screenshot)
- `site/styles.css`: responsive layout, brand styling, keyboard focus, and reduced-motion support
- `site/favicon.svg`: temporary letterform, not Relift's finalized icon
- `.github/workflows/pages.yml`: deploys **only** the `site/` directory to GitHub Pages

## Deploy via GitHub Pages

1. Merge the splash-page pull request to `main`.
2. In **Settings → Pages → Build and deployment**, choose **GitHub Actions** as the source.
3. Under **Actions**, open **Deploy Relift splash page**. Run the workflow manually if a run was not triggered by the merge.
4. Check the deployment job for the actual Pages URL.

For this repository, the expected default URL is https://mlara417.github.io/relift-site/ (once enabled).

**Visibility:** This repository was private at setup. GitHub Pages on private repositories depends on your account/plan; publishing a public landing page is simplest with a public repository. Review repository visibility and Pages availability before deploying.

## Preview locally

```sh
python3 -m http.server 8000 --directory site
```

Open http://localhost:8000/.

## Launch checklist

- Select a real signup provider before adding a waitlist CTA. The present **Explore Relift** button scrolls to benefits and does not claim to collect signups.
- Replace the illustrative product preview with a verified in-app screenshot if desired.
- Add a real canonical URL and an absolute `og:image` when a permanent domain and visual have been chosen.
- Replace the temporary lettermark favicon with the approved app mark when finalized.
- Keep the static site and mobile application deployment separate.

Brand direction: deep navy `#0E1721`, cyan `#00A3E0`, white, system fonts, and calm, direct copy.
