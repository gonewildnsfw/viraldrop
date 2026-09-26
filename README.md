# ViralDrop

**Find it. Create it. Schedule it. Grow it.**

ViralDrop is a multi-workspace short-form content operating system for personal creators, businesses and agencies.

## v0.1
- Public landing page
- Supabase email/password authentication
- Personal and business onboarding UI
- Dashboard shell
- GitHub Pages build configuration
- Supabase-backed multi-tenant data model (backend project)

## Local development
1. Copy `.env.example` to `.env.local`.
2. Add the Supabase project URL and **publishable** key. Never put a service-role/secret key in the browser app.
3. Run `npm install` then `npm run dev`.

## Deployment
The included GitHub Actions workflow builds the Vite app and deploys `dist/` to GitHub Pages. Configure repository Actions variables:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`

Private integrations such as Buffer tokens, billing secrets and AI provider secrets belong in server-side functions, not this public repository's frontend bundle.
