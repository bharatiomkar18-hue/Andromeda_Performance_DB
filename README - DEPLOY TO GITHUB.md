# Andromeda HTML Dashboard - GitHub Deployment Guide

This package publishes the dashboard as a static HTML page.

## What To Upload

Upload these files to the GitHub repository root:

- `index.html`
- `.nojekyll`
- `UPDATE FROM ANDROMEDA DASHBOARD.bat` is optional and is only for the laptop that runs Andromeda.

## First-Time GitHub Setup

1. Create a GitHub repository for the dashboard.
2. Keep the repository private/internal if shipment and tracking ID data should not be public.
3. Upload `index.html` and `.nojekyll` to the repository root.
4. Go to repository `Settings`.
5. Open `Pages` from the left menu.
6. Under `Build and deployment`, set `Source` to `Deploy from a branch`.
7. Select the branch, usually `main`, and folder `/root`.
8. Save.
9. Wait a few minutes and open the Pages URL shown by GitHub.

GitHub's docs describe Pages as static hosting for HTML/CSS/JavaScript files from a repository:
https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages

GitHub's quickstart shows the Pages branch deployment flow:
https://docs.github.com/en/pages/quickstart

## Daily Refresh

After the Andromeda BAT run:

1. Open `C:\Andromeda\Dashboard`.
2. Confirm `Andromeda_Dashboard.html` is updated.
3. Copy it into this GitHub package/repository folder.
4. Rename or overwrite it as `index.html`.
5. Commit/upload the changed `index.html` to GitHub.
6. Wait for GitHub Pages to refresh.

On the Andromeda laptop, you can use `UPDATE FROM ANDROMEDA DASHBOARD.bat` to copy the latest dashboard into this folder as `index.html`.

## Important Security Note

The dashboard can include latest tracking-ID drilldown data from `OverallReport.csv`. Do not publish this in a public repository unless the data is approved for public viewing.
