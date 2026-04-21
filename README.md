# AI Cyber Laws Assistant Server

AI Cyber Laws Assistant is a Gemini-powered legal-tech Q&A platform that helps non-technical users understand Indian cyber laws through a guided, browser-based experience. This repository contains the Express, PostgreSQL, Prisma, and TypeScript backend that powers authentication, chat responses, community interactions, and user data management for the platform.

Built to support a dashboard-style frontend, the server handles secure sign-in flows, chat section storage, community post persistence, and AI response generation through Google Gemini. It also serves as the data layer for the platform's cyber awareness features and user profile experience.

The project was developed by a 4-person team and is designed to make cyber law guidance easier to access, understand, and apply for everyday users.

Frontend repository: [AI Cyber Laws Assistant Client](https://github.com/Sourish-Kanna/AI-Cyber-Laws-Assistant)

## What It Provides

- Authentication endpoints for email and Google login
- Chat APIs powered by Gemini
- Community post and interaction APIs
- User profile and chat section management
- PostgreSQL persistence through Prisma and Knex-based database access

## Prerequisites

- Node.js 18+
- PostgreSQL
- A Google OAuth client
- A Gemini API key

## Environment Setup

Create a `.env` file in the `Server` folder before starting the app. A sample configuration is available in `.env-local`.

Required variables:

- `DATABASE_URL`
- `DB_HOST`
- `DB_USER`
- `DB_PASSWORD`
- `DB_NAME`
- `DB_PORT`
- `PORT`
- `CLIENT_ORIGIN_PORT`
- `CLIENT_PORT`
- `GEMINI_API_KEY`
- `GOOGLE_CLIENT_ID`
- `GOOGLE_CLIENT_SECRET`

## Install And Run

```bash
npm install
```

```bash
npx prisma migrate dev --name add_community_tab
```

```bash
npm run dev
```

## Scripts

- `npm run dev` - starts the API with nodemon
- `npm run build` - compiles the TypeScript server

## API Routes

- `/api/v1/auth`
- `/api/v1/users`
- `/api/v1/chat`
- `/api/v1/community`

## Notes

- The server reads from `.env` at startup.
- The root health check returns a simple JSON `ok` response.
