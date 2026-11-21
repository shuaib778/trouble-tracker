# 🎫 Trouble Tracker — Unified IT Operations Platform

> 🟢 **Live Production System** | [tt.drikict.net](https://tt.drikict.net) | Drik ICT Ltd.

A production-grade unified platform combining **Helpdesk & SLA Ticket Management** with **Real-Time OLT Fiber Network Diagnostics** — currently used daily by the entire NOC and operations team.

---

## ✨ Core Features

### 🎫 Helpdesk & SLA Management
- **Multi-role access control:** Super Admin → Admin → NOC Agent
- **Real-time complaint log** with SLA countdown timers per ticket
- **SLA breach alerting** — automatic red-flag when ticket exceeds SLA window
- **Priority system:** 🔴 High · 🟡 Medium · 🟢 Low with color-coded dashboard
- **Status workflow:** Pending → In Progress → Resolved
- **Customer downtime tracking** per incident (minutes/hours)
- **Shift handover (Link Shift)** workflow for NOC engineers
- **Device Collect** tracking for field technicians
- **Excel export** for management SLA reporting

### 📡 Integrated OLT Diagnostic Monitor (/olt-monitor)
- Polls **12+ BDCOM EPON/GPON OLTs** in real time via Telnet/SSH
- Automatically classifies inactive ONUs into 3 fault types:
  - 💀 **Dying Gasp** — Power loss at customer premises (122 detected)
  - 🔌 **Wire Down** — Fiber cable cut / optical break (6 detected)
  - ⚡ **No Power/Signal** — ONU removed or port issue (52 detected)
- Shows per-ONU: customer name, address, service package, OLT, PON port, Rx Power, downtime
- Sortable, searchable fault table with Excel download for field teams

---

## 📊 Production Metrics

| Metric | Value |
|---|---|
| Total Incidents Managed | **415+** |
| Resolve Rate | **96.4%** |
| High Priority Tickets | 249 |
| Medium Priority | 102 |
| Low Priority | 64 |
| OLT Sites Monitored | **12** |
| Inactive ONUs Detected | **128+** |
| Fault Identification Time | **< 5 min** (was 30+ min manually) |

---

## 🏗️ System Architecture

```
Browser (Multi-role Frontend)
        ↓
REST API Backend (Python Flask)
        ↓
SQLite Database ←→ Telnet/SSH Engine (Netmiko) → BDCOM OLT Devices
```

**Stack:** HTML · CSS · JavaScript · Python Flask · Netmiko · SQLite · REST API

---

## 💼 Business Impact

- Replaced unstructured WhatsApp/Excel complaint tracking with a fully auditable SLA system
- Reduced fiber fault identification: **30+ min → under 5 min**
- 96.4% SLA resolution rate — above industry standard of 80–90%
- Unified helpdesk + network diagnostics in a single production platform

---

*Developed and maintained by Mohammad Shuaib Hassan — Network Support Engineer, Drik ICT Ltd.*
