# TC-USU-010 - Retornar um usuário por identificador inválido

| Item                     | Valor                                                                   |
| ------------------------ | ----------------------------------------------------------------------- |
| **ID**                   | TC-USU-010                                                              |
| **Condição Relacionada** | CND-USU-015                                                             |
| **Prioridade**           | Alta                                                                    |
| **Tipo de Teste**        | Funcional - Negativo                                                    |
| **Objetivo**             | Validar que a API não retorne um usuário por um identificador inválido. |
| **Método HTTP**          | `GET`                                                                   |
| **Endpoint**             | `/usuarios/{_id}`                                                       |

---

## Pré-condições

- API disponível

- No mínimo, um usuário registrado previamente

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/usuarios/{_id}`,

2. Informar um identificador `_id` inválido no parâmetro de caminho do endpoint.

3. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- Retorno exibindo `id deve ter exatamente 16 caracteres alfanuméricos` como mensagem.
