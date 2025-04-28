# Spring Boot Desafio Itau

Este projeto é uma aplicação desenvolvida com **Spring Boot** que implementa uma API REST para gerenciar transações financeiras e fornecer estatísticas baseadas nas transações realizadas nos últimos 60 segundos. A aplicação foi construída com foco em simplicidade, desempenho e boas práticas de desenvolvimento.

## Tecnologias e Extensões Utilizadas

- **Spring Boot**: Framework principal para desenvolvimento da aplicação.
  - **Spring Boot Starter Web**: Para criação de APIs REST.
  - **Spring Boot Starter Validation**: Para validação de dados de entrada.
  - **Spring Boot Actuator**: Para monitoramento e métricas da aplicação.
  - **Spring Boot DevTools**: Para facilitar o desenvolvimento com recarregamento automático.

- **Jakarta Validation**: Para validação de objetos de entrada, como `@NotNull`.

- **Java 17**: Linguagem de programação utilizada, conforme especificado no `pom.xml`.

- **Maven**: Gerenciador de dependências e build.

  ## Estrutura do Projeto

A estrutura do projeto segue o padrão recomendado pelo Spring Boot, com separação clara entre as camadas de controle, serviço e modelo. Abaixo estão os principais diretórios e arquivos:

- **`src/main/java`**: Contém o código-fonte principal da aplicação.
  - **`controller`**: Contém os controladores REST, como `TransactionController` e `StatisticsController`.
  - **`service`**: Contém a lógica de negócios, como a classe `TransactionService`.
  - **`models`**: Contém as classes de modelo, como `Transaction`.
  - **`dto`**: Contém os objetos de transferência de dados, como `TransactionRequest` e `StatisticsResponse`.

- **`src/main/resources`**: Contém os arquivos de configuração, como `application.properties`.

- **`src/test/java`**: Contém os testes unitários e de integração.

## Funcionalidades

### Transações
- **Endpoint `/transacao`**:
  - **POST**: Permite criar uma nova transação. Valida se o valor é positivo e se a data/hora não está no futuro.
  - **DELETE**: Remove todas as transações registradas.

### Estatísticas
- **Endpoint `/estatistica`**:
  - **GET**: Retorna estatísticas das transações realizadas nos últimos 60 segundos, incluindo soma, média, valor máximo, valor mínimo e contagem.

## OBS.
- A aplicação estará disponível em localhost:8080/estatistica e localhost:8080/transacao

## Melhorias Futuras
- Implementar persistência de dados com um banco de dados relacional ou não relacional.
- Adicionar autenticação e autorização para os endpoints.
- Melhorar a cobertura de testes com testes de integração e de carga.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).
```

