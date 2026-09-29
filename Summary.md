
<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-light.svg">
  <img src="assets/banner-light.svg" alt="Campus Connect: find your club, build your story" width="100%">
</picture>

# Project summary

**Campus Connect** · Team NexMind (Team-003) · IIT Madras BS Degree, Software Engineering Project, May 2026

[Repository](https://github.com/1mystic/MAY2026-Team-003/) ·
[Live app](https://campus-connect-swe.vercel.app/) ·
[API docs](https://campusconnect.itshrestha.dev/docs)

</div>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## The problem

Student club leaders on most campuses run everything through a patchwork of Instagram DMs, WhatsApp groups, Google Forms, spreadsheets and Canva. Membership is tracked by hand, event attendance is guesswork, and certificates are made one at a time and can't be verified by anyone else. Students struggle to discover clubs, and administrators have little visibility into what clubs actually do.

Campus Connect replaces that patchwork with one connected workflow for the whole club lifecycle. It was built for the course brief *Community Services Platform*, in the subdomain *Student Club Management for Higher Education Institutions*.

## Who it's for

| Users | Who they are | What they do on the platform |
|---|---|---|
| **Students** (primary) | Undergraduates and club members | Discover clubs, send join requests, register for events, check in, receive results, download verifiable certificates, raise issues |
| **Club leaders** (secondary) | Club heads and event coordinators | Create and run clubs and events, approve members, mark attendance, declare results, post announcements, resolve issues |
| **Campus admins** (secondary) | Campus council and student affairs staff | Approve or reject new clubs, configure the college's verified email domain, monitor campus-wide activity |
| **Institution** (tertiary) | Registrar, dean, student body representatives | Don't use it directly, but their asks for credibility and verifiable records shaped the certificates and leaderboard |

Personas and stories come from Milestone 1 research: three interviews and one written submission from a student body representative.

## What was built

Eighteen user stories across seven epics, all delivered by the final submission.

| Epic | What it covers |
|---|---|
| **1. Platform foundation** | College registration, signup and login on a verified college email domain, password recovery by real email, Google Sign-In |
| **2. Club discovery and membership** | Club directory and profiles, join requests, membership approval, club registration and admin approval |
| **3. Event lifecycle** | Create, publish, register, check in, declare results (winner, runner-up, participant), edit and cancel |
| **4. Communication and issues** | Club announcements with a consolidated feed, member-raised issues, leader resolution |
| **5. Certificates** | PDFs generated automatically when results are declared, a student certificate wallet, public verification by serial number and QR code |
| **6. AI club finder** | Natural-language club matching against real college data through a bounded tool-calling agent |
| **7. Recognition** | Campus-wide leaderboard ranked by events run, membership growth and participation |

### Two features worth highlighting

**Results to certificates with no manual step.** One API call declares the winner and runner-up, marks every other attendee as a participant, renders a certificate PDF per attendee from an SVG template, uploads it to S3, records a serial number and URL, and notifies the student. Every certificate carries a QR code that resolves to a public `/verify/<serial>` page, so anyone can check it.

**An AI assistant that can't invent a club.** The finder is a Claude Haiku 4.5 agent that either answers or calls a tool such as `search_clubs` or `get_event`. Three limits bound it: a budget on iterations, tool calls and tokens that forces a final answer; a grounding gate that only lets the reply name entities a tool actually returned; and a deterministic recommender that takes over if the model is unreachable. Students always get an answer, and it always comes from real data.

## How it's built

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg">
  <img src="assets/architecture-light.svg" alt="High-level system architecture" width="100%">
</picture>

A Vue 3 single-page app talks to a FastAPI backend over HTTPS with JWT bearer tokens. Routes call a service layer, which reaches PostgreSQL through a repository layer, so persistence never leaks into route handlers. Every entity is scoped to a college, which keeps one institution's data invisible to another. The Anthropic API key stays server-side.

| Layer | Technology |
|---|---|
| Frontend | Vue 3 (Composition API), Vite, Pinia, Vue Router, a vanilla CSS design-token system |
| Backend | FastAPI, Python 3.12+, async SQLAlchemy, Alembic, Pydantic |
| Database | PostgreSQL on Neon serverless with connection pooling |
| Auth | JWT (access, refresh and single-use reset tokens), Google Identity Services |
| AI | Anthropic Claude Haiku 4.5 |
| Storage and email | AWS S3 for banners, avatars and certificate PDFs; Resend SMTP with Jinja2 templates |
| Certificates | Server-side SVG-to-PDF rendering with an embedded QR code |
| Testing and tooling | pytest, pytest-asyncio, a disposable per-run PostgreSQL schema, uv, npm, GitHub Actions |
| Deployment | Docker, Vercel (frontend), Render (backend) |
| Docs | OpenAPI 3.1 and Swagger UI, generated from the routes and Pydantic models |

The design system is deliberately warm and role-accented: orange for students, green for club leaders, navy for administrators. It is meant to feel approachable to students while staying credible to institutional staff.

## How the project ran

| Milestone | Focus | Outcome |
|---|---|---|
| **1. Problem and research** | Interviews, personas, user stories | 18 stories in 7 epics, plus a future-scope list to keep out-of-scope ideas out of the backlog |
| **2. Design and foundation** | ERD, API surface, visual design system | FastAPI and PostgreSQL backend structure; Vue 3 and Pinia frontend shell |
| **3. Sprint 1** | Core participation spine | Club registration and approval, memberships, events, attendance, results. Four bugs found and fixed, one documentation gap tracked |
| **4. Sprint 2** | Certificates, auth recovery, integration | Certificate module, single result-declaration endpoint, event reminders, password recovery. 459 passing backend tests |
| **5. Final** | AI finder, leaderboard, Google Sign-In, uploads | Carried-over items closed and remaining modules wired to the live backend |

Sprint 2 was shaped directly by feedback from the same users interviewed in Milestone 1. Work was tracked in GitHub Issues, labelled by milestone and closed with a reference to the commit or pull request that fixed it, plus a Trello Kanban board and a three-tier Git strategy (`main` → `dev` → `feature/name-task`).

Everything reported as delivered was checked against live infrastructure rather than assumed: password recovery was confirmed with a real email through production SMTP, and the AI finder and certificate module were exercised against real seeded campus data, not mocks.

## Team NexMind

| Member | Role |
|---|---|
| **Atharv Khare** | Lead Product Manager, Frontend Developer |
| **Kavisha Tankle** | Scrum Master, QA Engineer |
| **Shrestha Srivastava** | Backend Lead, Code Reviewer |
| **Pawan Kumar Choudhary** | Backend Developer, Tester |
| **Shrishti Gupta** | Frontend Developer |

## Where to look next

| I want to… | Go to |
|---|---|
| Try the app | [campus-connect-swe.vercel.app](https://campus-connect-swe.vercel.app/), with demo logins in the [README](README.md#demo-accounts) |
| Explore the API | [Swagger UI](https://campusconnect.itshrestha.dev/docs) or [`backend/openapi.yaml`](backend/openapi.yaml) |
| Run it locally | [Getting started](README.md#getting-started) |
| Read the code | [`backend/`](backend/) and [`frontend/`](frontend/) |
