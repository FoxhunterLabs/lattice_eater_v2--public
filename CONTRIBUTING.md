# Contributing to Lattice Eater

Thanks for your interest in improving **Lattice Eater v2** — a human-gated autonomy system built for transparency and resilience.

## Guiding Principles
- **Human First**: All automation must remain auditable and overrideable.
- **Transparency**: No silent AI behavior. Every action should be logged, explained, or vetoed.
- **Iterate Fast, Log Everything**: Progress is tracked via SQLite and git, not memory.

## How to Contribute
1. **Fork** the repo
2. **Create** a branch (`feature/new-module` or `fix/clarity-metric`)
3. **Test** your change (`pytest` or `python app.py` for runtime verification)
4. **Submit** a pull request with:
   - What problem it solves
   - How it improves explainability or safety

## Code Style
- Python 3.11+ (PEP8 compliant)
- Avoid dynamic code execution (`eval`, etc.)
- Use async and type hints where possible

## Responsible Innovation
By contributing, you agree to uphold Foxhunter Labs’ mission:  
> “Build autonomy that explains itself — and asks permission before acting.”
