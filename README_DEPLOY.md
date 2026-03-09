# Autostyle Voting - Prepared Deploy Package

This package was cleaned from the original Anything export so you can deploy it on Railway.

## Included changes
- kept only the web app
- added production scripts (`build`, `start`)
- removed the original `.env` file from the package
- replaced Anything upload dependency with Uploadcare direct uploads
- added Railway config files
- added `.env.example`

## Recommended host
Railway is the safest option for this project because it is a React Router v7 SSR app with a database-backed backend.

## Environment variables
Create a `.env` file from `.env.example` and fill in:
- `DATABASE_URL`
- `AUTH_SECRET`
- `AUTH_URL`
- `APP_URL`
- `CORS_ORIGINS`
- `NEXT_PUBLIC_UPLOADCARE_PUBLIC_KEY`

## Required database
You still need to create/import your PostgreSQL schema and data. This package does not include your database dump.

## Local test
```bash
npm install
cp .env.example .env
npm run dev
```

## Railway deploy
1. Create a new Railway project
2. Add a PostgreSQL database
3. Upload this folder or connect it to GitHub
4. Add the environment variables from `.env.example`
5. Deploy

## Production start command
```bash
npm run start
```
