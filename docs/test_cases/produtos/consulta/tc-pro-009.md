# TC-PRO-009 - Buscar um produto específico pelo identificador

| Item                     | Valor                                                              |
| ------------------------ | ------------------------------------------------------------------ |
| **ID**                   | TC-PRO-009                                                         |
| **Condição Relacionada** | CND-PRO-031                                                        |
| **Prioridade**           | Alta                                                               |
| **Tipo de Teste**        | Funcional - Positivo                                               |
| **Objetivo**             | Validar que a API retorne um produto pelo seu identificador `_id`. |
| **Método HTTP**          | `GET`                                                              |
| **Endpoint**             | `/produtos/_id`                                                    |

---

## Pré-condições

- API disponível

- No mínimo, um produto deve ter sido cadastrado

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/produtos/_id`,

2. Informar o identificador `_id` do produto a ser retornado.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- Exibição do produto
