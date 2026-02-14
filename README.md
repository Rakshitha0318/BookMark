## Challenges Faced

### 1. Google OAuth Redirect Issues

During production deployment, Google authentication worked locally but failed to redirect correctly on the live Vercel domain.
This required proper configuration of redirect URLs in Supabase and dynamic redirect handling using window.location.origin.


### 2. Realtime Updates Not Syncing

Realtime bookmark updates across multiple tabs initially failed due to incorrect Supabase subscription configuration and missing RLS policies.
This was fixed by enabling realtime for the table and setting proper policies.



### 3. Environment Variables in Production

Application crashed in Vercel because Supabase URL and API keys were not configured in environment variables.
Resolved by adding them in Vercel project settings.



### 4. Redirect Loop in Production

After login, users remained on the homepage instead of navigating to the dashboard due to incorrect redirect logic.
Fixed by implementing proper OAuth callback flow and session detection.



### 5. Deployment & Git Issues

Faced multiple Git authentication and repository permission issues while pushing code to GitHub.
Resolved by configuring correct repository ownership and deployment branch in Vercel.


