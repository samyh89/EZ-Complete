# Sources

All seven source prompts are by **ERIC AHI**. EZ-Complete combines them into three skills so the user has fewer doors to choose between when their brain is already overloaded. Originally framed for ADHD, but the underlying patterns (paralysis, time-blindness, drift, overwhelm, under-stimulation) are common enough that anyone can use this.

## The 7 original prompts

### 1. Task Paralysis Breaker
> "I'm staring at [Task] and I can't start. Break it into ridiculously small steps that each take less than 1 minute. Give me the very first step and tell me exactly what to do with my hands to begin."

### 2. Dopamine Menu Builder
> "I'm feeling under-stimulated. Create a dopamine menu for me with 5-minute appetizers for quick movement, 20-minute entrees for deep work, and 10-minute sides for creative play so I can stay engaged."

### 3. Virtual Body Double
> "Act as my virtual body double for the next 30 minutes. I'll tell you what I'm working on, and I want you to check in every 10 minutes to ask for a status update and help keep me focused."

### 4. Context-Switching Reset
> "I just finished [Task A] and need to start [Task B], but my brain is stuck. Create a 3-minute mental reset routine to help me switch between these two tasks."

### 5. Boring Task Gamifier
> "I have a boring task: [Task]. Help me gamify it by connecting it to my current interest: [Interest]. Turn it into a quest where completing the task unlocks a reward."

### 6. Time-Blindness Reality Check
> "I think [Project] will take 20 minutes, but it usually takes much longer. Help me time-map it by identifying 3 hidden sub-tasks I might be forgetting so I can set a realistic deadline."

### 7. Open Loops Organizer
> "My brain feels full of open loops. I'll dump everything I'm worried about below. Categorize them into Now, Later, and Trash, then give me a one-sentence next step for each Now item."

## How the 7 became 3

Seven choices is too many when your brain is the problem. We grouped them by **what state you're in**, not by what technique they use:

### `/start-task` — you have a task but can't get into it
Merges **#1 Paralysis Breaker**, **#6 Time-Blindness Check**, and **#5 Boring Task Gamifier**.
The skill triages first: *can't start / underestimating time / boring?* Then it runs the matching flow. All three share the same trigger ("there's a task and I'm not doing it") but need different responses.

### `/stay-on-task` — you're working (or trying to) and need help keeping the thread
Merges **#3 Virtual Body Double** and **#4 Context-Switching Reset**.
Body Double mode is rebuilt around a human-driven phone timer — the user sets the timer, types `check` when it rings, and the skill responds. This keeps the skill stateless (one turn in, one turn out) so it works the same in the CLI today and in a future web app.

### `/brain-reset` — your brain itself is in the wrong state
Merges **#7 Open Loops Organizer** and **#2 Dopamine Menu Builder**.
Branches on **overwhelmed (dump everything out)** vs **under-stimulated (give me something to engage with)** — the two opposite failure modes that both look like "I can't work right now".
