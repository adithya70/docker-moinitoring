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

```

2. Directory Structure

```bash
docker-monitoring/
├── docker-compose.yml        # Main Docker Compose file
├── prometheus/
│   └── prometheus.yml        # Prometheus configuration
├── grafana/
│   └── provisioning/         # Grafana provisioning configs
├── loki/
│   └── loki-config.yml       # Loki configuration
├── promtail/
│   └── promtail-config.yml   # Promtail configuration
```
3. Configure Settings
Edit the configuration files as needed:

Prometheus: Adjust scrape intervals in prometheus/prometheus.yml.
Loki: Modify retention policies in loki/loki-config.yml.
Grafana: Change default admin credentials in docker-compose.yml.

4. Start the Monitoring Stack
```bash
docker-compose up -d
```

5. Access the Services
Prometheus: http://localhost:9090
Grafana: http://localhost:3000 (Default: admin/admin)
cAdvisor: http://localhost:8080

#Grafana Dashboards
Pre-Built Dashboards

#Adding Data Sources
Prometheus: Add Prometheus as a data source in Grafana.
Loki: Add Loki as a data source for log aggregation.

Add alerting rules in prometheus.yml.
Modify dashboards in Grafana for tailored metrics.
Backup Prometheus and Loki data regularly.

#Stopping and Cleaning Up
1. Stop the Monitoring Stack
To safely stop the monitoring stack without affecting the Docker containers, networks, or volumes, use the following command:

```bash
docker-compose down
This command will stop all running services and remove the containers but will keep the volumes and networks intact.
```

2. Remove Containers, Networks, and Volumes
If you want to completely remove the containers, networks, and volumes associated with the stack, use the following command:

```bash
docker-compose down --volumes --remove-orphans
--volumes: Removes all Docker volumes created by the stack.
--remove-orphans: Removes any orphaned containers not defined in the docker-compose.yml file.
```

3. Clean Up Docker Networks and Volumes (if needed)
Sometimes, unused networks and volumes persist even after stopping the services. To clean them up manually:

List all networks:
```bash
docker network ls
```
Remove unused networks:
```bash
docker network prune
```

List all volumes:
```bash
docker volume ls
```
Remove unused volumes:
```bash
docker volume prune
```
These commands will ensure that you safely remove any residual Docker components.

