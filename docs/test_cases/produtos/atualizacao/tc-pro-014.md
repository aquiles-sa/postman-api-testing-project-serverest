# TC-PRO-014 - Atualizar produto com o campo nome sem valor

| Item                     | Valor                                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-014                                                                            |
| **Condição Relacionada** | CND-PRO-036                                                                           |
| **Prioridade**           | Alta                                                                                  |
| **Tipo de Teste**        | Funcional - Negativo                                                                  |
| **Objetivo**             | Validar que a API não permita a atualização de um produto com o campo `nome` ausente. |
| **Método HTTP**          | `PUT`                                                                                 |
| **Endpoint**             | `/produtos/{_id}`                                                                     |

---

## Pré-condições

- API disponível

- Produto cadastrado previamente

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "",
  "preco": 375,
  "descricao": "Smartphone",
  "quantidade": 284
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Não preencher o campo `nome`,

3. Preencher os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `nome não pode ficar em branco`
