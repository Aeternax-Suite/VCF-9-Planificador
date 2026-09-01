# Contributing

Thanks for considering a contribution to the VVF/VCF 9 Planner — this project exists specifically to be improved by the VMware community, not to stay a one-person tool.

## Ways to contribute

- **Fix or improve a formula.** If you can point to official Broadcom/VMware documentation that corrects or refines a calculation (capacity, licensing, vSAN entitlement), open an issue with the source link, or a PR directly.
- **Update reference pricing.** Per-core prices and vSAN entitlements are estimates (Broadcom does not publish a public list) — if you have a more current or better-sourced reference figure, update the defaults in `index.html` and note your source in the PR description.
- **Add coverage.** Missing add-ons (Ransomware Recovery, Advanced Cyber Compliance, Private AI Foundation with NVIDIA, HCX standalone, etc.), a new edition, or a new comparison dimension are all welcome.
- **Translations.** The app ships with an ES/EN toggle built on a simple `I18N` dictionary object in `index.html` — adding a third language means adding one more object literal with the same keys.
- **Bug reports.** Screenshots, the input values you used, and what you expected vs. what you got are the fastest way to get a fix.

## Project constraints (please keep these)

- **Zero dependencies, single file.** `index.html` is intentionally self-contained (Google Fonts via CDN is the one exception). Please don't introduce a build step, a package manager, or a framework — the "open the file and it works" property is a feature.
- **No tracking, no backend.** Nothing in this app should phone home. The "Ask Claude" and "Search Google" boxes open new tabs to public sites; they do not call any API from within the page.
- **Formulas need a source.** Any change to the capacity or licensing math should link to the official documentation it's based on (Broadcom TechDocs, VMware.com) in the PR description, so the next person can verify it too.
- **Keep both languages in sync.** If you add or change a user-facing string, add it to both the `es` and `en` blocks of the `I18N` object.

## How to submit a change

1. Fork the repo and create a branch from `main`.
2. Make your change directly in `index.html`.
3. Open the file in a browser and sanity-check: does the app still calculate correctly with the default inputs, and with a few edge cases (e.g. 1 host, 1 socket, cores below the 16-core minimum)?
4. Open a pull request describing what changed and why, with a source link if it touches a formula or a price.

## Code of Conduct

This project follows the [Code of Conduct](./CODE_OF_CONDUCT.md) — please read it before participating.
