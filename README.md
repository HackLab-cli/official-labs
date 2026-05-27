# Official Labs

A curated collection of officially maintained cybersecurity labs for the **HackLab CLI**. Each lab is a self-contained vulnerable environment ready to spin up with Docker.

## Available Labs

### Single Image Labs

These labs use a single Docker image — just pull and run.

| Lab | Difficulty | Image | Topics |
|-----|-----------|-------|--------|
| [DVWA](./dvwa/) | Beginner | `vulnerables/web-dvwa:latest` | SQLi, XSS, CSRF, command injection, file upload |
| [WebGoat](./webgoat/) | Beginner | `webgoat/webgoat:latest` | OWASP Top 10, guided lessons, authentication |
| [Mutillidae II](./mutillidae/) | Intermediate | `webpwnized/mutillidae:latest` | 40+ vulns, XXE, LDAP injection, CSRF |
| [WrongSecrets](./wrongsecrets/) | Intermediate | `commjoen/wrongsecrets:latest` | Hardcoded secrets, vault misconfig, cloud creds |
| [VAmPI](./vampi/) | Intermediate | `erev0s/vampi:latest` | REST API security, BOLA, mass assignment, JWT |

### Docker Compose Labs

These labs use `docker-compose.yml` for multi-service setups.

| Lab | Difficulty | Services | Topics |
|-----|-----------|----------|--------|
| [DVNA](./dvna/) | Intermediate | Node.js + MongoDB | NoSQLi, SSRF, prototype pollution, deserialization |
| [XXE Lab](./xxe-lab/) | Intermediate | XML parser app | XXE injection, SSRF, blind XXE, OOB exfiltration |

## Quick Start

```bash
# Single image lab
hacklab add official-labs/dvwa
hacklab start dvwa

# Docker compose lab
hacklab add official-labs/dvna
hacklab start dvna

# List running labs
hacklab list

# Stop a lab
hacklab stop dvwa
```

## Lab Structure

Each lab directory contains:

- `lab.yml` — Lab manifest defining the challenge, objectives, and hints
- `docker-compose.yml` — (compose labs only) Multi-service Docker setup

## Difficulty Levels

- **Beginner** — Foundational vulnerabilities with clear attack surfaces
- **Intermediate** — Complex attack chains requiring multiple techniques
- **Advanced** — Real-world scenarios with hardened targets

## Contributing

To propose a new official lab:

1. Create a directory under `official-labs/`
2. Add a `lab.yml` manifest with at least 3 objectives
3. Include a `docker-compose.yml` if multi-service is needed
4. Submit a pull request with a description of the lab

## License

Part of the [HackLab CLI](https://github.com/HackLab-cli) project.
