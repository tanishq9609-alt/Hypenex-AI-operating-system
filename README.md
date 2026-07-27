# Hypenex AI Operating System

## Overview

The Hypenex AI Operating System is a modular AI-powered strategic framework designed to transform a raw venture idea into an evidence-backed, investor-ready company strategy.

It is not a single prompt.

It is a structured operating system made of specialised engines, where each engine has a defined responsibility, produces validated outputs, and passes those outputs to the next stage.

The system follows:

**Evidence → Understanding → Strategy → Validation → Communication**

The objective is to reduce founder bias, improve strategic decision-making, and create investor materials based on validated intelligence rather than assumptions.

---

# Core Operating Rules

Every engine operates under the rules defined in:

`00_Core_System.md`

The non-negotiable principles are:

- Evidence over opinion.
- Facts must be separated from assumptions.
- Hypotheses must be testable.
- Recommendations must have reasoning behind them.
- Sources must be identified.
- Weak conclusions must be challenged before acceptance.
- Red Team validation is required before strategic conclusions are finalised.

The system prioritises:

- Accuracy over excitement.
- Truth over persuasion.
- Strategic clarity over unnecessary complexity.

---

# Engine Map

Each engine has two related files:

- A `_Engine.md` file, which defines that engine's purpose, objectives, and principles. **These are philosophy documents only — they are never run directly.**
- A `MASTER_PROMPT.md` file, which is the actual executable prompt handed to Claude to run that engine.

| Engine | Philosophy (reference only) | Executable prompt (run this) | Run by |
|---|---|---|---|
| Core System | `00_Core_System.md` | — (rules, not run) | — |
| Research | `01_Research_Engine.md` | `RESEARCH_MASTER_PROMPT.md` | Claude |
| Strategy | `02_Strategy_Engine.md` | `02_STRATEGY_MASTER_PROMPT.md` | Claude |
| Product | `03_Product_Engine.md` | `03_PRODUCT_MASTER_PROMPT.md` | Claude |
| AI | `04_AI_Engine.md` | `04_AI_MASTER_PROMPT.md` | Claude |
| Finance | `05_Finance_Engine.md` | `05_FINANCE_MASTER_PROMPT.md` | Claude |
| GTM | `06_GTM_Engine.md` | `06_GTM_MASTER_PROMPT.md` | Claude |
| Investor | `07_Investor_Engine.md` | `07_INVESTOR_MASTER_PROMPT.md` | Claude |
| Red Team | `08_Red_Team_Engine.md` | `08_RED_TEAM_MASTER_PROMPT.md` | Claude — **in a brand-new conversation** (see Step 8 below) |
| Strategy Bible | `09_Strategy_Bible.md` | `09_STRATEGY_BIBLE_MASTER_PROMPT.md` | Claude (compiles only — generates no new content) |
| Pitch Deck | — | `10_Pitch_Deck_Engine.md` | GPT (transforms only — introduces no new facts) |

---

# How to Run This System

Each step below produces a validated output that the next step depends on. Do not skip a step or run them out of order — every engine after Research explicitly refuses to begin if its required upstream inputs are missing.

**0. Complete `HYPENEX_INPUT_BRIEF.md`.**
The operator provides initial venture context before activating Claude. This is an input questionnaire, not a final analysis.

**1. Give Claude `RESEARCH_MASTER_PROMPT.md`.**
Claude executes Stages 1–4 (Market, Competitor, Customer, Investor research) in order, each gated by an inline Red Team review, per the rules in `00_Core_System.md`. Save progress to `SESSION_STATE.md` as instructed in the prompt.

**2. Give Claude `02_STRATEGY_MASTER_PROMPT.md`.**
Requires Step 1's completed research. Produces validated strategic direction, business model logic, and competitive positioning.

**3. Give Claude `03_PRODUCT_MASTER_PROMPT.md`.**
Requires Step 2's completed Strategy output. Produces validated product vision, capabilities, and roadmap logic.

**4. Give Claude `04_AI_MASTER_PROMPT.md`.**
Requires Steps 2 and 3. Determines whether AI is actually required for the prioritised product capabilities, and assesses technical feasibility.

**5. Give Claude `05_FINANCE_MASTER_PROMPT.md`.**
Requires Steps 2, 3, and 4. Produces revenue model, unit economics, and capital requirements — every projection includes a base case and a stress-tested downside case.

**6. Give Claude `06_GTM_MASTER_PROMPT.md`.**
Requires Steps 2, 3, and 5. Produces customer segments, channel strategy, and market entry sequencing, designed within the CAC constraints Step 5 established.

**7. Give Claude `07_INVESTOR_MASTER_PROMPT.md`.**
Requires all of Steps 2 through 6. Produces investor-fit analysis, objection analysis, and a target investor list — sourced and dated, never invented from memory.

**8. Give Claude `08_RED_TEAM_MASTER_PROMPT.md`, in a brand-new, separate conversation.**
This step must **not** run in the same conversation as any of Steps 1–7. Paste in only the final validated outputs of Steps 1–7 (not reasoning traces, not the inline red-team discussions already embedded in each step). This engine independently attacks the venture from first principles, then checks whether each risk was actually addressed, and produces a verdict (ACCEPTED / REVISED / REMOVED / RETURNED FOR FURTHER VALIDATION) for every major claim, plus a Strategy Bible Clearance Report. If any engine's output is returned or revised, go back and re-run that specific engine (repeat the relevant step above), then re-run Red Team again before continuing.

**9. Give Claude `09_STRATEGY_BIBLE_MASTER_PROMPT.md`.**
Requires Step 8's Clearance Report. Claude compiles `09_Strategy_Bible.md` section by section — but only claims marked ACCEPTED in Step 8 are included. Anything without an ACCEPTED verdict is written into the document as "Not yet validated for inclusion," never silently omitted or invented.

**10. Hand the completed Strategy Bible to GPT**, along with the rules in `10_Pitch_Deck_Engine.md`, following the transfer instructions in `HANDOFF_TO_GPT.md` (paste as text, not as a file or link).

**11. GPT transforms the Bible into pitch deck content.**
GPT does not introduce new facts, numbers, or claims — only what already exists in the validated Strategy Bible.

**Output:** an investor-ready pitch deck, fully traceable back to sourced research and independently validated at every stage.

GPT's other role — the one used to build `02_STRATEGY_MASTER_PROMPT.md` through `09_STRATEGY_BIBLE_MASTER_PROMPT.md` themselves — is complete. From here on, GPT is only used for Steps 10–11 above.
