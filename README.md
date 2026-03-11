# The Job Office

A unified job search system: one assistant that routes between Analyzer, Company Researcher, Cover Letter, Tracker, and Content Writer. You set up Shared once (resumes, voice, preferences) and use one folder in Cowork or a Claude project. Natural language — "analyze this role," "research this company," "draft a cover letter," "what's in my pipeline" — and the system routes to the right tool and can chain between them.

---

## What's in the system

- **system-prompt.md** — The orchestrator. Load this and use it for everything. On first use it will offer to run setup (preferences and resume); after that it routes your messages to the right tool.
- **ONBOARDING.md** — The setup flow. You don't load it yourself — the system offers to run it when you're not set up yet.
- **VOICE-QUIZ.md** — Optional voice setup. The Cover Letter and Content Writer tools will offer to run it when your voice files aren't filled in yet.
- **Shared/** — Your data: pipeline, preferences, resumes, and voice rules. All tools read from here. Set up during onboarding; grows as you use the system.
- **Content-Writer/, Analyzer/, Company-Researcher/, Cover-Letter/, Tracker/** — Five tool folders. The orchestrator loads them automatically when you need them.

---

## New to Cowork?

Cowork is a desktop AI tool that works with files on your computer. Here's the basic idea:

1. You point Cowork at a folder on your machine — for the Job Office, that's this folder.
2. You start a session by loading a file as your "system prompt" — the instructions that tell the AI what to do.
3. The AI reads and writes files in your folder, so your analyses, cover letters, and pipeline all save automatically between sessions.

To load a file in Cowork: start a new session, select this folder as your workspace, and choose the file you want as the starting prompt.

---

## How to get started

1. **Download or clone** this folder to your computer.
2. **Start a Cowork session**, point it at this folder, and load **system-prompt.md** as your starting prompt. On first use the system will offer to run setup — say yes and it'll ask a few questions (preferences and resume), then drop you into the Job Office. Takes about 5 minutes.
3. **For future sessions**, load **system-prompt.md** again. That's your day-to-day entry point.
4. Before your first cover letter or content, the tools will offer to run voice setup if you haven't filled it in yet.

---

## Recommended workflow

**Apply phase:** Find a role → **Analyzer** (fit score, qualifications, gaps) → **Company Researcher** (is the company worth it?) → **Cover Letter** (draft + resume suggestions) → **Tracker** (mark Applied, set follow-up). See [WORKFLOW.md](WORKFLOW.md) for the full sequence and flow diagram.

**Prep phase (when you get an interview):** Questions, STAR stories, prep doc. An Interview Prep tool is planned; until then you can use the Tracker to update status to Interviewing and log contacts.

---

## How to run it

**Cowork:** Store this folder on your machine, start a Cowork session, and point it at this folder. On first use, the system will offer to run setup — say yes and it'll ask a few questions and get your preferences and resume in place, then drop you into the Job Office. For all future sessions, the system starts automatically. Research, analyses, and cover letters save to the folder; pipeline and indexes stay in sync.

**Claude project:** Create a project and add this folder as project knowledge. Paste `system-prompt.md` into Custom Instructions so the orchestrator runs automatically. On first use it will offer to run setup — say yes and it'll walk you through preferences and resume (it uses ONBOARDING.md from the project). Voice setup is offered by the Cover Letter and Content Writer tools when you need it.

**Standalone:** You can also run a single tool by pointing your AI at that tool's folder (e.g. `Analyzer/` or `Cover-Letter/`) and loading its `system-prompt.md`. No orchestrator; that tool runs on its own.

---

## How the system grows

As you use it, the pipeline and indexes (Analyses, Research, Cover Letter Output) fill in. You can add roles manually in Tracker or run them through Analyzer and Company Researcher first. An Interview Prep tool is planned; when it exists, the chain will extend to prep docs and STAR stories. The system is designed so new tools plug in without changing the ones you already have.
