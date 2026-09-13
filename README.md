# open-webui

Add open-webui helm repo:
```bash
helm repo add open-webui https://helm.openwebui.com/
```

Install open-webui:
```bash
helm upgrade -i open-webui open-webui/open-webui \
  --namespace open-webui \
  --create-namespace \
  --set persistence.storageClass=ceph-block \
  --set pipelines.persistence.storageClass=ceph-block \
  --set ollama.persistentVolume.storageClass=ceph-block
```

http://localhost:8080

Access the Web UI:
```bash
kubectl -n open-webui port-forward svc/open-webui 8080:80
```

