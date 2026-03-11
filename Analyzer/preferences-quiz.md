# Preferences Quiz

Run this quiz when `../Shared/preferences.md` does not exist. Tell the user: "Before we dig into any roles, I want to set up your preferences file so I can flag jobs that don't fit what you're looking for. I'll ask you a few quick questions."

Ask the following questions one at a time, waiting for a response before moving to the next:

1. "Where do you want to work? Remote only, hybrid, in-person, or open to any?"
2. "Any geographic constraints? For example, only roles commutable to a specific city, or only US-based if remote?"
3. "What company size are you open to? For example, small (under 100), mid-size (100–1,000), or large/enterprise (1,000+)?"
4. "Is there a minimum salary or total comp you won't go below?"
5. "Are there any industries, company types, or causes you wouldn't work for?"
6. "Anything else that's a hard no — travel requirements, specific role structures, management vs. IC, or anything else you'd want flagged?"

After collecting all answers, write a summary back to the user in plain prose — not a list. Something like: "Here's what I've got: you're looking for [location/remote preference], [geography], [company size], with [compensation if they shared it]. [Industries or types they ruled out.] [Any other hard nos.]" Use their actual answers; this is just the structure. Ask them to confirm or correct anything before writing the file.

Once confirmed, output the completed preferences block in a code block so the user can copy it regardless of their setup:

```
# Job Preferences

## Location
[Their answer]

## Geography
[Their answer]

## Company Size
[Their answer]

## Compensation
[Their answer]

## Off-Limits
[Their answer]

## Other Hard Nos
[Their answer]
```

Then tell the user: "Here's your preferences file. Depending on how you're running this:
- **Cowork or Claude Code**: I'll save this as `Shared/preferences.md` in your workspace and load it automatically next session.
- **Claude Projects**: Add this as a file in your project knowledge and I'll pick it up on startup.
- **Plain chat session**: Copy this block and paste it at the start of any future session so I have your preferences on hand."

If you have access to a persistent workspace, save the file as `../Shared/preferences.md` now. If not, the copied block is sufficient.
