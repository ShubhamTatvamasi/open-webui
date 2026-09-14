# ollama

Download model:
```bash
kubectl -n open-webui exec deploy/open-webui-ollama -- \
  ollama pull qwen3:0.6b
```

```
ollama pull qwen3.8:latest
ollama pull deepseek-v4.1-flash:cloud 
```

Check the running processes:
```bash
kubectl -n open-webui exec deploy/open-webui-ollama -- \
  ollama ps
```

```
NAME          ID              SIZE      PROCESSOR    CONTEXT    UNTIL
qwen3:0.6b    7df6b6e09427    930 MB    100% GPU     4096       4 minutes from now
```

Stop Process:
```bash
kubectl -n open-webui exec deploy/open-webui-ollama -- \
  ollama stop qwen3:0.6b
```
