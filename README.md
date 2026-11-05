# Eva Managing

A French-language corporate website for Eva Managing, built to present the organization, its services, events, news, partners, and contact information through a responsive editorial-style experience.

## Project overview

The public-facing website is structured as a single-page experience with dedicated sections for:

- Organization introduction and founder presentation
- Services and upcoming events
- News and announcements loaded from Supabase
- Forum registration entry point
- Frequently asked questions
- Contact information and partner presentation

The repository also includes an administration area for managing news content.

## Admin content management

The admin interface provides:

- Supabase authentication
- News listing and dashboard summaries
- Create, edit, and delete operations for news items
- Draft and publish status management
- Optional image URL for news entries

Administrative access is intended to be enforced by Supabase authentication and database policies. Client-side checks are not a substitute for server-side authorization or Row Level Security.

## Technology

- **React 18**
- **TypeScript**
- **Vite**
- **Tailwind CSS**
- **shadcn/ui and Radix UI**
- **Framer Motion**
- **Supabase**
- **React Router**
- **TanStack Query**

## Requirements

- Node.js
- npm

## Local development

Install dependencies:

```bash
npm install
```

Create a local `.env` file with the Supabase project configuration:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_publishable_key
```

Start the development server:

```bash
npm run dev
```

Vite is configured to use port **8080**.

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server |
| `npm run build` | Build the production application |
| `npm run build:dev` | Build using development mode |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
| `npm run test` | Run the Vitest test suite |
| `npm run test:watch` | Run tests in watch mode |

## Supabase setup

The application uses Supabase for authentication and news content. Configure the project URL and publishable key through environment variables. Apply restrictive Row Level Security policies to the relevant tables so only authorized administrators can create, update, or delete content.

Never put a Supabase service-role key or other privileged secret in a frontend environment variable.

## Notes

This README documents the repository's visible application structure and development workflow. Production readiness depends on the deployment configuration, Supabase schema, authentication settings, and database security policies being correctly configured.
