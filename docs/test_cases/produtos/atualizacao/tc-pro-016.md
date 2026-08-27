# TC-PRO-016 - Atualizar produto com o campo de preço com valor negativo

| Item                     | Valor                                                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-016                                                                                        |
| **Condição Relacionada** | CND-PRO-037                                                                                       |
| **Prioridade**           | Alta                                                                                              |
| **Tipo de Teste**        | Funcional - Negativo                                                                              |
| **Objetivo**             | Validar que a API não permita a atualização de um produto com o campo `preco` com valor negativo. |
| **Método HTTP**          | `PUT`                                                                                             |
| **Endpoint**             | `/produtos/{_id}`                                                                                 |

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
  "nome": "Motorola g56",
  "preco": -99,
  "descricao": "Smartphone",
  "quantidade": 284
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Preencher o campo `preco` com um valor negativo,

3. Preencher os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `preco deve ser um número positivo`
