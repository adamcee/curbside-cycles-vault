---
title: Curbside Cycles — Example Vault
---
# Curbside Cycles — Example Vault

Curbside Cycles is a fictional one-person business: a former bike-shop mechanic runs a repair van that comes to commuters at their workplace. The question for the year is whether one van can pay a full-time wage.

This vault is the founder's project memory, five weeks in. The AI agents read it at the start of every session and keep it up to date, and the sections below show how each part of the method looks for a small business with no software in it.

It's an example for the [Agentic Vault](https://github.com/adamcee/agentic-vault), a template for giving AI sessions persistent project memory. Explore it as a website at [adamcee.github.io/curbside-cycles-vault](https://adamcee.github.io/curbside-cycles-vault/), or clone this repo and open the folder in Obsidian.

## Start Here

[AGENTS.md](AGENTS.md) is the first file every AI session reads. It says what the business is, what the founder is working on now, which decisions are settled, and what the last session did.

## Picking Up Where the Last Session Left Off

- **The checkpoint.** The top of [AGENTS.md](AGENTS.md) summarizes the last session in two sentences, so a new session starts from there instead of from zero.
- **The session log.** Every session adds one line saying which AI tool did what: [session history](session-history.md).
- **A hand-over note.** The last session stopped halfway through designing membership tiers, so it left a note with what's done and what's next: [resume note](drafts/2026-10-09-resume-membership-tiers.md).

## Two Task Lists

- **The AI's list.** Every action item an AI session finds goes into one ledger, the [implementation plan](prototype/implementation-plan.md).
- **The founder's list.** The founder keeps a short list of their own and copies items over from the ledger on Fridays. No AI writes to [their list](prototype/human-task-list.md).
- **A decision still being made.** Members who book every three weeks would use more than the one service a month the membership covers. The founder is deciding what a second visit should cost, and the AI drafts that decision in chat without writing it until the founder approves. It's listed under "Decisions Owed" in the [ledger](prototype/implementation-plan.md).

## Decisions That Changed

Each decision record says what was chosen, what was rejected, and why. When evidence changes a decision, a new record replaces the old one and both stay on file.

- **The first choice of customer.** The founder chose to serve daily commuters at their workplace, and a survey and the pilot both backed it up: [the decision](decisions/product/PDR-P001-workplace-commuter-focus.md).
- **Per-visit pricing became a membership.** A one-month pilot showed regulars came back every three to four weeks and workplaces asked for a monthly plan, so a $45 membership replaced per-visit pricing: [the old decision](decisions/product/PDR-P002-per-visit-pricing.md) and [its replacement](decisions/product/PDR-P004-membership-plus-per-visit.md).
- **An idea turned down.** A storefront workshop was rejected because its rent was too high before demand is proven, and the record stays so nobody proposes it again without new reasons: [the rejection](decisions/rejected/PDR-P003-storefront-workshop-lease.md).

## Following One Finding Through the Vault

When new evidence arrives, the agent checks which decisions it affects. Here is one finding traced end to end.

1. **The pilot finds a pattern.** Over 52 pilot visits, regulars rebooked every 20 to 27 days and often compared prices with shops: [pilot results](research/pilot-month-results.md).
2. **An old decision is marked weakened.** The per-visit pricing record gets a dated note saying the pilot undercuts it: [per-visit pricing](decisions/product/PDR-P002-per-visit-pricing.md).
3. **A new decision replaces it.** The membership record explains what changed and links the pilot data: [membership pricing](decisions/product/PDR-P004-membership-plus-per-visit.md).

## Kinds of Research

Each research doc carries a tag for how solid its evidence is; everything here is `emerging`, since each comes from one small round.

- **A survey.** 41 commuters answered questions about repairs and booking: [commuter survey](research/commuter-survey-2026-09.md).
- **A pilot.** A month of real bookings, visits, and revenue: [pilot results](research/pilot-month-results.md).
- **A price scan.** What six nearby bike shops charge, written up by an AI and fact-checked before it entered the vault: [price scan](research/local-price-scan.md).

## Ideas Before They're Decisions

Raw ideas get a short note until they're promoted to a decision, rejected, or folded into something else.

- **Promoted.** A monthly membership became the new pricing decision: [the idea](ideas/monthly-membership.md).
- **Rejected.** E-bike battery service was turned down because each battery maker needs its own diagnostic tool and the insurance cost more: [the idea](ideas/e-bike-battery-service.md).
- **Still open.** Weekend stops at apartment buildings are waiting until the membership launches: [the idea](ideas/apartment-building-weekend-stops.md).

## Checking AI Writing Before It Counts

AI-written material waits in `drafts/` until a person checks it.

- **A report that passed.** The AI's price scan was tightened and an invented claim removed before it entered the vault. The untouched original is kept beside it: [the clean version](research/local-price-scan.md) and [the original](research/_source-local-price-scan.md).
- **A draft still waiting.** An AI memo proposing membership tiers is still raw, and one tier would pay less than the founder's minimum hourly rate: [the draft](drafts/membership-tier-options.md).
- **A claim backed up later.** The booking-tool decision first marked "commuters prefer booking online" as unsourced; the pilot later confirmed it, and the flag became a link: [the booking-tool decision](decisions/technical/ADR-T001-online-booking-tool.md).
