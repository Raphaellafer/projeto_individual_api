# Bottlenecks

## Bottleneck 1: dependencia do provedor externo

O `exchange-service` depende da AwesomeAPI para obter cotacoes. Se o provedor externo ficar lento ou indisponivel, a conversao de moeda do `order-service` e afetada.

Tratamentos implementados:

- timeout curto na chamada HTTP para falhar rapido;
- traducao de erros de rede para resposta `502`;
- traducao de pares de moeda inexistentes para resposta `422`;
- testes cobrindo falha do provedor e moeda rejeitada.

Arquivos:

- `app/clients/awesome_api_client.py`
- `app/exceptions.py`
- `tests/test_exchange_api.py`

## Bottleneck 2: falta de visibilidade operacional

Sem metricas, uma lentidao ou aumento de erro no servico de cambio seria dificil de diagnosticar durante teste de carga ou execucao em Kubernetes.

Tratamentos implementados:

- endpoint `GET /metrics` com `prometheus-fastapi-instrumentator`;
- instrumentacao automatica das rotas FastAPI;
- teste automatizado garantindo que o endpoint de metricas esta exposto;
- manifests Kubernetes com probes para acompanhar saude do servico.

Arquivos:

- `app/main.py`
- `tests/test_exchange_api.py`
- `k8s/deployment.yaml`

## Bottlenecks do projeto em grupo

O projeto em grupo tambem documenta:

- cache Redis no `product-service`;
- observabilidade com Prometheus e Grafana para a stack completa.

Referencia: <https://insper-aulas.github.io/micro_api_26.1/exercicios/bottlenecks/>
