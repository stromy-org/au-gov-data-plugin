---
name: au-setup
description: >
  Day-0 setup for the AU Gov Data connector: how to add the Australian
  government data connector to Claude, sign in with the Microsoft account
  Stromy invited, confirm it works, and where to go next. Use whenever someone
  is new to this plugin, asks how to connect or set up AU Gov Data, sees
  "needs authentication" or "not connected" on the connector, or asks what the
  Australian data tools can do before any connector is switched on. This skill
  ships inside the plugin and needs no connector, so it still answers when
  nothing else is switched on. Not for the research itself: once connected,
  use au-guide.
metadata:
  stromy-local: "true"
  stromy-client-summary: "Start here: add the AU Gov Data connector, sign in, and confirm it works."
---

# AU Gov Data — getting connected

This plugin gives you Australian government research inside Claude: Hansard across
every Australian parliament (refreshed daily), federal legislation, procurement and
grants, political finance, statistics, lobbyist and consultation registers, and more.
The skills in this plugin know how to ask; the **AU Gov Data connector** is the engine
that answers. You add the connector once, on your account, and it travels with you into
every conversation.

## Before you start

You need two things, and Stromy provides both:

- An invitation to the **AU Gov Data** connector, sent to the Microsoft account you gave
  Stromy. Access is invitation-only, so the sign-in step below only works for an
  invited account.
- This plugin, installed. If you can read this skill, that part is done.

## 1. Add the connector

1. In Claude, open **Settings → Connectors** (on claude.ai, or in the desktop app).
2. Choose **Add custom connector**.
3. Name it `AU Gov Data` and paste this URL:
   `https://au-gov-data.braveforest-e73e8541.northeurope.azurecontainerapps.io/mcp`
4. Save. Claude opens a Microsoft sign-in page: sign in with the invited account and
   accept the permission prompt.

If sign-in says your account is not assigned to the application, the invitation has
not reached that account yet. Tell Stromy which address you signed in with.

## 2. Switch it on in a chat

Connectors are off by default in each new conversation. Open the tools menu in the
chat (the **+** or connectors button next to the message box), switch **AU Gov Data**
on, then ask:

> describe my workspace

Claude lists the plugin, its skills, and the connectors that are switched on. If
`AU Gov Data` is in that list, you are connected.

## 3. First question

Keep the first Hansard question small. The corpus is several gigabytes and loads on
first use after a quiet period, so the first call can take about a minute; after that
it is fast. A good opener bounds the jurisdiction and the dates, for example:

> What did the Victorian lower house say about short-stay accommodation in September 2026?

Then ask for more: a comparison across states, a speaker's record on a topic, which
bills mention a term, who lobbies on it, what was procured, what the ABS says.

## Where to go next

- **au-guide** — the full orientation: what to ask for, what the Hansard corpus can
  do that nothing else can, and the caveats to expect.
- **au-gov-data** — the research workflow: one question across the federal and state
  record, with sources named.

## Two snags, and the fix

- **"Connected" but every call fails.** The connector was added but the sign-in did
  not complete, or the token expired. Open **Settings → Connectors**, remove the
  AU Gov Data connector, add it again and sign in.
- **Skills look missing or out of date.** Start a new conversation. If the plugin
  still looks stale, reinstall it from the marketplace address Stromy gave you.
