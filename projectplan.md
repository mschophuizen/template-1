# Development Plan: Waiting List SaaS Application

## Phase 1: Foundation & Core API

1.  **Initialize Projects:**
    *   Set up Next.js frontend (`/src/app`).
    *   Set up NestJS backend (separate repository or monorepo).
    *   Configure Firebase project (Auth, Firestore, Storage).
    *   Integrate Tailwind CSS v4 with Next.js.
2.  **Define Core Models:**
    *   `User`: Firebase Auth UID, email, associated waitlists.
    *   `Waitlist`: ID, name, description, owner (User UID), creation date, subscriber count.
    *   `Subscriber`: ID, email, waitlist ID, subscription date, status (e.g., pending, confirmed).
3.  **Implement tRPC API Layer:**
    *   Set up tRPC router in NestJS.
    *   Define initial procedures for CRUD operations on `Waitlist` and `Subscriber`.
    *   Integrate tRPC client in Next.js.
4.  **Set Up Authentication:**
    *   Integrate Firebase Authentication using `next-auth`.
    *   Implement sign-up, sign-in, sign-out flows.
    *   Protect relevant API routes and frontend pages.

## Phase 2: Waitlist Management

5.  **Waitlist Creation Feature:**
    *   Frontend: Create form (React Hook Form) in the user dashboard for new waitlist details. Use Server Actions.
    *   Backend: Implement NestJS service and tRPC procedure to create and store `Waitlist` documents in Firestore, associated with the authenticated user.
6.  **Waitlist Dashboard:**
    *   Frontend: Create authenticated page displaying user's created waitlists (list view). Fetch data using tRPC client.
    *   Backend: Implement tRPC procedure to fetch waitlists owned by the authenticated user.
7.  **View Waitlist Details:**
    *   Frontend: Page to display details of a specific waitlist, including its subscribers.
    *   Backend: Implement tRPC procedure to fetch a specific waitlist and its associated subscribers.

## Phase 3: Public Subscription & Deployment

8.  **Public Subscription Form:**
    *   Frontend: Create a public-facing, shareable page/component for a specific waitlist allowing users to enter their email. Use Server Actions.
    *   Backend: Implement public tRPC procedure (or Route Handler) to add a `Subscriber` to the specified `Waitlist` in Firestore. Include basic validation (e.g., valid email format).
9.  **Deployment Configuration:**
    *   Configure Vercel for Next.js frontend deployment.
    *   Choose deployment strategy for NestJS backend (e.g., Vercel Serverless Functions, Firebase Functions, dedicated server). Configure environment variables.
10. **Initial Deployment:** Deploy frontend and backend to staging/production environments.

## Phase 4: Testing & Documentation

11. **Testing:**
    *   Implement unit tests for critical NestJS services and utility functions.
    *   Implement integration tests for API endpoints (tRPC procedures).
    *   Implement basic end-to-end tests for core user flows (signup, create waitlist, subscribe).
12. **Documentation:**
    *   Update `README.md` with setup and usage instructions.
    *   Document API endpoints in `API.md`.
    *   Update `STRUCTURE.md` if necessary.
    *   Add JSDoc comments to all functions, components, and types.
    *   Maintain `CHANGELOG.md`.

## Ongoing Tasks:

*   Adhere strictly to TypeScript standards (strict mode, no `any`, Zod validation).
*   Follow Next.js App Router patterns (Server Components default, `use client` where needed).
*   Implement mobile-first responsive design with Tailwind CSS.
*   Ensure proper error handling and loading states throughout the application.
*   Maintain clean development environment practices (`dev:clean`, `build:clean`).
