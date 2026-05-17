# Raumigo – Legal Pages

Static website with the legal documents of the Raumigo iOS app.
Hosted via GitHub Pages.

## Pages

- `index.html` – Overview (German)
- `agb.html` – Terms and Conditions (German) – as of 17 May 2026 (Version `2026-05-17`)
- `datenschutz.html` – Privacy Policy (German) – as of 17 May 2026
- `privacy.html` – Privacy Policy (English) – as of 17 May 2026
- `impressum.html` – Legal Notice (German)
- `APPSTORE_TEXTS.md` – App Store metadata (DE / EN / ES)
- `Auftragsdatenverarbeitungsvertrag.pdf` – TelemetryDeck supplementary data-protection agreement (German – authoritative)

## Versioning & AGB Re-acceptance

The in-app Terms of Service (AGB) use `AGBConfig.currentVersion` (currently **`"2026-05-17"`**) to detect changes.
When this website's AGB text is changed substantively, bump the version constant in the app so users are prompted to re-accept.

### `2026-05-17` (current)

Substantively changes the **TelemetryDeck consent flow**:
- The previous default-off toggle in onboarding was replaced by a **forced-choice screen with two equally weighted buttons** ("Share statistics" / "Don't share"). The "Accept and continue" button is locked until the user has actively picked one of the two.
- This makes consent an "unambiguous affirmative action" within the meaning of Art. 4 No. 11 / Art. 7 GDPR and conforms with EuGH "Planet49" (C-673/17). No pre-selection, no dark-pattern nudging (both buttons share the same size, colour and weight).
- Internally tracked via a new `mm.analytics.consentDecisionMade` flag (separate from `mm.analytics.consent`), so we can distinguish "never decided" from "actively declined".
- Wording in `agb.html` §3c, `datenschutz.html` 8.1, `privacy.html` 8.1 and the App-Store privacy section was synchronised to reflect the active-choice mechanism instead of "default off".
- Existing users who had already accepted version `2026-05-16` are sent through the onboarding once more so they make an explicit active choice.

### `2026-05-16`

- §1: explicit indication that the provider is a natural person and **not currently** registered in the commercial register.
- §3c: rewording of the analytics paragraph (later superseded by `2026-05-17`).
- §7a: new clause on user behaviour and user-generated content (no infringement of third-party rights, no scanning of premises/objects/persons without authorization, no illegal/pornographic/violent content; provider may suspend usage in case of substantial violations; user indemnifies provider).
- §12: new clause on the Apple App Store (Apple is not party to the contract; Apple as third-party beneficiary for user-related provisions).
- §13: new precautionary clause on consumer rights and right of withdrawal – currently no statutory withdrawal right because the app is free; will apply automatically once paid features are introduced (§§ 312c ff., 327 ff., 312g, 355 BGB).
- §14: consumer dispute resolution – ODR-platform link removed because the EU Online Dispute Resolution platform was discontinued by the European Commission on 20 July 2025; only the national VSBG-statement (§ 36 VSBG) remains.

The privacy policy (Stand 17 May 2026) includes:
- precautionary clause on third-country transfers (Section 9, Art. 44 et seq. GDPR);
- detailed list of technical and organisational measures (Section 10, Art. 32 GDPR);
- TelemetryDeck section split into 8.1 legal basis & consent (Art. 6(1)(a) GDPR + § 25 (1) TDDDG, **active choice required during onboarding** — no implicit default opt-in or opt-out), 8.2 transmitted data (now explicitly clarifying that pseudonymous data is still personal data per Art. 4(1) GDPR & Recital 26), 8.3 storage location, retention and deletion, 8.4 contractual safeguards (correctly described as a *data-protection supplementary agreement* – TelemetryDeck explicitly excludes Art. 28 / Art. 26 GDPR roles).

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
