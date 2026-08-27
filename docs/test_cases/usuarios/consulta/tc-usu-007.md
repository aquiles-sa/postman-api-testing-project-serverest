# TC-USU-007 - Retornar todos os usuários cadastrados

| Item                     | Valor                                                               |
| ------------------------ | ------------------------------------------------------------------- |
| **ID**                   | TC-USU-007                                                          |
| **Condição Relacionada** | CND-USU-012                                                         |
| **Prioridade**           | Alta                                                                |
| **Tipo de Teste**        | Funcional - Positivo                                                |
| **Objetivo**             | Validar que a API retorne todos os usuários cadastrados no sistema. |
| **Método HTTP**          | `GET`                                                               |
| **Endpoint**             | `/usuarios`                                                         |

---

## Pré-condições

- API disponível

- No mínimo, um usuário registrado previamente

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/usuarios`,

2. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- Quantidade de usuários cadastrados

- Uma lista que contém todos os usuários cadastrados
