# Autokart Automotives — Free Showroom TV Display

A zero-backend showroom slideshow for Autokart Automotives.

## What it does
- Reads the Autokart vehicle CSV feed.
- Automatically rotates through inventory.
- Rotates through each vehicle's photos.
- Refreshes inventory every 15 minutes.
- Designed for a 16:9 showroom TV in full-screen browser mode.
- No database, paid hosting, Node.js, or app installation is required.

## Important: why GitHub Pages + the Action are included
The supplied S3 CSV may not allow browser cross-origin (CORS) requests. To make the TV URL reliable, the included GitHub Action copies the CSV into this same website every 15 minutes. The TV therefore reads `data.csv` from the same website.

## One-time setup (free)
1. Create a free GitHub account.
2. Create a new public repository, for example `autokart-showroom-display`.
3. Upload the contents of this ZIP to the repository.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **GitHub Actions**.
6. The included workflow will publish the site.
7. Open the published Pages URL on the showroom TV and use the browser's full-screen mode.

Your TV will only need the final GitHub Pages URL.

## Updating
The GitHub Action runs every 15 minutes and also runs whenever the workflow is manually started. The TV page itself refreshes its local inventory every 15 minutes.

## If your CSV provider changes the feed
Edit `.github/workflows/update-feed.yml` and replace `FEED_URL`.

## TV tips
- Use landscape/16:9.
- Enable browser full-screen.
- Disable screen sleep / auto power-off.
- If the TV browser has a "keep screen awake" option, enable it.
