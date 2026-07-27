# 11_WEB_APP_ARCHITECTURE

## Purpose

This document defines how the Hypenex AI Operating System — currently a set of markdown prompts run manually through Claude and GPT — could be converted into a working software application.

This is an architecture specification, not an implementation. It translates the prose "Must Contain" / "Inputs" / "Outputs" rules already defined across `00_Core_System.md` through `10_Pitch_Deck_Engine.md` into a structure a real system could be built against.

This document does not change how the system runs today. Every rule described here already exists in prose form in the engine files; this document only formalizes it for the purpose of eventual software conversion.

---

## Core Model: Engines as Pipeline Nodes

Every engine in this system already has three properties, defined in each `MASTER_PROMPT.md` file's "Engine Architecture" section:

- **Inputs** — what it requires before it can run.
- **Outputs** — what it produces.
- **Consumed by** — which engines depend on its output.

This is already a directed acyclic graph. A software implementation would represent each engine as a pipeline node with a typed input schema and a typed output schema, rather than a paragraph of prose.

### Pipeline graph (current sequence)
