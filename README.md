# Relift website

Relift's lightweight, mobile-first website for the iPhone TestFlight beta. Static HTML and CSS only: no JavaScript, package manager, third-party assets, analytics, forms, cookies or build step.

## Contents

- `site/index.html`: page content, semantic HTML, metadata, and an **illustrative** workout concept (not a screenshot)
- `site/styles.css`: responsive layout, brand styling, keyboard focus, and reduced-motion support
- `site/favicon.png`: **byte-for-byte Concept 08 v4 favicon**, copied from `Mlara417/relift/src/assets/images/favicon.png` (48 × 48)
- `site/apple-touch-icon.png`: **byte-for-byte Concept 08 v4 app icon**, copied from `Mlara417/relift/src/assets/images/icon.png` (1024 × 1024)
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
- The original v4 **custom wordmark SVG** is not currently committed to either repository, and raw source ZIP extraction was unavailable from Library. The temporary invented cyan-period treatment is removed, leaving plain text `Relift` as a noncanonical fallback. **Replace this with the exact `01_Logos/Vector_SVG` wordmark export from the original v4 pack** before claiming full website logo fidelity; do not trace or recreate it.
- Concept 08 v4 artwork is cleared for internal integration, not unconditional public release. Complete designer and rights signoff before treating it as fully approved.
- Keep the static site and mobile application deployment separate.

## v4 asset provenance

Original pack: `Relift_Brand_Kit_v4_Release_Review.zip`, Concept 08 (October 2026).

| Website asset | Verified source Git blob SHA | Source SHA-256 |
| --- | --- | --- |
| `site/favicon.png` | `47ddad3036ae19fed21bf841a10883aa063a9af2` | `56536dca52aaf7e808acd9b8fd455d4ca06573f4ad9b1c271117102ffce40083` |
| `site/apple-touch-icon.png` | `4bfa7b3b1f0d4b424f5ed2783a10e079b2e75285` | `506cb7df60180f792033ef109c76b66f4710dd5688be9f5c3600e45711a9fe9b` |

GitHub verified each binary blob has the **identical Git SHA-1** as the checked-in source file. SHA-256 values are from `Mlara417/relift/docs/brand/asset-provenance-v4.json`.

Brand direction: deep navy `#0E1721`, cyan `#00A3E0`, white, system fonts for body content, and calm, direct copy. The **logo remains custom vector artwork**; don't represent the current fallback text as the official wordmark.
