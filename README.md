# open-webui

Add open-webui helm repo:
```bash
helm repo add open-webui https://helm.openwebui.com/
```

Install open-webui:
```bash
helm upgrade -i open-webui open-webui/open-webui \
  --namespace open-webui \
  --create-namespace
```
