# API de Temperatura e Umidade

API REST em Node.js/Express para armazenar leituras de temperatura e umidade. Os dados ficam em memória (são perdidos ao reiniciar o servidor).

## Como rodar

```bash
npm install express cors
node index.js
```

Servidor sobe em `http://localhost:3000`.

## Endpoints

Rota base: `/api/dados`

| Método | Rota | Descrição |
|---|---|---|
| GET | `/api/dados` | Lista todas as leituras |
| GET | `/api/dados/:id` | Busca uma leitura pelo id |
| POST | `/api/dados` | Cria uma nova leitura |
| PUT | `/api/dados/:id` | Atualiza uma leitura |
| DELETE | `/api/dados/:id` | Remove uma leitura |

## Formato dos dados

```json
{
  "id": 1,
  "temperatura": 25,
  "umidade": 50,
  "hora": "11:00"
}
```

No POST e PUT, envie `temperatura`, `umidade` e `hora` no body. O `id` é gerado automaticamente.

## Tecnologias

- Node.js
- Express
- CORS
