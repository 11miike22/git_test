# ShredGo Driver Waitlist

Standalone website for the ShredGo Manchester-only driver pre-registration page.

## Local preview

Open `index.html` in a browser, or serve the folder locally:

```bash
cd /Users/michaelokeyusuf/Claude/ShredGoDriverWaitlist
python3 -m http.server 5173
```

Then visit `http://localhost:5173`.

## Backend

Production submissions post to `/api/waitlist` and are saved in Supabase table:

`public.shredgo_driver_waitlist_submissions`

Run `supabase/waitlist.sql` in the Supabase SQL editor before launch.

Required Vercel environment variables:

- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`
- `IP_HASH_SALT` (optional, but recommended)

## Tracking

`index.html` includes empty `window.SHREDGO_TRACKING.metaPixelId` and
`window.SHREDGO_TRACKING.tiktokPixelId` placeholders. Add real pixel IDs and
official pixel snippets there when they are available. No fake IDs are included.

## Build

```bash
npm run check
npm run build
```
