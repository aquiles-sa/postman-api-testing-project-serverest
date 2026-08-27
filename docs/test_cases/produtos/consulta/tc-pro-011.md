# TC-PRO-011 - Buscar um produto por identificador inválido

| Item                     | Valor                                                                   |
| ------------------------ | ----------------------------------------------------------------------- |
| **ID**                   | TC-PRO-011                                                              |
| **Condição Relacionada** | CND-PRO-033                                                             |
| **Prioridade**           | Alta                                                                    |
| **Tipo de Teste**        | Funcional - Negativo                                                    |
| **Objetivo**             | Validar que a API não retorne um produto por um identificador inválido. |
| **Método HTTP**          | `GET`                                                                   |
| **Endpoint**             | `/produtos/_id`                                                         |

---

## Pré-condições

- API disponível

- No mínimo, um produto deve ter sido cadastrado

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/produtos/_id`,

2. Informar um identificador `_id` inválido como parâmetro do caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `id deve ter exatamente 16 caracteres alfanuméricos`
