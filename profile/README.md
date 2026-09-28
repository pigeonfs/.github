# Pigeon

**Transactional email you run on your own Amazon SES account.**

Product and docs live at **[pigeonfs.com](https://pigeonfs.com)**.

Pigeon is the dashboard, API, and SMTP layer in front of SES. You keep the AWS identity, deliverability, and sending reputation. Teams get domains, API keys, SMTP credentials, templates, metrics, logs, and Stripe billing without handing mail over to a third-party sender.

## What we ship

- **HTTP API** — `POST /api/emails` with a Bearer `pg_` key
- **SMTP** — drop-in host for Rails, Django, WordPress, and anything that already speaks SMTP
- **Dashboard** — domains (DKIM, SPF, DMARC), keys, sends, webhooks, quotas
- **Official clients** — Node, Python, Go, Java, Rust, CLI, Phoenix/Swoosh, MCP, and React Email

## Repositories

| Repo | Role |
| --- | --- |
| [pigeon](https://github.com/pigeonfs/pigeon) | Phoenix app: API, dashboard, SMTP, SES |
| [pigeon-node](https://github.com/pigeonfs/pigeon-node) | Node.js SDK |
| [pigeon-python](https://github.com/pigeonfs/pigeon-python) | Python SDK |
| [pigeon-go](https://github.com/pigeonfs/pigeon-go) | Go SDK |
| [pigeon-java](https://github.com/pigeonfs/pigeon-java) | Java SDK |
| [pigeon-rust](https://github.com/pigeonfs/pigeon-rust) | Rust SDK |
| [pigeon-cli](https://github.com/pigeonfs/pigeon-cli) | Command-line client |
| [pigeon-phoenix](https://github.com/pigeonfs/pigeon-phoenix) | Elixir client and Swoosh adapter |
| [pigeon-mcp](https://github.com/pigeonfs/pigeon-mcp) | MCP server for Cursor and Claude Code |
| [react-email](https://github.com/pigeonfs/react-email) | React components for HTML email |

SDKs install from this org. Each client uses the same HTTP API and `PIGEON_BASE_URL`.

## Start here

1. Open **[pigeonfs.com](https://pigeonfs.com)**
2. Verify a domain, mint an API key or SMTP user
3. Send with curl, SMTP, or an official SDK

```bash
curl -X POST https://pigeonfs.com/api/emails \
  -H "Authorization: Bearer pg_your_key" \
  -H "Content-Type: application/json" \
  -d '{"from":"Ada <ada@yourdomain.com>","to":["person@example.com"],"subject":"Hello","html":"<p>Hello</p>"}'
```

Pigeon is a [bitscorp](https://bitscorp.co) product. The GitHub org is **pigeonfs**.
