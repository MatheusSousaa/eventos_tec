# 🚀 Eventos-TEC API

API REST desenvolvida com **Java e Spring Boot** para gerenciamento de eventos, endereços e cupons de desconto.

O projeto foi desenvolvido com foco em boas práticas de desenvolvimento backend e integração com serviços da **AWS**, utilizando **PostgreSQL no Amazon RDS** e **Amazon S3** para armazenamento de imagens.

## 🛠️ Tecnologias utilizadas

* **Java 26**
* **Spring Boot 4.1.1**
* Spring Web
* Spring Data JPA
* Spring Security
* PostgreSQL
* **Amazon RDS**
* **Amazon S3**
* Flyway
* Lombok
* Maven
* Postman
* IntelliJ IDEA

## 🏗️ Arquitetura

A aplicação foi organizada em camadas, buscando separar as responsabilidades do sistema:

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

Também são utilizados **DTOs** para controlar os dados enviados e recebidos pela API.

## ⚙️ Funcionalidades

### 🎫 Eventos

* Cadastro de eventos
* Consulta de eventos
* Consulta de evento por ID
* Paginação
* Filtros por título, cidade, estado e período
* Cadastro de eventos presenciais e remotos
* Upload de imagens para o Amazon S3

### 🎟️ Cupons

* Cadastro de cupons vinculados a eventos
* Definição de percentual de desconto
* Controle de validade dos cupons
* Consulta de cupons relacionados a eventos

### 🏠 Endereços

* Cadastro de endereços relacionados aos eventos
* Informações de cidade, estado e UF

## ☁️ AWS

O projeto também possui integração com serviços da Amazon Web Services:

* **Amazon RDS:** hospedagem do banco de dados PostgreSQL.
* **Amazon S3:** armazenamento das imagens dos eventos.

As migrações do banco de dados são controladas utilizando **Flyway**, permitindo versionar e aplicar as alterações do schema de forma organizada.

## 📌 Principais endpoints

| Método | Endpoint                      | Descrição                   |
| ------ | ----------------------------- | --------------------------- |
| `POST` | `/api/event`                  | Cria um evento              |
| `GET`  | `/api/event`                  | Lista eventos               |
| `GET`  | `/api/event/{eventId}`        | Busca um evento pelo ID     |
| `POST` | `/api/coupon/event/{eventId}` | Adiciona um cupom ao evento |

## 🚀 Como executar

### Pré-requisitos

* Java JDK 26
* Maven
* PostgreSQL ou acesso ao Amazon RDS
* Conta/bucket configurado no Amazon S3

### Clone o projeto

```bash
git clone https://github.com/MatheusSousaa/eventos-tec.git
cd eventos-tec
```

### Configuração

Configure as informações do banco de dados e da AWS no ambiente da aplicação.

Exemplo:

```properties
spring.datasource.url=jdbc:postgresql://SEU-ENDPOINT/postgres
spring.datasource.username=SEU_USU_
```
