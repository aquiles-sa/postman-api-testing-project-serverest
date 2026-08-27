# TC-LOG-002 - Login com senha inválida

| Campo                    | Valor                                                                                                                            |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-002                                                                                                                       |
| **Condição Relacionada** | CND-LOG-002                                                                                                                      |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                             |
| **Prioridade**           | Alta                                                                                                                             |
| **Objetivo**             | Validar que a API não permite o login de um usuário utilizando uma senha inválida, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                           |
| **Endpoint**             | `/login`                                                                                                                         |

---

## Pré-condições

- API disponível.

- Usuário previamente cadastrado.

---

## Massa de Teste

```json
{
  "email": "fulano@qa.com",
  "password": "SenhaErrada123"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/login`,

2. Informar um e-mail válido,

3. Informar uma senha inválida,

4. Executar a requisição.

--- 

## Resultado Esperado

- Status Code `401`

- A resposta deve ter como mensagem `"Email e/ou senha inválidos"` ou um aviso similar
