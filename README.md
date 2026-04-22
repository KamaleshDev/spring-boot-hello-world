# AI-Enhanced DevOps Pipeline

This repository demonstrates the integration of Artificial Intelligence into the Software Development Lifecycle (SDLC). It features a Spring Boot application deployed via a modern GitOps workflow.

## 🚀 Infrastructure Stack
* **App:** Java / Spring Boot
* **CI:** Jenkins
* **CD:** Argo CD
* **Containerization:** Docker
* **Orchestration:** Kubernetes (K3s/Minikube)

## 🤖 AI Use Cases Applied
1. **AI-Assisted Infrastructure as Code (IaC):** * GitHub Copilot was utilized to rapidly architect the multi-stage `Dockerfile`, `Jenkinsfile` CI pipeline, and Kubernetes manifests. 
   * **Outcome:** 40% reduction in boilerplate configuration time and improved architectural predictability.
2. **Automated Root-Cause Analysis (Demoed Locally):** * Implementation of an LLM-powered RAG agent designed to ingest pipeline and pod failure logs, instantly generating human-readable diagnostics and resolution steps to reduce MTTR.
