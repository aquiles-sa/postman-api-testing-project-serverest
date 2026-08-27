# TC-PRO-007 - Cadastro de um produto já registrado

| Item                     | Valor                                                                           |
| ------------------------ | ------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-007                                                                      |
| **Condição Relacionada** | CND-PRO-029                                                                     |
| **Prioridade**           | Alta                                                                            |
| **Tipo de Teste**        | Funcional - Negativo                                                            |
| **Objetivo**             | Validar que a API não permita cadastro de um produto já registrado previamente. |
| **Método HTTP**          | `POST`                                                                          |
| **Endpoint**             | `/produtos`                                                                     |

---

## Pré-condições

- API disponível

- O produto já deve ter sido registrado anteriormente

- Usuário autenticado com token de acesso válido

- Usuário com permissão para cadastrar produtos (administrador)

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/produtos`,

2. Preencher o campo `nome`,

3. Preencher o campo `preco`,

4. Preencher o campo `descricao`,

5. Preencher o campo `quantidade`,

6. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `Já existe um produto com esse nome`
