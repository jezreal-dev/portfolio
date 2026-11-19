# Jezreal Momoh — Personal Portfolio (PF-04 refresh)

The PF-04 portfolio is a small static site that can be understood and deployed without a build system.

Live site: <https://jezreal-momoh-portfolio.netlify.app>

## Files & Deliverables

- `site/` — deployable static website folder (HTML, CSS, assets, CV, favicon, robots.txt, sitemap.xml).
- `site/index.html` — page content, project links, dynamic contact form with honeypot, verified FlyRank Graduate badge, and CV link.
- `site/styles.css` — typography, colors, spacing, responsive layout, form styling, and badge styling.
- `site/assets/og-card.png` — verified 1200x630 social preview card.
- `site/assets/Jezreal_Momoh_Backend_AI_Engineer_CV.pdf` — verified Backend AI Engineer CV.
- `BREAK_YOUR_OWN_SITE.md` — Week 9 Checkpoint 2 hardening audit (5 fix-nows + 5 known limitations).
- `Break_Your_Own_Site_Jezreal_Momoh.pdf` — official submission PDF for Break Your Own Site.
- `HOW_TO_ADD_A_CASE_STUDY.md` — Week 9 keep-building 30-minute protocol to add new case studies.
- `Impact_Project_Portfolio_Habit_Jezreal_Momoh.pdf` — official submission PDF for the keep-building habit.
- `MAKE_IT_DO_SOMETHING.md` — Week 6 dynamic feature explainer (backend definition, feature breakdown, data flow).
- `Make_It_Do_Something_Jezreal_Momoh.pdf` — official submission PDF for Make It Do Something.
- `SURVIVE_THE_CRIT.md` — Week 7 design review critique feedback and actions.
- `MOBILE_FIX_LOG.md` — Week 7 mobile viewport and touch audit log.
- `evidence/empty-but-live-mobile-proof.png` — Week 4 evidence image.

## Master Directory Across Both Tracks
To view all assignments across both Backend AI Engineering and General AI Fluency, see:
[`../ASSIGNMENTS_DIRECTORY.md`](../ASSIGNMENTS_DIRECTORY.md)

## Preview locally

Open `site/index.html` in a browser. No package install, build command, or server is required for this static page.

## Deploy after review

The live site was uploaded manually through Netlify. To publish updates, upload the `site/` folder from the existing site's Deploys page. Do not use Netlify Drop for later updates; that would create another site. `index.html` is at the deploy folder root. The contact section links to the 15-minute Calendly event.

The Git repository tracks `https://github.com/jezreal-dev/portfolio.git`, while production updates are deployed manually by uploading the `site/` folder on Netlify rather than continuous deployment hooks.
