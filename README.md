<p align="center">
  <img src="./header.png" alt="Miroslav Strugarevic DevOps and Platform Engineering header" width="100%">
</p>

# Miroslav Strugarević

**Senior DevOps / Platform Engineer**

I design reliable cloud platforms, delivery pipelines, infrastructure automation, and operational tooling with a focus on maintainability, security, and failure-aware engineering.

I have approximately 15 years of experience in IT, including approximately 10 years across DevOps, cloud infrastructure, automation, platform engineering, and production operations.

## Featured Engineering Work

### [aws-security-auditor](https://github.com/mstrugarevic1/aws-security-auditor)

A Python CLI for read-only AWS account posture reviews across common security, cost, and governance checks.

- Uses read-only AWS List, Get, and Describe operations with a local allowlist wrapper that blocks unapproved operations before boto3 is called.
- Supports named profiles, STS AssumeRole, optional external IDs, region selection, region exclusions, and global/account-level checks.
- Produces structured findings with severity filtering, `fail-on` exit behavior, and table, JSON, Markdown, and CSV output.
- Includes Slack notification support without printing webhook URLs or changing scan exit behavior on notification failure.
- Packaged as a Python CLI with Ruff, mypy strict mode, pytest coverage, and GitHub Actions CI.

Demonstrates: AWS security automation, safe permission boundaries, maintainable Python CLI design, structured findings, and testable operational tooling.

Relevant links: [README](https://github.com/mstrugarevic1/aws-security-auditor), [example config](https://github.com/mstrugarevic1/aws-security-auditor/blob/main/examples/aws-security-auditor.toml), [example report](https://github.com/mstrugarevic1/aws-security-auditor/blob/main/examples/report.md), [read-only client](https://github.com/mstrugarevic1/aws-security-auditor/blob/main/src/aws_security_auditor/readonly_client.py)

### [ops-diagnostics-toolkit](https://github.com/mstrugarevic1/ops-diagnostics-toolkit)

A read-only Linux diagnostics toolkit for repeatable system, network, DNS, TLS, service, and host pressure checks.

- Provides focused commands for disk usage, systemd service health, listening ports, DNS resolution, TLS expiry, and host pressure.
- Uses non-destructive Bash scripts with explicit input validation, clear error messages, and predictable exit codes.
- Produces monitoring-friendly terminal output and documents how to interpret results and limitations.
- Includes ShellCheck, shfmt, Bats tests with command fixtures, smoke checks, and version consistency validation.
- Provides Debian package generation with Bash version checks and command aliases without the `.sh` suffix.

Demonstrates: practical Linux troubleshooting, shell engineering, safe automation, packaging, release management, and monitoring integration.

Relevant links: [README](https://github.com/mstrugarevic1/ops-diagnostics-toolkit), [scripts](https://github.com/mstrugarevic1/ops-diagnostics-toolkit/tree/main/scripts), [tests](https://github.com/mstrugarevic1/ops-diagnostics-toolkit/tree/main/tests), [Makefile](https://github.com/mstrugarevic1/ops-diagnostics-toolkit/blob/main/Makefile)

### [aws-ecs-internal-service-monitor](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor)

An AWS ECS/Fargate reference implementation for internal HTTP service monitoring with separated API, scheduler, and worker roles.

- Runs locally with an in-memory repository, in-memory queue, and log notifications; AWS mode uses DynamoDB, SQS, and SNS when configured.
- Separates API responsibilities from scheduler queueing and worker check execution.
- Includes retry-oriented worker behavior, idempotent result handling, failure threshold alerts, recovery notifications, and DLQ-oriented failure scenarios.
- Provides Terraform modules for networking, ECS, ECR, DynamoDB, SQS/SNS messaging, and observability resources.
- Documents architecture, deployment boundaries, security considerations, observability, failure scenarios, limitations, and cost cleanup.

Demonstrates: event-driven AWS architecture, asynchronous processing, infrastructure as code, service separation, observability, and explicit operational boundaries.

Relevant links: [README](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor), [architecture](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor/blob/main/docs/architecture.md), [deployment notes](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor/blob/main/docs/deployment.md), [failure scenarios](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor/blob/main/docs/failure-scenarios.md), [security considerations](https://github.com/mstrugarevic1/aws-ecs-internal-service-monitor/blob/main/docs/security-considerations.md)

### [docs](https://github.com/mstrugarevic1/docs)

An engineering knowledge base for infrastructure architecture, migration planning, disaster recovery, CI/CD, Kubernetes, Terraform, and operational readiness.

- Covers Terraform monolith decomposition, state separation, dependency direction, state boundaries, and blast-radius reduction.
- Documents disaster recovery concepts including RTO, RPO, failover, failback, AWS and hybrid recovery patterns, and operational validation.
- Includes Kubernetes migration planning, Rancher 1.6 to EKS migration guidance, CNI comparison, resource sizing, and production readiness checklists.
- Provides CI/CD standards, incident response guidance, observability checklists, cloud migration risk planning, and ADR templates.

Demonstrates: architecture communication, migration planning, failure-aware design, operational documentation, and the ability to explain complex infrastructure decisions clearly.

Relevant links: [Terraform monolith decomposition](https://github.com/mstrugarevic1/docs/blob/main/terraform-monolith-decomposition.md), [AWS and hybrid disaster recovery](https://github.com/mstrugarevic1/docs/blob/main/disaster-recovery-aws-hybrid.md), [Rancher 1.6 to Amazon EKS migration](https://github.com/mstrugarevic1/docs/blob/main/rancher-1-6-to-aws-eks-migration.md), [production readiness checklist](https://github.com/mstrugarevic1/docs/blob/main/production-readiness-checklist.md)

## Engineering Focus

**Cloud and platform engineering**  
AWS, Kubernetes, ECS, container platforms, networking, IAM, cloud connectivity, and platform foundations.

**Infrastructure as Code**  
Terraform, reusable infrastructure patterns, state isolation, migration planning, dependency management, and controlled change.

**Delivery and automation**  
CI/CD pipelines, GitHub Actions, Jenkins, deployment safety, release workflows, rollback design, and developer enablement.

**Reliability and observability**  
Monitoring, alerting, logs, metrics, health checks, incident response, RTO/RPO, failure analysis, and operational readiness.

**Security and governance**  
Least privilege, read-only auditing, secrets handling, policy controls, security validation, and safe automation.

## How I Approach Engineering

- Prefer safe, read-only, and least-privilege defaults.
- Design rollback and failure behavior before deployment.
- Keep automation understandable enough to operate under pressure.
- Test operational tooling and make outputs predictable.
- Treat documentation, diagrams, and runbooks as part of the system.

## Additional Labs and Examples

- [k8s-examples](https://github.com/mstrugarevic1/k8s-examples) — example: Kubernetes manifests, SLO demos, Gatekeeper policies, and namespace onboarding patterns for test clusters.
- [kind-istio-mtls-lab](https://github.com/mstrugarevic1/kind-istio-mtls-lab) — lab: local kind and Istio mTLS environment with sidecar injection, Kiali, Prometheus, Grafana, fault injection, and circuit breaking.
- [haproxy-canary-lab](https://github.com/mstrugarevic1/haproxy-canary-lab) — lab: HAProxy weighted canary traffic shifting, active health checks, Runtime API changes, and rollback behavior.
- [gemini-cli-wrapper](https://github.com/mstrugarevic1/gemini-cli-wrapper) — tool: shell wrapper pattern for AI CLI pre-flight checks, git context validation, Gitleaks scans, and sandboxed execution.

## Background

My background spans production infrastructure, Linux operations, cloud platforms, automation, troubleshooting, delivery systems, and cross-functional engineering work. I have worked across environments where reliability, change control, incident response, and clear operational ownership matter.

I am interested in Senior DevOps, Platform Engineering, SRE, and Cloud Engineering roles where infrastructure work needs to be reliable, maintainable, secure, and understandable by the teams that operate it.

## Contact

- GitHub: [mstrugarevic1](https://github.com/mstrugarevic1)
- Email: [mstrugarevic1@icloud.com](mailto:mstrugarevic1@icloud.com)

Recommendation letter available on request.
