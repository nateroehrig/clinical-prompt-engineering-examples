# MTSS Tier 2 Student Support Plan

This example demonstrates how a structured prompt can generate a clear, actionable MTSS Tier 2 student support plan from a small amount of educator-provided data. It is designed to reflect real-world Tier 2 planning needs, where teachers and support teams often supply fragmented notes and need a coherent, strengths-based, implementation-ready plan.

This scenario uses a hybrid profile very common in MTSS:
- Academic: inconsistent work completion and reduced follow-through
- Mild behavior/engagement: off-task behavior, avoidance, variable participation

---

## What this prompt demonstrates

- Uses a simple structured JSON input format that mirrors MTSS team workflows  
- Produces a non-deficit problem statement  
- Includes a hypothesis for why the concern may be occurring while staying within a Tier 2 scope  
- Identifies a small set of high-leverage Tier 2 strategies tailored to the described patterns  
- Builds progress monitoring aligned with the concern and easy for teachers to implement  
- Gives clear teacher-facing implementation steps  
- Structures the plan over a realistic 6–8 week Tier 2 cycle  

The prompt prioritizes:

- Strengths-based, non-pathologizing language  
- Educator-friendly clarity  
- Repeatability of structure and tone  
- Avoidance of jargon and speculative clinical interpretation  

---

## Files Included

- **sample_input.json**  
  A realistic set of educator notes including strengths, concerns, patterns, strategies tried, and contextual constraints.

- **prompt.md**  
  The core prompt (written in Markdown with a YAML-style system block) describing exactly how the model should transform the input JSON into a Tier 2 plan.

- **sample_output_good.md**  
  A high-quality model output demonstrating the target structure, clarity, and level of detail.
