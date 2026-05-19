# ML Data Quality Validation

## 1. Purpose
This document defines how machine learning data will be validated before training, before deployment, and during ongoing monitoring. The goal is to ensure data is complete, accurate, consistent, timely, and suitable for the intended ML use case [web:98][web:100][web:104].

## 2. Scope
This validation applies to:
- Training data.
- Validation and test data.
- Feature store inputs.
- Batch and streaming data sources.
- Labels and target variables.
- Production inference data.

## 3. Validation Principles
- Validate data at ingestion and before model training.
- Treat schema and distribution checks as mandatory.
- Track lineage and version every dataset.
- Flag anomalies early to prevent downstream model defects.
- Re-run checks when source systems or data pipelines change [web:98][web:102][web:104].

## 4. Data Quality Dimensions

| Dimension | What to Check | Typical Failure |
|---|---|---|
| Completeness | Missing values, empty columns, missing rows | Incomplete records |
| Accuracy | Correctness against trusted source | Wrong labels or values |
| Consistency | Same meaning across systems | Conflicting values |
| Validity | Format, type, range, and schema | Invalid field values |
| Timeliness | Data freshness and update latency | Stale data |
| Uniqueness | Duplicate records and entities | Double counting |
| Integrity | Referential and relational correctness | Broken joins or missing keys |

## 5. Validation Checklist

### Schema validation
- [ ] Input schema matches expected structure.
- [ ] Column names and types are correct.
- [ ] Required fields are present.
- [ ] Unexpected fields are reviewed.
- [ ] Feature transformations are versioned.

### Completeness checks
- [ ] Missing value rate is within threshold.
- [ ] Critical fields have no unacceptable nulls.
- [ ] Empty records are removed or explained.
- [ ] Label coverage is sufficient.

### Accuracy checks
- [ ] Values match trusted sources where available.
- [ ] Labels are spot-checked or audited.
- [ ] Outliers are reviewed for correctness.
- [ ] Business rules are applied to validate records.

### Consistency checks
- [ ] Formats are standardized.
- [ ] Units and encodings are aligned.
- [ ] Cross-table values reconcile.
- [ ] Duplicate entity definitions are resolved.

### Timeliness checks
- [ ] Data freshness meets SLA.
- [ ] Late-arriving records are handled correctly.
- [ ] Time windows match the intended prediction horizon.
- [ ] Stale records are excluded where needed.

### Uniqueness checks
- [ ] Duplicate rows are identified.
- [ ] Duplicate entities are deduplicated.
- [ ] Primary key integrity is confirmed.
- [ ] Duplicate labels are not present.

### Feature quality checks
- [ ] Feature distributions are reasonable.
- [ ] High-cardinality fields are controlled.
- [ ] Leakage-prone fields are excluded.
- [ ] Feature drift baseline is established.

### Label quality checks
- [ ] Labels are aligned with the target definition.
- [ ] Labeling guidelines are documented.
- [ ] Inter-annotator agreement is reviewed if applicable.
- [ ] No future information leaks into labels.

## 6. Test Metrics

| Metric | Description | Target |
|---|---|---:|
| Missing Rate | Percentage of null or missing values | <= defined threshold |
| Duplicate Rate | Percentage of duplicate records | <= defined threshold |
| Schema Error Rate | Invalid fields or types | 0 critical errors |
| Freshness Lag | Delay between source and availability | <= SLA |
| Label Accuracy | Correctness of labels | >= defined threshold |
| Drift Score | Change from baseline distribution | <= defined threshold |

## 7. Remediation Workflow
1. Detect the data issue.
2. Classify severity and affected dataset.
3. Notify the data owner.
4. Apply correction or exclusion rules.
5. Re-run validation.
6. Record the result and evidence.

## 8. Roles and Responsibilities
- Data engineers: implement validation rules and fix pipeline issues.
- Data scientists: define thresholds and inspect feature quality.
- QA: verify validation coverage and result reporting.
- Business owners: confirm data definitions and label correctness.
- Security / compliance: review sensitive data handling.

## 9. Acceptance Criteria
Data is approved for ML use when:
- Schema checks pass.
- Critical completeness and accuracy thresholds are met.
- No unresolved high-severity issues remain.
- Data lineage and versioning are recorded.
- The dataset is approved for the intended use case [web:99][web:100][web:105].

## 10. Reporting
Each validation run should produce:
- Dataset version.
- Validation date.
- Rule execution summary.
- Failed checks and severity.
- Remediation status.
- Approval sign-off.

## 11. Review Cadence
- On every data ingestion release.
- Before every model training run.
- After source system changes.
- On a scheduled basis for production monitoring.

## 12. Approval
- Data engineering sign-off: __________
- Data science sign-off: __________
- QA sign-off: __________
- Business sign-off: __________
