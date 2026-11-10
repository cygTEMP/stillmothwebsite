# stillmoth.com

Source for the Stillmoth website, hosted on Netlify.

- `index.html`: home page with the list of apps
- `privacy.html`: privacy policy for all Stillmoth apps, linking to each app's own policy
- `apps/<app>/index.html`: one page per app
- `apps/<app>/privacy/index.html`: that app's privacy policy, served at stillmoth.com/apps/<app>/privacy/ (use this URL in the app and its store listing)
- `apps/<app>/icon.png`: the app icon, 176 px square
- `style.css`: shared styles for every page

Plain HTML with no build step. Netlify publishes the repository root, so every push to `main` deploys the live site.

## Adding an app

1. Copy `apps/fijit/` to `apps/<new-app>/` and replace the icon, text and privacy details.
2. Add a row for it at the top of the apps list in `index.html`.
3. Add a link to its privacy page under "Each app" in `privacy.html`.

The security headers in `netlify.toml` only allow the site's own files and Google Fonts, so anything loaded from another site must be added there too.
