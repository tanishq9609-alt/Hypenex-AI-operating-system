# HANDOFF TO GPT

## Purpose

This document defines how a completed Strategy Bible moves from Claude into GPT for pitch deck conversion.

Claude produces the Strategy Bible. GPT never does research and never introduces new facts — it only transforms what is already validated in the Bible into pitch deck content, per `10_Pitch_Deck_Engine.md`.

## How to Move the Strategy Bible

Paste the completed `09_Strategy_Bible.md` content directly into the GPT conversation as text, along with the rules in `10_Pitch_Deck_Engine.md`.

Do not hand this off as a shared file, zip, or link. Browsing and file-fetching tools are not reliably able to retrieve and unzip binary files or repo archives, so a link or attachment may silently fail to load the full document — GPT would then be working from an incomplete Bible without either party realising it. Pasting the text directly guarantees GPT has received the exact, complete, validated content.

If the Bible is too long for a single message, split it into clearly labelled parts (e.g. "Part 1 of 3 — Sections 1–5") and confirm GPT has received all parts before it begins converting content.

---

# Human Operator Checklist

Before starting GPT handoff:

Confirm:

- [ ] Claude has completed the Strategy Bible.
- [ ] Red Team validation has been completed.
- [ ] The final Strategy Bible version is being used.
- [ ] The entire document has been copied.
- [ ] Multiple parts are clearly labelled if split.

After GPT creates the pitch deck:

Review:

- [ ] All claims trace back to the Strategy Bible.
- [ ] No unsupported numbers appear.
- [ ] No new assumptions have been introduced.
- [ ] Investor concerns are addressed.
- [ ] The pitch accurately represents the validated strategy.

---

# Operating Principle

Claude discovers and validates the strategy.

GPT communicates the validated strategy.

The handoff exists to preserve the integrity of the system between these two stages.
