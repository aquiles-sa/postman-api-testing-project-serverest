# TC-USU-011 - Atualizar usuário existente

| Item                     | Valor                                                                             |
| ------------------------ | --------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-011                                                                        |
| **Condição Relacionada** | CND-USU-016                                                                       |
| **Prioridade**           | Alta                                                                              |
| **Tipo de Teste**        | Funcional - Positivo                                                              |
| **Objetivo**             | Validar que a API permita a atualização válida e completa de um usuário existente |
| **Método HTTP**          | `PUT`                                                                             |
| **Endpoint**             | `/usuarios/{_id}`                                                                 |

---

## Pré-condições

- API disponível

- Usuário cadastrado previamente

---

## Massa de Teste

```json
{
  "nome": "Araujo dos anjos",
  "email": "arauanjo@qa.com.br",
  "password": "teste",
  "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `PUT` para o endpoint `/usuarios/{_id}`,

2. Informar o identificador `_id` do usuário a ser editado como parâmetro do caminho do endpoiint,

3. Atualizar o campo `nome`,

4. Atualizar o campo `preco`,

5. Atualizar o campo `descricao`,

6. Atualizar o campo `quantidade`,

7. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- Retornar a mensagem `Registro alterado com sucesso`
