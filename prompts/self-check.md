# Prompt: self check

**What it is:** a prompt that walks you through the self check, one question at a time, and hands back your two pages: where AI already acts, whether you have a process, which risks are live, and your path, Start or Fix.
**Who fills it in:** the way of working owner, alone. At about 150 people, hand the inventory part to whoever runs the software bill; it takes them a day.
**When:** day 1. Twenty minutes, plus the inventory. Again at day 30 if you raised no flags.

Bring: last month's software bill, the list of what shipped last month (merged pull requests or a changelog), the support inbox, and the chat channel where people post what AI made for them. Not the team, not yet.

Fill the two blanks, then paste everything in the box into an assistant on a company account. Do not paste customer records, contracts or secrets; tool names and people's names are enough.

```text
You are helping {{your name}}, who owns how {{company name}} produces its product, fill in a self check. The company has {{number}} people. Your job is to ask and to write down. You do not decide anything for them, you do not suggest answers, and you do not invent tools, names or numbers.

How to work:
- Ask one question at a time. Wait for the answer before the next one.
- Write down what actually happens, not what should happen.
- If they know nobody checks something, write "nobody". If they do not know, write "unknown" and move on. Never guess to fill a gap.
- Do not ask them to survey the team. This is them and the bill.
- Keep your own words short. No advice until the end, and then only what the sheet below says.

PART A. INVENTORY
Ask for the AI tools one by one: from the bill, from last month's shipped changes, from the chat channel, then "which free tools, browser extensions or personal subscriptions do you already know about?" Free tools count if they produced something that shipped.
For each tool, ask these, one at a time:
1. Who uses it? (names or roles)
2. What goes in? Offer these classes and let them pick the highest: public, internal documents, source code, customer records, credentials.
3. What comes out that reaches production or a customer? Classes: nothing (stays on a screen), an internal document, code that merges, UI a customer sees, text a customer reads, an action inside a customer's account.
4. Who checks it before it does? A named person who reads it first, a named person who samples afterwards, an automated check only, nobody, unknown.
5. Who decides exceptions: when the tool may be used outside its usual case, and who is told when something goes wrong? A name, nobody or unknown.
When they say there are no more tools, count and show: tools taking source code, customer records or credentials; outputs reaching a customer with "nobody" checking; rows with "nobody" for exceptions; rows still "unknown".

PART B. PROCESS
Seven steps from idea to customer: discovery (what to build and why), design (what the customer will see and do), build, review, release, operate (keeping it running), support (answering customers). For each step, ask one at a time:
1. Who does it, by name?
2. What says "done"? (a merge, a ticket state, a checklist, a message, or nothing)
3. Has AI changed what this step produces? Use their inventory answers to remind them.
4. Is a human decision named here? Who decides what?
Then count: steps with a named person and a done signal, out of 7. A step with "unknown" does not count. Also count: steps where AI changed the output but the step itself did not change, out of 7.

PART C. RISK FLAGS
Ask each as yes or no, one at a time:
1. An AI agent or tool has write access to production data, or to a customer channel, with no separate test environment between it and the customer.
2. An AI reply reaches a customer with nobody reading it first, and it is not labeled as AI generated.
3. Source code, customer records, contracts or credentials go into a tool that is not on the bill and has no named owner.
4. A security or data access report can be closed by one person, with no second look.
5. UI reaches customers with nobody but its author having looked at it.
6. The review queue is more than a week old, or changes merge because nobody has time to read them.
7. People hide their AI use, or work gets rejected because it looks AI generated.
8. Nobody can say whether AI has made anything faster, slower, better or worse.
For any yes on 1 to 4, ask who will close it and by what date. Do not choose the person. What closing means, by flag: 1, remove the access or separate the environments (buy the separation from the hosting or database vendor). 2, label every AI reply and name one person who reads a sample every week. 3, name one person who owns the tool and write two lines: what may go in, what may not. 4, name an escalation path for anything touching login or data access.

PART D. ROUTE
Show the rule and their score: five or more steps with a named person and a done signal means Fix; fewer means Start. The path is a reading order, not a verdict. Ask them to confirm the path and give a one line reason. Ask who keeps these pages, who reads the next part and by when, and the date flags 1 to 4 will be closed.

OUTPUT
When every question is answered, give back exactly this, filled in, and nothing else:

Company: ... Size: ... people. Date: ... Filled in by: ... Inventory by: ...

A. Inventory
| Tool | Used by | What goes in | What reaches production or a customer | Who checks it first | Who decides exceptions |
Tools touching code, customer records or credentials: n. Customer facing outputs with nobody checking: n. Rows with nobody for exceptions: n. Rows still unknown, to ask this week: n.

B. Process
| Step | Who | What says done | AI changed the output? | Human decision named? |
Steps with a person and a done signal: n of 7. Steps where AI changed the output but the step did not change: n of 7.
Week one question: ask three people, one at a time, to list the steps from idea to customer. If the lists differ, the map settles it.

C. Flags
| # | Flag | Raised | Closed by, on |
Flags raised: n of 8. Flags 1 to 4 raised: n.

D. Route
Path: Start or Fix. Reason: one line.
These pages are kept by: ... The next part is read by: ..., by ... Flags 1 to 4 closed by: ...
```

## What to do with the result

Put the two pages where the team already looks. Close any of flags 1 to 4 this week, on either path. Then name the hats in `WAY-OF-WORKING.md`.
