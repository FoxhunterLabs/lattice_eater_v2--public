# Lattice Eater v2
**Human-Gated Autonomy Runtime**

> **"Autonomy that explains every decision — and asks permission."**

Built in **one day**. Runs **offline**. Logs **everything**.

---

## 🧠 What It Is
A **local-first**, **auditable**, **self-tuning** autonomy engine.

- ⚡ **20 Hz simulation loop** — synthetic detections + alerts
- 🧩 **Adaptive thresholds** — clarity + alert-rate feedback loop
- 🪪 **Every change logged** — tamper-resistant SQLite ledger
- ✋ **Human approval/veto** — via `/apply`, `/veto` API endpoints
- 📊 **Real-time metrics** — Prometheus `/metrics`
- 🖥️ **Terminal cockpit** — Textual TUI dashboard

> **No cloud. No black boxes. No trust required.**

---

## ⚙️ Core Principles
| Principle | Implementation |
|------------|----------------|
| **Human in the Loop** | All tuning suggestions require explicit approval |
| **Auditability** | Every tick, flush, and decision → SHA-256 ledger |
| **Observability** | `/metrics` + TUI = real-time insight |
| **Edge Ready** | Runs on a Raspberry Pi in a bunker |

---

## 🚀 Status
**Private Prototype:** v2  
**Public Spec:** This repo  

**Next Steps**
- ROS 2 integration → real drone loop-back  
- SBIR Phase I ($250 K target)  
- Multi-agent reasoning + graph context

---

## 🧩 Architecture Overview
| Layer | Role | Tech |
|--------|------|------|
| **Perception Bus** | Event routing | NATS 2.10 / AsyncIO In-Process Bus |
| **Evaluator** | Drift detection + auto-tuning | SQLite (WAL mode, batched writes) |
| **Human Gate** | Approve / veto changes | FastAPI endpoints (`/apply`, `/veto`) |
| **Observability** | Live system health | Prometheus + Textual TUI |

---

### 🔐 Audit Chain
Each event → `SHA256(event_json)` → `audit.log`  
Replay any session:  
```bash
sqlite3 lattice_eater.db "SELECT * FROM runs LIMIT 10;"
```

---

## 🎮 Demo Flow
1. Simulation produces low-clarity frames  
2. Evaluator suggests: “Clarity < 40 → lower threshold”  
3. Human reviews in TUI → clicks **Approve**  
4. Threshold updates → recorded with actor ID  
5. Prometheus shows `lattice_conf_threshold` drop

> **Built for defense. Ready for audit.**

---

## 👤 Contact
**Joseph Wells**  
Founder · Foxhunter Labs  
📧 [joseph@foxhunterlabs.com](mailto:joseph@foxhunterlabs.com)  
🔗 [LinkedIn](https://linkedin.com/in/josephwells) | [GitHub](https://github.com/FoxhunterLabs)

---

**MIT License · © Foxhunter Labs**
