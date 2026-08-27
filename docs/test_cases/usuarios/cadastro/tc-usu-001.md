# TC-USU-001 - Cadastro válido de usuário

| Item                     | Valor                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-001                                                                          |
| **Condição Relacionada** | CND-USU-006                                                                         |
| **Prioridade**           | Alta                                                                                |
| **Tipo de Teste**        | Funcional - Positivo                                                                |
| **Objetivo**             | Validar que a API permita que um usuário realize cadastro utilizando dados válidos. |
| **Método HTTP**          | `POST`                                                                              |
| **Endpoint**             | `/usuarios`                                                                         |

---

## Pré-condições

- API disponível

- Endereço de e-mail não cadastrado previamente

---

## Massa de Teste

```json
{
  "nome": "Jonas da Silva",
  "email": "emailTeste@qa.com.br",
  "password": "teste",
  "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST` para o endpoint `/usuarios`,

2. Preencher o campo `nome`,

3. Preencher o campo `email`,

4. Preencher o campo `password`

5. Preencher o campo `administrador` como `true` ou `false`,

6. Executar a requisição.

---

## Resultado Esperado

- Status Code `201`

- A resposta deve conter a mensagem `Cadastro realizado com sucesso`

- Um campo `_id` deve ser gerado
