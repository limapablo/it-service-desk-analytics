# Contributing

This repository is primarily a portfolio and learning project, but suggestions, bug reports and improvements are welcome.

## Development principles

- Keep transformations reproducible.
- Prefer reusable code in `src/` over notebook-only logic.
- Document assumptions behind KPIs and data-quality rules.
- Avoid introducing metrics that cannot be justified from the source data.
- Keep SQL readable and modular.
- Add tests when introducing reusable transformation logic.

## Suggested workflow

1. Open an issue describing the proposed change.
2. Create a focused branch.
3. Keep commits small and descriptive.
4. Update documentation when business logic changes.
5. Open a pull request describing the analytical or technical impact.

## Commit style

Examples:

```text
feat: add ticket aging calculation
fix: handle malformed closing dates
refactor: move cleaning logic into reusable pipeline
docs: document backlog metric definition
test: add validation for duplicate ticket ids
```
