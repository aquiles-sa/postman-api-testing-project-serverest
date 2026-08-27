# TC-USU-018 - Exclusão de um usuário

| Item                     | Valor                                                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-018                                                                                  |
| **Condição Relacionada** | CND-USU-022                                                                                 |
| **Prioridade**           | Alta                                                                                        |
| **Tipo de Teste**        | Funcional - Positivo                                                                        |
| **Objetivo**             | Validar que a API permita a exclusão de um usuário específico pelo seu identificador `_id`. |
| **Método HTTP**          | `DELETE`                                                                                    |
| **Endpoint**             | `/usuarios/{_id}`                                                                           |

---

## Pré-condições

- API disponível

- No mínimo, um usuário cadastrado no sistema.

---

## Passos

1. Enviar uma requisição HTTP `DELETE` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser deletado como parâmetro do caminho do endpoint,

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- A resposta deve ter como mensagem `Registro excluído com sucesso`
