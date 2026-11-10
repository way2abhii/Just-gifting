# Deploy JustGifting frontend to Vercel

This repository is configured for Vercel to build the Vite/React frontend from the repository root. The `Page 1` through `Page 6` folders must remain alongside `app/` because the Vite app imports screens from those folders.

## Deploy
1. Push this project to a GitHub repository (or import the ZIP into a new repository).
2. In Vercel, choose **Add New → Project** and import that GitHub repository.
3. Keep the project **Root Directory** set to `./` (the repository root), not `app/`.
4. Vercel should detect the settings in `vercel.json`. If it asks, use:
   - Install command: `npm --prefix app ci`
   - Build command: `npm --prefix app run build`
   - Output directory: `app/dist`
5. Deploy.

## Important scope / current limitations
- This deployment serves the React frontend only. The Python FastAPI backend in `backend/` is not deployed by this Vercel configuration; deploy it separately (for example, to Render) if/when the frontend is connected to it.
- The current frontend uses in-memory/sample data in `app/src/context/AppContext.jsx`; it does not persist changes across reloads and is not currently calling the FastAPI backend.
- No Supabase credentials are needed for the current sample-data frontend. Never put a Supabase service-role key in a `VITE_` variable or frontend code.
