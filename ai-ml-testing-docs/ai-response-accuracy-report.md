# AI Response Accuracy Report

## Report Overview
- **Model Name:** Sample AI Model / LLM
- **Version:** v1.0.0
- **Evaluation Date:** 2026-05-19
- **Prepared By:** QA / AI Evaluation Team
- **Status:** Pending / Passed / Failed

## Purpose
This report evaluates whether AI responses are factually correct, relevant to the prompt, complete, and consistent with the expected answer. Accuracy evaluation should use reference answers or verified sources where possible, along with structured metrics and human review [web:87][web:90][web:94].

## Scope
This report covers:
- Factual correctness.
- Instruction adherence.
- Completeness.
- Hallucination detection.
- Consistency across repeated prompts.
- Safety-related accuracy issues.
- Human rating and automated scoring, where applicable.

## Evaluation Summary
The model was tested against a curated set of prompts with known expected answers or reference materials. Responses were reviewed for factual accuracy, omission errors, unsupported claims, and alignment with the intended output format [web:87][web:91][web:95].

## Accuracy Metrics

| Metric | Definition | Target | Actual Result | Status |
|---|---|---:|---:|---|
| Exact Match Rate | Percent of responses matching the reference answer |  |  | ☐ Pass / ☐ Fail |
| Factual Accuracy | Percent of factual statements verified as correct |  |  | ☐ Pass / ☐ Fail |
| Hallucination Rate | Percent of unsupported claims |  |  | ☐ Pass / ☐ Fail |
| Instruction Adherence | Percent of prompts followed correctly |  |  | ☐ Pass / ☐ Fail |
| Completeness Score | Percent of required items addressed |  |  | ☐ Pass / ☐ Fail |
| Consistency Score | Similarity across repeated runs |  |  | ☐ Pass / ☐ Fail |

## Test Set Summary

| Test ID | Prompt Type | Reference Source | Expected Result | Actual Result | Pass / Fail |
|---|---|---|---|---|---|
| T-01 | Factual Q&A |  |  |  |  |
| T-02 | Summarization |  |  |  |  |
| T-03 | Extraction |  |  |  |  |
| T-04 | Instruction following |  |  |  |  |
| T-05 | Multi-step reasoning |  |  |  |  |

## Error Analysis
- Unsupported facts were identified in responses where no reference evidence was provided.
- Some responses may be correct in content but incomplete in scope.
- Minor formatting deviations should be separated from factual errors.
- Repeated prompts should be used to detect inconsistency or unstable outputs [web:90][web:92][web:96].

## Findings

| Issue ID | Description | Severity | Frequency | Owner | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Root Causes
- Missing or weak reference data.
- Ambiguous prompt instructions.
- Overly broad model response generation.
- Insufficient guardrails for uncertain claims.
- Incomplete evaluation dataset.

## Recommendations
- Use verified reference answers for accuracy testing.
- Add a hallucination check for unsupported statements.
- Score responses across multiple dimensions, not only exact match.
- Review edge cases and ambiguous prompts separately.
- Re-run validation after prompt or model changes [web:87][web:91][web:95].

## Approval
- **QA Sign-off:** __________
- **AI Evaluation Lead:** __________
- **Product Owner:** __________
- **Release Decision:** __________

## Notes
- Keep reference answers and scoring rubrics with the report.
- Log model version, prompt version, and dataset version.
- Re-test after every model update or prompt revision.
