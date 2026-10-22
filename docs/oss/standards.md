# RexCode Open Source standards

This is the shared presentation and community standard for RexCode Digital's Shopify developer tools. Product repositories carry their runnable, product-specific files; update those copies alongside this standard when it changes.

## Product identity and README

Use the family label “RexCode Open Source · Shopify developer tools”, followed by the product name and one factual sentence describing its task. Use the restrained palette `#22B8B2`, `#79DED9`, `#79BCE8`, dark neutrals and cool greys. Keep README content readable in GitHub light and dark themes. Do not imitate Shopify's logo or imply Shopify endorsement.

Keep this section order in each README:

1. Product identity and current status badges
2. Features
3. Install and run
4. GitHub Action
5. Example output
6. Supported capabilities and evidence
7. Limitations and privacy
8. Documentation
9. Related RexCode OSS tools
10. Contributing and support
11. Security
12. Licence and affiliation

Use current npm, CI, CodeQL, Scorecard, Node.js 22+ and licence badges where their sources are available. Avoid download counts, adoption claims and redundant badges. Examples must be runnable and output must come from the current CLI. Action examples must pin a released immutable commit SHA and state the release tag. List the package engine as Node.js `>=22`; the Action runtime is Node 24. Node 20 CI jobs are compatibility checks, not a support promise.

## Issue forms

Keep one YAML Issue Form for each supported report type. Request only information needed to reproduce or assess a report and remind people not to include merchant/customer data, credentials, tokens, private source, or production secrets.
Preserve valid repository triage labels when replacing forms; do not reference labels that do not exist.

- Bug: tool version; Node/npm versions; operating system; CLI or Action mode; reproduction; expected and actual results; optional sanitised output.
- Feature: problem and use case; proposed behaviour; Shopify evidence when applicable; compatibility and alternatives.
- Compatibility: tool version; Shopify API version and surface; operating system/runtime; official Shopify evidence; a minimal sanitised reproduction; expected and observed behaviour.

Keep vulnerability reporting as a repository-specific private security contact in `config.yml`. Do not solicit vulnerability details in public forms. Keep a separate support contact link.

## Contribution and support files

Use one PR template with Summary, Motivation, Changes, Tests performed, Compatibility, Security and privacy, Shopify source/evidence, Release impact and a concise checklist. Product-specific tests belong in that checklist.

Keep contribution terms accurate to each repository's licence. Document commands that actually exist in package scripts. State the solo-maintainer model without implying independent approval is required when branch protection does not require it. Contributors should review and understand changes they submit.

Keep `SECURITY.md` focused on private reporting, supported-version policy and scanner boundaries. Keep `SUPPORT.md` focused on safe reproductions and public support channels. Use the same baseline expectations in each `CODE_OF_CONDUCT.md` and keep its private contact route valid.

## Technical and release claims

Describe static analysis as evidence, not proof. Preserve each product's uncertainty states and API-version boundaries. Never claim App Store approval, compliance, security, or unused permissions are guaranteed.

Keep release and Action references aligned with the latest published package. A source change that is not in a release must be labelled as such. Do not publish a package for documentation, repository metadata, template, or CI-only changes. Keep immutable release tags intact.

The product repositories link back to this standard at [RexCode-Digital/.github](https://github.com/RexCode-Digital/.github/blob/main/docs/oss/standards.md). Update the standard and local implementations in the same review cycle.
