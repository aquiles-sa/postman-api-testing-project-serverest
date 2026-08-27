# TC-PRO-013 - Atualizar produto com identificador inexistente

| Item                     | Valor                                                                                                                                                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-013                                                                                                                                                                                  |
| **Condição Relacionada** | CND-PRO-035                                                                                                                                                                                 |
| **Prioridade**           | Alta                                                                                                                                                                                        |
| **Tipo de Teste**        | Funcional - Positivo                                                                                                                                                                        |
| **Objetivo**             | Validar que a API permita a criação de um produto, caso o identificador `_id` não esteja registrado. Ao atualizar um produto com identificador `_id` inexistente, o mesmo produto é criado. |
| **Método HTTP**          | `PUT`                                                                                                                                                                                       |
| **Endpoint**             | `/produtos/{_id}`                                                                                                                                                                           |

---

## Pré-condições

- API disponível

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "Samsung BEM Aleatório",
  "preco": 375,
  "descricao": "Smartphone",
  "quantidade": 284
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Informar um identificador `_id` inexistente como parâmetro de caminho do endpoint,

3. Preencher todos os campos,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `201`

- A resposta deve ter como mensagem `Cadastro realizado com sucesso`
