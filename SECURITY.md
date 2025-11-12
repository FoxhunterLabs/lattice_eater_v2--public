# Security & Responsible AI Policy

**Last updated:** November 2025

## Disclosure
If you find a vulnerability or misbehavior:
- Email **security@foxhunterlabs.com**
- Do not open a public issue before confirming a fix window

We commit to responding within **72 hours** and resolving confirmed issues within **30 days**.

## Scope
Applies to:
- Lattice Eater runtime (FastAPI app, Evaluator, SQLite logging)
- CLI tools and simulation loops
- Any API endpoints (`/apply`, `/veto`, `/metrics`)

## Responsible AI Statement
Lattice Eater is designed for *human-gated autonomy*.  
- All tuning or decision automation must be explainable and reversible.  
- No deployment should operate without human confirmation of threshold changes.  
- Audit logs (SQLite + SHA-256) must remain intact in all environments.

## Ethics & Use
This software is not intended for:
- Lethal autonomous weapon systems (LAWS)
- Unsupervised kinetic control
- Covert or untraceable AI systems

Foxhunter Labs supports **defensive**, **transparent**, and **human-aligned** autonomy development only.
