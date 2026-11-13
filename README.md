# NASA Space Explorer

A single-page, browser-based space mission engineering and exploration game.

## Run locally

Open `index.html` in a modern browser. An internet connection is recommended because the current UI loads Tailwind CSS, Google Fonts, and mission-card placeholder images from public CDNs.

## Save data

The game stores the current mission in browser `localStorage` under `spaceExplorerSave`. Saves are local to the browser and device; they do not sync between devices or browsers.

## Publish with GitHub Pages

1. Create a **public** GitHub repository named `SPACE-EXPLORE-GAME`.
2. Upload `index.html` and `README.md` to the repository root (do not put them inside another folder).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then click **Save**.
6. Wait for GitHub Pages to finish publishing. The URL will be:
   `https://aalimv.github.io/SPACE-EXPLORE-GAME/`

No build command or backend server is required.

## Mars simulation changes in this deployment copy

- Mars now has a distinct saved state (`MARS_SIM`) instead of sharing the generic `EXPLORE` state.
- The Mars arrival action explicitly opens the Mars surface simulator.
- Loading a saved Mars mission restores the Mars surface simulator directly.
- Rover deployment, movement, objective completion, battery changes, and logs are saved locally.
- A Save button is available in the Mars surface HUD.
- The Firebase-only remote save dependency was removed for static hosting; browser-local saves are used instead.

## Deployment notes

- This is a static website and can be hosted on GitHub Pages.
- Local saves are not cloud saves. Clearing browser data or changing devices may remove/access a different save.
- Tailwind CSS, Google Fonts, and placeholder mission images are still loaded from external public services.
- The game should be manually tested at its published GitHub Pages URL after deployment, including the complete Mars arrival and rover flow.
