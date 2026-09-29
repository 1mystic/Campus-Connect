<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" alt="Campus Connect: find your club, build your story" width="100%">
</picture>

<br/>

[![Live demo](https://img.shields.io/badge/Live_demo-Open_app-F28229?style=for-the-badge&logo=vercel&logoColor=white)](https://campus-connect-swe.vercel.app/)
[![API docs](https://img.shields.io/badge/API_docs-Swagger_UI-4E9F5A?style=for-the-badge&logo=swagger&logoColor=white)](https://campusconnect.itshrestha.dev/docs)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-Spec-26364F?style=for-the-badge&logo=openapiinitiative&logoColor=white)](backend/openapi.yaml)

![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Vue](https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_Haiku_4.5-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Commits](https://img.shields.io/badge/commits-471-F28229?style=flat-square)
![PRs](https://img.shields.io/badge/PRs_merged-63-4E9F5A?style=flat-square)

**[Overview](#overview)** ·
**[Tech stack](#tech-stack)** ·
**[Architecture](#architecture)** ·
**[Getting started](#getting-started)** ·
**[Demo](#demo-accounts)** ·
**[Timeline](#timeline)** ·
**[Recognition](#recognition)** ·
**[Team](#team)**

</div>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Overview

**Campus Connect** is a multi-user platform that helps colleges run their student clubs end to end. Campus admins onboard the college and approve clubs, club leaders manage members, events and announcements, and students discover clubs, register for events and collect verifiable certificates.

| | |
|---|---|
| **Role-based dashboards** | Separate experiences for students, club leaders and campus admins |
| **Event lifecycle** | Draft, publish, register, mark attendance, declare results |
| **Verifiable certificates** | Auto-generated PDFs with a QR code that resolves to `/verify/<serial>` |
| **Leaderboard** | Clubs ranked on real activity scores |
| **Issue tracker** | Members raise issues and leaders answer them from a queue |
| **AI club finder** | A bounded tool-calling assistant that matches students to clubs |

### Built for every role

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/roles-dark.svg">
  <img src="assets/roles-light.svg" alt="Students, Club Leaders and Administrators" width="100%">
</picture>

### How it works

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/how-it-works-dark.svg">
  <img src="assets/how-it-works-light.svg" alt="Discover, Join, Attend, Get certified" width="100%">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Screenshot

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/landing.webp">
  <img src="assets/landing.webp" alt="Campus Connect landing page" width="100%">
</picture>
<br/><br/>
</div>

## Tech stack

<table>
<tr>
<td width="50%" valign="top">

### Backend

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=for-the-badge)
![Uvicorn](https://img.shields.io/badge/Uvicorn-499848?style=for-the-badge&logo=gunicorn&logoColor=white)
![JWT](https://img.shields.io/badge/python--jose_JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Google](https://img.shields.io/badge/Google_Sign--In-4285F4?style=for-the-badge&logo=google&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![Jinja](https://img.shields.io/badge/Jinja2-B41717?style=for-the-badge&logo=jinja&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-D97757?style=for-the-badge&logo=anthropic&logoColor=white)

`asyncpg` · `bcrypt` · `boto3` · `CairoSVG` · `qrcode`

</td>
<td width="50%" valign="top">

### Frontend

![Vue](https://img.shields.io/badge/Vue_3-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Pinia](https://img.shields.io/badge/Pinia-FFD859?style=for-the-badge&logo=pinia&logoColor=black)
![Vue Router](https://img.shields.io/badge/Vue_Router_4-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)
![Lucide](https://img.shields.io/badge/Lucide_Icons-F56040?style=for-the-badge&logo=lucide&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)
![CSS](https://img.shields.io/badge/CSS_design_system-1572B6?style=for-the-badge&logo=css3&logoColor=white)

`jwt-decode` · `Vue Test Utils`

### Tooling

![uv](https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=uv&logoColor=white)
![Node](https://img.shields.io/badge/Node_20+-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=for-the-badge&logo=openapiinitiative&logoColor=white)

</td>
</tr>
</table>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Architecture

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg">
  <img src="assets/architecture-dark.svg" alt="High-level system architecture" width="100%">
</picture>
</div>

The Vue 3 single-page app talks to the FastAPI backend over HTTPS with a JWT. Google Sign-In tokens are verified server-side. Routes call a service layer, which uses a repository layer for PostgreSQL and talks directly to S3 for banners, avatars and certificates. The AI agent loop calls Claude Haiku 4.5 and can call back into the service layer as tools.

### Event to certificate

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#FDE9D9','primaryBorderColor':'#F28229','primaryTextColor':'#2E211C','lineColor':'#7A8699','textColor':'#7A8699','secondaryColor':'#E3F1E5','tertiaryColor':'#FDFBF9','noteBkgColor':'#FBF0D2','noteTextColor':'#2E211C','actorLineColor':'#7A8699','labelBoxBkgColor':'#FBF0D2','labelTextColor':'#2E211C','actorBkg':'#FDE9D9','actorBorder':'#F28229','actorTextColor':'#2E211C','signalColor':'#7A8699','signalTextColor':'#7A8699'}}}%%
sequenceDiagram
    autonumber
    actor S as Student
    actor L as Club leader
    participant API as Backend API
    participant DB as PostgreSQL
    participant R as Certificate renderer
    participant S3 as AWS S3

    S->>API: POST /events/{id}/register
    API->>DB: create EventRegistration
    API-->>S: registration confirmed
    Note over S,L: Event day
    L->>API: mark attendance
    API->>DB: checked_in = true
    L->>API: PATCH /events/{id}/results
    API->>DB: set winner, runner-up, participants
    API->>R: render certificate PDF (per attendee)
    R->>S3: upload PDF
    S3-->>API: public URL
    API->>DB: create Certificate (serial, url)
    API-->>S: result and certificate notification
```

### AI club finder

The assistant is a bounded tool-calling loop. It can only name clubs and events that a tool actually returned, and it falls back to a deterministic recommender if the model is unreachable.

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#FDE9D9','primaryBorderColor':'#F28229','primaryTextColor':'#2E211C','lineColor':'#7A8699','textColor':'#7A8699','secondaryColor':'#E3F1E5','tertiaryColor':'#FDFBF9','edgeLabelBackground':'transparent'}}}%%
flowchart TD
    Q([Student asks a question]) --> D{Model decides:<br/>answer or call a tool?}
    D -- tool_use --> T[Execute tool<br/>search_clubs, get_event, ...]
    T --> A[Append tool result to conversation]
    A --> B{Budget exceeded?<br/>iterations, tool calls, tokens}
    B -- no --> D
    B -- yes --> F[Force final answer from what was gathered]
    D -- end_turn --> G
    F --> G[Grounding gate:<br/>only name entities a tool returned]
    D -. model unreachable .-> X[Deterministic recommender<br/>degraded fallback]
    G --> R([Reply shown to student])
    X --> R

    classDef brand fill:#FDE9D9,stroke:#F28229,color:#2E211C;
    classDef safe fill:#E3F1E5,stroke:#4E9F5A,color:#2E211C;
    classDef fallback fill:#E4ECF8,stroke:#26364F,color:#2E211C;
    class D,T,A,B,F brand;
    class G safe;
    class X fallback;
```

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Getting started

<details open>
<summary><b>Prerequisites</b></summary>

<br/>

- Python 3.12+ (managed by [uv](https://docs.astral.sh/uv/))
- Node 20+ and npm 10+
- A PostgreSQL database (plus a separate throwaway one for tests)

</details>

### 1. Clone

```bash
git clone https://github.com/Srivastava-Shrestha/MAY2026-Team-003.git
cd MAY2026-Team-003
```

### 2. Backend

```bash
# install uv (Linux/macOS)
curl -LsSf https://astral.sh/uv/install.sh | sh
# install uv (Windows)
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

cd backend
uv sync
cp .env.example .env        # then fill in the values
uv run alembic upgrade head
uv run uvicorn main:app --reload
```

The API runs at `http://localhost:8000`, with Swagger UI at `/docs` and ReDoc at `/redoc`.

> [!IMPORTANT]
> `DATABASE_URL` must use the `postgresql+asyncpg://` scheme. Point `TEST_DATABASE_URL` at a throwaway database: the test suite drops every table on teardown, so it must never share a database with `DATABASE_URL`.

Generate a JWT secret with:

```bash
python -c "import secrets; print(secrets.token_urlsafe(64))"
```

### 3. Frontend

In a new terminal:

```bash
cd frontend
npm install
```

Create `frontend/.env`:

```bash
VITE_API_URL=http://localhost:8000
VITE_GOOGLE_CLIENT_ID=your-google-oauth-client-id
```

`VITE_GOOGLE_CLIENT_ID` must match `GOOGLE_CLIENT_ID` in the backend `.env`. Leave it blank to run without Google Sign-In.

```bash
npm run dev
```

The app runs at `http://localhost:5173`.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Demo accounts

Every demo account signs in with the password `12345678`.

| Role | Email | What it demonstrates |
|---|---|---|
| **Campus Admin** | `shrestha@ds.study.iitm.ac.in` | Club approval queue, all clubs by status, college leaderboard |
| **Club Leader** | `aarav.menon@ds.study.iitm.ac.in` | Leads CodeCrafters with 5 members. Create and publish events, mark attendance, declare results, answer the issue queue, post announcements |
| **Member** | `sara.khan@ds.study.iitm.ac.in` | Holds 3 certificates (WINNER, RUNNER_UP, PARTICIPANT), plus notifications and event registrations |

<details>
<summary>More demo students</summary>

<br/>

All on `@ds.study.iitm.ac.in`: `diya.sharma`, `kabir.rao`, `ananya.iyer`, `meera.nair`, `rohan.gupta`, `ishita.bose`, `vikram.reddy`, `aditya.verma`, `nikita.joshi`, `arjun.pillai`.

</details>

### What the demo data covers

The demo runs on one full college, **IIT Madras BS Degree** (`ds.study.iitm.ac.in`). Club names, descriptions, logos and social links come from the real IITM BS societies. Every column of every table is populated and every enum value appears at least once.

| | Count | Details |
|---|:---:|---|
| **Clubs** | 7 | ACTIVE: CodeCrafters, IRIS, AKORD, RAAHAT. PENDING: Women in Tech. REJECTED: Heighers eSports. ARCHIVED: Deva-Bhasha Sanskrit Society |
| **Events** | 9 | 4 completed with results, 3 upcoming, 1 draft, 1 cancelled. One has no capacity limit |
| **Certificates** | 15 | Real PDFs with QR codes. 13 on S3 and 2 on the Postgres fallback path |
| **Memberships** | 23 | Approved, pending and rejected |
| **Announcements** | 7 | All 5 categories, 2 pinned |
| **Issues** | 6 | All 5 categories and all 3 statuses |
| **Notifications** | 10 | All 5 types |

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">

  <br>
</picture>


## Recognition

🏆 **Campus Connect won the Best Project Award** in the BSCS3001 Software Engineering Project, IIT Madras BS Degree (May 2026).

<div align="center">
  <img src="assets/award-certificate.png" alt="Best Project Award certificate" width="70%">
</div>


## Timeline

<a href="Milestones/Timeline.md">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/timeline-dark.svg">
  <img src="assets/timeline-light.svg" alt="Project timeline: five milestones from research on 28 June to final submission on 23 August 2026, then the Best Project Award" width="100%">
</picture>
</a>

Read the full dated breakdown in [`Milestones/Timeline.md`](Milestones/Timeline.md).

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/divider-dark.svg">
  <img src="assets/divider-light.svg" width="100%" alt="">
</picture>

## Team

**Team 003 (Nexmind)** 

| Member | Role | Commits | PRs (merged) | Branches |
|---|---|:---:|:---:|:---:|
| **Shrestha** | Backend and System Architect | 248 | 32 (27) | 21 |
| **Shrishti** | Frontend | 10 | 12 (10) | 10 |
| **Atharv** | Product Manager | 71 | 13 (13) | 7 |
| **Pawan** | Testing | 46 | 14 (13) | 13 |
| **Kavisha** | Scrum Master | 4 | 0 | 0 |
| `github-actions[bot]` | CI automation | 92 | 0 | 0 |
| | **Total** | **471** | **71 (63)** | **51** |


## Documentation

| Where | What |
|---|---|
| [`Summary.md`](Summary.md) | Project summary: problem, users, features, architecture and team |
| [`Milestones/Timeline.md`](Milestones/Timeline.md) | Dated project timeline from topic selection to the final submission |
| [`backend/README.md`](backend/README.md) | Backend setup, configuration and testing |
| [`frontend/README.md`](frontend/README.md) | Frontend setup, structure and design system |
| [`backend/openapi.yaml`](backend/openapi.yaml) | Full API spec with endpoints, user story mapping, role matrix and error catalogue |
| [`RULES.md`](RULES.md) | Team working agreement |

<br/>

<div align="center">

**Find your club. Build your story.**

Made by Team Nexmind | Thank you 🐻

Original repository: [Srivastava-Shrestha/MAY2026-Team-003](https://github.com/Srivastava-Shrestha/MAY2026-Team-003)

</div>
