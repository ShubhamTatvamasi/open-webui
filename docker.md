# Docker

http://localhost:3000

Start Open Web UI localy for getting access to the dashboard:
```bash
docker run -d \
  -p 3000:8080 \
  --add-host=host.docker.internal:host-gateway \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main
```

Cleanup:
```bash
docker volume rm open-webui
```
