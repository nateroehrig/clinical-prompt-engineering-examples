# Clinical Prompt Engineering Examples

This repository showcases examples of clinical prompt engineering grounded in developmental psychology, school psychology, and real-world product experience.

The projects reflect my work as a licensed school psychologist and as a Clinical Prompt Engineer on a clinical team supporting developmental assessment, diagnostic decision support, MTSS workflows, and caregiver-facing communication.

The portfolio focuses on three things:

1. Designing prompts that reflect real clinical reasoning and best practices.  
2. Structuring inputs and outputs (JSON, YAML) for clarity, consistency, and reproducibility.  
3. Evaluating LLM responses for accuracy, safety, and usefulness for caregivers and educators.

---

## Repository Structure

Current structure:

- `01-assessment-summaries/`  
  Parent friendly summaries of standardized assessments (for example Vineland-3, cognitive testing) generated from structured JSON input.

- `02-behavior-support-plans/`  
  Prompts that generate behavior support plans using student data, contextual information, and intervention logic aligned with school-based MTSS and behavior-analytic principles.

- `03-mtss-tier2-support-plans/`  
  Prompts that generate Tier 2 MTSS student support plans that integrate concerns, goals, and intervention steps in a structured, school-ready format.

Each folder includes:

- `prompt.md` or `prompt.yaml` – The core prompt template with comments.  
- `sample_input.json` – Structured example input representing what a production system might pass into the model.  
- `sample_output_good.md` – A strong model response that meets criteria.  
- `sample_output_needs_revision.md` – A realistic but imperfect example to illustrate evaluation and iterative improvement.  
- `evaluation.md` – How I evaluate outputs, identify issues, and revise prompts.

---

## Project 1: Parent Friendly Assessment Summary

**Goal**  
Generate a parent friendly summary of a child’s assessment that is:

- Accurate and clinically grounded  
- Easy to understand  
- Strengths based  
- Clear about functional implications and next steps  

**Workflow**

1. **Input:** structured JSON including:  
   - Assessment scores and interpretations  
   - Developmental and educational history  
   - Observations and caregiver concerns  

2. **Prompt guides the model to:**  
   - Explain results in plain language  
   - Highlight strengths and protective factors  
   - Describe areas of need without jargon  
   - Suggest practical strategies for home and school  

3. **Output:** a narrative summary similar to what families receive after an evaluation.

This project demonstrates:

- Prompting from structured JSON  
- Translating technical data into accessible language  
- Ensuring accuracy and safety when explaining assessment findings  
- Iterative refinement to reduce hallucinations and improve clarity  

---

## Project 2: Behavior Support Plan Generator

**Goal**  
Generate a behavior support plan that:

- Defines the behavior clearly  
- Reflects an understanding of potential functions  
- Includes proactive, instructional, and response strategies  
- Aligns with typical MTSS and school-based behavior practices  

**Workflow**

1. **Input:** JSON including:  
   - Target behavior definition and examples  
   - Setting events and triggers  
   - Motivators and strengths  
   - Current supports and constraints  

2. **Prompt guides the model to:**  
   - Offer a brief, hypothesis-level functional understanding  
   - Propose realistic proactive and instructional strategies  
   - Outline how adults can respond consistently and safely  

3. **Output:** a structured behavior support plan that can be reviewed and adapted by a school team.

---

## Project 3: MTSS Tier 2 Student Support Plan

**Goal**  
Generate a Tier 2 MTSS support plan for a single student that:

- Summarizes core concerns in family-friendly language  
- Identifies goals and practical interventions  
- Suggests reasonable progress monitoring ideas  

**Workflow**

1. **Input:** JSON including:  
   - Presenting concerns and indicators  
   - Previous interventions  
   - Strengths, interests, and contextual factors  

2. **Prompt guides the model to:**  
   - Clarify the concern  
   - Recommend Tier 2 strategies that fit typical school conditions  
   - Describe what progress looks like in concrete terms  

3. **Output:** a structured plan aligned with school MTSS workflows.

---

## Prompt Engineering Principles Used Across Projects

1. **Role clarity**  
   Define the model’s professional role and responsibilities.

2. **Explicit goals and constraints**  
   Set tone, audience, content limits, and guardrails to prevent clinical or educational inaccuracies.

3. **Structured input and output**  
   Use JSON input schemas and consistent output sections for reproducibility.

4. **Embedded evaluation criteria**  
   Include instructions that mitigate hallucination, overinterpretation, or inaccurate conclusions.

5. **Iteration informed by failures**  
   Evaluate outputs systematically and revise prompts to address common failure modes.

---

## Evaluation Approach

Each project includes criteria for assessing:

### Clinical and educational accuracy  
Does the response adhere to evidence-based practices and match the provided data?

### Safety and ethics  
Does the response avoid harmful labels, blame, overconfident diagnostic statements, or unrealistic claims?

### Readability and usefulness  
Would a caregiver or educator quickly understand the key points and identify next steps?

### Model-specific error patterns  
Examples include:  
- Contradictions  
- Hallucinated data  
- Unsupported diagnostic language  
- Overly generic strategies  

---

## Who This Repo Is For

- **Hiring managers** evaluating my ability to:  
  - Design clinically sound, guardrail-heavy prompts  
  - Work with structured data workflows  
  - Produce safe, accurate, repeatable outputs  
  - Document evaluation and iteration clearly  

- **Clinicians and educators** exploring how LLMs can be used to:  
  - Translate assessment data into accessible summaries  
  - Support MTSS and behavior planning  
  - Generate practical intervention ideas for home and school  
