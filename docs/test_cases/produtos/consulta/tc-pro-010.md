# TC-PRO-010 - Buscar um produto inexistente

| Item                     | Valor                                                                      |
| ------------------------ | -------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-010                                                                 |
| **Condição Relacionada** | CND-PRO-032                                                                |
| **Prioridade**           | Alta                                                                       |
| **Tipo de Teste**        | Funcional - Positivo                                                       |
| **Objetivo**             | Validar que a API não retorne um produto por um identificador inexistente. |
| **Método HTTP**          | `GET`                                                                      |
| **Endpoint**             | `/produtos/_id`                                                            |

---

## Pré-condições

- API disponível

- No mínimo, um produto deve ter sido cadastrado

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/produtos/_id`,

2. Informar um identificador `_id` inexistente como parâmetro do caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `404`

- A resposta deve conter a mensagem `Produto não encontrado`
