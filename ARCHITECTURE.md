# Architecture Overview

### Layers
| Layer | Role | Tech |
|------|------|------|
| **Perception Bus** | Event routing | NATS 2.10 or in-process |
| **Evaluator** | Drift detection + tuning | SQLite + batched writes |
| **Human Gate** | Approve/veto changes | `/apply`, `/veto` endpoints |
| **Observability** | Live system health | Prometheus + Textual TUI |

### Audit Chain
Every event → `SHA-256(event_json)` → appended to `audit.log`  
Forensic replay:  
```bash
sqlite3 lattice_eater.db "SELECT * FROM runs LIMIT 10"
```

---

## Demo Flow
1. Sim loop generates blurry data  
2. Evaluator: “Clarity < 40 → suggest lower threshold”  
3. Human sees in TUI → clicks **Approve**  
4. Threshold updates → **logged with actor ID**  
5. Prometheus shows `lattice_conf_threshold` drop

---

**Built for defense. Ready for audit.**
