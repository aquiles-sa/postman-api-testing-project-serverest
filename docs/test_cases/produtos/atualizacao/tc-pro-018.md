# TC-PRO-018 - Atualizar produto com o campo de quantidade sem valor

| Item                     | Valor                                                                                         |
| ------------------------ | --------------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-018                                                                                    |
| **Condição Relacionada** | CND-PRO-039                                                                                   |
| **Prioridade**           | Alta                                                                                          |
| **Tipo de Teste**        | Funcional - Negativo                                                                          |
| **Objetivo**             | Validar que a API não permita a atualização de um produto com o campo `quantidade` sem valor. |
| **Método HTTP**          | `PUT`                                                                                         |
| **Endpoint**             | `/produtos/{_id}`                                                                             |

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
  "descricao": "Smartphone",
  "quantidade": ""
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Não preencher o campo `quantidade`,

3. Preencher os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `quantidade deve ser um número`
