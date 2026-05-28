# Atividades Realizadas

## Microservico individual: Exchange API

O microservico individual implementado por Raphael foi o `exchange-service`.

Entregas principais:

- endpoint `GET /exchanges/{from_currency}/{to_currency}`;
- validacao do header `id-account`;
- normalizacao de codigos de moeda;
- integracao com a AwesomeAPI;
- resposta com `sell`, `buy`, `date` e `id-account`;
- endpoint `GET /metrics` para Prometheus;
- testes automatizados para sucesso, erro de autenticacao, moeda invalida, falha do provedor externo e metricas.

Codigo fonte nesta entrega:

- `app/main.py`
- `app/services/exchange_service.py`
- `app/clients/awesome_api_client.py`
- `app/models.py`
- `app/exceptions.py`
- `tests/test_exchange_api.py`

## Atividades do projeto em grupo

O projeto em grupo consolidou os seguintes servicos:

- `account-service`
- `auth-service`
- `gateway-service`
- `product-service`
- `order-service`
- `exchange-service`

As atividades de Jenkins, MiniKube, Kubernetes, EKS, teste de carga, custos e PaaS estao documentadas no repositorio de grupo:

- <https://github.com/insper-aulas/micro_api_26.1>
- <https://insper-aulas.github.io/micro_api_26.1/>
