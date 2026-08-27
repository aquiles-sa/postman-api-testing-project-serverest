# TC-LOG-001 - Login com credenciais válidas

| Campo                    | Valor                                                                            |
| ------------------------ | -------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-001                                                                       |
| **Condição Relacionada** | CND-LOG-001                                                                      |
| **Tipo de Teste**        | Funcional - Positivo                                                             |
| **Prioridade**           | Alta                                                                             |
| **Objetivo**             | Validar que um usuário consiga realizar login utilizando as credenciais válidas. |
| **Método HTTP**          | `POST`                                                                           |
| **Endpoint**             | `/login`                                                                         |

---

## Pré-condições

- API disponível.

- Usuário previamente cadastrado.

---

## Massa de Teste

```json
{
  "email": "fulano@qa.com",
  "password": "teste"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/login`,

2. Informar um e-mail válido,

3. Informar uma senha válida,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- A resposta deve conter e exibir uma mensagem de sucesso

- Um token `JWT` deve ser retornado no corpo da resposta (Response Body)
