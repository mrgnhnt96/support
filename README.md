# MRGNHNT — Support & Privacy

Public support pages and privacy policies for MRGNHNT, LLC apps, hosted on
GitHub Pages. The App Store and Google Play both require a reachable privacy
policy URL and support URL per app; this is where they point.

**Live:** https://mrgnhnt96.github.io/support/

## Layout

```
index.html            landing page, lists every app
style.css             shared styling
<app-slug>/
  index.html          app hub
  privacy/index.html  privacy policy
  support/index.html  support page
```

## Adding an app

Copy the `gun-fu/` directory, rename it, edit the three pages, and add a card to
the root `index.html`. Keep the privacy policy honest about which SDKs the app
actually ships — it is a legal document, and App Review reads it.

## Notes

- `.nojekyll` is present so GitHub serves the files as-is rather than running
  them through Jekyll.
- Pages are plain HTML with no build step, so what is in the repo is what is
  served.
