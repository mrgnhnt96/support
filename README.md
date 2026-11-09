# MRGNHNT — Support & Privacy

Public support pages and privacy policies for MRGNHNT, LLC apps, hosted on
GitHub Pages. The App Store and Google Play both require a reachable privacy
policy URL and support URL per app; this is where they point.

**Live:** https://mrgnhnt.com/support/

The account has a custom domain, so project pages are served from the apex
domain rather than `mrgnhnt96.github.io`. Both resolve; use the apex one in
store listings.

## Layout

```
index.html            landing page, lists every app
style.css             shared styling
icon-180.png          MRGNHNT icon (favicon for the landing page)
sitemap.xml           every page, with the date it last changed
404.html              not-found page (absolute /support/ links)
docs/marketing/       page brief: what each claim on the pages rests on
<app-slug>/
  index.html          app hub
  icon-180.png        the app's icon, 180x180 (favicon for its pages)
  share-v1.png        1200x630 share image (the Play feature graphic, padded)
  privacy/index.html  privacy policy
  support/index.html  support page
```

## Adding an app

Copy the `gun-fu/` directory, rename it, edit the three pages (including each
page's description and canonical URL), swap in the app's icon, add a card to the
root `index.html`, and add the three URLs to `sitemap.xml`. Record what each
privacy statement rests on in `docs/marketing/page-brief.md`. Keep the privacy
policy honest about which SDKs the app actually ships — it is a legal document, and App Review reads it.

## Notes

- `.nojekyll` is present so GitHub serves the files as-is rather than running
  them through Jekyll.
- Pages are plain HTML with no build step, so what is in the repo is what is
  served.
