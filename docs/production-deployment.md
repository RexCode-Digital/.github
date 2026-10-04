# RexCode production deployment procedure

This procedure covers the commercial Shopify applications hosted on Vercel:

| Product | GitHub repository | Production domain |
| --- | --- | --- |
| SpecDesk | `RexCode-Digital/specdesk` | `specdesk.rexcode.co.uk` |
| LotTrace | `RexCode-Digital/lottrace` | `lottrace.rexcode.co.uk` |
| ApproveLane | `RexCode-Digital/rexcode-proof` | `approvelane.rexcode.co.uk` |
| Belumi Loyalty | `RexCode-Digital/belumi-loyalty` | `belumi.rexcode.co.uk` |

## Deployment policy

- Pull requests use Vercel Preview deployments for review.
- `main` remains each project's production branch. A push to `main` may create a Vercel Production deployment, but Vercel's **Auto-assign Custom Production Domains** setting is disabled for all four projects. A new build therefore does not take over the customer-facing domains automatically.
- The current production domains remain attached to the last intentionally promoted deployment.
- An authorized Vercel project administrator must explicitly promote a reviewed build before it serves the production domains.

## Intentional production release

1. Merge the approved change to `main` through the repository's normal protected-branch process.
2. In Vercel, open the matching project and inspect the deployment for the exact merged commit. Confirm it is **Ready**, is a **Production** deployment, and passed the required repository checks.
3. Open the deployment's actions and choose **Promote to Production**. Confirm the target project and domains before completing the promotion.
4. Verify that the project lists the expected domains and that each domain serves the newly promoted deployment. Run the product's smoke checks and confirm the critical Shopify callback/authentication paths.
5. Record the release commit, deployment URL, promotion time, and verification outcome in the product's release record.

Do not promote Preview deployments, an unverified commit, or a deployment with failed checks. Do not disconnect a project or remove its production domains to control releases.

## Current platform account boundary

The Vercel projects currently reside in the `Efe's projects Pro` team. The production-domain promotion guard is in place, but Vercel project/team administration has not yet moved to a RexCode-controlled Vercel team. Resolve the account/team ownership separately, after confirming the plan and billing impact; keep existing project access and domains intact during that change.
