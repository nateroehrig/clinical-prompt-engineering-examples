# Evaluation of MTSS Tier 2 Student Support Plan Outputs

This document evaluates two model outputs generated from the same input JSON:
1. `sample_output_good.md`  
2. `sample_output_needs_revision.md`  

The purpose is to illustrate how systematic evaluation guides iterative prompt refinement to ensure clarity, accuracy, and alignment with MTSS Tier 2 best practices.

---

## Evaluation Criteria

Outputs were reviewed across the following dimensions:

1. **Accuracy and Input Fidelity**  
   - Uses only information present in the input JSON  
   - Avoids speculation, assumptions, or invented details  

2. **Alignment with MTSS Tier 2 Practices**  
   - Focus on skill-building and access supports  
   - Avoids diagnostic or clinical reasoning  
   - Provides feasible strategies that fit typical classroom constraints  

3. **Actionability and Clarity**  
   - Provides clearly structured, teacher-facing steps  
   - Uses strengths-based, non-pathologizing language  
   - Produces a plan that could realistically be implemented  

4. **Format Adherence**  
   - Follows the required section structure from `prompt.md`  
   - Maintains consistent tone and organization  

5. **Bias and Ethical Considerations**  
   - Avoids labeling, deficit framing, or punitive approaches  
   - Respects student dignity and developmentally appropriate framing  

---

# Evaluation of High-Quality Output (`sample_output_good.md`)

### Strengths

- **High input fidelity**: The plan stays strictly within the provided data, avoiding assumptions or invented causes.  
- **Clear MTSS alignment**: Strategies are skill-oriented, supportive, feasible, and appropriate for Tier 2.  
- **Actionable and specific**: Each strategy contains teacher actions, student actions, and clear frequency.  
- **Consistent formatting**: All required sections are present and well structured.  
- **Strengths-based tone**: The plan begins by highlighting Jordan’s assets in a clear, respectful manner.  
- **Practical progress monitoring**: Measures align directly with the described concerns and can be tracked easily.  
- **Review timeline**: Matches the 8-week timeframe in the JSON.

### Areas for continued refinement
- Continue tightening strategy descriptions to ensure maximal feasibility in high-class-size settings.  
- Could add slightly more precision to what qualifies as improved performance (already quite strong).  

Overall, this output meets expectations for an educator-ready Tier 2 support plan.

---

# Evaluation of Needs Revision Output (`sample_output_needs_revision.md`)

### Major Issues

- **Speculative clinical language**: Introduces anxiety, ADHD-like symptoms, learning disabilities, and motivation assumptions not supported by data.  
- **Deficit-based framing**: Words like “refuses,” “shuts down,” and “needs to be pushed” do not align with MTSS or strengths-based practice.  
- **Incorrect MTSS level**: Uses punitive or ineffective strategies (e.g., recess work completion, behavior charts without clear purpose).  
- **Poor structure**: Missing required sections and lacking consistent formatting.  
- **Low actionability**: Strategies are vague, generic, or not feasible (e.g., “remind him frequently”).  
- **Input inaccuracies**: Asserts chronic behavior patterns not present in the JSON.  
- **Minimal strengths integration**: Strengths not meaningfully incorporated into the plan.  

This output reflects common pitfalls in naive model generations and underscores the need for strong prompt guardrails.

---

# Summary

Evaluating outputs through these criteria supports:

- Better prompt iteration  
- More reliable educator-facing outputs  
- Ethical and developmentally aligned reasoning  
- Prevention of overgeneralization, bias, and invented details  
- High-quality MTSS Tier 2 planning workflows  

The comparison highlights how explicit structure, guardrails, and reasoning constraints dramatically improve the usefulness and safety of AI-generated student support plans.
