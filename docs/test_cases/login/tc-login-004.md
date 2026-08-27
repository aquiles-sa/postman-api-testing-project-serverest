# TC-LOG-004 - Login com ambos os campos vazios

| Campo                    | Valor                                                                                                                             |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-LOG-004                                                                                                                        |
| **Condição Relacionada** | CND-LOG-004                                                                                                                       |
| **Tipo de Teste**        | Funcional - Negativo                                                                                                              |
| **Prioridade**           | Alta                                                                                                                              |
| **Objetivo**             | Validar que a API não permite o login de um usuário sem o preenchimento dos campos, retornando uma resposta de erro especificada. |
| **Método HTTP**          | `POST`                                                                                                                            |
| **Endpoint**             | `/login`                                                                                                                          |

---

## Pré-condições

- API disponível.

- Usuário previamente cadastrado ou não.

---

## Massa de teste

```json
{
    "email": "",
    "password": ""
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/login`,

2. Não preencher o campo `email`,

3. Não preencher o campo `password`,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve conter a mensagem `email não pode ficar em branco`

- A resposta deve conter a mensagem `password não pode ficar em branco` 
