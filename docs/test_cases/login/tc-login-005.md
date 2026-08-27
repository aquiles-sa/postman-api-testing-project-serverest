# TC-LOG-005 - Login com senha sem valor

| Campo                    | Valor                                                                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-005                                                                                                                          |
| **Condição Relacionada** | CND-LOG-004                                                                                                                         |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                                |
| **Prioridade**           | Alta                                                                                                                                |
| **Objetivo**             | Validar que a API não permite o login de um usuário com o campo `password` sem valor, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                              |
| **Endpoint**             | `/login`                                                                                                                            |

---

## Pré-condições

1. API disponível.

2. Usuário previamente cadastrado.

---

## Massa de Teste

```json
{
    "email": "fulano@qa.com",
    "password": ""
}
```

---

## Passos

- Enviar uma requisição HTTP `POST` para o endpoint `/login`,

- Preencher o campo `email`,

- Não preencher o campo `password`,

- Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `password não pode ficar em branco`
