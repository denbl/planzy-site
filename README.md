# planzy.ai

The Planzy website: one landing page and two legal pages (`/privacy`, `/terms`). Plain HTML with no build step; images and fonts live in `assets/`.

## Deployment

- Netlify, project `planzy-ai` (AfterDot team). Every push to `main` deploys automatically.
- The canonical address is `planzy.ai`; `www.planzy.ai` redirects to it.
- `help.planzy.ai` is the former Intercom help center. Old article links from the app redirect to `/privacy` and `/terms` (`netlify.toml`).
- The "Powered by Netlify" badge is turned off in the project settings.

## DNS (GoDaddy)

- `@` A → `75.2.60.5`
- `www` CNAME → `planzy-ai.netlify.app`
- `help` CNAME → `planzy-ai.netlify.app`
- Do not touch MX, TXT (SPF, Google verifications), `s1/s2._domainkey` (SendGrid) or `_…acm-validations.aws`: email and the API certificate depend on them.

## Where things are

- The phone wall in the hero: the `.wall-cols` block in `index.html`. Five columns, three screens each; never put the same screen in neighbouring columns.
- The app is iOS only: every button links to `https://apps.apple.com/app/id6499276047`.
- The `/privacy` and `/terms` texts are based on the app's code (October 2026). Publisher: Artem Ptashnik, contact help@planzy.ai.
