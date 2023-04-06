# HAI Annual Report

This repo contains a Netlify-hosted static website for HAI's Annual Report.  The site is hosted under SWS's Netlify account. You can login to Netlify here: https://app.netlify.com/

- Netlify URL: https://hai-annual-report.netlify.app/
- Live Stanford URL: http://hai-annual-report.stanford.edu/

This repo hosts all annual report websites for each year in separate branches starting in 2022. Only one year's website is live at a time. In previous years the sites were hosted in their own repo's:
- [SU-SWS/hai-2021-annual-report](https://github.com/SU-SWS/hai-2021-annual-report)
- [SU-SWS/hai-2020-annual-report](https://github.com/SU-SWS/hai-2020-annual-report)

## Netlify Basics
- The Netlify site is directly connected to this repo through Github.
- When code is merged into the branch configured as the Netlify base/deploy branch for the site, Netlify deploys the code to the live site.
- The active year's website branch is configured as the Netlify base/deploy branch.
- The `/public` directory is where the static site files are (it is the `docroot` in other words).
    - The repo root is for Netlify configuration files.

### Making a new deployment
1. Fetch the latest code for the active year's branch
1. Create a new branch for your changes
1. Make changes
    - If supplied with new site files don't copy them over the existing files in the branch -- wipe the `/public` directory and replace with new files.
1. After making changes, commit them, push up to repo, and create a PR.
    - Make sure the PR is set to merge into the active year's branch (it should be by default).
1. Netlify will run a few tests on the PR and also create a preview URL.
    - Wait for tests/checks to pass and then inspect/review the preview briefly for basic QA.
1. Once the code is ready to deploy, squash and merge the PR into the active year's branch.
    - Whenever the active year's branch code is changed, it triggers a new deployment.

### Adding a new Annual Report site
1. Create a branch for the year of the Annual Report (e.g., `2022`)
1. Copy the `netlify.toml` and `lambda/.gitkeep` files from the most recent year's branch.
1. Create a new `/public` directory and copy the new site files in.
1. Push up the site.
1. In Netlify, change the deploy branch.
