# AWS EC2 Monitoring with Prometheus, Grafana & Alertmanager

aws-ec2-monitoring-prometheus-grafana-alertmanager/
│
├── README.md
├── screenshots/
│   ├── prometheus-targets.png
│   ├── prometheus-alerts.png
│   ├── grafana-dashboard.png
│   └── alertmanager-ui.png
│
├── prometheus/
│   ├── prometheus.yml
│   └── alerts.yml
│
├── alertmanager/
│   └── alertmanager.yml
│
├── systemd/
│   ├── prometheus.service
│   ├── node_exporter.service
│   └── alertmanager.service
│
└── docs/
    ├── installation-guide.md
    └── architecture.md

## Project Overview

Implemented a complete monitoring and alerting solution on AWS EC2 using Prometheus, Node Exporter, Grafana, and Alertmanager.

The solution provides:

- Real-time CPU monitoring
- Memory utilization tracking
- Disk usage monitoring
- Grafana dashboards and visualization
- Email alert notifications
- Infrastructure observability

---

## Architecture

AWS EC2 Instance
|
├── Node Exporter (9100)
|
├── Prometheus (9090)
|
├── Alertmanager (9093)
|
└── Grafana (3000)

---

## Technologies Used

- AWS EC2 (Ubuntu)
- Prometheus
- Node Exporter
- Alertmanager
- Grafana
- Linux
- Systemd

---

## Monitoring Metrics

### CPU Usage

- Tracks CPU utilization
- Alerts when usage exceeds threshold

### Memory Usage

- Monitors RAM consumption
- Generates alerts on high utilization

### Disk Usage

- Tracks filesystem consumption
- Sends alerts on low available space

---

## Alerting

Email notifications configured using Alertmanager and Gmail SMTP.

Alert Types:

- High CPU Usage
- High Memory Usage
- High Disk Usage

---

## Screenshots

### Prometheus Targets

![Prometheus Targets](screenshots/prometheus-targets.png)

### Prometheus Alerts

![Prometheus Alerts](screenshots/prometheus-alerts.png)

### Grafana Dashboard

![Grafana Dashboard](screenshots/grafana-dashboard.png)

### Alertmanager

![Alertmanager](screenshots/alertmanager-ui.png)

---

## Key Learnings

- Prometheus monitoring architecture
- Metrics collection using Node Exporter
- Alert rule creation
- Alertmanager configuration
- Grafana dashboard creation
- AWS Infrastructure Monitoring
