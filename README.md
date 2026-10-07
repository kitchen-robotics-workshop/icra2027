# Now and Future of Kitchen Robotics

A complete static workshop website for the proposed full-day ICRA 2027 workshop. No installation or build step is needed. All styling and navigation are inside `site/index.html`; the page also works without JavaScript.

## Preview

Open `site/index.html` in a browser. Alternatively, from this directory run `python3 -m http.server 8000 --directory site` and visit http://localhost:8000.

## Publish with GitHub Pages

1. Create a public GitHub repository named `kitchen-robotics-icra2027`, with `main` as its default branch.
2. Upload the contents of this folder to the repository root. The repository should contain `README.md`, `site/index.html`, `site/.nojekyll`, and `.github/workflows/pages.yml`. Do not upload the ZIP itself or nest these under an extra parent folder. Some file pickers hide dot-directories; check that the workflow is present on GitHub.
3. Open repository **Settings → Pages**. Under **Build and deployment**, select **GitHub Actions** as the source.
4. Open **Actions → Publish workshop website → Run workflow**, selecting `main`. Future pushes to `main` deploy automatically.
5. After the workflow succeeds, the deployment link appears in **Settings → Pages** and the workflow summary. For this repository name, the usual address is `https://YOUR-USERNAME.github.io/kitchen-robotics-icra2027/`.

If uploading hidden folders is awkward, upload `site/index.html` and `site/.nojekyll` first, then use **Add file → Create new file** with the exact name `.github/workflows/pages.yml` and paste the provided workflow. No personal access token is needed for the workflow.

The workflow follows GitHub's official static-site Pages setup: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages.

## Edit the website

Use GitHub's pencil button on `site/index.html`. Search for a section heading or organizer name, edit, and commit to `main`.

- Update proposal status in the hero, page title, description, and footer after acceptance.
- Add the confirmed workshop date and room to the hero facts.
- The speaker cards and individual program slots are tentative. Update their status only after participation is confirmed. Lining Yao’s topic is a proposed discussion focus, not an agreed talk title. The chef is unnamed.
- Fumiya Iida is listed at the University of Tokyo, as verified against its current faculty directory.
- Verify that Yi Zhang's supplied organizer email should be the public contact address.
- Finalize the submission dates, platform, reference allowance, archival policy, and presentation format. Replace the announcement with a working submission link once submissions open.
- Finalize the program. The source contains two incompatible timetable versions; this site uses the detailed version as an illustrative draft. The chef slot is provisionally 16:10–16:40 and Josie Hughes follows at 16:40–17:10; all allocations are subject to confirmation.
- Organizer and speaker portraits are bundled in `site/images/`. Profile and photo-source links are intentionally omitted from the website. See `PHOTO_SOURCES.md` for internal provenance, and replace portraits with approved images when supplied.

The website labels proposed speaker candidates as tentative throughout. It does not claim workshop acceptance. No unofficial IEEE logos or invented photographs are included.

## Files

| Path | Purpose |
| --- | --- |
| `site/index.html` | Entire responsive website, including CSS and a small mobile-menu script |
| `site/.nojekyll` | Prevents Jekyll processing when using a branch-based deployment |
| `.github/workflows/pages.yml` | Automatic deployment of the `site` folder on pushes to `main` |
| `README.md` | Preview, publishing, and editing instructions |

Only `site/` is deployed, so these instructions are not part of the public website. No tracking, forms, third-party scripts, external fonts, or runtime dependencies are required.
