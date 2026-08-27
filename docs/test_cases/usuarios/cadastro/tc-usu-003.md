# TC-USU-003 - Cadastro de usuário com nome em branco

| Item                     | Valor                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------- |
| **ID**                   | TC-USU-003                                                                          |
| **Condição Relacionada** | CND-USU-008                                                                         |
| **Prioridade**           | Média                                                                               |
| **Tipo de Teste**        | Funcional - Negativo                                                                |
| **Objetivo**             | Validar que a API não permita que um usuário realize cadastro com o nome sem valor. |
| **Método HTTP**          | `POST`                                                                              |
| **Endpoint**             | `/usuarios`                                                                         |

---

## Pré-condições

- API disponível

- O e-mail utilizado na requisição não deve estar previamente cadastrado

---

## Massa de Teste

```json
{
  "nome": "",
  "email": "testandoEmail@qa.com.br",
  "password": "senhatres",
  "administrador": "true"
}
```

---

## Passos

1. Enviar uma requisição HTTP `POST`para o endpoint `/usuarios`,

2. Não preencher o campo `nome`,

3. Preencher todos os campos restantes,

4. Executar a requisição.

---

## Resultado Esperado

- Status Code `400`

- A resposta deve ter como mensagem `nome não pode ficar em branco`
