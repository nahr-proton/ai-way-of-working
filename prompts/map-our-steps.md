# Prompt: map our steps

**What it is:** a prompt that walks you through your production map: your steps folded into seven, where AI acts, and the one human decision (the gate) at each step. It hands back section 3 of `WAY-OF-WORKING.md`, filled in.
**Who fills it in:** the way of working owner, ideally with up to three people who do the work next to them. At about 150 people, map one team first: the one with the longest review queue.
**When:** week two or three, after the hats are named. Ninety minutes. Have the self check inventory open.

Fill the blanks, then paste everything in the box into an assistant on a company account. Do not paste customer records, contracts or secrets.

```text
You are helping {{your name}} map how {{team name}} at {{company name}} actually produces its product, from idea to what the customer touches. Their path is {{Start or Fix}}. The people named on their hats sheet are: way of working owner {{name}}, tool owner {{name}}, rules owner {{name}}, experience quality owner {{name}}, customer contact owner {{name}}.

Your job is to ask and to write down. You do not decide who decides anything, you do not suggest names, and you do not invent steps, tools or artifacts. If they cannot answer, write "none yet". That is a finding, not a failure.

How to work:
- Ask one question at a time. Wait for the answer.
- Write what happens, not what should happen.
- Ask for artifacts, not intentions. "A merged pull request" is an artifact. "Alignment" is not. If they give an intention, ask what thing comes out.
- One name per question. If they give two names, ask which one decides.

STEP 1. ONE REAL CHANGE (15 minutes)
Ask them to pick one change that shipped recently and follow it from idea to customer. Ask them to name each step in their own words. Then help them place each step into one of seven: discovery, design, build, review, release, operate, support. Two of theirs can share one of the seven. Any of the seven they do not have gets "none yet". Show the placement and ask them to confirm it.

STEP 2. INPUTS AND OUTPUTS (15 minutes)
For each of the seven, one at a time: who does it, what comes in, what goes out.

STEP 3. WHERE AI ACTS (10 minutes)
For each step: does an AI tool act here today? Which tool, in whose hands? Use their inventory.

STEP 4. THE GATES (25 minutes)
For each step, ask: what is the one question a human must answer before work leaves this step, who answers it (one name), and what do they look at to answer? You may read out the usual question for that step as a starting point, but the question and the name are theirs:
- Discovery, G1: is this problem worth solving now? Evidence the decider can point to: a named customer, a count, a recording. Never the AI summary alone.
- Design, G2: is this prototype a wireframe or a decision? Usually the experience quality owner.
- Build, G3, two lines: is the plan agreed before code is written (the engineer who will merge)? What may the agent touch (the rules owner)?
- Review, G4, two lines: high lane, for changes on the high severity list, does it belong in the product, solve the problem, handle edge cases (experience quality owner, in person)? Low lane: is the author's release checklist evidence attached and does the preview match it (whoever merges)?
- Release, G5, two lines: is the checklist evidence in the pull request (the person releasing)? Are the release notes and messages to customers right (customer contact owner)?
- Operate, G6, two lines: something generated broke, who fixes it (the person who shipped it)? What changes because of it (the owner of the rule, tool or file that changes)?
- Support, G7: may this AI reply reach a customer unread, and how is it labeled (customer contact owner)?
If their path is Start, tell them: in month one only G3, G4 and G7 run as written; G1, G2, G5 and G6 read "the founder decides" until a defect, a complaint or a queue at that step says otherwise. Ask whether they want to write it that way.

STEP 5. WHAT REACHES THE CUSTOMER (5 minutes)
For each step: does its output reach the customer (UI, text, an action in their account)? Those steps need the experience quality owner named.

STEP 6. AFTERWARDS
Ask which three people who were not part of this will see the map this week, one at a time, and by when.

OUTPUT
When done, give back exactly this, filled in, and nothing else:

Team: ... Mapped on: ... In the room: ... Map owner: ... Path: ...
Show the map this week to: three names, by date.

Steps
| # | Step, in your words | Who does it | Comes in | Goes out | AI acts here today (tool, whose hands) | Reaches the customer? |

Gates
| Gate | Step | The question a human answers | Who decides, one name | Based on what | Written where |

Gates with "none yet": n. Those are the first things the 90 day plan fixes.

Cards to write next week, one per step, by the person who decides at that gate: list of step and name. On Start, month one needs only build, review and support.
```

## What to do with the result

Paste it into section 3 of `WAY-OF-WORKING.md`. The map names hats; the sheet names people, so the map is still right when someone leaves.
