# Relift website

Relift's lightweight, mobile-first website for the iPhone TestFlight beta. Static HTML and CSS only: no JavaScript, package manager, third-party assets, analytics, forms, cookies or build step.

## Contents

- `site/index.html`: page content, semantic HTML, metadata, and an **illustrative** workout concept (not a screenshot)
- `site/styles.css`: responsive layout, brand styling, keyboard focus, and reduced-motion support
- `site/relift-wordmark-reversed.svg`: exact Concept 08 v4 custom reversed wordmark SVG, sourced from `01_Logos/Vector_SVG/relift-wordmark-reversed.svg`. Use on navy backgrounds without adding a detached mark
- `site/favicon.svg`: exact v4 optical favicon from `03_Web/Favicons/favicon.svg`
- `site/favicon.png`: exact v4 48 × 48 favicon from `02_App/Expo/favicon.png` (identical to the v4 web export)
- `site/apple-touch-icon.png`: exact v4 **web** 180 × 180 touch icon from `03_Web/Favicons/apple-touch-icon.png`
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

- The primary and footer CTAs link directly to the [Relift iPhone beta on TestFlight](https://testflight.apple.com/join/KT2D6ewM); verify invite capacity and availability before public promotion.
- Replace the illustrative product preview with a verified in-app screenshot when ready; the concept is intentionally retained for now.
- Add a real canonical URL and an absolute `og:image` when a permanent domain and visual have been chosen.
- Add PR validation and browser checks in a future change; this branch intentionally keeps the existing deployment workflow.
- The source v4 **reversed custom wordmark SVG** is now used in both header and footer. Do not retype, distort, recolor, add a detached symbol, or lock marketing copy into the logo.
- Concept 08 v4 art is cleared for internal integration, not unconditional public release. The v4 wordmark master is itself a JPEG-derived traced path, so original-art/design approval and legal rights/trademark clearance remain public-release gates.
- Keep the static site and mobile application deployment separate.

## v4 asset provenance

Original pack: `Relift_Brand_Kit_v4_Release_Review.zip`, Concept 08 (October 2026).

| Website asset | Verified source Git blob SHA | Source SHA-256 |
| --- | --- | --- |
| `site/relift-wordmark-reversed.svg` | `f4ea5eef801c59621d1613325e6f9c3942516a32` | `d11f3887451084a3804a3278fe4001cb14bf2bd3644a8ecf41bd514e1f0a857f` |
| `site/favicon.svg` | `248461cb82fb21a723956828b809232a7bf95a8a` | `b05575c675ee894c9fab8f0ac04bf77c7f24cd929e87a04acd606715adeb57d5` |
| `site/favicon.png` | `47ddad3036ae19fed21bf841a10883aa063a9af2` | `56536dca52aaf7e808acd9b8fd455d4ca06573f4ad9b1c271117102ffce40083` |
| `site/apple-touch-icon.png` | `7c9c5274f38257395f78b417a92cca93c350fe85` | `d84aa492ccb6119ed558103c3c7ab0f843472e0df540533bf736407df35000c6` |

The Git blob SHAs and SHA-256 hashes for the wordmark SVG, website favicon SVG and 180px touch icon were computed from the uploaded original v4 ZIP and checked against the files created in GitHub. The 48px favicon matches the integrated v4 app export in `Mlara417/relift` and its existing source provenance manifest.

Brand direction: deep navy `#0E1721`, cyan `#00A3E0`, white, native system fonts for content, and calm, direct copy. The identity is the **original custom vector artwork**, not retyped text or a newly approximated mark.
