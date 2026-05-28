# API

Base local: `http://localhost:8000`.

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/` | Health check do servico |
| `GET` | `/exchanges/{from}/{to}` | Consulta cotacao |
| `GET` | `/metrics` | Metricas Prometheus |

## Exemplo

```http
GET /exchanges/USD/BRL
id-account: 70
```

```json
{
  "sell": 5.74,
  "buy": 5.73,
  "date": "2026-05-20 09:00:00",
  "id-account": "70"
}
```

## Erros

| Status | Cenario |
| --- | --- |
| `401` | Header `id-account` ausente ou vazio |
| `422` | Codigo de moeda invalido ou par rejeitado pelo provedor |
| `502` | Falha ou resposta inesperada da AwesomeAPI |
