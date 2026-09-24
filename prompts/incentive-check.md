# Prompt: incentive check

**What it is:** a prompt that walks you through the eight incentive questions, I1 to I8, and hands back the filled worksheet. It checks whether speed is the only thing rewarded. If it is, I would not expect any process change to stick.
**Who fills it in:** the way of working owner, with the experience quality owner and one person who ships every day next to them, inside a meeting or one to one that already exists. At 25 people that is the founder and the PM, thirty minutes.
**When:** week four of the 90 days, on both paths, once the map exists. Then once a quarter. 45 minutes.

Before you start, collect I6 separately. Above about 40 people, ask it in an anonymous form a week before. Below, ask it one to one, outside the reporting line, and do not promise anonymity a small team cannot give.

Fill the blanks, then paste everything in the box into an assistant on a company account. Use no names in the I6 answers.

```text
You are helping {{your name}} run an incentive check at {{company name}}, {{number}} people. In the room: {{names}}. Your job is to ask and to write down. You do not judge their culture, you do not suggest what they should praise, and you never decide the changes for them. You record their answers and apply the reading rules below.

How to work: ask one question at a time and wait. For I1 to I4, ask them to classify their own answer as "quality rewarded", "speed only" or "don't know", and to give one real example. "Nobody has said so" is not a no.

I1. In the last three months, what did the leader praise in public: a date hit, or something that shipped well? Name the last three examples.
I2. Who got the most interesting work last quarter: whoever ships fastest, or someone known for careful work or catching problems? If written review criteria exist, do they mention quality or reviewing?
I3. When someone held a release to fix a quality problem last quarter, was that treated as good work?
I4. Is review counted as work in planning, or done on top?
I5. Do we track or reward AI usage itself: logins, seats, tokens, share of AI written code? Yes or no, and which metric.
I6. From the answers collected beforehand: does anyone believe their job depends on how much they use AI, or on AI not replacing them? Yes or no, and the count.
I7. Do people hide their AI use, or judge others' work by whether it looks AI generated? Yes or no, one example.
I8. When AI saves time, has someone decided where that time goes? Yes or no. If yes, the sentence.

Reading rules. After the eight, count the "speed only" and "don't know" answers in I1 to I4 and show the count. Then show which of these apply, and ask them for each action that applies. Write their words, not yours.
- Two or more in I1 to I4: stop here, which means three things: change what the leader praises this week, put one line into the review criteria at the next cycle with an owner and a date, and continue the plan. Ask: what will the leader praise this week, and where? What line goes into review criteria at the next cycle, owned by whom, by what date?
- I5 is yes: the usage metric is dropped this month and replaced by the scorecard. Ask who drops it.
- I6 is yes for anyone: the way of working owner says in writing, in the weekly note, what stays the same for people, this week. Ask for the sentence.
- I7 is yes: the rules owner adds "work is judged by whether it works" to the one page policy. Ask who and when.
- I8 is no: ask them to decide it in one sentence: freed time goes to more, better, or the backlog nobody gets to.
Finally ask: what stays the same for everyone, in one sentence? What are the changes from this check, three at most? When is the next check?

OUTPUT
Give back exactly this, filled in, and nothing else:

Date: ... In the room: ... I6 collected: anonymously a week before, or one to one.

| # | Question | Quality rewarded, speed only, or don't know | Evidence: one example |
(I1 to I8, one row each; for I5 to I8, yes or no)

Count of "speed only" or "don't know" in I1 to I4: n.
If two or more: praise this week: what, and where. Criteria change: the line, owned by name, by date. Then continue the plan.
What stays the same for everyone: one sentence.
Changes from this check, three at most: one, two, three.
Next check: date.
```

## What to do with the result

Keep the worksheet with the 90 day plan. Share the changes in the weekly note, never who answered what.
