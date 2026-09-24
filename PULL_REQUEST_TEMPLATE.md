<!--
What it is: the release checklist evidence, for any change that alters what the customer sees, however it was made.
Who fills it in: the author runs the checks and attaches the evidence. Whoever merges confirms the evidence is there, in about two minutes, and writes their name on the last line.
When: before asking for review. Put this file where your code host looks for a pull request template (as of September 2026, for example, one host reads .github/PULL_REQUEST_TEMPLATE.md).

This comment is for you while you write. It does not show once the pull request is posted.

No customer facing change? Write "No customer facing change" and delete the checklist below.

LANE. Does the change touch anything on the high severity list (patterns.md, section 8)? Yes: high lane. Finish this checklist, then book the experience quality owner, who reviews it in person. No: low lane. Whoever merges confirms the evidence and the experience quality owner samples five merged low lane changes a week.

WHICH CHECKS
  Words only, on an existing screen: 1, 2, 18 to 21
  Look only, style or layout on an existing screen, no new behavior: 1 to 6, 14, 16, 17
  Anything else, a new screen, new or changed behavior, or anything in the high lane: all 23

THE 23 CHECKS (usual severity if it fails)
Before you start
  1  Open the running preview, not the code. Do the task start to finish, as a customer would. No preview per change yet: record your screen doing the task
  2  Check the lane (above)
Consistency
  3  Every button, field, dialog, table and message comes from the components in patterns.md (S3)
  4  The same action has the same name and place as elsewhere in the product (S3)
  5  No new colors, font sizes or spacing values (S4, S3 if visible at a glance)
  6  Works at phone width and on a wide screen (S3, S2 if the task cannot be finished on a phone)
States
  7  Empty: sign in as the empty test account. One sentence says what goes here, one action adds the first item (S2 if a new user could think it is broken)
  8  Loading: slow the network. Something shows it is working; buttons cannot be pressed twice (S3, S2 if a double submit is possible)
  9  Error: switch off the network or enter wrong input. The message says what happened and what to do; what the user typed is still there (S2, S1 if work is lost)
  10 Success: the user can see it worked (S2, S1 if it says success when it failed)
  11 Too much: long names, accented characters, the hundred item test account. Nothing overlaps or gets cut in a way that changes meaning (S3)
  12 Not allowed: sign in as the no rights test account. A clear message, never someone else's data (S1 if data shows, S2 if the page breaks)
Accessibility basics
  13 Keyboard only: Tab, Enter, Space, arrows. Everything reachable, in a sensible order, focus always visible (S1 if the task cannot be finished, S2 if focus disappears)
  14 Run the browser's accessibility checker or a free extension. No new errors in what this change touches. Old errors go in the baseline and do not block (S2 per new error on the task, S3 elsewhere)
  15 Every form field has a visible label, not only placeholder text (S2)
  16 Zoom to 200 percent: still readable and usable (S2)
  17 Color is not the only signal: errors in red also say so in words or with an icon (S2)
Copy
  18 Words match the word list in patterns.md (S3)
  19 Buttons say what they do: "Delete invoice", not "OK" (S3, S2 if a destructive button is vague)
  20 No placeholder text, lorem ipsum, TODO or test data a customer could see (S2)
  21 Nothing states a price, a policy, a legal term or a promise unless its owner checked it (S1, and high lane anyway)
Behavior
  22 Destructive actions ask first, or can be undone (S1 if one click loses data with no way back)
  23 Nothing was added that nobody asked for. Compare with the ticket (S3)

SEVERITY
  S1 Blocker: cannot finish a core task, or harmed (data, money, access, a false statement). Does not ship
  S2 Major: finishes only with a workaround, a guess or a support contact, or a group of users badly served. Does not ship without written acceptance from the experience quality owner
  S3 Minor: notices, slows down, reaches the right outcome. Ships, logged
  S4 Polish: most users would not notice. Ships, batched
  Unsure between two levels? Pick the higher one. Found an S1 or S2 in the low lane? Stop and hand it to the experience quality owner the same day.

WHOEVER MERGES: check that every line below has its attachment and that the preview matches it. Do not rerun the checklist. Merge only then, and write your name on the last line. You ship it under your name and own it as if you made it by hand.
-->

## Release checklist evidence (the author fills this in)
Lane: {{high / low}}. High lane: book {{experience quality owner}} after this.
Kind of change: {{words only / look only / anything else}}. Checks run: {{short version, or all 23}}.

Preview: {{link}}, or screen recording of the task: {{attachment}}

One screenshot per state the change touches (write "not touched" where it does not):
- Empty (empty test account): {{attachment}}
- Loading: {{attachment}}
- Error: {{attachment}}
- Success: {{attachment}}
- Too much (hundred item test account): {{attachment}}
- Not allowed (no rights test account): {{attachment}}
- Phone width: {{attachment}}

Accessibility checker result, new errors only: {{attachment or "none new"}}
Keyboard only, task finished: {{yes, or the defect}}
Price, policy or promise text checked by its owner: {{name, or "none in this change"}}

Defects found: {{none, or S1 to S4 with one line each}}
Author: {{name}}. Date: {{date}}.
Evidence confirmed by (whoever merges): {{name}}
