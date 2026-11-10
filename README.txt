# Mouse Boss Website Starter

## What's included
- `index.html`: responsive front-end preview for dashboard, order sales, daily summary, expenses, inventory, product list, and staff/access page.
- `supabase_schema.sql`: starting database schema and row-level security policies for a real multi-user Supabase setup.

## Important preview limitation
The current `index.html` is a local browser preview. Demo login is not real authentication; records are saved only in the browser's localStorage on that device. It is NOT yet an online multi-user bookkeeping system. Do not enter real customer details or rely on this preview as the official ledger.

## To publish as an online website
1. Create a Supabase project and keep its project URL and anon key.
2. Run `supabase_schema.sql` in Supabase SQL Editor.
3. Configure real Supabase Auth (email/password), create the owner profile, and invite staff accounts.
4. Connect the front end to Supabase using the project URL and anon key. Keep the service_role key server-side only.
5. Deploy the site folder to Vercel or Netlify and choose a free subdomain such as `mouse-boss.vercel.app`.
6. Test owner/staff permissions, backups, stock calculations, and weekly/monthly/yearly reports before using for live business.

## Suggested role rules
- Owner: full dashboard, costs, profits, reports, staff administration, product setup.
- Staff: enter sales, expenses and stock movements; hide owner-only cost/profit reports if that is your business policy.

## Data-entry rule
For a given sale, use either `Order Sales` or `Daily Summary`, never both, to avoid double-counting.
