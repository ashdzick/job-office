# The Job Office

Analyze roles, research companies, write cover letters, and track your pipeline — all in one place, in natural language. Set it up once and use it like a colleague: "analyze this role," "research this company," "draft a cover letter," "what's in my pipeline."

## Getting started

You can run the Job Office two ways: in Cowork (recommended) or as a Claude Project.

**Option 1: Cowork (recommended)**

Requirements: A [Cowork](https://claude.ai) subscription.

1. Download or clone this repo to your computer.
2. Open Cowork, start a new session, and select this folder as your workspace.
3. Load `system-prompt.md` as your starting prompt.
4. On first use the system will offer to run setup — say yes. It takes about 5 minutes and asks for your preferences and resume.

After that, load `system-prompt.md` at the start of each session. That's your permanent entry point.

**Option 2: Claude Project**

Requirements: A Claude Pro, Team, or Enterprise subscription.

1. Create a new Project in Claude.
2. Paste the contents of `system-prompt.md` into the Project Instructions field.
3. Upload your resume and any other files from `Shared/` as Project knowledge.
4. Start a conversation and follow the onboarding prompts.

The Project approach means you don't need to load anything at the start of each conversation — the instructions are always active. The tradeoff is that file management is manual (you update uploads yourself rather than editing files directly).

## What's included

**Five tools, one orchestrator:**

The **Analyzer** scores job fit, breaks down qualifications, and flags gaps. The **Company Researcher** looks into funding, culture, and growth to help you decide whether a company is worth your time. The **Cover Letter** tool drafts letters in your voice using context from the analysis and research. The **Tracker** manages your pipeline. The **Content Writer** helps with LinkedIn and other job search content.

Everything routes through a single `system-prompt.md` so you only ever load one file.

**Shared memory across tools:**

All five tools read from a `Shared/` folder: your resumes, preferences, voice rules, and pipeline. Set it up once during onboarding and it stays current as you work.

## Recommended workflow

**When you find a role:**

1. Paste the job description into the Analyzer. Get a fit score, qualification breakdown, and resume suggestions.
2. Run Company Researcher on the company — funding, culture, whether it's worth pursuing.
3. Draft a cover letter with the Cover Letter tool. It uses your analysis and company research automatically.
4. Log the role in Tracker and mark it Applied when you send.

**When you get an interview:**

Update the Tracker to Interviewing. An Interview Prep tool (questions, STAR stories, prep doc) is on the roadmap.

See [WORKFLOW.md](WORKFLOW.md) for the full sequence and a flow diagram.

## File structure

```
/
├── system-prompt.md        # Load this. Routes everything.
├── ONBOARDING.md           # Runs automatically on first use
├── VOICE-QUIZ.md           # Optional — sets up your writing voice
├── WORKFLOW.md             # Full workflow guide
├── Shared/                 # Your data (resumes, preferences, pipeline, voice)
├── Analyzer/               # Job fit scoring and qualification breakdown
├── Company-Researcher/     # Funding, culture, and growth research
├── Cover-Letter/           # Drafts in your voice using analysis + research
├── Content-Writer/         # LinkedIn and job search content
└── Tracker/                # Application pipeline management
```

## Running individual tools

You can also run any tool on its own by loading its `system-prompt.md` directly. Useful if you only need one piece of the system.

