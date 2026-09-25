# Operator Runbook

This document outlines tasks that **humans** (operators, developers, maintainers) must perform manually. It is a living checklist for setup, deployment, and maintenance.

## Accounts & Services
- [ ] **Cloud provider account** (AWS/Azure/GCP/other) with appropriate IAM roles.
- [ ] **CI/CD pipeline** configured (GitHub Actions, GitLab CI, Jenkins, etc.).
- [ ] **Monitoring/alerting** (Datadog, Sentry, CloudWatch, etc.) set up.
- [ ] **Secret management** (Vault, AWS Secrets Manager, etc.) accessible to the deployment pipeline.

## Environment Variables
**Never commit secrets.** Store them in environment variables or a secure secret manager.

### Required for Local Development
- `API_KEY` – Placeholder for external API key.
- `DATABASE_URL` – Placeholder for database connection string.
- `LOG_LEVEL` – Default: `info`.

### Required for Production
- `SECRET_KEY` – Cryptographic secret for session/token signing.
- `DATABASE_URL` – Production database connection.
- `SENTRY_DSN` – Error‑tracking service DSN (if used).
- `ALLOWED_HOSTS` – Comma‑separated list of allowed hostnames.

## Deployment Checklist
- [ ] **Build artifact** created (Docker image, binary, package).
- [ ] **Infrastructure** provisioned (Terraform, CloudFormation, etc.).
- [ ] **Database migrations** applied (if any).
- [ ] **Health checks** passing.
- [ ] **Traffic routing** updated (load balancer, DNS, ingress).
- [ ] **Backup/rollback** plan verified.

## Webhook & External Integrations
- [ ] **Webhook endpoints** registered with external services (GitHub, Stripe, etc.).
- [ ] **DNS records** configured (CNAME, A, etc.).
- [ ] **SSL/TLS certificates** provisioned and renewed automatically.

## Maintenance Tasks
- [ ] **Log rotation** configured.
- [ ] **Database backups** scheduled and tested.
- [ ] **Dependency updates** monitored (Dependabot, Renovate, etc.).
- [ ] **Security patches** applied promptly.

## Emergency Procedures
- [ ] **Secrets rotation** process documented.
- [ ] **Incident response** runbook accessible.
- [ ] **Contact list** (who to notify) up‑to‑date.

---

**Version**: [OPERATOR_TASKS_001] | **Last Reviewed**: [DATE]
<!-- Update this runbook when new operational steps are introduced. -->