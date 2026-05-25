# EZ-Complete

Three small helpers you can call up by name when your brain isn't cooperating. Built originally with ADHD in mind, but honestly — task paralysis, time-blindness, boring chores, scattered focus, and overwhelm hit almost everyone. If any of that sounds like you, this is for you. Based on prompts by **ERIC AHI**.

## What is this?

EZ-Complete is an add-on that gives an AI assistant three new commands to help you actually get things done:

- **`/start-task`** — when there's a thing you need to do and you can't make yourself start.
- **`/stay-on-task`** — when you're working but keep drifting, or you just finished one thing and your brain won't move to the next.
- **`/brain-reset`** — when your head is either too full to think, or so empty that you're just scrolling.

You type the command, the helper asks you one short question, you answer, and it walks you through. That's it.

It works with **any AI chat tool that can load skills from markdown files** — Claude Code, other agent harnesses, or any setup that reads `SKILL.md`-style files. Nothing in the skills themselves is tied to one tool. If your assistant has a way to load skills, this works.

## Who is this for?

Anyone who struggles with starting, finishing, or staying with a task. That includes people with ADHD (diagnosed or not), but it also includes a lot of people who just have busy lives, bad days, or brains that don't always cooperate. The advice that assumes you already have executive function in stock doesn't help when you don't. These prompts meet you where you are.

## How to install

The plugin is just a folder of markdown files. Point your AI tool at them however it expects.

**Claude Code (plugin format):**
```
/plugin install ez-complete
```
Or copy the `plugin/` directory into your Claude Code plugins folder.

**Any other harness or agent that supports skills:**
Copy the three skill folders inside `plugin/skills/` (`start-task/`, `stay-on-task/`, `brain-reset/`) into wherever your tool looks for skills. Each one is a self-contained `SKILL.md` with frontmatter and instructions — no code, no dependencies.

**Bare minimum (any chat tool, no skill system):**
Open one of the `SKILL.md` files and paste its body into the chat. The assistant will follow it.

Once installed, the three commands show up when you type `/`.

## What each one does — one example each

### `/start-task`

> **You:** /start-task
> **Helper:** Quick check — which one is this? A) I can't start, B) I keep thinking it's quick but it never is, C) it's boring and I keep avoiding it.
> **You:** A. I have to file my taxes.
> **Helper:** Right now, do this: open the drawer where last year's tax folder is. Then: pull the folder out and put it on the table. Then: open it to the first page…

### `/stay-on-task`

> **You:** /stay-on-task
> **Helper:** Which one is this? A) body double, B) context switch.
> **You:** A. Working on the slides.
> **Helper:** Set a phone timer for 10 minutes. When it rings, come back and type **check**. I'll ask how it's going.
> *(10 minutes later)*
> **You:** check
> **Helper:** How's it going — still on slides, or did you drift?

### `/brain-reset`

> **You:** /brain-reset
> **Helper:** Which one is this? A) overwhelmed, B) under-stimulated.
> **You:** B. I've been scrolling for an hour.
> **Helper:** Here's a menu. Pick one. Appetizers (5 min): 1) walk to the mailbox and back, 2) do 20 jumping jacks, 3) refill your water bottle. Entrées (20 min): …

## Credit

All seven of the source prompts EZ-Complete is built on were written by **ERIC AHI**. See `SOURCES.md` for the originals and how they were grouped into the three skills.

## Files

- `plugin/` — the actual installable add-on
- `SOURCES.md` — the seven original prompts and the grouping rationale
- `SMOKE_TEST.md` — example conversations showing each skill working
