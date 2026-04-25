# Raumigo – Legal Pages

Static website with the legal documents of the Raumigo iOS app.
Hosted via GitHub Pages.

## Pages

- `index.html` – Overview (German)
- `agb.html` – Terms and Conditions (German) – as of 25 April 2026
- `datenschutz.html` – Privacy Policy (German) – as of May 2026
- `privacy.html` – Privacy Policy (English) – as of May 2026
- `impressum.html` – Legal Notice (German)
- `APPSTORE_TEXTS.md` – App Store metadata (DE / EN / ES)

## Versioning & AGB Re-acceptance

The in-app Terms of Service (AGB) use `AGBConfig.currentVersion` (currently `"2026-04-25"`) to detect changes.
When this website's AGB text is changed substantively, bump the version constant in the app so users are prompted to re-accept.

The current AGB version **`2026-04-25`** introduces:
- New §3a "Größencheck / Visueller Quickcheck" – clarifies that the new visual size-check feature is a pure 3D visualization (no collision check, no pass / no-pass).
- New §3b "Kollisionsberechnung – Beta-Funktion" – explicitly classifies the full collision calculation (with rotation / optimisation search and pass / no-pass estimate) as a **Beta function**, including the LiDAR-based CarFit trunk scan, with explicit acknowledgement of false-positive / false-negative possibility, runtime variance and ongoing changes.
- Stand updated to *25. April 2026*.

The previous AGB version **`2026-06`** introduced:
- §5a: explicit catalogue of what the app does **not** evaluate (weight, centre of gravity, load capacity, grip, material behaviour, personnel deployment, slip/tip/fall/pinch/crush/impact hazards, load distribution, traffic / insurance / occupational-safety / accident-prevention requirements, execution risks).
- Explicit clause: *"In particular, risks of injury, health and property damage are not evaluated."*
- Wording upgrade in §6: *"on own responsibility and at own risk"* (instead of merely *"own responsibility"*).
- CarFit module (trunk / vehicle fit) explicitly included in the scope.

## Setup

1. Create a GitHub repository (e.g. `raumigo-legal`).
2. Push these files to the `main` branch.
3. **Settings → Pages → Source:** `main` / `/ (root)`.
4. Pages become available at `https://YOUR-USERNAME.github.io/raumigo-legal/`.
5. In App Store Connect:
   - **Privacy Policy URL:** `…/privacy.html` (English version, required by Apple)
   - Optional support URL linking to `index.html` as "legal information hub".

## Wording Guidelines (keep consistent!)

Raumigo positions itself as an **assistive tool for non-binding geometric estimation**, not as a guarantee or clearance system.

Preferred:
- "non-binding geometric estimate"
- "likely fits" / "likely does not fit"
- "geometric orientation suggestion"
- "check on-site yourself"

Avoid:
- "guaranteed", "safe", "optimal", "approved", "cleared"
- "calculates reliably", "ensures"
- Anything suggesting absolute correctness or that the app replaces on-site verification.
