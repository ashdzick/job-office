# The Job Office

A unified job search system: one assistant that routes between Analyzer, Company Researcher, Cover Letter, Tracker, and Content Writer. You set up Shared once (resumes, voice, preferences) and use one folder in Cowork or a Claude project. Natural language — "analyze this role," "research this company," "draft a cover letter," "what's in my pipeline" — and the system routes to the right tool and can chain between them.

---

## What's in the system

- **system-prompt.md** — The orchestrator. Load this as your system prompt or project instructions. It routes your messages to the right tool and handles handoffs (e.g. Analyzer → Cover Letter).
- **Shared/** — Pipeline (tracked roles), preferences (run the Analyzer once to create this), Resumes, and voice (voice-rules.md, avoid-patterns.md). All tools that need your data read from here.
- **Content-Writer/, Analyzer/, Company-Researcher/, Cover-Letter/, Tracker/** — Five tool folders. Each has its own system prompt and supporting files. The orchestrator loads them when you route to that tool.

---

## How to get started

1. **Clone or download** this folder.
2. **Fill Shared:** Add at least one resume to `Shared/Resumes/`. Fill in `Shared/voice/voice-rules.md` and `Shared/voice/avoid-patterns.md` so output sounds like you. Run the **Analyzer** once so it can create `Shared/preferences.md` (or add preferences manually). Until preferences exist, Company Researcher and Analyzer won't flag personal fit.
3. **Point your AI tool** at this folder and load the root `system-prompt.md` (see integration options below).
4. **Use it:** "Paste the job description," "research Acme Corp," "draft a cover letter for the role we just analyzed," "what's in my pipeline," "help me write a LinkedIn post."

---

## Recommended workflow

**Apply phase:** Find a role → **Analyzer** (fit score, qualifications, gaps) → **Company Researcher** (is the company worth it?) → **Cover Letter** (draft + resume suggestions) → **Tracker** (mark Applied, set follow-up). See [WORKFLOW.md](WORKFLOW.md) for the full sequence and flow diagram.

**Prep phase (when you get an interview):** Questions, STAR stories, prep doc. An Interview Prep tool is planned; until then you can use the Tracker to update status to Interviewing and log contacts.

---

## How to run it

**Cowork:** Store this folder on your machine, start a Cowork session, and point it at this folder. The orchestrator runs automatically. Research, analyses, and cover letters save to the folder; pipeline and indexes stay in sync.

**Claude project:** Create a project, add this folder as project knowledge, and paste the contents of `system-prompt.md` into Custom Instructions. Each conversation will have the Job Office available.

**Standalone:** You can also run a single tool by pointing your AI at that tool's folder (e.g. `Analyzer/` or `Cover-Letter/`) and loading its `system-prompt.md`. No orchestrator; that tool runs on its own.

---

## How the system grows

As you use it, the pipeline and indexes (Analyses, Research, Cover Letter Output) fill in. You can add roles manually in Tracker or run them through Analyzer and Company Researcher first. An Interview Prep tool is planned; when it exists, the chain will extend to prep docs and STAR stories. The system is designed so new tools plug in without changing the ones you already have.
