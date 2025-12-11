# Clinical Prompt Engineering Examples

This repository showcases examples of clinical prompt engineering grounded in developmental and school psychology.  

The projects are inspired by my work as a licensed school psychologist and as a Clinical Prompt Engineer on a clinical team that supported developmental assessment, diagnostic decision support, and parent guidance.

The focus is on three things:

1. Designing prompts that reflect real clinical reasoning and best practices.  
2. Structuring inputs and outputs (JSON, YAML) in a clear and reproducible way.  
3. Evaluating LLM responses for accuracy, safety, and usefulness for parents and educators.

---

## Repository Structure

Planned structure:

- `01-assessment-summaries/`  
  Parent friendly summaries of standardized assessments (for example Vineland, cognitive tests) from structured JSON input.

- `02-clinical-integrations/`  
  Prompts that integrate information across sources, such as rating scales, interviews, and observations, to produce a coherent clinical picture.

- `03-parent-guidance-plans/`  
  Prompts that translate assessment findings into practical, step by step strategies for home and school.

Each folder will include:

- `prompt.md` or `prompt.yaml`  
  The core prompt template with comments.

- `sample_input.json`  
  Structured example input data that simulates what a production system might pass to the model.

- `sample_output_good.md`  
  A strong model response that meets criteria.

- `sample_output_needs_revision.md`  
  A realistic but imperfect response, useful for illustrating evaluation and iteration.

- `evaluation.md`  
  How I evaluate outputs and iterate on prompts, including success criteria and common failure modes.

---

## Project 1: Parent Friendly Assessment Summary

**Goal**  
Generate a parent friendly summary of a child’s assessment that is:

- Accurate and clinically grounded.  
- Written in everyday language.  
- Strengths based.  
- Clear about next steps at home and at school.

**High level flow**

1. Input: structured JSON that includes:
   - Assessment scores and interpretations.  
   - Key developmental history.  
   - Observations and concerns.  
2. The prompt guides the model to:
   - Explain results in plain language.  
   - Highlight strengths and protective factors.  
   - Describe areas of need without jargon.  
   - Suggest practical, realistic strategies for home and school.  
3. Output: a narrative summary that a parent could receive after an evaluation.

This project reflects work I did on:

- Prompting from structured JSON.  
- Aligning language with best practices in developmental and school psychology.  
- Iterating until outputs were accurate, respectful, and easy for parents to understand.

---

## Prompt Engineering Principles Used

Across projects in this repo I use a consistent set of prompt engineering principles:

1. **Role clarity**  
   Define the model as a specific professional identity, for example:  
   “You are a licensed school psychologist who specializes in explaining assessment results to caregivers.”

2. **Explicit goals and constraints**  
   Tell the model exactly what we are trying to achieve and what we want to avoid, including:
   - Audience (for example caregivers with no formal training).  
   - Tone (collaborative, non blaming, hopeful, realistic).  
   - Content constraints (no diagnoses that are not supported, no speculation beyond the data).

3. **Structured input and output**  
   Use JSON for input and clear sections in the output, such as:
   - Overview  
   - Strengths  
   - Areas of need  
   - What this means day to day  
   - Strategies at home  
   - Strategies at school

4. **Evaluation criteria baked into the prompt**  
   Include instructions that reinforce evaluation criteria, for example:
   - “If the scores do not clearly support a diagnosis, do not name one. Describe patterns of strengths and needs instead.”  
   - “Use concrete examples that parents are likely to see at home or in the classroom.”

5. **Iteration guided by failures**  
   Each `evaluation.md` file describes:
   - Common issues found in early outputs.  
   - How prompts were revised to address these issues.  
   - Checks used to prevent serious errors, such as hallucinated test scores or unsupported diagnostic claims.

---

## Evaluation Approach

Each project includes an `evaluation.md` that covers:

- **Clinical accuracy**  
  Does the response reflect the data correctly and use language that would be acceptable in a real report or feedback session?

- **Safety and ethics**  
  Does the response avoid harmful labels, blame, or unrealistic guarantees?  
  Does it respect family diversity and uncertainty in the data?

- **Readability and usefulness**  
  Could a parent or educator:
  - Read this one time and understand the key points?  
  - Identify 1 to 3 clear actions they can take in the next week?

- **Model specific failure modes**  
  For example:
  - Overconfident diagnostic statements.  
  - Inconsistent use of the same scores.  
  - Adding details that are not present in the input.

Where possible, I describe evaluation in a way that could be converted later into automated checks or rubric scoring.

---

## Who This Repo Is For

- Hiring managers or collaborators who want to see how I:
  - Translate clinical practice into prompt design.  
  - Work with structured data such as JSON.  
  - Evaluate and iterate on prompts in a systematic way.

- Educators, school psychologists, and clinicians who are curious about how LLMs can:
  - Support clear communication with parents.  
  - Bridge formal assessments and everyday life at home and school.

---

## Next Steps

Planned additions:

- `01-assessment-summaries/` folder with:
  - A complete example prompt.  
  - Sample JSON input and outputs.  
  - An evaluation document.

- Additional projects that show:
  - Integration across multiple rating scales.  
  - MTSS and IEP related guidance framed for caregivers.  
  - Behavioral and executive functioning strategy plans for home and school.

As I add content, I will keep the prompts and evaluation criteria transparent so that others can see the reasoning behind each design decision.

