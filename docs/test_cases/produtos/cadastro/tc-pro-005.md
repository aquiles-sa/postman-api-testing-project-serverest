# TC-PRO-005 - Cadastro de produto com o campo de descrição sem valor

| Item                     | Valor                                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-005                                                                            |
| **Condição Relacionada** | CND-PRO-027                                                                           |
| **Prioridade**           | Média                                                                                 |
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
  "descricao": "",
  "quantidade": 110
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/produtos`,

2. Não preencher o campo `descricao`,

3. Preencher todos os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `descricao não pode ficar em branco`
