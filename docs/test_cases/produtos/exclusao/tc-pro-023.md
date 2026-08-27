# TC-PRO-023 - Exluir um produto por identificador inválido

| Item                     | Valor                                                                        |
| ------------------------ | ---------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-023                                                                   |
| **Condição Relacionada** | CND-PRO-043                                                                  |
| **Prioridade**           | Alta                                                                         |
| **Tipo de Teste**        | Funcional - Negativo                                                         |
| **Objetivo**             | Validar que a API não exclua um produto por um identificador `_id` inválido. |
| **Método HTTP**          | `DELETE`                                                                     |
| **Endpoint**             | `/produtos/{_id}`                                                            |

---

## Pré-condições

- API disponível

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Passos

1. Enviar uma requisição HTTP `DELETE` para o endpoint `/produtos/{_id}`,

2. Informar um identificador `_id` inválido como parâmetro do caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `id deve ter exatamente 16 caracteres alfanuméricos`
