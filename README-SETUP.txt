MAIN DATA BACKEND — ANDROID/GITHUB/NETLIFY SETUP

FILES
- package.json
- netlify.toml
- netlify/functions/profile.js

WHAT THIS DOES
- Adds a Netlify Function at /.netlify/functions/profile
- Calls Data Station's profile endpoint from the server side.
- Reads the private token from a Netlify environment variable.

IMPORTANT
This starter only implements the profile/balance request using the endpoint previously identified:
https://datastation.com.ng/api/profile/
It does NOT yet implement airtime/data purchases, payments, user accounts, wallets, refunds, or transaction records. Those require checking the current Data Station API documentation and the chosen payment provider's API.

UPLOAD
1. In your GitHub main-data repository, create folders and files exactly as shown.
2. Add the contents of each file below to the matching file in GitHub.
3. In Netlify, open your site > Site configuration > Environment variables.
4. Add:
   Key: DATASTATION_TOKEN
   Value: your private Data Station API token
5. Save, then redeploy the site.
6. Test:
   https://YOUR-SITE-NAME.netlify.app/.netlify/functions/profile

SECURITY
- Never paste your API token into index.html, GitHub files, screenshots, or public messages.
- If you previously committed a token to a public repository or shared it, rotate/regenerate it in Data Station.
- CORS is set to * for initial testing. Before public launch, restrict it to your own website domain and add authentication/rate limits.

NOTE
If your existing netlify.toml has other settings, merge these settings rather than blindly replacing the file. Keep a backup first.
