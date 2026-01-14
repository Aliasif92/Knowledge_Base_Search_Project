# Security Policy

If you discover a security issue, please do not open a public issue first.

## Reporting

- Create a private report by emailing the maintainer listed in `pyproject.toml` (replace with your real address).
- Include steps to reproduce and any proof-of-concept.

## Scope

This project is a local CLI tool. Typical issues could include:
- Unsafe handling of file paths
- Insecure temporary files
- Injection risks in SQLite queries (mitigated by parameterization)
