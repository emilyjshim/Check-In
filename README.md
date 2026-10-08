# Check-In

This is a simple static check-in website. To let Emily and Evan see each other's
latest check-in from different devices, the page uses a Supabase database.

## Connect Supabase

1. Create a free project at [supabase.com](https://supabase.com/).
2. In the Supabase dashboard, open **SQL Editor**, create a query, paste in the
   contents of [supabase-setup.sql](./supabase-setup.sql), and run it. This
   creates the table and enables the public access needed by this demo.
3. In the dashboard, open **Project Settings → API** (or **API Keys**) and copy
   the Project URL and the publishable key. The legacy `anon` key also works.
4. In `index.html`, replace `YOUR_SUPABASE_PROJECT_URL` and
   `YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY` with those values. Do not use a
   `service_role` or secret key in this website.
5. Save the file and publish the site with GitHub Pages. Open the published
   page on each device to submit check-ins.

## Privacy note

This demo intentionally allows anyone who can access the published page to
read and submit check-ins. The Supabase URL and publishable/anon key are visible
in the website, and the database policies allow public reading and writing.
Only share non-sensitive information. To keep answers private, add user
authentication and restrict the database policies before using it for personal
information.