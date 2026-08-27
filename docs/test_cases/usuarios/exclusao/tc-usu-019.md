# TC-USU-019 - Exclusão de um usuário inexistente

| Item                     | Valor                                                                                                     |
| ------------------------ | --------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-019                                                                                                |
| **Condição Relacionada** | CND-USU-023                                                                                               |
| **Prioridade**           | Alta                                                                                                      |
| **Tipo de Teste**        | Funcional - Positivo                                                                                      |
| **Objetivo**             | Validar que a API não permita a exclusão de um usuário específico por um identificador `_id` inexistente. |
| **Método HTTP**          | `DELETE`                                                                                                  |
| **Endpoint**             | `/usuarios/{_id}`                                                                                         |

---

## Pré-condições

- API disponível

- No mínimo, um usuário cadastrado no sistema.

---

## Passos

1. Enviar uma requisição HTTP `DELETE` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` inexistente como parâmetro do caminho do endpoint,

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- A resposta deve ter como mensagem `Nenhum registro excluído`
