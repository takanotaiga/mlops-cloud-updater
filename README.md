# mlops-cloud-updater

Release/update helper repository for MLOps Cloud.

This repository currently contains a small compose file for running the backend `system-manager` image. It is separate from the main development compose in `../mlops-cloud`.

## Files

| File | Purpose |
|---|---|
| `docker-compose.yml` | Runs `system-manager` from a published backend image |
| `AGENTS.md` | Agent/developer notes for this repository |

## Security

`system-manager` uses SSH credentials.

```yaml
environment:
  SSH_USERNAME: USER_NAME
  SSH_PASSWORD: PASSWORD
```

Replace placeholders through a secure deployment mechanism. Do not commit real credentials.

## Validation

```bash
docker compose config
```

Use `../mlops-cloud` for local integrated development and E2E testing.
