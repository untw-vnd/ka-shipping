---
title: Database troubleshooting
description: Troubleshooting database issues
---

## PGAdmin

### Add PGAdmin to your `compose.yaml` file

Add the following service to your `compose.yaml` file to run PGAdmin:

```yaml
pgadmin:
  image: "dpage/pgadmin4:8"
  restart: "unless-stopped"
  environment:
    - PGADMIN_DEFAULT_EMAIL=kerp@knights-apparel.com
    - PGADMIN_DEFAULT_PASSWORD=SuperSecret
    - PGADMIN_DISABLE_POSTFIX=true
  depends_on:
    postgres:
      condition: service_healthy
  labels:
    - "traefik.http.routers.pgadmin.rule=Host(`pgadmin.docker.localhost`)"
```

### Run PGAdmin

Run the following command to start PGAdmin:

```powershell
docker compose up --detach pgadmin
```

### Access PGAdmin

Open a web browser and go to `http://pgadmin.docker.localhost`.
