# TC-USU-008 - Retornar um usuário específico

| Item                     | Valor                                                        |
| ------------------------ | ------------------------------------------------------------ |
| **ID**                   | TC-USU-008                                                   |
| **Condição Relacionada** | CND-USU-013                                                  |
| **Prioridade**           | Alta                                                         |
| **Tipo de Teste**        | Funcional - Positivo                                         |
| **Objetivo**             | Validar que a API retorne um usuário pelo seu identificador. |
| **Método HTTP**          | `GET`                                                        |
| **Endpoint**             | `/usuarios/{_id}`                                            |

---

## Pré-condições

- API disponível

- No mínimo, um usuário registrado previamente

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/usuarios/{id}`,

2. Informar o identificador `id` do usuário no parâmetro de caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- Retorno exibindo o usuário procurado pelo seu respectivo `_id`
