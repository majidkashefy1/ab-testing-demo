# 🧪 A/B Testing Infrastructure Demo

This project demonstrates a **semi-real infrastructure A/B testing setup** using:
- NGINX (load balancing)
- Two versions of a Flask app
- Prometheus (metrics)
- Grafana (monitoring dashboard)

## ⚙️ Architecture

    ┌──────────────┐
    │   NGINX LB   │
    │50% A / 50% B │
    └──────┬───────┘
           │
           |
    ┌──────|───────────────┐
    │ │                    │
    ┌───────┐ ┌────────┐   │
    │ App V1│ │ App V2 │   │
    └───────┘ └────────┘   │
    │                      │
    ┌────────────┐         │
    │ Prometheus │         │
    │ Grafana │  │         │
    └────────────┘         │
    │                      │
    └──────────────────────┘

## 🚀 Run the Project

```bash
git clone https://github.com/majidkashefy1/ab-testing-demo.git
cd ab-testing-demo
docker compose up -d --build

Then visit:

Service	URL
NGINX Load Balancer	http://localhost:8080
Prometheus	http://localhost:9090
Grafana	http://localhost:3000
```
| Component          | Purpose                          |
| ------------------ | -------------------------------- |
| **Flask**          | Lightweight Python web framework |
| **NGINX**          | Load balancer for A/B routing    |
| **Prometheus**     | Metrics collection               |
| **Grafana**        | Visualization dashboards         |
| **Docker Compose** | Multi-service orchestration      |



---
