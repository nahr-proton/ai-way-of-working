<!--
What it is: the one file every AI tool reads before it makes a screen, a component or text a customer sees. Copy it to the root of your main repo.
Who fills it in: the experience quality owner (a designer if there is one, otherwise the PM, never an engineer). Changes after that go through a pull request they approve.
When: in an afternoon, before the third screen is generated. The states, the accessibility block, three components and five words are enough for week one. It grows from defects.
-->

# patterns.md

Owner: {{experience quality owner}}. Last changed: {{date}}.
Read this before generating or changing any screen, component or text the customer sees.
If a rule here conflicts with a request, follow the rule and say so.

## 1. Who uses this product
{{Two lines. Who they are, what they come to do, on which device.}}

## 2. Principles
Five at most. Each one settles a tie.
1. {{Example: Never lose the user's work. Keep what they typed on error. Confirm before deleting.}}
2. {{Example: Clarity over density. When in doubt, show less and link to more.}}
3. {{principle}}

## 3. Components
Use these. Do not create a new component without asking {{name}}.

| Need | Use | Path |
|---|---|---|
| Main action on a screen | Primary button, one per screen | {{path}} |
| Other actions | Secondary button | {{path}} |
| Confirm a destructive action | Confirm dialog that names the thing being deleted | {{path}} |
| A list of records | Table | {{path}} |
| A form field | Field with a visible label above the input | {{path}} |
| Feedback after an action | Toast for success, inline message for errors | {{path}} |
| Nothing here yet | Empty state: one sentence on what goes here, one action to add it | {{path}} |

## 4. Tokens
Colors, type sizes and spacing come from {{path to tokens}}.
No new color values. No new font sizes. No new spacing values.

## 5. Every screen has these states
Empty, loading, error, success, and too much (long names, many items).
A screen missing one of them is not done.

## 6. Words
Voice: {{three words, for example plain, calm, specific}}.

| We say | We do not say |
|---|---|
| {{workspace}} | {{project, space}} |
| {{Delete}} | {{Remove, Erase}} |

Buttons say what they do: "Delete invoice", not "OK".
Errors say what happened and what to do next. No error codes on their own. No blame.
Never write a price, a policy, a legal term or a promise. Write {{PLACEHOLDER}} and flag it for {{name}}.

## 7. Accessibility, always
Every form field has a visible label.
Every image that carries meaning has alternative text. Decorative images are marked decorative.
Every icon button has a text name.
Everything works with the keyboard alone, in reading order, with visible focus.
Text contrast meets WCAG AA.
Color is never the only signal.
Every screen works at 200 percent zoom.

## 8. Stop and ask a human
Do not generate or change these without {{experience quality owner}} involved:
{{the high severity list, one paragraph: new flows that touch money, account, data or first time use; money; account and access; customer data; first time experience; anything that cannot be undone in one step; legal and policy text; flows customers complained about}}

## 9. Known mistakes
A defect seen three times becomes a rule here.

| Added | Mistake | Rule |
|---|---|---|
| {{date}} | {{Example: generated tables had no empty state}} | {{Every table shows the empty state component when it has no rows}} |
