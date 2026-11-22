# Case study: Daily Huddle

## The problem

Standups drift in two ways: the same person always opens, and updates turn into discussions. Most teams fix this with good intentions and a facilitator who gives up after a week. This app makes the fair version the default and keeps the evidence, so the team can see whether its standup is getting shorter.

## From a small tool to an app

Version 0 was a one-screen tool on my portfolio site, picked because it was quick to build. It worked, but it only stored data. For 0.1.0 I asked what a user would need to come back every week, and what the app should show them that they could not see before. The answer shaped three decisions.

## Decisions

### 1. Make fair rotation the default order

A random shuffle feels fair but is not: the same person can open three days in a row. The first speaker sets the tone and length for everyone else.

**Decision:** Default to fair rotation: whoever has gone first least often goes first, ties broken by who went first longest ago, then random. The rest of the order is shuffled.

Full record: [docs/decisions/0001-fair-rotation-by-default.md](decisions/0001-fair-rotation-by-default.md)

### 2. Show the timer, never cut people off

Hard cut-offs make standups robotic and people resent them. No timer at all lets them drift.

**Decision:** The timer turns red and the line says "over, park it?" when time is up, with an optional short sound. The facilitator decides when to move on.

Full record: [docs/decisions/0002-visible-timer-no-cut-off.md](decisions/0002-visible-timer-no-cut-off.md)

### 3. Keep names and history in the browser

Meeting history with names and blockers is team information. It should not leave the facilitator's device without them choosing to.

**Decision:** Teams, history, blockers and parked topics are stored in local storage. The summary and CSV are the only ways out, and the user triggers both.

Full record: [docs/decisions/0003-history-stays-local.md](decisions/0003-history-stays-local.md)

## What it does now

- **Teams:** save several teams, each with its own members, minutes per person, meeting timebox, prompts and sound setting.
- **Speaking order:** fair rotation (whoever went first least often goes first), random shuffle, alphabetical or team order. Tick who is here.
- **Live huddle:** big name and timer, a bar for the person and a bar for the whole meeting, the prompts, Pause, Back, Not here, Next and End now. Optional sound and vibration when time is up. Keyboard shortcuts. Keeps the screen awake.
- **Blockers:** note a blocker against the current speaker in one line.
- **Parking lot:** topics for after the meeting, each with an owner.
- **Summary:** order, times, who was not here, blockers and parked topics, ready to paste into chat.
- **History:** number of huddles, average length, share within the timebox, share of turns over time, a chart of the last 14 huddles, who went first, and a CSV download.

## What I would measure

There is no usage data yet, so there are no findings. These are hypotheses to test with real users.

| Measure | Definition | Target |
|---|---|---|
| Meeting length | Median huddle length against the timebox, week over week | [x] min |
| Overruns | Share of turns over the per person time | [x]% |
| Fairness | Spread of who went first after 20 huddles | [x] |

## What I would do next

1. Shared history for teams that rotate the facilitator
2. A short daily summary posted to a chat channel, on request
3. Blocker follow-up: carry open blockers into the next huddle

## My role

I defined the problem, the users, the features and the decisions, and tested every flow on desktop and phone widths.
