# Agent Operating Instructions

This repository is used to store and evolve skills, prompts, and coding practices.

## Default Workflow (Mandatory)

All non-trivial coding tasks must follow this order:

1. Research
2. Planning
3. Annotation cycle
4. Implementation
5. Feedback and iteration

Do not skip directly to implementation for non-trivial work.

## Phase 1: Research

- Read relevant code deeply before proposing changes.
- Write findings to a persistent markdown file such as `research.md`.
- Include architecture constraints, existing patterns, and potential risks.
- If research is incomplete or uncertain, continue research before planning.

## Phase 2: Planning

- Create a detailed `plan.md` before writing code.
- Base the plan on actual repository code, not assumptions.
- Include:
  - target files
  - approach and tradeoffs
  - migration or compatibility concerns
  - validation strategy (tests, type checks, lint)

## Annotation Cycle (Human-in-the-loop)

- Treat `plan.md` as the single review surface.
- Incorporate user inline notes directly into the plan.
- Repeat update cycles until the plan is explicitly approved.
- Explicit guardrail: do not implement while plan review is ongoing.

## Todo Breakdown Before Coding

- Add a granular checklist to `plan.md` with phases and tasks.
- Use this checklist as execution tracking.
- Mark completed tasks during implementation.

## Phase 3: Implementation

When implementation is approved:

- Execute the approved plan completely.
- Keep code simple and maintainable.
- Avoid unnecessary comments and avoid over-engineering.
- Respect strict typing; do not introduce `any` or `unknown` without explicit justification.
- Continuously validate with type checks and relevant tests.

## Feedback During Implementation

- Accept short corrective feedback and apply it quickly.
- For UI/behavior parity, reuse existing project patterns and reference implementations.
- If implementation goes in the wrong direction, prefer revert + narrow re-scope over patching a bad path.

## Decision Rights

- Agent executes.
- Human decides scope, tradeoffs, API/interface stability, and what to skip.

## Core Principle

Separate thinking from typing:

- research prevents ignorant changes
- planning prevents wrong changes
- annotation injects domain judgment
- implementation becomes mechanical

## Baseline Coding Rules

Apply Rob Pike's rules as default coding heuristics:

- `materials/frameworks/rob-pike-5-rules.md`
