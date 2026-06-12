# GenAIxSysEng

This repository is a demonstration project showcasing how **generative AI** (via GitHub Copilot) can support a **Systems Engineer** throughout the full development lifecycle of an embedded system, following the **V-model** and **MBSE/INCOSE** guidelines.

The exemplary system is a **lightweight traffic light controller** running on a Raspberry Pi with three LEDs (red, yellow, green). It cycles through the standard traffic light sequence (red → green → yellow → red) and allows an operator to toggle all lights off and back on via a button.

---

## How to Use This Repository

The repository walks through the left-hand side of the V-model — from use cases down to implementation — using AI-assisted prompts at each phase. Each step builds on the previous one.

### Step 1 — Use Case Analysis (`docs/use_cases.md`)

Open `docs/exemplary_prompts/use_case_diagram.txt` to find the prompts used to generate the use case diagram and textual specifications in `docs/use_cases.md`. Use these as a starting point or adapt them for your own system.

### Step 2 — System Requirements (`docs/requirements.md`)

Open `docs/exemplary_prompts/requirements.txt` to find the prompt used to derive the INCOSE-compliant system requirements from the use cases into `docs/requirements.md`.

### Step 3 — Implementation (`src/`)

The `src/` directory contains the implementation code for the traffic light system. The GitHub Copilot agent (configured via `.github/copilot-instructions.md`) acts as a Senior Systems Engineer and can assist with generating, reviewing, and refining the code against the requirements.

### Step 4 — Testing (`tests/`)

The `tests/` directory is intended for test cases that verify the implementation against the system requirements, closing the right-hand side of the V-model.

---

## Project Structure

```
.github/
  copilot-instructions.md   # Copilot system prompt — defines the AI's role and rules
docs/
  use_cases.md              # Use case diagram and textual specifications
  requirements.md           # INCOSE-compliant system requirements table
  exemplary_prompts/        # Prompts used at each V-model phase
src/                        # Implementation source code
tests/                      # Test suite
```

---

## Prerequisites

- **VS Code** with the **GitHub Copilot** extension (agent mode enabled)
- A **Raspberry Pi** with three LEDs (red, yellow, green) and two push buttons wired to GPIO pins (for running the actual hardware implementation)
