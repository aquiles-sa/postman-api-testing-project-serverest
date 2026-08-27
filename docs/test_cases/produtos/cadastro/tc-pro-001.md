# TC-PRO-001 - Cadastro válido de um produto

| Item                     | Valor                                                                      |
| ------------------------ | -------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-001                                                                 |
| **Condição Relacionada** | CND-PRO-024                                                                |
| **Prioridade**           | Alta                                                                       |
| **Tipo de Teste**        | Funcional - Positivo                                                       |
| **Objetivo**             | Validar que a API permita cadastro de um produto utilizando dados válidos. |
| **Método HTTP**          | `POST`                                                                     |
| **Endpoint**             | `/produtos`                                                                |

---

## Pré-condições

- API disponível

- O produto não pode ter sido registrado anteriormente

- Usuário autenticado com token de acesso válido

- Usuário com permissão para cadastrar produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "Lenovo New Vision",
  "preco": 330,
  "descricao": "Notebook",
  "quantidade": 297
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/produtos`,

2. Preencher o campo `nome`,

3. Preencher o campo `preco`,

4. Preencher o campo `descricao`,

5. Preencher o campo `quantidade`,

6. Executar a requisição.

---

## Resultado Esperado

- Status Code `201`

- A resposta deve ter como mensagem `Cadastro realizado com sucesso`

- Um identificador `_id` deve ser gerado automaticamente para o produto cadastrado
