# TC-LOG-006 - Login com senha preenchida com tipo de dado inválido

| Campo                    | Valor                                                                                                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-006                                                                                                                                        |
| **Condição Relacionada** | CND-LOG-002                                                                                                                                       |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                                              |
| **Prioridade**           | Alta                                                                                                                                              |
| **Objetivo**             | Validar que a API não permite o login de um usuário utilizando uma senha com tipo de dado inválido, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                                            |
| **Endpoint**             | `/login`                                                                                                                                          |

---

## Pré-condições

- API deve estar disponível

- Usuário previamente cadastrado

---

## Massa de Teste

```json
{
    "email": "fulano@qa.com",
    "password": 1234
}
```

--- 

## Passos

1. Enviar uma requisição `POST`para o endpoint `/login`,

2. Preencher o campo `email`,

3. Preencher o campo `password` com tipo de dado que não seja `string`,

4. Executar a requisição.

---

## Resultados Esperados

- Status Code `400`

- A resposta deve ter como mensagem `"Email e/ou senha inválidos"` ou um aviso similar
