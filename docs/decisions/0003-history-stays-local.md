# 0003: Keep names and history in the browser

**Status:** accepted, 0.1.0

## Context

Meeting history with names and blockers is team information. It should not leave the facilitator's device without them choosing to.

## Decision

Teams, history, blockers and parked topics are stored in local storage. The summary and CSV are the only ways out, and the user triggers both.

## Tradeoff

- No account, nothing to approve with IT.
- History lives on one device. A rotating facilitator would split it, which a shared store could fix later.
- Clearing browser data deletes history.
