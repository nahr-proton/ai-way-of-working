# Way of working

**What it is:** three sheets on one page: who wears which hat, who decides what, and your production map with a named human decision at every step.
**Who fills it in:** the way of working owner, whoever runs how the team produces (founder, CTO, Head of Product, COO).
**When:** the hats and decision rights in week one: an afternoon to name them, confirmed within the week. The map in week two or three, ninety minutes. Review every three months.

Put the finished page where the team already looks, not in a new tool. A hat is a set of decisions added to a job someone already has. Nobody is hired for it, and the org chart stays as it is.

---

## 1. Hats

Company size today: {{number}} people. Path: {{Start or Fix}}. Sheet owner: {{name}}. Review date: {{date, three months from now}}.

| Hat | Decides | Name | Since | Hours per week | Backup when away |
|---|---|---|---|---|---|
| Way of working owner | Any change to a production step. Who wears which hat | {{name}} | {{date}} | {{hours}} | {{name}} |
| Tool owner | Whether a tool comes in or stays. Keeps the inventory | {{name}} | {{date}} | {{hours}} | {{name}} |
| Rules owner | Data sources, agent access, exceptions. Keeps the one page policy | {{name}} | {{date}} | {{hours}} | {{name}} |
| Experience quality owner | Whether AI generated UI or copy is fit to ship. Keeps `patterns.md`, the severity scale, the high severity list, the release checklist | {{name}} | {{date}} | {{hours}} | {{name}} |
| Practice champion, optional below about 50 people | Nothing. Runs the demo slot and keeps shared prompts tidy | {{name or none}} | {{date}} | {{hours}} | none needed |
| Customer contact owner, one name for the 90 days | Whether an AI reply reaches a customer unread, and how it is labeled. Not the words on screens | {{name}} | {{date}} | {{hours}} | {{name}} |

Rules for filling it in:

| Rule | At about 25 people | At about 80 | At about 150 to 200 |
|---|---|---|---|
| One name per hat. Two names is a committee | Yes | Yes | Yes |
| Most hats per head | Three | Two | One, except the way of working owner, who may also hold rules |
| Tool owner and rules owner | The same person, beyond the 90 days too | Separate | Separate |
| Experience quality owner | A designer if there is one, otherwise the PM, never an engineer | The same | One designer holds the company hat for two quarters; the others hold it in their areas |

Whoever merges, publishes or sends an AI generated change owns it as if they made it by hand. That is a rule, not a hat, so it needs no name here.

Hours per head, added up: {{name}}: {{hours}}. {{name}}: {{hours}}. {{name}}: {{hours}}. What each of them stops doing to make room: {{one line per head}}.

The PM's own high lane changes and prototypes go to: {{the founder who talks to customers most}}.

At a small design team, company hat holder: {{name}}, until {{date}}, with {{hours}} hours a week off {{other work}}. Their decisions are confirmed in writing by {{way of working owner}}. Disagreements between designers go to the hat holder. Between the hat holder and a PM: {{way of working owner}}.

---

## 2. Decision rights

Decides: one person says yes or no. Consulted: asked before, with a date to answer by; silence by that date means the decider decides. Informed: told after, in writing, where people already read. No row creates a meeting.

| Decision | Decides | Consulted, and by when | Informed, where |
|---|---|---|---|
| A new AI tool comes in | {{tool owner}} | {{rules owner}}, if it touches customer data, code or credentials; decision within two working days | {{weekly note, channel}} |
| A data source is allowed into an AI tool | {{rules owner}} | {{tool owner}}, {{whoever handles that data}}; decision within five working days | {{where}} |
| An agent gets write access to a system | {{rules owner}} | {{tool owner}}, {{engineer running the agent}}; decision within three working days | {{way of working owner}} |
| AI generated UI ships to customers | {{experience quality owner}} for the high lane; whoever merges for the low lane | {{PM}} on whether it should exist, {{engineer}} on how it is built | {{where}} |
| An AI reply reaches a customer unread | {{customer contact owner}} | {{experience quality owner}}, {{rules owner}} | {{way of working owner}} |
| A production step changes | {{way of working owner}} | {{the hat owners the step touches}} | {{everyone, where}} |
| An exception to a rule | {{rules owner}}, logged with an end date at {{location}} | {{who asked}} | {{tool owner}} |
| Something AI generated broke | The person who shipped it fixes it and writes three lines: what happened, what the tool did, what changes | {{tool owner}}, {{rules owner}}, {{experience quality owner}} if a user saw it | {{way of working owner}} |
| Who wears which hat | {{way of working owner}} | The person taking the hat | {{everyone, where}} |

**Fix path only: who decides today.** Fill the middle column before the right one. Change only the rows where they differ. If more than three differ, pick three for this quarter.

| Decision | Who decides today, in practice | Who decides from {{date}} | Changes? |
|---|---|---|---|
| A new AI tool comes in | {{name or "whoever expenses it"}} | {{name}} | {{yes or no}} |
| A data source is allowed into an AI tool | {{name or "nobody"}} | {{name}} | {{yes or no}} |
| An agent gets write access | {{name or "whoever sets it up"}} | {{name}} | {{yes or no}} |
| AI generated UI ships | {{name or "whoever merges"}} | {{name}} | {{yes or no}} |
| An AI reply reaches a customer unread | {{name or "the tool"}} | {{name}} | {{yes or no}} |
| A production step changes | {{name}} | {{name}} | {{yes or no}} |

The three things that change this quarter: {{one}}, {{two}}, {{three}}. What stays the same for everyone else: {{one sentence}}.

---

## 3. Production map

Team: {{name}}. Mapped on: {{date}}. Map owner: {{way of working owner}}. Path: {{Start or Fix}}.

How to fill it: follow one real recent change from idea to customer and write what actually happened, not what should have. Ninety minutes, best with three people who do the work (`prompts/map-our-steps.md` walks you through it). Then show the map to three people who were not there, one at a time: {{three names}}. Where they would draw it differently: {{where, or nowhere}}.

**Start minimum.** On the Start path, month one runs only three gates as written: G3 (plan before code), G4 (review lanes) and G7 (AI replies to customers). G1, G2, G5 and G6 read "the founder decides" until a signal says otherwise: a defect, a complaint or a queue at that step.

### Steps

Fold your own steps into the seven. Write "none yet" where you have no such step.

| # | Step, in your words | Who does it | Comes in | Goes out | AI acts here today (tool, whose hands) | Reaches the customer? |
|---|---|---|---|---|---|---|
| 1 Discovery | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 2 Design | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 3 Build | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 4 Review | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 5 Release | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 6 Operate | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |
| 7 Support | {{step}} | {{name}} | {{artifact}} | {{artifact}} | {{tool, name or none}} | {{yes or no}} |

Artifacts, not intentions: "a merged pull request" is an artifact, "alignment" is not.

### Gates

A gate is the one question a named person answers before work leaves a step, on evidence, never because a tool said it was fine. One name per question; a gate with two questions has two lines. The questions below are the defaults; reword them if yours differ.

| Gate | The question | Usually decided by | Who decides, one name | Based on what | Written where |
|---|---|---|---|---|---|
| G1 Discovery | Is this problem worth solving now? | The PM, or the founder who talks to customers most | {{name}} | {{customer evidence: a named customer, a count, a recording; never the AI summary alone}} | {{where}} |
| G2 Design | Is this prototype a wireframe or a decision? | Experience quality owner | {{name}} | {{answers the G1 problem, follows patterns.md, handles empty, error and first time states}} | {{where}} |
| G3 Build | Is the plan agreed before code is written? | The engineer who will merge | {{name}} | {{the design output, the data contract}} | {{where}} |
| G3 Build | What may the agent touch? | Rules owner (approval A3) | {{name}} | {{the access list; separate environments, no write to production}} | {{where}} |
| G4 Review, high lane | Does this belong in the product, does it solve the problem, does it handle edge cases? | Experience quality owner, in person | {{name}} | {{the preview, opened before the diff; the high severity list}} | {{where}} |
| G4 Review, low lane | Is the author's release checklist evidence attached, and does the preview match it? | Whoever merges | Whoever merges | {{the evidence in the pull request; the preview}} | {{where}} |
| G5 Release | Is the release checklist evidence in the pull request? | The person releasing | {{name}} | {{the evidence, not the demo}} | {{where}} |
| G5 Release | Are the release notes and messages to customers right? | Customer contact owner | {{name}} | {{a read against the written standard}} | {{where}} |
| G6 Operate | Something generated broke: who fixes it? | The person who shipped it | The person who shipped it | {{three lines: what happened, what the tool did, what changes}} | {{where}} |
| G6 Operate | What changes because of it? | The owner of the rule, tool or file that changes | {{name}} | {{the three lines; the monthly numbers}} | {{where}} |
| G7 Support | May this AI reply reach a customer unread, and how is it labeled? | Customer contact owner | {{name}} | {{the reply class list; a weekly sample read}} | {{where}} |

Gates with "none yet": {{n}}. Those are the first things the 90 day plan fixes.

### The card the team gets

One per step, written in the week after the map by the person who decides at that gate. About twenty minutes each. On the Start path, month one needs only three: build, review and support.

| Step | Gate | Who decides | Based on what | What goes wrong for the user if this is skipped | Written by, on |
|---|---|---|---|---|---|
| {{step}} | {{the question}} | {{one name}} | {{evidence}} | {{one line}} | {{name, date}} |

### First use case

Score each candidate 1 low to 3 high. The first one has value 2 or 3, and risk, effort and experience impact all at 1. It is usually a review habit, not a new tool: the reviewer opens the preview before the diff, or the engineer agrees the plan before the agent writes code.

| Candidate | Step | Value | Risk | Effort | Experience impact | Verdict |
|---|---|---|---|---|---|---|
| {{candidate}} | {{step}} | {{1 to 3}} | {{1 to 3}} | {{1 to 3}} | {{1 to 3}} | {{first, later, no}} |

First use case: {{candidate}}. Team: {{name}}. Owner: {{name}}. Starts: {{date}}. Ends: {{date, 30 days later}}. The number we will read at the end: {{one number from sheets/scorecard.csv}}.

Next review of this page: {{date}}, by {{name}}.
