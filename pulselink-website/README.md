# PulseLink — marketing site

A static, no-build-step marketing site for PulseLink. Plain HTML/CSS/JS — no framework, no bundler. Open `index.html` in a browser or deploy the folder as-is to any static host (GitHub Pages, Netlify, Vercel).

## Structure

```
index.html      Homepage
about.html      Story, values, team, competitive landscape, funding model
contact.html    Contact form + info (form is front-end only, see below)
faq.html        FAQ accordion, grouped by audience
privacy.html    Privacy Policy (placeholder — needs legal review)
terms.html      Terms of Service (placeholder — needs legal review)
styles.css      Shared stylesheet for all pages
```

## Before this goes live

Search the codebase for the word **placeholder** — every instance flags something that needs a real answer before launch:

- **Team section** (`about.html`) — swap in real founders, roles, and bios. This is one of the highest-trust-impact sections on the site for something asking people to hand over medical records.
- **Traction stats** (`index.html`, `.traction` section) — replace `[X]` with real pilot numbers, or remove the section entirely until there's something to show.
- **Contact details** (`contact.html`) — the phone number was intentionally left as "available on request" rather than a fake number. Add a real one, or keep the current copy.
- **Privacy Policy & Terms** — solid starting drafts, but not lawyer-reviewed. Given this handles medical and insurance data, have them reviewed against Kenya's Data Protection Act (2019) before publishing.
- **Regulatory status** (`index.html` Trust section, `about.html` landscape section) — confirm and state actual ODPC registration and SHA/NHIF integration status.
- **Funding model** (`about.html`) — confirm real pricing before publishing the placeholder copy.

## Known limitations

- The contact form doesn't send email yet — wire it to Formspree, a serverless function, or your backend of choice.
- No Swahili translation yet — there's a "coming soon" badge on the homepage as a placeholder for that work.
- No analytics included.

## Local development

No build step required. Any static file server works, e.g.:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
