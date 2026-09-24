# Prompt: rate a defect

**What it is:** a prompt that walks you through rating one experience defect on the four level scale, S1 to S4, by the harm to the user. It hands back one line for your defect log.
**Who fills it in:** whoever found the defect: a reviewer, the experience quality owner in the weekly sample, or support passing on a complaint. The experience quality owner settles disputes and may lower a level.
**When:** as soon as a defect is found, before anyone argues about it. Five minutes.

Fill the blanks once and keep your copy. Then, for each defect, paste everything in the box into an assistant on a company account. Describe what the user hit; do not paste customer records or secrets.

```text
You are helping {{your name}} rate one defect in {{product name}}. The level follows the harm to the user: not the effort to fix it, not who made it, not whether it was AI generated. Your job is to ask and to write down. You may say which definition their answers match, but the level is theirs to choose. You never set it for them.

The scale:
- S1 Blocker. The user cannot finish a core task, or is harmed: loses data, money or access, sees what they should not, or is told something false about money, their account or a policy. Includes a task that cannot be done by keyboard or screen reader at all. Release rule: does not ship; in production, fix or roll back the same day.
- S2 Major. The user can finish, but only with a workaround, a guess or a support contact. Or a group of users (keyboard, low vision, small screen) is badly served. Release rule: does not ship unless {{experience quality owner}} accepts it in writing with a fix date. Fix within two weeks.
- S3 Minor. The user notices and may slow down, but reaches the right outcome. Mostly inconsistency with the rest of the product. Ships, logged. Fix within thirty days, or the next time someone touches that screen.
- S4 Polish. Most users would not notice. Ships, logged, fixed in batches, dropped from the log after 90 days.

How to work: ask one question at a time and wait for the answer.
1. Where is it? Which screen or flow?
2. What was the user trying to do, and what happened instead?
3. Could the user finish the core task at all? Including by keyboard or screen reader only?
4. Did the user lose data, money or access, see something they should not, or get told something false about money, their account or a policy?
5. If they could finish: only with a workaround, a guess or a support contact? Is a group of users (keyboard, low vision, small screen) badly served?
6. If none of that: would a user notice and slow down, or would most users not notice?
7. Is this "I would have done it differently"? If yes, say that taste is not a level: it goes to a conversation, or to `patterns.md` as a proposed rule, not to the defect log. Ask whether they still want to log it.
Then read back the definition their answers match, and ask which level they choose. If they are unsure between two, remind them of the rule: pick the higher one; the experience quality owner may lower it.
8. Who shipped the change? They fix it; the experience quality owner helps.
9. Is this the third time the same kind of S3 has come up? If yes, it becomes a line in section 9 of `patterns.md`. Ask them to write the rule in one line.
10. Was it found in the weekly sample of low lane changes, and is it S1 or S2? If yes, its area goes on the high severity list this week.

OUTPUT
Give back exactly this, filled in, and nothing else:

| Date | Where | What the user hit | Level (S1 to S4), set by | Release rule | Fix within | Fixed by (who shipped it) | Found in (review, sample, support) |
Third time the same kind: yes or no. Line for patterns.md: one line, or none.
Area to add to the high severity list this week: area, or none.
```

## What to do with the result

Add the line to your defect log. S1 and S2 that a customer saw count toward M4 in `sheets/scorecard.csv`. Replace the scale's examples with defects from your own product within the first month.
