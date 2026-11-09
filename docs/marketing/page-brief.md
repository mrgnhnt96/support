# Page brief

- Type and state: Supporting pages (support and privacy) for store apps, live. Not a marketing page:
  the App Store and Google Play listings link here.
- Audience: players of MRGNHNT apps who need help, and App Review and Play review checking the
  listing's support and privacy URLs.
- The page's one job: give a working support contact and a privacy policy that matches each app.
- Primary CTA: "Email mrgnhnt96@gmail.com" (mailto).
- Secondary action: none.
- Search phrases: "stickman gun-fu support", "stickman gun-fu privacy policy",
  "stickman gun-fu restore purchases", "stickman gun-fu refund".
- Objections: "Is there a real person behind this?" (answered by the email); "What does the game do
  with my data?" (the privacy policy); "How do I get my purchase back?" (Restore Purchases).
- Analytics and cookies: none. The pages load one stylesheet and one icon.
- Store links here: the game's App Store metadata points `supportUrl`, `privacyPolicyUrl` and
  `marketingUrl` at `/support/gun-fu/support/`, `/support/gun-fu/privacy/` and `/support/gun-fu/`.

## Claims

Checked against the game's repository (`flutter/gun_fu`, commit `95137a1`, 14 Aug 2026) on
9 Nov 2026 unless the row says otherwise.

| Claim on the page | Evidence |
| --- | --- |
| No account, sign-up or login; no server of our own | `pubspec.yaml` dependencies: no auth or backend package |
| Progress (stats, coins, weapons, upgrades, achievements, settings) stays on the device | `shared_preferences` is the only storage package |
| Ads through Google AdMob, interstitial and optional rewarded | `google_mobile_ads` in `pubspec.yaml`; interstitial and rewarded ads in `lib/` |
| iOS asks through App Tracking Transparency first | `app_tracking_transparency` in `pubspec.yaml`; `requestTrackingAuthorization` in `lib/`; `NSUserTrackingUsageDescription` in `ios/Runner/Info.plist` |
| Purchases go through the stores and RevenueCat | `purchases_flutter` in `pubspec.yaml`; `restorePurchases` in `lib/` |
| Leaderboards and achievements through Game Center and Play Games | `games_services` in `pubspec.yaml` |
| No other analytics or crash SDKs | No Firebase, analytics, Crashlytics, Sentry, PostHog or Amplitude in `pubspec.yaml` or `lib/` |
| Remove Ads, Restore Purchases, Armory, Shield, Focus, Normal and Epic exist | Names found in `lib/` |
| Rated 12+, not directed at children under 13 | Owner's word: privacy policy as written by Morgan Hunt, 14 Aug 2026 (commit `bd23369`) |
| Retention and deletion of the RevenueCat purchase record on request by email | Owner's commitment, added 9 Nov 2026; awaiting confirmation (below) |
| Ad data kept under Google's retention policy | https://policies.google.com/technologies/retention |
| Share image on the game's pages is the game's real Play feature graphic | `gun_fu/metadata/play/en-US/images/featureGraphic.png`, padded to 1200x630 on its own background colour |
| Removed: "Google's consent form asks in the EEA and UK before ads load" | Not in the game: no consent-form call anywhere in `lib/` |

## Waiting on a person

- Morgan: confirm you'll handle email requests to delete a player's RevenueCat purchase record, and
  that the third-party protection sentence in the privacy policy is one you stand behind.
- Morgan: confirm the store age rating (the policy says 12+) once the listings are set.
- Morgan: add `Sitemap: https://mrgnhnt.com/support/sitemap.xml` to the apex `robots.txt` (personal
  site repository), or submit it in Search Console.
- Morgan, after deploy: verify the pages in Google Search Console and Bing Webmaster Tools.
