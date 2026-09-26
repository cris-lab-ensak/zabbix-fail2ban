# 📊 Infrastructure Monitoring with Zabbix + Fail2Ban

> **CRIS Club** — Academic Year 2025/2026

## 📌 About This Project

This project combines **Zabbix** (infrastructure monitoring) and **Fail2Ban** (automated intrusion prevention) to create a proactive security monitoring system that detects threats and automatically blocks malicious activity.

## 📄 Document

| File | Description |
|------|-------------|
| `projet zabbix+fail2ban[2].pdf` | Full project documentation (French) |

## 🎯 Objectives

- Monitor servers, network devices, and services with Zabbix
- Automatically block brute-force and intrusion attempts using Fail2Ban
- Integrate Fail2Ban alerts into the Zabbix dashboard
- Create custom triggers and notifications for security events

## 🛠️ Technologies & Tools

| Tool | Role |
|------|------|
| **Zabbix** | Infrastructure monitoring — metrics, alerts, dashboards |
| **Fail2Ban** | Log-based intrusion prevention — auto IP banning |
| **Linux (Debian/Ubuntu)** | Host OS for services |
| **SMTP / Telegram Bot** | Alert notifications |
| **iptables / firewalld** | Firewall rules backend for Fail2Ban |

## 🗂️ Architecture

```
[Monitored Hosts / Services]
          ↓
    [Zabbix Agent]
          ↓
   [Zabbix Server] ←→ [Zabbix Web UI / Dashboards]
          ↓
  [Custom Script Bridge]
          ↓
     [Fail2Ban]
          ↓
 [iptables — Block malicious IPs]
```

## 🔔 Alert Flow

1. Fail2Ban detects brute-force attempt in logs
2. Fail2Ban bans the IP via iptables
3. Zabbix receives a custom trigger
4. Admin is notified via email / Telegram

## 🏫 About CRIS Club

**CRIS** (Cybersecurity Research & Innovation Students) is a student-led cybersecurity club focused on hands-on learning, research projects, and real-world security challenges.

📅 Academic Year: **2025/2026**

---

> 📬 For questions or contributions, open an issue or contact the CRIS Club team.
