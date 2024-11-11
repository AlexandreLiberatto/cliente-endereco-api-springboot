# Desafio de Projeto: API RESTful com Java e Spring Boot

Este repositório contém o projeto desenvolvido como parte do desafio do bootcamp de Java com Spring Boot da Claro, oferecido pela [DIO](https://web.dio.me/). O objetivo deste projeto é consolidar conhecimentos em desenvolvimento de APIs RESTful utilizando Java e Spring Boot, com a aplicação de alguns padrões de design.

## 🛠️ Tecnologias Utilizadas

- **Java**: Linguagem principal utilizada no desenvolvimento da aplicação.
- **Spring Boot**: Framework para criação de aplicações stand-alone e de produção com base em Spring.
- **Spring Data JPA**: Abordagem de persistência de dados com base no JPA, facilitando a integração com o banco de dados.
- **H2 Database**: Banco de dados em memória para testes e desenvolvimento rápido.
- **OpenFeign**: Cliente HTTP para integração com a API ViaCEP.
- **API ViaCEP**: Serviço de consulta de endereços a partir do CEP.

## 🔍 Visão Geral do Projeto

O projeto consiste em uma API RESTful para gerenciamento de clientes e endereços, onde é possível realizar operações de criação, leitura, atualização e remoção de clientes. Os dados de endereço são obtidos automaticamente via integração com a API do ViaCEP, facilitando a obtenção de informações completas a partir do CEP informado.

### Estrutura do Projeto

- `ClienteRestController`: Controlador principal da API, responsável por expor os endpoints de gerenciamento de clientes e endereços.
- `Cliente` e `Endereco`: Modelos de dados para representar as entidades do sistema.
- `ClienteService`: Interface que aplica o padrão Strategy, definindo os serviços de negócio para o domínio de clientes.
- `ViaCepService`: Interface Feign para a integração com a API ViaCEP, aplicando o padrão de design Facade para simplificar as operações de consulta de endereço.
- `Application`: Classe principal para iniciar a aplicação Spring Boot.

## 🧩 Padrões de Design Aplicados

- **Facade**: O controlador (`ClienteRestController`) age como uma fachada, escondendo a complexidade da lógica de negócio e integração externa, e expondo uma interface simples para o consumidor da API.
- **Strategy**: A interface `ClienteService` permite definir diferentes estratégias de serviço para o cliente, tornando a lógica de negócio mais flexível e expansível.
- **Singleton**: A instância do Spring Boot Application segue o padrão Singleton, garantindo que uma única instância da aplicação esteja em execução.

## 🚀 Como Executar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/AlexandreLiberatto/cliente-endereco-api-springboot.git
   ```

2. **Navegue até o diretório do projeto:**
   ```bash
   cd cliente-endereco-api-springboot
   ```

3. **Execute o projeto com Maven:**
   ```bash
   ./mvnw spring-boot:run
   ```
   Ou importe o projeto em uma IDE como IntelliJ ou Eclipse e execute a classe `Application`.

4. **Acesse a API**  
   A API estará disponível em: `http://localhost:8080/clientes`

## 📝 Endpoints Disponíveis

| Método | Endpoint        | Descrição                             |
|--------|------------------|---------------------------------------|
| GET    | `/clientes`     | Retorna todos os clientes             |
| GET    | `/clientes/{id}`| Retorna um cliente específico         |
| POST   | `/clientes`     | Cadastra um novo cliente              |
| PUT    | `/clientes/{id}`| Atualiza um cliente existente         |
| DELETE | `/clientes/{id}`| Remove um cliente                     |

## 📖 Desafios e Aprendizados

Durante o desenvolvimento deste projeto, foi possível praticar a integração de APIs externas, consolidar conceitos de padrões de projeto e aprofundar conhecimentos no ecossistema Spring. Este projeto é um exemplo prático da aplicação dos padrões e das boas práticas recomendadas no desenvolvimento de APIs RESTful em Java.

## 🏅 Sobre o Bootcamp

Este projeto foi desenvolvido como parte do Bootcamp da Claro oferecido pela [DIO](https://web.dio.me/). O bootcamp é uma excelente oportunidade para desenvolvedores aprimorarem suas habilidades com foco em Java e Spring Boot, explorando ferramentas e práticas amplamente utilizadas na indústria de software.


