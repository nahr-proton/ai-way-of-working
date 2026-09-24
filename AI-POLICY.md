# AI use policy, one page

**What it is:** the one page of rules for AI at work: what is allowed, with what data, and who says yes first. Everything above the line is the page you post; the notes below it are for you.
**Who fills it in:** the rules owner, whoever sets these rules. At about 25 people, the founder or CTO.
**When:** a day to fill in. Post it within the week and read it aloud at a meeting you already hold. Review it every three months.

Replace every {{blank}} with a name or a link. Cut any line that does not apply. If it runs past one page, cut again. The page is for everyone, so it uses plain words, not hat names or ids.

---

## {{Company}} AI use policy

Version {{n}}, {{date}}. Owner: {{name of the person who owns these rules}}. Next review: {{date, three months from now}}.

**Why this page exists.** If something is not on this page, it is allowed. Unsure? Ask {{name}} in {{channel}}. You get an answer within two working days. This page says what is fine, what needs care, and what is off limits.

**Always.** You stand behind everything you ship, send or merge, whoever or whatever wrote it. Work is judged by whether it works, not by whether it looks AI generated.

**Allowed**
- Any tool on the inventory ({{link}}), with the data levels listed for it.
- Any tool at all with level 1 data, the kind we would publish. Tell {{name of the person who owns the tool list}} the same week, so it goes on the inventory.
- Drafting, summarizing, research, code, tests and prototypes.
- Prototypes to explore an idea. A prototype is a wireframe until {{name of the person who owns what customers see}} says otherwise, however finished it looks.
- {{add}}

**Allowed with care**
- Level 3 data: only in tools cleared for that source, listed on the inventory ({{link}}).
- UI or copy for customers: open the preview before the diff, run the release checklist and attach what it asks for to the pull request ({{link}}), ship under your own name.
- AI replies to customers: labeled as AI. They never state policy, price, refunds or legal terms without a person. {{name of the person who owns replies to customers}} decides which reply types go out unread.
- Agents that act: only in {{separate environment}}, with written access from {{name of the person who owns these rules}}.
- {{add}}

**Not allowed**
- Passwords, API keys or tokens in any AI tool or chat. Use {{secrets manager}}.
- Level 2 or 3 data in personal accounts or in tools not on the inventory. For personal accounts already in use, the dates below apply.
- Agents in production, customer data or customer channels without written access.
- AI deciding about people (hiring, performance, pay, a customer's credit) without a person making the final call. Before starting, check the AI Act high risk list with {{name of the person who owns these rules}}.
- {{add}}

**Personal accounts already in use.** Nobody is in trouble for use before this page. Tell {{name of the person who owns the tool list}} which ones you use by {{date, one week after posting}}. Level 3 data stays out of them from today. Everything else moves to {{business plan}} by {{date, about 30 days after posting}}.

**Data levels.** 1 Open: anything we would publish. 2 Internal: code, specs, designs, roadmap, aggregate analytics. 3 Restricted: personal data, customer content, contracts, financials, employee and candidate data, secrets. When in doubt, pick the higher level.

**Who says yes first.** A new tool that will touch level 2 or 3 data: {{name of the person who owns the tool list}}, within two working days. A new source of level 3 data: {{name of the person who owns these rules}}, within five working days. An agent that writes to a system: {{name of the person who owns these rules}}, within three working days. UI or copy for customers: {{name of the person who owns what customers see}} looks in person at anything on the list of screens that always get a second look ({{link}}); whoever merges checks the rest, with the release checklist.

**When something goes wrong.** Tell {{name}} in {{channel}} the same day. Whoever shipped it writes three lines: what happened, what the tool did, what changes. Reporting is never what gets someone in trouble.

**Exceptions.** Ask {{name of the person who owns these rules}}. Every exception has an end date and goes in the log ({{link}}).

---

## Notes for the rules owner (not posted)

### The approvals behind "who says yes first"

Three approvals and one review gate. Nothing else needs a yes. Each approval goes on the tool's row in `sheets/inventory.csv`.

| Id | When it applies | Decides | Answer within | A yes needs |
|---|---|---|---|---|
| A1 New tool | Level 2 or 3 data is about to touch an AI tool not on the inventory, paid or free, including an AI feature switched on in a tool you already have. With level 1 data, any tool may be used at once and goes on the inventory the same week | Tool owner, after asking the rules owner | 2 working days | A row on the inventory: owner, kind, account type, highest data level, cost, who approved and when |
| A2 New level 3 source | Customer records, tickets, contracts, employee or candidate data go into an AI tool for the first time | Rules owner, after asking the tool owner and whoever handles that data day to day | 5 working days | Processing terms in place (the vendor's standard data processing terms are usually enough). Purpose in one sentence. Only the fields the purpose needs. The source written on the tool's row |
| A3 Agent write access | An agent gets write access to a repository, database, production system or customer channel, or wider permissions than before | Rules owner, after asking the tool owner and the engineer who runs the agent | 3 working days | Separate from production. No production credentials. A deny list the agent never touches without a person: login, permissions, secrets, billing, public APIs, data access. Restore tested. Grant on the tool's row, with a name and an end date |
| G4 UI to customers | UI or copy made with AI is about to reach customers | High lane: the experience quality owner, in person. Low lane: whoever merges | Before merge | The release checklist evidence in the pull request (`PULL_REQUEST_TEMPLATE.md`). No record on the inventory |

### Which kinds of tools may touch which level

Sorted by kind, not by product. Product names change every quarter.

| Kind of tool | Level 1 | Level 2 | Level 3 |
|---|---|---|---|
| Consumer tool on a personal account, free or paid | Yes | No | No |
| Business plan of a chat or assistant tool: company account, admin controls, no training on your data by contract | Yes | Yes | Only sources cleared through A2 |
| Coding assistant with access to the repo, on a company account (on a personal account, the first row applies) | Yes | Yes | No real customer data in prompts, fixtures or test data |
| Agent that acts: writes to a repo, a database or a customer channel | Yes | Yes, in a separate environment | Only through A3 |
| AI feature inside a tool you already pay for | Yes | After the tool owner checks the terms | As for a business plan |
| Self hosted or private deployment | Yes | Yes | Sources cleared through A2 |

AI features switched on inside tools already on the bill count as new tools.

### Where the page meets the law

Information, not legal advice. A plain reading of the EU AI Act and GDPR, checked on 23 September 2026. Both reach you if your customers, users or staff are in the EU. Read the official text or ask a lawyer before you rely on a line.

| Line on the page | Law it maps to |
|---|---|
| New level 3 sources cleared, and listed on the inventory | GDPR Articles 5 and 28 |
| AI replies labeled | AI Act Article 50 |
| AI does not decide about people without a person making the final call; the high risk list is checked first | AI Act high risk list, GDPR Article 22 |
| Training by doing real work in pairs, recorded | AI Act Article 4 |

### Exceptions log

Keep it next to the inventory. The oldest close first.

| Opened | Rule | Who asked | Why | Decided by | Ends |
|---|---|---|---|---|---|
| {{date}} | {{rule}} | {{name}} | {{one line}} | {{rules owner}} | {{date}} |

### This week

- [ ] Rules owner named on the hats sheet (`WAY-OF-WORKING.md`)
- [ ] Every blank on the page filled, and the page still fits on one page
- [ ] Every tool on the inventory has a kind, an account type and a highest data level
- [ ] Both dates for personal accounts already in use written on the page
- [ ] Page posted at {{where the team already looks}}
- [ ] Read aloud at {{existing meeting}}, ten minutes, questions answered on the spot
- [ ] Review date in the rules owner's calendar
