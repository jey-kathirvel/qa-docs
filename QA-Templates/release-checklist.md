# Release Checklist Template

## Project Information
- **Project Name:** 
- **Release Version:** 
- **Release Date:** 
- **Prepared By:** 
- **Release Manager:** 
- **Environment:** Dev / Test / Staging / Production

## Release Summary
Briefly describe what is being released and the purpose of the release. A release checklist typically covers engineering, QA, deployment, documentation, and support readiness before sign-off [web:183][web:185][web:191].

## Pre-Release Checklist

### Planning
- [ ] Requirements or user stories for this release are approved.
- [ ] Scope is frozen for the release window.
- [ ] Risks and dependencies are identified.
- [ ] Release owner and approvers are assigned.

### Development
- [ ] All planned development work is complete.
- [ ] Code is peer reviewed.
- [ ] Unit tests are updated and passing.
- [ ] No unresolved critical code defects remain.

### QA
- [ ] Test plan is updated.
- [ ] Test cases are updated.
- [ ] Smoke tests pass on the final build.
- [ ] Regression tests pass.
- [ ] All critical defects are resolved or waived.
- [ ] Test evidence is attached.

### Deployment
- [ ] Deployment scripts are ready.
- [ ] Build artifact is tagged and versioned.
- [ ] Release configuration is correct.
- [ ] Rollback plan is prepared.
- [ ] Backup of environment or critical data is completed.

### Documentation
- [ ] Release notes are completed.
- [ ] User documentation is updated.
- [ ] Installation or upgrade instructions are updated.
- [ ] Known issues are documented.

### Support Readiness
- [ ] Support team is informed.
- [ ] Monitoring and alerting are enabled.
- [ ] Training or communication has been completed.
- [ ] Stakeholders are ready for release.

### Compliance / Legal
- [ ] Licenses and third-party components are reviewed.
- [ ] Compliance checks are complete.
- [ ] Required approvals are collected.

## Release Approval Table

| Area | Status | Owner | Comments |
|---|---|---|---|
| Planning |  |  |  |
| Development |  |  |  |
| QA |  |  |  |
| Deployment |  |  |  |
| Documentation |  |  |  |
| Support |  |  |  |
| Compliance |  |  |  |

## Go / No-Go Decision
- **Decision:** Go / No-Go
- **Decision Owner:** 
- **Decision Time:** 
- **Notes:** 

## Post-Release Checklist
- [ ] Deployment completed successfully.
- [ ] Smoke verification passed in target environment.
- [ ] Logs and monitoring are being reviewed.
- [ ] Stakeholders are notified of release completion.
- [ ] Any incidents are logged and assigned.

## Sign-Off
- **QA Lead:** __________
- **Release Manager:** __________
- **Product Owner:** __________
- **DevOps Lead:** __________
