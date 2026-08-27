# TC-PRO-021 - Exclusão de um produto cadastrado

| Item                     | Valor                                                                            |
| ------------------------ | -------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-021                                                                       |
| **Condição Relacionada** | CND-PRO-041                                                                      |
| **Prioridade**           | Alta                                                                             |
| **Tipo de Teste**        | Funcional - Positivo                                                             |
| **Objetivo**             | Validar que a API permita a exclusão de um produto pelo seu identificador `_id`. |
| **Método HTTP**          | `DELETE`                                                                         |
| **Endpoint**             | `/produtos/{_id}`                                                                |

---

## Pré-condições

- API disponível

- Produto a ser deletado estar cadastrado

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Passos

1. Enviar uma requisição HTTP `DELETE` para o endpoint `/produtos/{_id}`,

2. Informar o identificador `_id` do produto a ser deletado como parâmetro do caminho do endpoint,

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- A resposta deve ter como mensagem `Resgistro excluído com sucesso`
