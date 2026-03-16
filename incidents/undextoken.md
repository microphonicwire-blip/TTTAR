---
layout: default
title: "I007 – Attempted Token Grab via Fake Bot"
parent: Incidents
nav_order: 7
---

# I007 – Attempted Token Grab via Fake Bot

| Field | Details |
|-------|---------|
| **Incident ID** | I007 |
| **Date** | 2025 |
| **Perpetrator** | [Undex](../people/undex) |
| **Severity** | 🔴 Critical |
| **Status** | Confirmed |

---

## Summary

Undex created and distributed a fake Discord bot under the name **"FG Utility Plus"**, presenting it as an unofficial Federal Gamers utility bot with features including server stats, WOS game integration, and rank tracking. The bot's OAuth invite link requested the `bot` and `applications.commands` scopes, but the linked authorisation page had been manipulated to also silently request a user token through a phishing overlay hosted on a lookalike domain.

At least **three members** clicked through the full authorisation flow before the link was flagged by a member who noticed the redirect domain did not match Discord's CDN.

---

## Timeline

| Time | Event |
|------|-------|
| Day 1, 14:02 | Undex posts bot invite in `#server-bots` with a convincing embed |
| Day 1, 14:45 | First member authorises the bot |
| Day 1, 17:30 | Second and third members authorise |
| Day 2, 09:11 | Member "rktfall" flags the redirect domain as suspicious |
| Day 2, 09:34 | Joshua removes the message and begins investigation |
| Day 2, 11:00 | Undex confronted; initially denies involvement, then goes offline |
| Day 2, 13:22 | Undex's authorship of the bot confirmed via shared hosting metadata |

---

## Impact

- Three member accounts potentially compromised
- Affected members were advised to immediately reset passwords and revoke all OAuth sessions
- One affected member reported unauthorised login attempts from an Argentinian IP within 6 hours of authorising the bot

---

## Response

Undex was immediately suspended pending investigation. Following confirmation of authorship the suspension was made permanent. The fake bot was reported to Discord Trust & Safety.
