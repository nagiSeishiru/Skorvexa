# Skorvexa – Canli Skor · website

Static website for the Skorvexa iPhone app (App Store id `6826925784`): home, privacy policy, terms and support, in the app's dark theme. Plain HTML and CSS: no build step, no dependencies, no tracking.

| Page | Path |
| --- | --- |
| Home | `/` |
| Privacy Policy | `/privacy/` |
| Terms & Conditions | `/terms/` |
| Support | `/support/` |
| Not found | `404.html` |

## Deploy

Pick one. Each serves this repository's root as-is.

- **Vercel**: import the repo, framework preset *Other*, leave build command and output directory empty. `vercel.json` adds trailing-slash redirects and security headers.
- **Netlify**: import the repo; `netlify.toml` publishes the root with no build. `_headers` sets security and cache headers. Netlify Drop also works (drag this folder).
- **GitHub Pages**: Settings → Pages → *Deploy from a branch* → `main` / `(root)`. `.nojekyll` turns off Jekyll. All links are relative, so it also works at `https://<user>.github.io/<repo>/`.

## After deploying

1. Replace the placeholder support e-mail in `support/index.html` (marked `TODO(release)`).
2. Give the app the live address: `AppLinks.site` in the app's `lib/config/links.dart`, or `--dart-define=SITE_URL=https://your-domain` when building.
3. In App Store Connect use `https://your-domain/privacy/` as the Privacy Policy URL and `https://your-domain/support/` as the Support URL.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

Inter, the same typeface as the app, is bundled under the SIL Open Font License (`assets/fonts/OFL.txt`).
