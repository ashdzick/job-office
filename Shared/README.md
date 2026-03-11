# Shared

This folder is the backbone of the Job Office. All tools read from here. Set it up once and everything stays in sync.

---

## What goes where

**Resumes/** — Add your resume(s) as .md or .pdf files. If you have multiple versions (e.g. one for design roles, one for product), add them all. The Analyzer will recommend which one to use for each role.

**voice/voice-rules.md** — Describe how you write: register (formal vs. casual), tone, sentence length, preferred phrasing, anything that makes your writing sound like you and not generic AI. The Cover Letter and Content Writer tools read this before drafting anything.

**voice/avoid-patterns.md** — Phrases and structures you want cut. Add to this over time as you notice things that don't sound right.

**preferences.md** — Your job search preferences: location, remote policy, company size, compensation floor, hard nos. This file is created when you run **ONBOARDING.md** from the Job Office folder. Until it exists, the Analyzer and Company Researcher will prompt you to run onboarding so they can flag personal fit.

**pipeline.md** — Your application pipeline. This is managed by the system; you don't need to edit it by hand. The Analyzer, Company Researcher, Cover Letter, and Tracker all write to it.

---

## Setup order

1. Run **ONBOARDING.md** from the Job Office folder first — it creates preferences.md and gets your resume into Resumes/
2. Fill in voice/voice-rules.md and voice/avoid-patterns.md when you're ready to draft cover letters or content (or run VOICE-QUIZ.md)
3. After that, all tools are ready to use
