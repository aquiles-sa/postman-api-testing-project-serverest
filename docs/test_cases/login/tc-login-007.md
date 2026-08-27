# TC-LOG-007 - Login com email sem valor

| Campo                    | Valor                                                                                                                            |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-007                                                                                                                       |
| **Condição Relacionada** | CND-LOG-005                                                                                                                      |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                             |
| **Prioridade**           | Alta                                                                                                                             |
| **Objetivo**             | Validar que a API não permite o login de um usuário com o campo `email` sem valor, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                           |
| **Endpoint**             | `/login`                                                                                                                         |

---

## Pré-condições

- API disponível

- Usuário não deve ter feito cadastro anteriormente.

---

## Massa de Teste

```json
{
    "email": "",
    "password": "teste"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/login`,

2. Não preencher o campo `email`,

3. Preencher o campo `password`,

4. Executar a requisição.

---

## Resultados Esperados

- Status Code `400`

- A resposta deve ter como mensagem `"email não pode ficar em branco"` ou um aviso similar
