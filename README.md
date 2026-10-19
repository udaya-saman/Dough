# Dough Timing

A lightweight, mobile-first dough timing calculator designed for GitHub Pages and phone home-screen use. It runs without external libraries or a backend.

## Features

- Large native time picker designed for easy touch adjustment on phones.
- Calculates the starting time plus each category's duration.
- Editable hour and minute settings for Large, Medium, Small, Birizza, Cinnamon, and GD.
- Saves changed durations on the device so they remain after reopening the app.
- Reset-to-default button.
- Handles times that pass midnight and labels the next day.
- Progressive Web App setup with a web manifest and service worker for offline use after the first visit.

## Default durations

| Dough type | Hours | Minutes |
|---|---:|---:|
| Large | 2 | 40 |
| Medium | 2 | 10 |
| Small | 1 | 50 |
| Birizza | 1 | 15 |
| Cinnamon | 1 | 15 |
| GD | 2 | 30 |

## Publish on GitHub Pages

1. Create a GitHub repository (for example, `dough-timing`).
2. Upload **all files in this folder** to the repository's root. Keep `index.html`, `manifest.webmanifest`, `service-worker.js`, and `icon.svg` together.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose the `main` branch and `/(root)`, then save.
6. Open the published Pages URL on your phone.

GitHub Pages uses HTTPS, which is required for service-worker/offline functionality. If you update the app later, the service-worker cache version can be incremented in `service-worker.js` (change `dough-timing-v1`).

## Add it to your phone

- **Android / Chrome:** open the published URL, open the browser menu, and choose **Install app** or **Add to Home screen** if offered.
- **iPhone / Safari:** open the published URL, tap **Share**, then **Add to Home Screen**.

This is an installable web app (PWA), not a store-submitted native iOS/Android app. Its calculations work offline after the app has been loaded and cached once.
