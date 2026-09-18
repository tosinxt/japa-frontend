# JapaTalent — Frontend

The public-facing website for JapaTalent, a career platform offering job listings, courses/upskilling, career coaching, and a CV-revamp service.

Built with [Next.js 14](https://nextjs.org/) (App Router), Tailwind CSS, MUI, and Zustand for state management.

## Getting Started

Install dependencies and run the dev server:

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the result.

### Environment variables

Create a `.env` (or `.env.local`) with:

```bash
NEXT_PUBLIC_API_URL=https://api.japatalent.com/japa/v1/   # backend API base URL
NEXT_PUBLIC_RECAPTCHA_SITE_KEY=your-recaptcha-site-key    # Google reCAPTCHA on signup
```

`NEXT_PUBLIC_API_URL` falls back to the production API if unset — override it to point at a local backend during development.

## Project structure

- `app/(pages)/` — public routes: `jobs`, `courses`, `applied`, `careerCoaching`
- `app/(auth)/` — auth routes: `signup`, `login`, `reset`, `resetEmail`, `verifyAccount`
- `app/store/store.js` — single Zustand store for auth/session state and API calls
- `app/components/` — shared UI components

## Deployment

Deployed on [Vercel](https://vercel.com). Pushing to `main` triggers a production deploy.
