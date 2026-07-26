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

The Hypenex AI Operating System consists of the following engines:
| Engine | File | Run by |
|---|---|---|
| Core System | `00_Core_System.md` | — (rules, not run) |
| Research | `01_Research_Engine.md` | Claude |
| Strategy | `02_Strategy_Engine.md` | Claude |
| Product | `03_Product_Engine.md` | Claude |
| AI | `04_AI_Engine.md` | Claude |
| Finance | `05_Finance_Engine.md` | Claude |
| GTM | `06_GTM_Engine.md` | Claude |
| Investor | `07_Investor_Engine.md` | Claude |
| Red Team | `08_Red_Team_Engine.md` | Claude |
| Strategy Bible | `09_Strategy_Bible.md` | Claude (compiles) |
| Pitch Deck | `10_Pitch_Deck_Engine.md` | GPT (transforms only) |

---

# How to Run This System

1. Give Claude `RESEARCH_MASTER_PROMPT.md` as a single prompt. Claude executes Stages 1–4 (Market, Competitor, Customer, Investor research) in order, each gated by Red Team review, per the rules in `00_Core_System.md` and `08_Red_Team_Engine.md`.
2. Claude compiles validated findings into the `09_Strategy_Bible.md` structure.
3. The completed Strategy Bible is handed to GPT, along with the rules in `10_Pitch_Deck_Engine.md`.
4. GPT transforms the Bible into pitch deck content. GPT does not introduce new facts, numbers, or claims — only what already exists in the Bible.
5. Output: an investor-ready pitch deck, fully traceable back to sourced research.

GPT's other role — the one used to build `04_AI_Engine.md` through `10_Pitch_Deck_Engine.md` themselves — is complete. From here on, GPT is only used for Step 4 above.
