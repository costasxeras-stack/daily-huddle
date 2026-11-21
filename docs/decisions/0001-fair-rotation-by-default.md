# 0001: Make fair rotation the default order

**Status:** accepted, 0.1.0

## Context

A random shuffle feels fair but is not: the same person can open three days in a row. The first speaker sets the tone and length for everyone else.

## Decision

Default to fair rotation: whoever has gone first least often goes first, ties broken by who went first longest ago, then random. The rest of the order is shuffled.

## Tradeoff

- Over a few weeks everyone opens about equally, and the History tab shows it.
- Needs history, so the first few huddles look like a shuffle.
- Random, alphabetical and team order stay available for teams that prefer them.
