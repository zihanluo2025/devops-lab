# DevOps Lab

A practical DevOps portfolio project demonstrating containerisation, CI/CD,
Kubernetes, Infrastructure as Code, monitoring, and load testing.

## What this repository demonstrates

- Docker / Docker Compose
- GitHub Actions CI
- Kubernetes Deployment and Service
- Terraform for AWS
- Prometheus monitoring
- K6 load testing
- Automated daily health checks

> `reports/latest.md` is generated automatically by GitHub Actions.
> Automated reports are intentionally labelled and are not presented as manual coding work.

## Architecture

```text
devops-lab/
├── app/
├── docker/
├── kubernetes/
├── terraform/
├── monitoring/
├── k6/
├── scripts/
├── reports/
└── .github/workflows/
```

## Run locally

```bash
docker compose up --build
```

Open:

```text
http://localhost:8080
```

## Run load test

Install k6, then:

```bash
k6 run k6/smoke-test.js
```

## CI/CD

The CI workflow:

1. validates Python syntax
2. builds the Docker image
3. validates Kubernetes YAML
4. validates Terraform formatting
5. runs a simple container health check

A scheduled workflow also runs once per day and records an automated repository
health report when the generated content changes.

## Portfolio roadmap

- [x] Dockerised sample service
- [x] GitHub Actions CI
- [x] Kubernetes manifests
- [x] Terraform starter
- [x] Prometheus configuration
- [x] K6 smoke test
- [ ] Add AWS ECR deployment
- [ ] Add EKS deployment
- [ ] Add Grafana dashboard
- [ ] Add Alertmanager
- [ ] Add Trivy image scanning
- [ ] Add Terraform remote state
