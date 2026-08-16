# 🏠 Production-Grade Self-Hosted Homelab

A modular, production-ready infrastructure repository documenting the progressive hardening, security orchestration, and containerized deployment of my personal homeserver.

---

## 🏗️ Architecture & Roadmap

The repository is structured into distinct engineering phases, scaling from baseline core security up to advanced runtime observation and automation:

* **[`phase1/`](./phase1)**: Core Security, Identity Management & Remediation Layer
    * **CrowdSec Security Engine**: Threat intelligence, log parsing, and behavioural analysis.
    * **CrowdSec Firewall Bouncer (`iptables`)**: Active remediation layer automatically dropping malicious IPs.
    * **Docker & System Log Acquisition**: Real-time log ingestion pipeline tailing host authentication (`auth.log`) and container logs.
    * **Authentik IAM**: Zero-trust identity provider ready for forward/proxy authentication middleware.
* **`phase2/`** *(Upcoming)*: Runtime Security & Supply Chain Verification (Falco, Cosign/Syft, OPA)
* **`phase3/`** *(Upcoming)*: Observability, Metrics & Dashboarding (Prometheus, Grafana, Glance)

---

## 🚀 Getting Started

Clone the repository and navigate into the desired phase directory to spin up services using Docker Compose.

\`\`\`bash
git clone https://github.com/Vezzyyy/homelab.git
cd homelab/phase1
\`\`\`

Make sure to copy and configure your environment variables before bringing up the stack:

\`\`\`bash
cp .env.example .env
docker compose up -d
\`\`\`
