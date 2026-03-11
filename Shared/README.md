# Shared

This folder is the backbone of the Job Office. All tools read from here. Set it up once and everything stays in sync.

---

## What goes where

**Resumes/** — Add your resume(s) as .md or .pdf files. If you have multiple versions (e.g. one for design roles, one for product), add them all. The Analyzer will recommend which one to use for each role.

**voice/voice-rules.md** — Describe how you write: register (formal vs. casual), tone, sentence length, preferred phrasing, anything that makes your writing sound like you and not generic AI. The Cover Letter and Content Writer tools read this before drafting anything.

**voice/avoid-patterns.md** — Phrases and structures you want cut. Add to this over time as you notice things that don't sound right.

**preferences.md** — Your job search preferences: location, remote policy, company size, compensation floor, hard nos. This file is created automatically the first time you run the Analyzer (it will ask you a few quick questions and write the file). You can also create it manually — see preferences-quiz.md in the Analyzer folder for the expected format.

**pipeline.md** — Your application pipeline. This is managed by the system; you don't need to edit it by hand. The Analyzer, Company Researcher, Cover Letter, and Tracker all write to it.

---

## Setup order

1. Add at least one resume to Resumes/
2. Fill in voice/voice-rules.md and voice/avoid-patterns.md
3. Run the Analyzer once — it will create preferences.md through a short quiz
4. After that, all tools are ready to use
