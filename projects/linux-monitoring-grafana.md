# 📊 Linux Server Monitoring with Prometheus & Grafana

## 📌 Summary

Deployed a full monitoring stack using **Prometheus**, **Node Exporter**, and **Grafana** to track performance metrics of critical Linux servers. This improved visibility, alerting, and system reliability for operations and engineering teams.

---

## 🔧 Tools & Technologies

- Grafana (Dashboarding & Alerting)
- Prometheus (Time-series DB)
- Node Exporter (Linux metrics)
- Linux (RHEL, Ubuntu)
- Systemd services
- Custom Alerts via Email / Telegram

---

## 🔍 What I Did

- Installed **Prometheus** and **Node Exporter** on multiple VMs
- Created custom **prometheus.yml** to scrape from all hosts
- Integrated with **Grafana** and built dashboards:
  - CPU, RAM, Disk, Load Average
  - Network I/O and uptime
- Configured **Grafana Alerts** for:
  - High CPU usage
  - Low disk space
  - Service down (systemd)
- Integrated Telegram bot & email alerts

---

## 🖼️ Dashboard Examples

> *(Bisa ditambahkan screenshot dashboard atau konfigurasi alert nanti)*

- 🧠 CPU + Memory Heatmap
- 💽 Disk Usage per Mount Point
- 📈 Load Trends per Host
- 🔔 Real-time Alerts on incidents

---

## 🤔 Challenges Faced

| Problem | Solution |
|--------|----------|
| Node Exporter not running after reboot | Created persistent systemd unit |
| Too many false alerts | Added alert thresholds + silence during backup windows |
| Prometheus retention issue | Mounted external volume for TSDB data |

---

## 📈 Outcome

- Reduced MTTR for system issues by ~30%
- Provided historical trends to assist in capacity planning
- Helped infra team catch issues before end users did

---

## 🧪 Future Improvements

- Add exporters for MySQL, NGINX, and PostgreSQL
- Setup Loki for log aggregation
- Explore integration with PagerDuty / Opsgenie
