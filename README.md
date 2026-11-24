# Vincit Turku Christmas Party Gala 2026

The invitation page for the Vincit Turku Christmas party on 4.12.2026 at the Turku Office.
It shows the schedule, the dress code and a link to the awards voting form.

The page is published with GitHub Pages:
https://suvikankare.github.io/vincitgala/

GitHub Pages publishes the `main` branch. A change is live a minute or two after it is merged.

## Files

| Path | Content |
| --- | --- |
| `index.html` | The page |
| `style.css` | All styles |
| `images/` | Icons and the background image |
| `fonts/` | The Comic Relief and Courier Prime fonts, with their licenses |
| `bells.mp3` | The music in the audio player |

The page is plain HTML and CSS. It has no build step and no dependencies to install.

## Run it on your computer

Start a web server in the repository folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser.

## Things to know before you change the page

- **Cursor effect.** The fairy dust cursor comes from the `cursor-effects` package on unpkg.com.
  The `<script>` tag has a fixed version and an `integrity` hash.
  If you change the version, you must also update the hash, or the browser does not run the script.
  To get the hash for a version, run:

  ```bash
  curl -sSL https://unpkg.com/cursor-effects@1.0.18/dist/browser.js | openssl dgst -sha384 -binary | openssl base64 -A
  ```

  Put `sha384-` in front of the output.
- **Fonts.** Only the Latin characters and the weights that the page uses are included:
  Comic Relief regular and bold, and Courier Prime bold.
  If you use another weight or style, add its file to `fonts/` and an `@font-face` rule to `style.css`.
- **Images.** Every `<img>` has `width` and `height` with the real size of the file.
  Keep them correct when you change an image.
- **Link preview.** The `og:` meta tags in `<head>` control the preview card in Teams, Slack and other apps.
  They use the full GitHub Pages address.
