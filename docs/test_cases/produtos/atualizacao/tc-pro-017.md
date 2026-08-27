# TC-PRO-017 - Atualizar produto com o campo de descrição em branco

| Item                     | Valor                                                                                        |
| ------------------------ | -------------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-017                                                                                   |
| **Condição Relacionada** | CND-PRO-038                                                                                  |
| **Prioridade**           | Alta                                                                                         |
| **Tipo de Teste**        | Funcional - Negativo                                                                         |
| **Objetivo**             | Validar que a API não permita a atualização de um produto com o campo `descricao` sem valor. |
| **Método HTTP**          | `PUT`                                                                                        |
| **Endpoint**             | `/produtos/{_id}`                                                                            |

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
  "preco": 230,
  "descricao": "",
  "quantidade": 284
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Não preencher o campo `descricao`,

3. Preencher os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `descricao não pode ficar em branco`
