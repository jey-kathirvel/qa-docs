# Pipeline Verification Checklist

## Source Control
- [ ] Branch naming follows team standard.
- [ ] Pull request has required reviewers.
- [ ] Commit message is clear and traceable.
- [ ] No direct commits to protected branches.

## Code Quality
- [ ] Linting passes.
- [ ] Formatting checks pass.
- [ ] Static code analysis passes.
- [ ] Code coverage meets minimum threshold.
- [ ] No critical or blocker findings remain.

## Security
- [ ] Secrets scan passes.
- [ ] Dependency vulnerability scan passes.
- [ ] SAST findings are reviewed and triaged.
- [ ] Container image scan passes, if applicable.
- [ ] License compliance is verified, if required.

## Build
- [ ] Build completes successfully.
- [ ] Version number is generated correctly.
- [ ] Artifact is stored in the approved repository.
- [ ] Build is reproducible from the same commit.
- [ ] Build logs are retained.

## Test
- [ ] Unit tests pass.
- [ ] Integration tests pass.
- [ ] API tests pass.
- [ ] Smoke tests pass.
- [ ] Regression tests pass for release candidates.
- [ ] Database migration tests pass, if applicable.
- [ ] UI tests pass, if the product includes a frontend.

## Environment
- [ ] Required environment variables are configured.
- [ ] Test data is available and sanitized.
- [ ] Services and dependencies are reachable.
- [ ] Configuration matches the target environment.
- [ ] Infrastructure is deployed from version-controlled templates.

## Deployment
- [ ] Deployment plan is approved.
- [ ] Rollback steps are documented and validated.
- [ ] Release notes are prepared.
- [ ] Health checks pass after deployment.
- [ ] Monitoring and alerting are active.

## Release Readiness
- [ ] No open Severity 1 defects.
- [ ] Accepted exceptions are documented.
- [ ] QA sign-off is recorded.
- [ ] Business approval is recorded, if needed.
- [ ] Go/no-go decision is captured.

## Post-Deploy
- [ ] Key user flows work in staging or production.
- [ ] Logs show no critical errors.
- [ ] Metrics are within expected ranges.
- [ ] Smoke verification is completed.
- [ ] Support team is informed of the release.

## Go/No-Go Rule
- **Go:** all blocking checks pass and approvals are complete.
- **No-go:** any critical build, test, security, or deployment issue remains.
