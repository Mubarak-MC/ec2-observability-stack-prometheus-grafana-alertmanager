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

<img width="1462" height="837" alt="Grafana Dashboard 1" src="https://github.com/user-attachments/assets/0dbf4b70-a961-4a22-bba6-0ca0225b81e0" />


## Alerting

Email notifications configured using Alertmanager and Gmail SMTP.
<img width="1837" height="852" alt="Screenshot 2026-06-12 190321" src="https://github.com/user-attachments/assets/ecd82a5d-3186-4bcb-8135-420edd30ec06" />


Alert Types:

- High CPU Usage
- High Memory Usage
- High Disk Usage

---

## Screenshots

### Prometheus Targets

![Prometheus Targets](screenshots/prometheus-targets.png)
<img width="1891" height="852" alt="Prometheus health" src="https://github.com/user-attachments/assets/384eb66f-88a9-4bea-82bc-193d6d7bce61" />


### Prometheus Alerts

![Prometheus Alerts](screenshots/prometheus-alerts.png)
<img width="1907" height="872" alt="Prometheus CPU usage firing alert" src="https://github.com/user-attachments/assets/93100100-1c13-402e-92bd-700a82553eba" />


### Grafana Dashboard

<img width="1902" height="871" alt="Grafana Dashboard" src="https://github.com/user-attachments/assets/c0f76a81-4f41-435a-a87c-3b6575f94b65" />


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
