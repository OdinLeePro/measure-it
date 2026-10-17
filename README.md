# LLM Judge Validation & Noise Floor Analysis

An automated evaluation harness designed to test and validate an AI-driven triage system. This project establishes a robust testing framework to measure Large Language Model (LLM) performance, validate secondary "LLM Judges," and calculate statistical noise floors across prompt iterations.

### My Contributions & Engineering Focus
While the baseline AI triage application was provided as part of an AI Systems Engineering curriculum, my work focused entirely on building the evaluation architecture:
*   **Golden Dataset Generation:** Designed a comprehensive 71-ticket testing dataset (`golden.json`) featuring realistic intents, adversarial inputs, and edge cases mapped directly to business policy constraints.
*   **Python Evaluation Logic:** Extended baseline scoring scripts to include custom validation functions, ensuring numeric outputs strictly adhered to policy caps and identifying model hallucinations.
*   **LLM Judge Architecture:** Designed a secondary prompt rubric to act as an "LLM Judge" evaluating the primary model's textual rationale. Validated this judge's accuracy by cross-referencing its outputs against 30 manually hand-labeled tickets to identify leniency and failure patterns.
*   **Noise Floor Analysis:** Executed multi-run sweeps (5 iterations per slice) to establish a baseline noise floor, proving whether prompt modifications yielded statistically significant improvements or just random variance.
