# TC-PRO-019 - Atualizar produto com o campo de quantidade com valor negativo

| Item                     | Valor                                                                                                  |
| ------------------------ | ------------------------------------------------------------------------------------------------------ |
| **ID**                   | TC-PRO-019                                                                                             |
| **Condição Relacionada** | CND-PRO-039                                                                                            |
| **Prioridade**           | Alta                                                                                                   |
| **Tipo de Teste**        | Funcional - Negativo                                                                                   |
| **Objetivo**             | Validar que a API não permita a atualização de um produto com o campo `quantidade` com valor negativo. |
| **Método HTTP**          | `PUT`                                                                                                  |
| **Endpoint**             | `/produtos/{_id}`                                                                                      |

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
  "nome": "Motorola g30",
  "preco": 199,
  "descricao": "Smartphone",
  "quantidade": -284
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Preencher o campo `quantidade` com um valor negativo,

3. Preencher os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `quantidade deve ser maior ou igual a 0`
