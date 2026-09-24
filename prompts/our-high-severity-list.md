# Prompt: our high severity list

**What it is:** a prompt that walks you through writing your high severity list: the areas of your product where a defect is likely and costly, written down in advance. A change that touches the list goes to the high lane and gets an in person review. It hands back the list as a table and as one paragraph.
**Who fills it in:** the experience quality owner. Send the paragraph to the PMs for agreement in writing; no meeting needed.
**When:** week three on Start, week four on Fix. Checkpoint 1 at day 30 does not pass until it exists. Thirty minutes, then again after two weeks of use.

Fill the blanks, then paste everything in the box into an assistant on a company account. Do not paste customer records or secrets.

```text
You are helping {{your name}}, who owns experience quality for {{product name}}, write the high severity list. It names the areas where a defect (S1: the user cannot finish or is harmed; S2: finishes only with a workaround, a guess or a support contact) would be likely and costly. Every change touching the list is reviewed in person by the experience quality owner; everything else is the low lane, checked by the author's release checklist and sampled weekly.

Your job is to ask and to write down. You do not add or remove an area for them, and you do not decide what is costly in their product. Keep the list narrow: every area on it costs review time.

How to work: go through the starter areas below one at a time. For each, ask: is this on our list? If yes, which screens, flows or actions does it cover in our product? Wait for the answer before the next area.

Starter areas:
1. New flows that touch money, account, data or first time use. (Other new flows go to the low lane.)
2. Money: prices, billing, checkout, refunds.
3. Account and access: sign up, sign in, permissions, deletion.
4. Customer data: what is shown to whom, imports, exports.
5. First time experience: onboarding, empty states for new accounts.
6. Anything that cannot be undone in one step.
7. Legal, policy or promise text.
8. Any flow customers complained about last quarter. Ask them to name the flows.

Then ask:
9. Is there an area of your own where an S1 or S2 would be likely and costly? Name it and what it covers.
10. Has the weekly sample found any S1 or S2 yet? Each one's area goes on the list.
11. Which PMs agree it, and by when?

If they are running this again after two weeks, ask first: what share of changes landed in the high lane? If more than a third, the list is too wide. Go through the areas again and ask which to narrow. The narrowing is theirs.

OUTPUT
Give back exactly this, filled in, and nothing else:

| Area | On our list? | What it covers in our product |

The list as one paragraph, for patterns.md section 8 and the hats sheet: ...

Agreed with: PM names, by date. High lane share to check on: date, two weeks from now.
```

## What to do with the result

Paste the paragraph into section 8 of `patterns.md` and next to the experience quality owner on the hats sheet. Send it to the PMs in writing and ask for a yes by the date.
