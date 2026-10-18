# BRIDGE Admin Console

This is the static production build of Bridge's admin dashboard, hosted at `/admin/`. It uses the same Supabase project and Google sign-in as the app. The page is public, but dashboard access requires an authenticated account with the `admin` role; database access remains protected by Supabase policies and server-side role checks.

No Supabase service-role key or moderation-provider secret is included in this static bundle. The browser bundle contains the project's public publishable/anon key, which is intended for client use and must be protected by Row Level Security.

## Required Supabase redirect URL

In Supabase Dashboard, open **Authentication → URL Configuration → Redirect URLs** and allow:

`https://md-rehanullah.github.io/BRIDGE-Policy-and-terms-/admin/`

Keep the existing app and account-deletion redirect URLs. The Google provider's authorized redirect URI remains the Supabase Auth callback shown in the Supabase provider settings.
