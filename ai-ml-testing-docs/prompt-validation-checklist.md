# Prompt Validation Checklist

## Purpose
Use this checklist to review prompts before sending them to an AI model. The goal is to make sure the prompt is clear, safe, specific, testable, and aligned to the intended output [web:78][web:80][web:85].

## Checklist

### Clarity
- [ ] The task is stated in one clear sentence.
- [ ] The desired output format is specified.
- [ ] The audience or use case is defined.
- [ ] Ambiguous terms are removed or explained.

### Context
- [ ] Enough background is provided for the model to answer correctly.
- [ ] Required source material is included.
- [ ] Relevant constraints are listed.
- [ ] Unnecessary details are removed.

### Specificity
- [ ] The prompt names the exact deliverable.
- [ ] The prompt includes scope boundaries.
- [ ] The prompt defines what to include and exclude.
- [ ] Any required style, tone, or length is stated.

### Accuracy
- [ ] Facts, dates, and numbers in the prompt are correct.
- [ ] Any assumptions are explicitly marked.
- [ ] The prompt does not force unsupported conclusions.
- [ ] The prompt asks for verification when needed.

### Safety and Compliance
- [ ] The prompt does not request disallowed content.
- [ ] No confidential, private, or sensitive data is exposed.
- [ ] The prompt avoids instructions that create legal or safety risk.
- [ ] The prompt respects policy, privacy, and copyright constraints.

### Output Control
- [ ] The response format is defined, such as list, table, JSON, or markdown.
- [ ] The level of detail is specified.
- [ ] The model is told whether to be concise or detailed.
- [ ] Any required headings or section order are given.

### Testing
- [ ] The prompt has been tested with a sample input.
- [ ] The output is checked for hallucinations.
- [ ] The output is checked for completeness.
- [ ] The output is checked for consistency with the prompt.

### Evaluation
- [ ] Success criteria are defined.
- [ ] The expected answer quality is known.
- [ ] Edge cases are considered.
- [ ] A fallback or retry plan exists if output quality is poor.

## Example Review Questions
- Does the prompt tell the model exactly what to do?
- Would another person interpret the prompt the same way?
- Can the output be measured against clear criteria?
- Does the prompt include enough information without overloading the model?

## Sign-Off
- **Prompt Owner:** __________
- **Reviewer:** __________
- **Approved for Use:** __________
