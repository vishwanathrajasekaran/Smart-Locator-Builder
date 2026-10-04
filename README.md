# Smart Locator Builder (own repo)

Static app. No build step, no API keys, no running costs. Screenshot reading uses Tesseract.js (OCR) in the browser, self-hosted in `ocr/`.

## Deploy
1. New GitHub repo `smart-locator-builder`, push this folder to the repo root.
2. Vercel > Add New > Project > import. Framework Preset: Other. No build command.
3. Name the project `smart-locator-builder` so its URL is https://smart-locator-builder.vercel.app
   (if you reuse your existing project, replace its files and keep that name).
4. Make sure the production URL opens without a Vercel login.
5. Public address is served through the gateway: https://tools.vishwanathrajasekaran.in/smart-locator/
   (gateway repo's vercel.json points at this project's URL; if your project URL differs, update it there).

## Notes
- robots.txt and sitemap.xml are served by the gateway, not here.
- canonical and og: tags already point to the tools.vishwanathrajasekaran.in address.
- Content-Security-Policy is report-only. After deploy, check the browser console, then rename the header to Content-Security-Policy.
- The Pro gate is client-side and demo only. Add real checkout and server-verified keys before charging.
