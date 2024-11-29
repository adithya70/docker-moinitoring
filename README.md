# Docker Monitoring Stack: Prometheus, Grafana, cAdvisor, and Loki

A complete Docker monitoring solution that provides real-time metrics, resource tracking, and log aggregation using **Prometheus**, **cAdvisor**, **Grafana**, **Loki**, and **Promtail**. This repository is designed for anyone who wants to monitor Docker containers effectively and visualize the data in Grafana.

---

## Features

- **Real-time Docker metrics**: Monitor CPU, memory, disk, and network usage.
- **Log aggregation**: Collect, store, and visualize logs with Loki and Promtail.
- **Host monitoring**: System-level metrics using Node Exporter.
- **Pre-built Grafana dashboards**: Easily import dashboards for quick insights.
- **Customizable**: Modify configurations to suit your requirements.

---

## Prerequisites

- **Docker** and **Docker Compose** installed.
- **Linux/Unix-based host** (recommended).

---

## How to Clone and Use

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/docker-monitoring.git
cd docker-monitoring
