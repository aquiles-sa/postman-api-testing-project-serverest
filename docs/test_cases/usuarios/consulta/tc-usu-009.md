# TC-USU-009 - Retornar um usuário inexistente

| Item                     | Valor                                                                      |
| ------------------------ | -------------------------------------------------------------------------- |
| **ID**                   | TC-USU-009                                                                 |
| **Condição Relacionada** | CND-USU-014                                                                |
| **Prioridade**           | Alta                                                                       |
| **Tipo de Teste**        | Funcional - Negativo                                                       |
| **Objetivo**             | Validar que a API não retorne um usuário por um identificador inexistente. |
| **Método HTTP**          | `GET`                                                                      |
| **Endpoint**             | `/usuarios/{_id}`                                                          |

---

## Pré-condições

- API disponível

- O identificador utilizado na requisição não deve pertencer a nenhum usuário registrado

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/usuarios/{_id}`,

2. Informar um identificador `_id` inexistente no parâmetro de caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `404`

- Retorno exibindo `usuário não encontrado` como mensagem.
