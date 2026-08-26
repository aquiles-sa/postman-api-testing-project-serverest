# Plano de Teste

## 1. Informações do Documento

| Item      | Valor          |
| --------- | -------------- |
| Projeto   | ServeRest      |
| Documento | Plano de teste |
| Versão    | 1.0            |
| Autor     | Aquiles Araujo |
| Data      | 30/07/2026     |

---

## 2. Objetivo

Garantir que as funcionalidades da API do ServeRest atendam aos requisitos funcionais especificados, apresentem comportamentos consistentes, retornem respostas corretas para diferentes cenários de utilização e validar status codes, payloads, regras de negócio e mensagens retornadas pela API. 

---

## 3. Escopo dos Testes

### Funcionalidades que serão testadas

#### Usuários

- Autenticação de usuários
- Cadastro de usuários
- Consulta de usuários
- Consulta de usuário pelo identificador
- Edição de usuário específico
- Remoção de usuário específico

---

#### Produtos

- Criação de produtos
- Consulta de produtos
- Consulta de produtos pelo identificador
- Edição de produto específico
- Remoção produto específico 

---

## 4. Estratégia de Teste

Serão executados testes manuais utilizando a ferramenta Postman.

Os testes serão organizados em Collections serão automatizados utilizando Scripts de Test e Collection Runner.

Os resultados serão documentados ao término da execução. 

## 5. Tipos de Teste

- Testes Funcionais
- Testes Positivos
- Testes Negativos
- Testes de Validação de Contrato (Response Body/Payload e Status Code)
- Testes de Regressão

## 6. Ambiente de Teste

| Item                | Valor                  |
| ------------------- | ---------------------- |
| Ambiente            | https://serverest.dev/ |
| Ferramenta          | Postman                |
| Formato             | JSON                   |
| Sistema Operacional | Windows 11             |
| Versionamento       | Git + GitHub           |

---

## 7. Critérios de Entrada

Os testes poderão ser iniciados se todos os critérios de 
entrada forem atendidos:

- API disponível;
- Documentação da API disponível;
- Endpoints publicados. 

## 8. Critérios de Saída

Os testes serão considerados concluídos se os critérios de saída forem correspondidos:

- Todos os casos de teste executados;
- Não existirem impedimentos sobre o uso da API.
- Todos os resultados dos testes foram documentados.

## 9. Ferramentas Utilizadas

- Postman
- Git
- GitHub
- Markdown

## 10. Entregáveis

Artefatos que serão produzidos ao longo da execução dos testes:

- Plano de Teste
- Cenários de Teste
- Casos de Teste
- Bug Report
- Relatório Final
- README do Projeto