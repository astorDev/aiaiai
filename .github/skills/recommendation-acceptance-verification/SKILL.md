---
name: recommendation-acceptance-verification
description: 'Define Verification criteria for investigation index creation (including inv-index workflows) when the goal is a recommendation. Trigger on choose/propose/recommend/compare-options requests. Success must be explicit user or stakeholder acceptance of the recommendation.'
argument-hint: 'Investigation goal or draft index content'
user-invocable: true
---

# Recommendation Acceptance Verification

Use this skill to write a correct Verification statement in investigation index files when the goal is to produce a recommendation.

## Outcome

Produce one atomic Verification sentence that is externally verifiable and means user acceptance of the recommendation.

## When To Use

- Investigation goal asks for recommendation, proposal, or decision guidance
- Success depends on user or stakeholder approval
- Existing Verification text is vague, internal, or artifact-based

## Input

- Goal statement from the investigation request
- Optional draft Problem Descriptions and Verification text

## Procedure

1. Classify the goal.
- If the goal is recommendation-oriented, continue.
- If the goal is execution-oriented (for example pass tests, fix runtime error), do not use this acceptance pattern.

2. Identify the decision owner.
- Prefer user acceptance.
- If user delegates decision authority, use named stakeholder acceptance.

3. Convert success into external validation.
- Success must be an explicit acceptance event, not internal artifact completion.
- Valid signals include a direct confirmation message that recommendation is accepted.

4. Write the Verification sentence.
- Use one sentence only.
- Keep it specific, atomic, and unambiguous.
- Avoid lists and avoid references to file creation as success.

5. Run quality checks.
- Can a third party determine pass or fail from observable evidence?
- Does the sentence express acceptance, not just delivery?
- Is there exactly one success condition?

## Verification Sentence Pattern

Investigation is successful only when the user explicitly confirms acceptance of the provided recommendation.

## Good Examples

- Investigation is successful only when the user explicitly confirms acceptance of the recommended option and asks to proceed with it.
- Investigation is successful only when the product owner explicitly approves one provided recommendation for implementation.

## Bad Examples

- Investigation is successful when recommendation.md is created.
- Investigation is successful when three options are compared.
- Investigation is successful when best effort recommendation is provided.

## Integration Note For inv-index

When creating buffer alias index files, apply this skill if Problem Descriptions indicates the requested outcome is a recommendation.
