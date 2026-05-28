# Exchange API

## Objetivo

O `exchange-service` fornece cotacoes de cambio para que o `order-service` possa converter valores de pedidos entre moedas.

## Responsabilidades

- Receber o par de moedas pela rota `GET /exchanges/{from_currency}/{to_currency}`.
- Exigir o contexto de conta pelo header `id-account`.
- Normalizar moedas para o formato de tres letras.
- Consultar a AwesomeAPI.
- Traduzir a resposta externa para o contrato interno do projeto.
- Expor metricas Prometheus em `GET /metrics`.

## Contrato principal

```http
GET /exchanges/USD/BRL
id-account: 0195ae95-5be7-7dd3-b35d-7a7d87c404fb
```

Resposta esperada:

```json
{
  "sell": 5.0038,
  "buy": 5.0008,
  "date": "2026-05-14 12:35:24",
  "id-account": "0195ae95-5be7-7dd3-b35d-7a7d87c404fb"
}
```

## Integracao no projeto

O fluxo principal e:

```text
gateway-service -> order-service -> exchange-service -> AwesomeAPI
```

O `gateway-service` resolve o usuario autenticado e propaga o identificador de conta. O `order-service` usa esse contexto para criar pedidos e chama o `exchange-service` quando precisa de conversao de moeda.
