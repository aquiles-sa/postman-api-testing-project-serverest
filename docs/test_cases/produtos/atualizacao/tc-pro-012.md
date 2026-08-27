# TC-PRO-012 - Atualizar produto existente

| Item                     | Valor                                                                              |
| ------------------------ | ---------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-012                                                                         |
| **Condição Relacionada** | CND-PRO-034                                                                        |
| **Prioridade**           | Alta                                                                               |
| **Tipo de Teste**        | Funcional - Positivo                                                               |
| **Objetivo**             | Validar que a API permita a atualização válida e completa de um cadastro existente |
| **Método HTTP**          | `PUT`                                                                              |
| **Endpoint**             | `/produtos/{_id}`                                                                  |

---

## Pré-condições

- API disponível

- Nome já existente do mesmo produto

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

- Status Code `200`

- A resposta deve ter como mensagem `Registro alterado com sucesso`
