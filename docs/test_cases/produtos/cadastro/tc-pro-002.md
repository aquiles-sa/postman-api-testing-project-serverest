# TC-PRO-002 - Cadastro de produto com o campo nome sem valor

| Item                     | Valor                                                                            |
| ------------------------ | -------------------------------------------------------------------------------- |
| **ID**                   | TC-PRO-002                                                                       |
| **Condição Relacionada** | CND-PRO-025                                                                      |
| **Prioridade**           | Alta                                                                             |
| **Tipo de Teste**        | Funcional - Negativo                                                             |
| **Objetivo**             | Validar que a API não permita cadastro de um produto com o campo `nome` ausente. |
| **Método HTTP**          | `POST`                                                                           |
| **Endpoint**             | `/produtos`                                                                      |

---

## Pré-condições

- API disponível

- Usuário autenticado com token de acesso válido

- Usuário com permissão para cadastrar produtos (administrador)

---

## Massa de Teste

```json
{
  "nome": "",
  "preco": 70,
  "descricao": "Teclado",
  "quantidade": 131
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/produtos`,

2. Não preencher o campo `nome`,

3. Preencher todos os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `nome não pode ficar em branco`
