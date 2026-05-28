# Desenvolvimento

## Execucao local

```bash
python -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

## Testes

```bash
pip install -r requirements-dev.txt
pytest -q
```

## Docker

```bash
docker build -t exchange-service .
docker run --rm -p 8000:8000 exchange-service
```

## Kubernetes

Os manifests ficam em `k8s/`:

- `configmap.yaml`
- `secrets.yaml`
- `deployment.yaml`
- `service.yaml`
