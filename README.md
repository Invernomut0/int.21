# Interrupt 21h — Cloudflare Pages website

Static website intended to provide the public-facing website, Privacy Policy, Terms of Service and data-deletion information for the Interrupt 21h TikTok integration.

## Before publishing

Replace every placeholder:

- `[INSERT LEGAL NAME]`
- `[INSERT PRIVACY EMAIL]`
- `[INSERT CONTACT EMAIL]`
- `[INSERT DATA-PRIVACY EMAIL]`
- `[INSERT REGISTERED ADDRESS OR COUNTRY, AS APPLICABLE]`
- `[INSERT GOVERNING LAW AND JURISDICTION]`

Do not submit the TikTok app with these placeholders still present.

## Structure

- `/index.html` — official website
- `/privacy.html` — Privacy Policy
- `/terms.html` — Terms of Service
- `/data-deletion.html` — data deletion request instructions
- `/styles.css` — shared styling
- `/assets/logo.png` — Interrupt 21h logo

## Cloudflare Pages

This is plain static HTML. No build step is required.

Cloudflare Pages settings:

- Production branch: `main`
- Build command: `exit 0`
- Build output directory: `/` (or the repository root)

After deployment, Cloudflare provides a `https://<project-name>.pages.dev` address.

Recommended project name:

`interrupt21h`

which should result in:

`https://interrupt21h.pages.dev`

If that project name is unavailable, choose another unique name such as `interrupt21h-app`.

## TikTok

Use:

Website URL:
`https://interrupt21h.pages.dev/`

Privacy Policy URL:
`https://interrupt21h.pages.dev/privacy.html`

Terms of Service URL:
`https://interrupt21h.pages.dev/terms.html`

Data deletion:
`https://interrupt21h.pages.dev/data-deletion.html`

For TikTok URL ownership verification, use TikTok Developer Portal → URL properties. If TikTok provides a verification/signature file for URL-prefix verification, place that exact file at the location TikTok specifies and redeploy.

## Important

The site is intentionally static. No TikTok access token, client secret or API credential belongs in these files. Keep secrets server-side/in environment variables in the actual application.

The legal text is a technical starting point, not legal advice. Review it with the actual operator/entity details and applicable law before production submission.
