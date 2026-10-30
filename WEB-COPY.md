# leve-web

Web/PWA copy of leve, split from `everydayou/leve` (the native iOS/Android app).
This copy has no `ios/` or `android/` folders and deploys to Vercel on every push,
so changes ship without Xcode, TestFlight or App Store review.

- Native-only plugins (camera, haptics, keyboard, share, HealthKit) are guarded in
  the code and simply do nothing in a browser.
- Data lives in each browser's own IndexedDB. It does not sync with the native app.
- Do NOT build or deploy with `VITE_SHARED_BETA=true` here: it embeds an Anthropic key in a
  public bundle. Leave `VITE_FOOD_SCAN_API_URL` unset unless the proxy is protected.
- First feature planned for this copy: the new first-open flow in `FIRST-OPEN-FLOW-CONCEPT.md`.
