# Container Testing Checklist

## Image Build
- [ ] Dockerfile or container definition is valid.
- [ ] Base image is approved and up to date.
- [ ] Image builds successfully.
- [ ] Image tag is versioned and traceable.
- [ ] No secrets are baked into the image.

## Image Security
- [ ] Vulnerability scan passes.
- [ ] No critical or high-severity issues remain.
- [ ] Image is signed, if required.
- [ ] License compliance is verified.
- [ ] Image comes from a trusted registry.

## Runtime Validation
- [ ] Container starts successfully.
- [ ] Container exits cleanly when stopped.
- [ ] Required environment variables are loaded.
- [ ] Mounted volumes are accessible.
- [ ] Ports are exposed only as intended.

## Application Health
- [ ] Health check endpoint returns success.
- [ ] Readiness probe passes.
- [ ] Liveness probe passes.
- [ ] Application logs are generated correctly.
- [ ] Error logging is working.

## Functional Testing
- [ ] Core application flows work inside the container.
- [ ] API endpoints respond correctly.
- [ ] Database connectivity works.
- [ ] External service integrations work.
- [ ] File upload or storage behavior is correct, if applicable.

## Resource Validation
- [ ] CPU usage is within limits.
- [ ] Memory usage is within limits.
- [ ] Disk usage is within limits.
- [ ] Container restarts do not cause failures.
- [ ] No memory leaks or crash loops are observed.

## Networking
- [ ] Container can reach required internal services.
- [ ] DNS resolution works.
- [ ] Firewall or network policy rules are correct.
- [ ] Service-to-service communication is allowed only where needed.
- [ ] No unintended public exposure exists.

## Orchestration Checks
- [ ] Kubernetes or orchestration manifest is valid, if applicable.
- [ ] Deployment replicas are correct.
- [ ] Rollout completes successfully.
- [ ] Scaling works as expected.
- [ ] Service discovery works correctly.

## Persistence and Data
- [ ] Persistent volume mounts work correctly.
- [ ] Data remains intact after restart.
- [ ] Backup and restore are verified, if applicable.
- [ ] Database migrations succeed.
- [ ] No data corruption occurs during container restart.

## Release Readiness
- [ ] Smoke tests pass after deployment.
- [ ] Monitoring and alerting are active.
- [ ] Logs are available in the centralized system.
- [ ] Rollback plan is documented.
- [ ] QA sign-off is recorded.

## Go / No-Go
- **Go:** all critical checks pass and no blocker defects remain.
- **No-go:** any build, security, runtime, or functional failure exists.
