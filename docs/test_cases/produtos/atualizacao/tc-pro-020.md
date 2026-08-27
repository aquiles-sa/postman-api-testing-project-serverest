# TC-PRO-020 - Atualizar produto já existente

| Item                     | Valor                                                                   |
| ------------------------ | ----------------------------------------------------------------------- |
| **ID**                   | TC-PRO-020                                                              |
| **Condição Relacionada** | CND-PRO-040                                                             |
| **Prioridade**           | Alta                                                                    |
| **Tipo de Teste**        | Funcional - Positivo                                                    |
| **Objetivo**             | Validar que a API não permita a atualização de um cadastro já existente |
| **Método HTTP**          | `PUT`                                                                   |
| **Endpoint**             | `/produtos/{_id}`                                                       |

---

## Pré-condições

- API disponível

- Nome já existente em um produto registrado

- Usuário autenticado com token de acesso válido

- Usuário com permissão para excluir produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "Logitech Vertical",
  "preco": 470,
  "descricao": "Mouse",
  "quantidade": 381
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/produtos/{_id}`,

2. Preencher o campo `nome`,

3. Preencher o campo `preco`,

4. Preencher o campo `descricao`,

5. Preencher o campo `quantidade`,

6. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `nome do produto já existente`
