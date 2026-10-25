# Episodes website

Public website, privacy policy, credits and support for **Episodes — TV Show Tracker**.

- Website: https://ebisbe.github.io/episodes-site/
- Repository: https://github.com/ebisbe/episodes-site
- Support: https://github.com/ebisbe/episodes-site/issues

This repository contains the static website, not the Android development repository.
The app is preparing for Google Play; the privacy page is explicitly pre-release
until the publisher identity and dedicated contact information are supplied.

## Preview

From this website repository's root:

```sh
python3 -m http.server 8000
```

Open `http://localhost:8000`. There is no build, dependency installation, analytics,
or JavaScript. All assets and page links are relative to support project-site paths.

If previewing the copy kept in the Android repository instead, run
`python3 -m http.server 8000 --directory website` from the Android repository root.

## Publish changes

GitHub Pages uses **Settings → Pages → Source → Deploy from a branch**, with
branch **main** and folder **/ (root)**. GitHub automatically deploys website
changes pushed to `main`; no custom workflow or build dependencies are needed.

Edit these files, preview locally, commit, and push to this website repository.
Check the Actions deployment, then the homepage, Privacy, Support and Credits pages.
The Android app's About screen links to these URLs.

The private Android checkout also keeps a copy under `website/`. When editing that
copy, copy only its **contents** to the public repository root, including
`.nojekyll`. Never copy the Android checkout, library backups, signing files or local
configuration. The two repositories can be maintained independently; there is no
automatic synchronization or token connecting them.

If you choose another repository name, update the Android `about_website`,
`about_privacy`, `about_support`, `about_credits` strings and the URLs in
  Android publishing guide, `support.html`, and this file before release.

## Complete before the Play release

- Create the dedicated Proton mailbox and add a `mailto:` link to Support and
  Privacy. Add the correct legal publisher/controller identity and address/contact
  information as applicable to your Spanish business and EEA trader status.
- Finalize the privacy policy (including support-data retention) against the shipped
  app, actual backup behavior and third-party services. Remove pre-release notices
  only when the missing information is supplied.
- Add an approved TMDB attribution logo in the app's About/Credits section and
  maintain the required text and JustWatch credit. Check attribution/logo terms
  before copying third-party assets to the public site.
- Capture current screenshots. Keep personal notes, real library backups and any
  account/payment information out of screenshots.
- When Play is live, replace the pre-launch notice with the actual Play listing
  link, and update the price explanation for the launch regions.
- Provide a **complete corresponding source** package for each distributed version,
  with licenses and build instructions, for example in this public repository's
  Releases. Link each specific archive from `credits.html`. Linking upstream alone
  does not provide this fork's source. Follow the publishing guide in the Android
  repository when preparing a source package.

Only public website files belong in this repository. GitHub Pages publishes the
website repository's root; it does not publish the private Android checkout.
