<h1 align="center">Hi, I'm Venkata Gopi 👋</h1>
<p align="center"><b>DevOps / Platform Engineer</b> · AWS · Kubernetes · Terraform · GitOps · CI/CD</p>

<p align="center">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white" />
  <img src="https://img.shields.io/badge/Argo%20CD-EF7B4D?style=flat&logo=argo&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white" />
</p>

I build the delivery systems around applications: infrastructure as code, pipelines that test and security-scan before anything ships, GitOps deployments, and monitoring that alerts on real user impact. My projects are small apps on purpose, so the focus stays on the platform, and each one is built, broken on purpose, fixed, and written up.

---

## ⭐ Featured project

### [EKS GitOps Platform with DevSecOps](https://github.com/venkatagopi-perumalla/eks-gitops-platform)

Three microservices on **Amazon EKS**. Infrastructure by **Terraform**, images built and scanned in **GitHub Actions**, deployments by **Argo CD**, secrets from **AWS Secrets Manager** via **EKS Pod Identity**, monitoring with **Prometheus, Grafana and Loki** against a 99.5% **SLO**.

<a href="https://github.com/venkatagopi-perumalla/eks-gitops-platform"><img src="https://raw.githubusercontent.com/venkatagopi-perumalla/eks-gitops-platform/main/docs/architecture.png" width="720" alt="EKS GitOps platform architecture" /></a>

- 🔒 Pipeline **blocked a release over 3 HIGH CVEs** (Trivy) until they were fixed — the scan was not weakened
- 🔁 CI never touches the cluster: it commits the new image tag to Git and Argo CD syncs it; manual `kubectl` changes are **self-healed**
- 📈 Processed **6,200+ orders** under load on EKS
- 🚨 Deliberate bad config → ~25% errors → **SLO fast-burn alert fired** → traced via Grafana, Loki and Argo CD → **rolled back with `git revert` in ~2 minutes** ([incident write-up](https://github.com/venkatagopi-perumalla/eks-gitops-platform/blob/main/docs/rca-001.md))
- 💰 Ran for about **$0.23/hour**, torn down the same day

---

## 🛠️ More projects

| Project | What it shows | Stack |
|---|---|---|
| [**learning-tracker**](https://github.com/venkatagopi-perumalla/learning-tracker) | 3-tier app with a CI pipeline that tests, runs the real stack in Compose, smoke-tests through Nginx and publishes images to GHCR | React 19, FastAPI, PostgreSQL, Docker multi-stage, GitHub Actions |
| [**devops-todo-api**](https://github.com/venkatagopi-perumalla/devops-todo-api) | REST API + web page + database, non-root containers with health checks, integration tests against real Postgres in CI | Flask, Gunicorn, Nginx, PostgreSQL, Docker Compose, GHCR |
| [**Aws-kubernetes-terraform**](https://github.com/venkatagopi-perumalla/Aws-kubernetes-terraform) | VPC, security groups and an EKS cluster as separate Terraform modules | Terraform, AWS VPC, EKS |
| [**Aws-cicd-terraform**](https://github.com/venkatagopi-perumalla/Aws-cicd-terraform) | Terraform plan/apply pipeline on AWS CodePipeline + CodeBuild, with IAM, S3 artifacts and remote state | Terraform, CodePipeline, CodeBuild, IAM |
| [**Shell-Script**](https://github.com/venkatagopi-perumalla/Shell-Script) | One script that creates an S3 bucket, IAM role and Lambda function and wires S3 upload events to Lambda and SNS | Bash, AWS CLI, S3, Lambda (Python), SNS |
| [**jenkins-demo**](https://github.com/venkatagopi-perumalla/jenkins-demo) · [**github-actions-demo**](https://github.com/venkatagopi-perumalla/github-actions-demo) | Webhook-triggered Jenkins pipeline with per-stage Docker agents; matrix CI on two Python versions | Jenkins, GitHub Actions |

---

## 🧰 Toolbox

- **Cloud:** AWS — EKS, EC2, VPC, IAM, ECR, S3, Lambda, Secrets Manager, CodePipeline
- **Containers & orchestration:** Docker, Docker Compose, Kubernetes, Helm, kind
- **IaC:** Terraform (modules, S3 remote state with locking)
- **CI/CD & GitOps:** GitHub Actions, Jenkins, Argo CD
- **Security:** Trivy, Gitleaks, SonarQube, least-privilege IAM, hardened containers
- **Observability:** Prometheus, Grafana, Loki, Grafana Alloy, SLOs and burn-rate alerts
- **Languages:** Python (FastAPI, Flask), Bash, YAML

## 🌱 Up next

Karpenter autoscaling · Argo Rollouts canary deploys · Kyverno policy-as-code · OpenTelemetry tracing

## 📫 Get in touch

Open to DevOps, platform and cloud engineering roles. Have a look at my projects, or open an issue on any repo to start a conversation.
