# TC-USU-002 - Cadastro de usuário com email duplicado

| Item                     | Valor                                                                                             |
| ------------------------ | ------------------------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-002                                                                                        |
| **Condição Relacionada** | CND-USU-007                                                                                       |
| **Prioridade**           | Alta                                                                                              |
| **Tipo de Teste**        | Funcional - Negativo                                                                              |
| **Objetivo**             | Validar que a API não permita que um usuário realize cadastro utilizando um e-mail já cadastrado. |
| **Método HTTP**          | `POST`                                                                                            |
| **Endpoint**             | `/usuarios`                                                                                       |

---

## Pré-condições

- API disponível

- Endereço de e-mail cadastrado previamente

---

## Massa de Teste

```json
{
  "nome": "João da Silva",
  "email": "beltrano@qa.com.br",
  "password": "senhadois",
  "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/usuarios`,

2. Preencher o campo `nome`,

3. Preencher o campo `email` com um endereço de e-mail já cadastrado,

4. Preencher o campo `password`

5. Preencher o campo `administrador` como `true` ou `false`,

6. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `Este email já está sendo utilizado` ou um aviso similar
