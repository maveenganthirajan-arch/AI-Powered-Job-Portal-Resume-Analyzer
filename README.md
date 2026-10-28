# TalentGlass AI — AI-Powered Job Portal & Resume Analyzer
### Complete Full-Stack Project Blueprint · Glassmorphism UI · 2026

TalentGlass AI is a production-ready, full-stack recruitment platform and intelligent ATS resume matching engine built using the **2026 Glassmorphism Design System**, **Next.js 14 App Router**, **TypeScript**, **Prisma ORM**, and an explainable **40/25/20/15 AI matching engine**.

---

## 📖 Table of Contents
1. [Quick Start & How to Run](#-quick-start--how-to-run)
2. [One-Click Demo Portals & Credentials](#-one-click-demo-portals--credentials)
3. [13 Complete Project Blueprint Sections](#-13-complete-project-blueprint-sections)
4. [Design System & Glassmorphism Rules](#-design-system--glassmorphism-rules)
5. [Architecture & Database ER Schema](#-architecture--database-er-schema)
6. [Explainable AI Matching Engine (40/25/20/15)](#-explainable-ai-matching-engine-40252015)
7. [REST API Route Handlers](#-rest-api-route-handlers)
8. [Production Deployment (Vercel + PostgreSQL)](#-production-deployment-vercel--postgresql)
9. [Troubleshooting & FAQs](#-troubleshooting--faqs)

---

## 🚀 Quick Start & How to Run

### Prerequisites
- **Node.js**: `v18.17.0` or higher (tested with `v24.x`)
- **npm**: `v9.x` or higher

### Step 1: Clone or Navigate to Project
```powershell
cd "c:\Users\MAVEEN G\Downloads\AI-Powered Job Portal & Resume Analyzer"
```

### Step 2: Install Dependencies
```powershell
npm install
```

### Step 3: Initialize Database & Seed Authentic Blueprint Data
TalentGlass AI uses a local SQLite database by default with zero configuration required, and is 100% compatible with PostgreSQL:
```powershell
# Sync database schema
npm run db:push

# Seed with authentic blueprint data (John Doe, Sarah Wilson, Google, Meta, Figma roles)
npm run db:seed
```

### Step 4: Run the Development Server
```powershell
npm run dev
```

Open your browser and navigate to:
👉 **[http://localhost:3000](http://localhost:3000)**

*(If port 3000 is occupied by another app, Next.js will automatically launch on [http://localhost:3001](http://localhost:3001).)*

### Step 5 (Optional): Run Production Build
```powershell
# Create optimized production build
npm run build

# Start production server
npm run start
```

---

## 🔑 One-Click Demo Portals & Credentials

The top navigation bar features a **One-Click Demo Switcher Pill** allowing you to switch instantly between Candidate and Recruiter views without logging out.

Alternatively, you can sign in directly from `/login`:

| Role | Name | Email | Password | Pre-loaded Data & Features |
|---|---|---|---|---|
| **Candidate** | John Doe | `john@example.com` | `password123` | 12 Applications (Google, Meta, Amazon, Figma, Netflix), 78% Resume Match Score, Profile Skills & Work History |
| **Recruiter** | Sarah Wilson | `sarah@techcorp.com` | `password123` | Google & TechCorp Org, 5 Active Jobs, 128 Applicants Pipeline, Stage Advancements (Interview, Shortlist, Reject) |

---

## 🗺 13 Complete Project Blueprint Sections

Visit the interactive visual inspector in the running app at **`/blueprint`** to explore all diagrams interactively!

### 1. Candidate Dashboard (`/candidate/dashboard`)
- **Welcome Banner**: "Welcome back, John!"
- **Metric Cards**: Applied Jobs (12, `+2 this week`), Interviews (3, `+1 this week`), Offers (0).
- **Recommended Openings**: Frontend Developer @ Google ($100k-$150k), Full Stack @ Meta ($90k-$130k), Software Engineer @ Microsoft ($110k-$160k).
- **Radial Score Gauge**: Dual-ring SVG gauge displaying **78% Good Match** with direct link to the analyzer.

### 2. Job Search Page (`/jobs`)
- **Hero Banner**: "Find Your Dream Job" with neon backdrop glow.
- **Search Bar**: Keyword search + Location filter with real-time query updates.
- **Category Chips**: Technology (12k+ jobs), Marketing, Design, Finance, Healthcare.
- **Job Cards**: Company monogram/logo, compensation badge, skill pills, 1-click apply modal.

### 3. Job Details Page (`/jobs/[id]`)
- **Header**: Senior Frontend Developer @ Google, Remote · Full-time, $100k - $150k.
- **Actions**: "Apply Now" (opens interactive modal) and "Save Job" bookmarking.
- **Content Tabs**: Overview, Requirements, Benefits, and Company information.
- **Job Highlights Sidebar**: Employment type, location, experience level, required tech stack chips.

### 4. Application Tracker (`/candidate/applications`)
- **Filter Tabs**: All (10), Applied (5), Interview (3), In Review (1), Offer (0), Rejected (1).
- **Application Table**: Role, company, status badge, applied date, snapshot match score.

### 5. Resume Analyzer Dashboard (`/candidate/resume`)
- **File Upload Area**: Drag & drop zone supporting PDF, DOCX, and TXT (5MB max).
- **Role Target Selector**: Compare against specific job postings or general benchmarks.
- **Analysis Results**: 78% overall score circular gauge, breakdown bars, Strengths list, Missing Skills list, Suggestions list, and AI Match assessment.

### 6. Recruiter Dashboard (`/recruiter/dashboard`)
- **Hiring Overview**: Total Jobs (5), Total Applicants (128), Shortlisted (18), Interviews (7).
- **Recent Applicants Table**: Alex Carter, Priya Sharma, Rahul Mehta, Emily Davis, James Wilson.
- **Direct Status Advancement**: 1-click status transitions and candidate inspection drawer.

### 7. System Architecture (`/blueprint`)
- Multi-tier visual diagram showing Client tier, Next.js application core, and persistence layer.

### 8. Database ER Diagram (`/blueprint#er`)
- Relational mapping of 10 Prisma models: `User`, `CandidateProfile`, `Company`, `Job`, `Resume`, `ResumeAnalysis`, `Application`, `SavedJob`, `Interview`, `Notification`.

### 9. Candidate Flow (`/blueprint#pipeline`)
- 4-step candidate journey from registration to real-time status tracking.

### 10. Resume Analysis Pipeline (`/blueprint#pipeline`)
- 6-step processing sequence: Upload -> Extract -> Normalize -> AI Provider -> Zod Validation -> Save & Show.

### 11. AI Matching Logic (`/blueprint#matching`)
- **Required Skills Match**: 40%
- **Relevant Experience**: 25%
- **Project Relevance**: 20%
- **Education / Certifications**: 15%

### 12. Development Timeline (`/blueprint#timeline`)
- Phased 8-stage roadmap covering Days 1–30.

### 13. Deployment Blueprint (`/blueprint#deployment`)
- Deployment architecture for Vercel, Managed PostgreSQL, and private cloud storage.

---

## 💎 Design System & Glassmorphism Rules

```css
/* Signature 2026 Glass Card */
.glass-card {
  background: rgba(255, 255, 255, 0.07);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.14);
  border-radius: 20px;
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.18);
}
```

- **App Background**: Midnight navy (`#0B1020`)
- **Primary Accent**: Electric violet (`#7C5CFC`)
- **AI Highlights**: Aqua (`#35D6C5`)
- **Cards**: Translucent frosted white with subtle ambient borders
- **Lighting**: Ambient radial violet and aqua glow orbs in corners

---

## 🏛 Architecture & Database ER Schema

### System Architecture
```
[ Candidates & Recruiters ]
         │ (HTTPS / Responsive UI)
         ▼
[ Next.js 14 App Router ]
   ├── Server Components (Fast SSR)
   ├── Route Handlers (/api/*)
   └── AI Orchestrator (40/25/20/15 Rubric)
         │
    ┌────┴──────────────────────────────┐
    ▼                                   ▼
[ Prisma ORM & Database ]       [ AI Providers ]
  ├── SQLite (Zero-config local)   ├── Google Gemini 1.5 Flash
  └── PostgreSQL (Neon/Supabase)   ├── OpenAI GPT-4o-mini
                                   └── Local Heuristic Fallback
```

### Relational Database Models
- **`User`**: Base identity (Candidate or Recruiter), email (unique), avatar, role.
- **`CandidateProfile`**: 1:1 with User, headline, bio, experience years, skills, education JSON.
- **`Company`**: 1:1 with Recruiter, name, logo, industry, team size, website.
- **`Job`**: 1:N with Company, title, location, salary range, requirements, skills, status.
- **`Resume`**: 1:N with User, uploaded file, extracted text, parsed skills dictionary.
- **`ResumeAnalysis`**: 1:1 with Resume & Job, overallScore, 4 breakdown scores, strengths, missing skills, suggestions.
- **`Application`**: Unique compound key `[candidateId, jobId]`, status enum, matchScore snapshot.
- **`Interview`**: Scheduled interview records linked to applications.
- **`SavedJob`**: Bookmarked jobs per candidate.
- **`Notification`**: Real-time alerts for application reviews and interview invites.

---

## 🧠 Explainable AI Matching Engine (40/25/20/15)

TalentGlass AI avoids black-box ranking and implements an **explainable 100% weighted scoring rubric**:

$$\text{Total Score} = (0.40 \times \text{Skills}) + (0.25 \times \text{Experience}) + (0.20 \times \text{Projects}) + (0.15 \times \text{Education})$$

1. **Required Skills Match (40% Weight)**: Evaluates exact and semantic intersection of candidate skills against job requirements.
2. **Relevant Experience Match (25% Weight)**: Scores seniority, role tenure, and domain alignment.
3. **Project Relevance Match (20% Weight)**: Analyzes measurable metrics (e.g. latency drop, performance optimization, scale, microservices).
4. **Education or Certifications Match (15% Weight)**: Degrees in CS/STEM, accredited bootcamps, and cloud certifications.

> [!NOTE]
> **API Flexibility**: If a `GEMINI_API_KEY` or `OPENAI_API_KEY` is set in `.env`, the engine queries LLM APIs with structured JSON schema output and prompt-injection shielding. If no key is configured, it seamlessly executes the smart built-in deterministic matching engine with zero latency.

---

## 🌐 REST API Route Handlers

All endpoints validate inputs with **Zod** and verify session authorization:

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/auth/login` | Authenticate user credentials & set session cookie |
| `POST` | `/api/auth/register` | Register new Candidate or Recruiter |
| `GET` | `/api/auth/me` | Fetch active session & candidate/recruiter stats |
| `POST` | `/api/auth/me` | One-click instant role toggle (`CANDIDATE` ↔ `RECRUITER`) |
| `GET` | `/api/jobs` | Search & filter jobs with pagination |
| `POST` | `/api/jobs` | Create new job posting (recruiter role required) |
| `GET` | `/api/jobs/:id` | Fetch full job details |
| `POST` | `/api/resumes/upload` | Upload & extract PDF, DOCX, or TXT resume |
| `GET` | `/api/resumes` | Retrieve user's resume library |
| `POST` | `/api/ai/analyze` | Run 40/25/20/15 AI matching analysis |
| `POST` | `/api/applications` | Submit job application with resume & match snapshot |
| `GET` | `/api/applications/me` | List candidate's submitted applications |
| `PATCH` | `/api/applications/:id/status` | Recruiter stage advancement (Shortlist, Interview, etc.) |
| `GET/POST`| `/api/saved-jobs` | Fetch or toggle saved bookmarks |
| `GET` | `/api/notifications` | Fetch user alerts & interview invites |

---

## 📦 Production Deployment (Vercel + PostgreSQL)

### 1. Managed PostgreSQL (Neon / Supabase / AWS RDS)
1. In `prisma/schema.prisma`, update the datasource provider:
   ```prisma
   datasource db {
     provider = "postgresql"
     url      = env("DATABASE_URL")
   }
   ```
2. In `.env`, add your PostgreSQL connection URL:
   ```env
   DATABASE_URL="postgresql://user:password@ep-sample.neon.tech/talentglass?sslmode=require"
   ```
3. Run `npm run db:push` to sync tables.

### 2. Deploying to Vercel
1. Push the repository to GitHub.
2. Import project in [Vercel](https://vercel.com).
3. Set Environment Variables: `DATABASE_URL`, `NEXTAUTH_SECRET`, and optionally `GEMINI_API_KEY` / `OPENAI_API_KEY`.
4. Deploy! Next.js App Router will serve both edge pages and serverless API handlers automatically.

---

## ❓ Troubleshooting & FAQs

- **Q: How do I re-seed sample data?**  
  Run `npm run db:seed`. It will refresh the database with candidate John Doe, recruiter Sarah Wilson, and 5 featured tech jobs.
- **Q: Port 3000 is already in use?**  
  Next.js automatically falls back to port 3001, or you can specify a port: `node ./node_modules/next/dist/bin/next dev -p 3005`.
- **Q: Where are uploaded resumes saved?**  
  In local development, files are securely stored in `/public/uploads/resumes/`. In production, set S3 environment variables to use private S3/R2 storage.
