# TC-LOG-003 - Login com e-mail não cadastrado

| Campo                    | Valor                                                                                                                                  |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-003                                                                                                                             |
| **Condição Relacionada** | CND-LOG-003                                                                                                                            |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                                   |
| **Prioridade**           | Alta                                                                                                                                   |
| **Objetivo**             | Validar que a API não permite o login de um usuário utilizando um e-mail não cadastrado, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                                 |
| **Endpoint**             | `/login`                                                                                                                               |

---

## Pré-condições

- API disponível.

- Usuário não deve ter feito cadastro anteriormente.

---

## Massa de Teste

```json
{
    "email": "emailnaocadastrado@qa.com",
    "password": "teste"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/login`,

2. Informar um e-mail não cadastrado,

3. Informar uma senha válida,

4. Executar a requisição.

---

## Resultado Esperado

1. Status Code `401`

2. A resposta deve ter como mensagem `"Email e/ou senha inválidos"` ou um aviso similar
