# Jezreal Momoh — Personal Portfolio (PF-04 refresh)

The PF-04 portfolio is a small static site that can be understood and deployed without a build system.

Live site: <https://jezreal-momoh-portfolio.netlify.app>

## Files

- `site/index.html` — page content, project links, dynamic contact form, and CV link.
- `site/styles.css` — colours, spacing, responsive layout, form styling, and focus states.
- `site/assets/jm-favicon.svg` — the browser-tab icon.
- `site/assets/Jezreal_Momoh_Backend_AI_Engineer_CV.pdf` — selected CV with a visible, clickable link to the live portfolio; review project and credential details before public release.
- `MAKE_IT_DO_SOMETHING.md` — Week 6 dynamic feature explainer (what a backend is, feature description, and step-by-step data flow).
- `evidence/empty-but-live-mobile-proof.png` — Week 4 evidence image; it is outside the deploy folder.

## Preview locally

Open `site/index.html` in a browser. No package install, build command, or server is required for this static page.

## Deploy after review

The live site was uploaded manually through Netlify. To publish updates, upload the `site/` folder from the existing site's Deploys page. Do not use Netlify Drop for later updates; that would create another site. `index.html` is at the deploy folder root. The contact section links to the 15-minute Calendly event.

The Git repository tracks `https://github.com/jezreal-dev/portfolio.git`, while production updates are deployed manually by uploading the `site/` folder on Netlify rather than continuous deployment hooks.
