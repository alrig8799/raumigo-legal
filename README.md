# Raumigo – Legal Pages

Static website with the legal documents of the Raumigo iOS app.
Hosted via GitHub Pages.

## Pages

- `index.html` – Overview (German)
- `agb.html` – Terms and Conditions (German) – as of 16 May 2026 (Version `2026-05-16`)
- `datenschutz.html` – Privacy Policy (German) – as of 16 May 2026
- `privacy.html` – Privacy Policy (English) – as of 16 May 2026
- `impressum.html` – Legal Notice (German)
- `APPSTORE_TEXTS.md` – App Store metadata (DE / EN / ES)
- `Auftragsdatenverarbeitungsvertrag.pdf` – TelemetryDeck supplementary data-protection agreement (German – authoritative)

## Versioning & AGB Re-acceptance

The in-app Terms of Service (AGB) use `AGBConfig.currentVersion` (currently **`"2026-05-16"`**) to detect changes.
When this website's AGB text is changed substantively, bump the version constant in the app so users are prompted to re-accept.

The current AGB version **`2026-05-16`** introduces:
- §1: explicit indication that the provider is a natural person and **not currently** registered in the commercial register.
- §3c: rewording of the analytics paragraph – the optional usage statistics are now **off by default** and only sent after explicit consent.
- §7a: new clause on user behaviour and user-generated content (no infringement of third-party rights, no scanning of premises/objects/persons without authorization, no illegal/pornographic/violent content; provider may suspend usage in case of substantial violations; user indemnifies provider).
- §12: new clause on the Apple App Store (Apple is not party to the contract; Apple as third-party beneficiary for user-related provisions).
- §13: new precautionary clause on consumer rights and right of withdrawal – currently no statutory withdrawal right because the app is free; will apply automatically once paid features are introduced (§§ 312c ff., 327 ff., 312g, 355 BGB).
- §14: consumer dispute resolution – ODR-platform link removed because the EU Online Dispute Resolution platform was discontinued by the European Commission on 20 July 2025; only the national VSBG-statement (§ 36 VSBG) remains.

The privacy policy (Stand 16 May 2026) introduces:
- precautionary clause on third-country transfers (Section 9, Art. 44 et seq. GDPR);
- detailed list of technical and organisational measures (Section 10, Art. 32 GDPR);
- TelemetryDeck section split into 8.1 legal basis & consent (Art. 6(1)(a) GDPR + § 25 (1) TDDDG, default off), 8.2 transmitted data (now explicitly clarifying that pseudonymous data is still personal data per Art. 4(1) GDPR & Recital 26), 8.3 storage location, retention and deletion, 8.4 contractual safeguards (correctly described as a *data-protection supplementary agreement* – TelemetryDeck explicitly excludes Art. 28 / Art. 26 GDPR roles).

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
