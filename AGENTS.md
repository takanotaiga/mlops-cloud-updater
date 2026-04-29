# AGENTS.md

This repository contains release/update helper configuration for MLOps Cloud.

## Current contents

- `docker-compose.yml`: runs `system-manager` from a published backend image.
- `README.md`: minimal repository description.

## Important notes

- This repo is not the main application compose. Use `../mlops-cloud` for development and E2E.
- `system-manager` uses SSH credentials. Treat `SSH_USERNAME` and `SSH_PASSWORD` as secrets.
- Do not commit real host credentials.
- Image tags should be intentional release tags or SHAs. Avoid silently changing them to `latest`.
- If changing update behavior, also update workspace-level docs in `../README.md` / `../ARCHITECTURE.md`.

## Validation

For compose changes:

```bash
docker compose config
```

If the referenced image is accessible and credentials are supplied in a safe local env, run a smoke test manually.
