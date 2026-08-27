# TC-PRO-022 - Exclusão de um produto inexistente

| Item                     | Valor                                                                                          |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-022                                                                                     |
| **Condição Relacionada** | CND-PRO-042                                                                                    |
| **Prioridade**           | Alta                                                                                           |
| **Tipo de Teste**        | Funcional - Negativo                                                                           |
| **Objetivo**             | Validar que a API não permita a exclusão de um produto por um identificador `_id` inexistente. |
| **Método HTTP**          | `DELETE`                                                                                       |
| **Endpoint**             | `/produtos/{_id}`                                                                              |

---

## Pré-condições

- API disponível

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Passos

1. Enviar uma requisição HTTP `DELETE` para o endpoint `/produtos/{_id}`,

2. Informar um identificador `_id` inexistente como parâmetro do caminho do endpoint,

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `404`

- A resposta deve ter como mensagem `Nenhum registro excluído`
