# Entrega Individual - Raphael Cimerman Lafer

Repositorio individual da disciplina **Platforms, Microservices, DevOps and APIs**.

Este repositorio contem:

- documentacao MkDocs da entrega individual;
- codigo fonte do microservico individual `exchange-service`;
- testes, `Dockerfile`, `Jenkinsfile` e manifests Kubernetes do `exchange-service`;
- links para o projeto em grupo e para todos os repositorios usados.

## Aluno e grupo

- Aluno: Raphael Cimerman Lafer
- Grupo: Pedro Henrique Vargas Sepulveda e Raphael Cimerman Lafer
- Projeto em grupo: <https://github.com/insper-aulas/micro_api_26.1>
- Documentacao do grupo: <https://insper-aulas.github.io/micro_api_26.1/>

## Como executar o Exchange Service

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

## Documentacao

```bash
pip install -r requirements-docs.txt
mkdocs serve
```
