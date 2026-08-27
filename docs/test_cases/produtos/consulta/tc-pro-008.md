# TC-PRO-008 - Listar todos os produtos cadastrados

| Item                     | Valor                                                    |
| ------------------------ | -------------------------------------------------------- |
| **ID**                   | TC-PRO-008                                               |
| **Condição Relacionada** | CND-PRO-030                                              |
| **Prioridade**           | Alta                                                     |
| **Tipo de Teste**        | Funcional - Positivo                                     |
| **Objetivo**             | Validar que a API retorne todos os produtos cadastrados. |
| **Método HTTP**          | `GET`                                                    |
| **Endpoint**             | `/produtos`                                              |

---

## Pré-condições

- API disponível

- No mínimo, um produto deve ter sido cadastrado

---

## Passos

1. Enviar uma requisição HTTP `GET` para o endpoint `/produtos`,

2. Executar a requisição.

---

## Resultado Esperado

- Status Code `200`

- Quantidade de produtos registrados exibida

- Lista de produtos cadastrados em exibição
