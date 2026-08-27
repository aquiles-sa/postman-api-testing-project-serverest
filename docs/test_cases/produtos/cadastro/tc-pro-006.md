# TC-PRO-006 - Cadastro de produto com o campo de quantidade sem valor

| Item                     | Valor                                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-006                                                                            |
| **Condição Relacionada** | CND-PRO-028                                                                           |
| **Prioridade**           | Alta                                                                                  |
| **Tipo de Teste**        | Funcional - Negativo                                                                  |
| **Objetivo**             | Validar que a API não permita cadastro de um produto com o campo `descricao` ausente. |
| **Método HTTP**          | `POST`                                                                                |
| **Endpoint**             | `/produtos`                                                                           |

---

## Pré-condições

- API disponível

- Usuário autenticado com token de acesso válido

- Usuário com permissão para cadastrar produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "Xbox One",
  "preco": 2000,
  "descricao": "Console de Jogos",
  "quantidade": ""
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/produtos`,

2. Não preencher o campo `quantidade`,

3. Preencher todos os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `quantidade deve ser um número`
