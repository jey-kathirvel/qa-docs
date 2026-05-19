# AI Hallucination Test Report

## Report Overview
- **Model Name:** Sample AI Model / LLM
- **Version:** v1.0.0
- **Test Date:** 2026-05-19
- **Prepared By:** QA / AI Evaluation Team
- **Status:** Pending / Passed / Failed

## Purpose
This report documents hallucination testing for AI-generated responses. Hallucination testing measures whether the model invents facts, contradicts provided context, or produces unverifiable statements, and it is commonly evaluated using context-grounded checks and human review [web:106][web:110][web:113].

## Scope
This report covers:
- Factual hallucinations.
- Context contradictions.
- Unsupported claims.
- Source-grounded response quality.
- Summarization hallucinations.
- Retrieval-augmented generation behavior, if applicable.

## Evaluation Summary
The model was tested using prompts with known reference context or verified source material. Responses were reviewed to detect contradictions, fabricated details, and statements that could not be supported by the provided context [web:108][web:112][web:115].

## Hallucination Metrics

| Metric | Definition | Target | Actual Result | Status |
|---|---|---:|---:|---|
| Hallucination Rate | Share of responses with unsupported claims |  |  | ☐ Pass / ☐ Fail |
| Contradiction Rate | Share of responses that conflict with context |  |  | ☐ Pass / ☐ Fail |
| Unsupported Fact Count | Number of fabricated facts found | 0 |  | ☐ Pass / ☐ Fail |
| Context Adherence | Response stays within provided context |  |  | ☐ Pass / ☐ Fail |
| Faithfulness Score | Response is grounded in source material |  |  | ☐ Pass / ☐ Fail |

## Test Set Summary

| Test ID | Prompt Type | Reference Context | Expected Result | Actual Result | Pass / Fail |
|---|---|---|---|---|---|
| H-01 | Fact-based Q&A |  |  |  |  |
| H-02 | Summarization |  |  |  |  |
| H-03 | Multi-step reasoning |  |  |  |  |
| H-04 | RAG response |  |  |  |  |
| H-05 | Context contradiction |  |  |  |  |

## Findings
- No hallucinations detected / hallucinations detected.
- Any fabricated content should be listed with the exact unsupported statement.
- Contradictions to source context should be flagged separately from omissions.
- Summarization tasks often require segment-level checking for localized hallucinations [web:107][web:109][web:113].

## Issues Log

| Issue ID | Description | Severity | Owner | ETA | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Root Cause Analysis
- Weak grounding in source context.
- Ambiguous prompt wording.
- Over-reliance on model priors.
- Retrieval misses or noisy context.
- Insufficient verification before output.

## Recommendations
- Use grounded evaluation with reference context.
- Check each factual claim against source material.
- Break long answers into smaller segments for verification.
- Add automated hallucination metrics where possible.
- Re-test after prompt, retrieval, or model changes [web:106][web:112][web:113].

## Sign-Off
- **QA Sign-off:** __________
- **AI Evaluation Lead:** __________
- **Product Owner:** __________
- **Release Decision:** __________

## Notes
- Save the prompt, reference context, and expected answer with this report.
- Record model version, prompt version, and dataset/versioned source identifiers.
- Re-run tests after every model update or retrieval change.
