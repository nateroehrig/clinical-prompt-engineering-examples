# Evaluation of Behavior Support Plan Outputs

This document outlines the criteria used to evaluate LLM-generated behavior support plans and describes how the `sample_output_good.md` meets expectations while `sample_output_needs_revision.md` illustrates common failure modes. This mirrors real evaluation workflows used in clinical prompt engineering for developmental and school psychology contexts.

---

## Evaluation Goals

A strong behavior support plan must be:

1. **Clinically accurate**  
   - Aligns with ABC data and hypothesized function  
   - Uses observable, operational language  
   - Avoids speculation or pathologizing  

2. **Strengths based and parent friendly**  
   - Written in supportive, everyday language  
   - Avoids blame and avoids moralizing statements  
   - Explains concepts clearly without jargon  

3. **Functionally aligned**  
   - Strategies must logically follow from the function of behavior  
   - Replacement behaviors must serve the same purpose  
   - Adult responses must reinforce desired behavior, not accidental reinforcement of the problem behavior  

4. **Structured and reproducible**  
   - Uses consistent section headers  
   - Produces a format that can be reused programmatically  
   - Follows the required output template  

5. **Safe and ethical**  
   - No unsupported diagnostic statements  
   - No speculation about trauma, intent, or home life  
   - Avoids stigmatizing language  

---

## Evaluation of Strong Output (`sample_output_good.md`)

The strong output demonstrates:

### **1. Accurate interpretation of the data**
- Clearly identifies the function as access to adult attention, which matches the ABC patterns.
- Does not introduce alternative explanations (e.g., avoidance, boredom) that are not supported.

### **2. Strengths-based framing**
- Highlights Aiden’s curiosity, motivation, and responsiveness to visuals.
- Uses these strengths to justify intervention choices (e.g., visual work steps).

### **3. Clear operational description**
- Restates the target behavior in understandable terms.
- Provides frequency, duration, and severity without jargon.

### **4. Function-based intervention recommendations**
- Prevention strategies reduce ambiguity and increase predictability.
- Replacement behaviors give Aiden appropriate ways to get attention.
- Adult responses minimize reinforcement of out-of-seat behavior.

### **5. Safe and supportive tone**
- No blaming language.
- Developmentally appropriate expectations.
- Warm, collaborative tone for caregivers.

### **6. Structured sections that match the template**
All required sections appear and are populated with clear, actionable content.

---

## Evaluation of Weak Output (`sample_output_needs_revision.md`)

This output includes several realistic failure modes commonly seen in unrefined LLM outputs.

### **1. Speculation beyond the data**
- Lists multiple possible functions without anchoring to the provided ABC data.
- Includes causes not supported in the input (“might be bored,” “might not want to try,” “hard to know for sure”).

### **2. Tone concerns**
- Phrases like “when he wants to” or “try harder” introduce judgment.
- Language is less strengths-based and less collaborative.

### **3. Poor functional alignment**
- Recommends giving immediate help when Aiden gets up, which reinforces the problem behavior.
- Suggests allowing movement breaks “whenever needed,” which may increase escape-maintained behavior if that were the case.
- Rewards for staying seated are generic and disconnected from function.

### **4. Missing key intervention components**
- No teaching strategies for replacement behaviors.
- No proactive strategies grounded in his strengths.
- No explanation of why the behavior occurs.

### **5. Lack of clear structure**
- Sections are inconsistent and incomplete.
- Missing required headings and clear formatting.

### **6. Safety and ethical concerns**
- Implies volitional control (“try harder”), which is inappropriate.
- Introduces unsupported interpretations of motivation.

These issues make it highly useful as a demonstration of how outputs are evaluated and why prompt iteration is necessary.

---

## How Outputs Inform Prompt Revisions

Issues in weak outputs typically signal the need for:

1. **Stronger constraints on speculation**  
   - Explicit instructions: “Do not suggest alternative functions beyond the ABC data.”

2. **Clearer structure enforcement**  
   - Requiring specific section headers prevents drifting or omissions.

3. **Explicit tone guidance**  
   - Emphasize supportive, nonjudgmental language.

4. **Explicit function-based intervention logic**  
   - Reinforce that prevention, teaching, and responses must connect to the hypothesized function.

5. **Guardrails against reinforcement errors**  
   - Prompts should forbid strategies that accidentally strengthen target behaviors.

6. **Reiteration of safety guidelines**  
   - No blame, no speculation, no invented data.

The final prompt in `prompt.yaml` reflects these revisions and constraints.

---

## Summary

This evaluation framework demonstrates the ability to:

- Detect clinical inaccuracies  
- Identify reinforcement errors and function mismatches  
- Assess alignment with structured templates  
- Apply ethical and safety principles  
- Iteratively refine prompts based on observed failure modes  

This process reflects real-world clinical prompt engineering and shows how structured reasoning ensures LLM outputs remain accurate, safe, and useful for caregivers and educators.
