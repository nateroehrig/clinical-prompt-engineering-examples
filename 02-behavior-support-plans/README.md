# Project 2: Behavior Support Plan

This project demonstrates how prompt engineering can generate clear, parent friendly behavior support plans from structured behavioral data. It reflects real-world clinical reasoning drawn from developmental and school psychology, functional behavior assessment (FBA), and positive behavior interventions.

The goal is to show how an LLM can transform structured inputs (such as ABC data, hypothesized function, and environment constraints) into a practical, strengths-based plan for caregivers and educators.

## Goals

The behavior support plan should be:

- Accurate to the data and grounded in functional behavior principles.
- Respectful, strengths-based, and written for parents and educators.
- Practical and realistic for home and school routines.
- Consistently structured so it can be reused programmatically.

## High-Level Flow

### **Input:**  
Structured JSON including:

- Student profile and strengths.
- Operational definition of the target behavior.
- ABC data samples.
- Hypothesized function of the behavior.
- Environment constraints.
- Intervention goals.

### **The prompt guides the model to:**

- Explain the behavior and its function in accessible, plain language.
- Highlight strengths and protective factors that support the plan.
- Organize intervention components into clear sections, such as:
  - Setting the child up for success (prevention strategies).
  - Teaching replacement or alternative behaviors.
  - Adult responses when the behavior occurs.
  - Monitoring progress.
- Avoid guessing, inventing data, over-pathologizing, or assigning diagnoses.

### **Output:**  
A behavior support plan that a parent and teacher can realistically use to guide the next several weeks of intervention.

## Files in This Project

Inside the `01-single-behavior-plan/` directory, you will find:

- **`prompt.yaml`**  
  A structured YAML prompt designed to ingest JSON and output a clear, function-based behavior plan.

- **`sample_input.json`**  
  Example structured data simulating the type of input a production system might send.

- **`sample_output_good.md`**  
  A strong, clinically accurate model response that aligns with the data.

- **`sample_output_needs_revision.md`**  
  A realistic but imperfect response used to highlight evaluation and iteration practices.

- **`evaluation.md`**  
  A document describing the evaluation criteria, success conditions, and common failure modes. This includes how I iterate on prompts to correct issues like vague strategies, misalignment with the function, or accidental hallucinations.

## Prompt Engineering Focus

This project continues the core prompt engineering principles described in the repository’s main README:

### **Role clarity**
The model is defined as a behavior specialist or school psychologist guiding caregivers.

### **Explicit goals and constraints**
Tone, safety rules, and audience requirements are specified so outputs are:

- Parent friendly  
- Nonjudgmental  
- Functionally grounded  
- Free of speculative diagnosis  

### **Structured input and reusable format**
The prompt consumes JSON and produces a consistently organized plan with labeled sections.

### **Embedded evaluation criteria**
The prompt includes instructions aligned with how I evaluate output quality, ensuring:

- Clinical accuracy  
- Safety  
- Readability  
- Actionability  

### **Iteration based on failure modes**
Evaluation describes:

- What went wrong in earlier outputs  
- How prompt revisions fixed those issues  
- Guardrails added to reduce errors and hallucination risk  

## Purpose of This Project

This project shows how LLMs can support caregivers and educators by transforming technical behavioral data into actionable plans. It highlights my ability to:

- Use structured data (JSON) in a clinical context  
- Translate psychological and behavioral science into practical language  
- Apply systematic prompt evaluation and iteration  
- Produce outputs aligned with ethical and developmentally appropriate practice  

This mirrors real work I did as a Clinical Prompt Engineer supporting developmental assessment, behavior planning, and caregiver guidance.
