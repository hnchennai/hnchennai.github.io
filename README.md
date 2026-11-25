# Chess Coach website

The public website for the Chess Coach Android app: https://hnchennai.github.io/

- `index.html`: home page.
- `app-ads.txt`: the list of authorised ad sellers. It must stay at the top level of the site.
- `style.css`, `icon.png`: shared styles and the app icon.
- `c/index.html`: the page a friend challenge link (`/c/?c=<code>`) shows when the app is not installed: Google Play, and "Open in Chess Coach" (an Android intent link). With the app installed, Android App Links open the app instead.
- `.well-known/assetlinks.json`: lets Android open challenge links in the app (App Links). Its two fingerprints are PLACEHOLDERS: replace them with the SHA-256 certificate fingerprints from Play Console > Test and release > App integrity (the app signing key and the upload key), format `AB:CD:...`. Check with `curl -I https://hnchennai.github.io/.well-known/assetlinks.json` that it answers 200 and `application/json`.

Plain HTML and CSS. No build step, no trackers, no third-party requests.

App source code: https://github.com/hnchennai/chess-coach
