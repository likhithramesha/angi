# Angi AI QA Reviewer - Vercel Deployment

This version keeps the Groq API key out of the browser by routing model calls through a Vercel serverless function at `/api/groq`.

## Deploy

1. Push this folder to a GitHub repo.
2. Import the repo in Vercel.
3. In Vercel Project Settings -> Environment Variables, add:
   - `GROQ_API_KEY` = your Groq API key
4. Redeploy the project.

## Local test

Create `.env.local`:

```bash
GROQ_API_KEY=your_groq_key_here
```

Then run:

```bash
npm i -g vercel
vercel dev
```
