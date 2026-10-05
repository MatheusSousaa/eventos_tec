# Eventos-TEC API 🚀

API RESTful desenvolvida em **Java** e **Spring Boot** para a gestão de eventos e cupons de desconto, integrada com serviços em nuvem da AWS (RDS PostgreSQL e S3).

## 🛠 Tecnologias e Ferramentas Utilizadas

* **Java 26**[cite: 1]
* **Spring Boot 4.1.1** (Spring Web, Spring Data JPA, Spring Security)[cite: 1]
* **Banco de Dados:** PostgreSQL (hospedado na **AWS RDS**)[cite: 1, 2]
* **Migrações:** Flyway[cite: 1]
* **Armazenamento em Nuvem:** **AWS S3** (para upload e gestão de imagens de eventos)[cite: 1, 4]
* **Ferramentas de Teste:** Postman[cite: 3]
* **Ambiente de Desenvolvimento:** IntelliJ IDEA[cite: 1]

## ⚙️ Arquitetura e Funcionalidades

A aplicação foi estruturada seguindo as melhores práticas de desenvolvimento backend, separando responsabilidades em camadas (Controllers, Services, Repositories e DTOs):

* **Gestão de Eventos:** Cadastro de eventos presenciais e remotos com suporte a upload de imagens diretamente para um bucket S3[cite: 4].
* **Listagem e Filtros:** Consulta paginada de eventos futuros e filtragem por título, cidade, UF e intervalo de datas.
* **Sistema de Cupons:** Associação de cupons de desconto com percentuais e prazos de validade atrelados a eventos específicos.

## 🚀 Como Executar o Projeto

1. **Pré-requisitos:**
   * Java JDK instalado (versão 26 ou compatível)[cite: 1].
   * Maven configurado.
   * Credenciais ativas da AWS (S3 e RDS PostgreSQL) configuradas no ambiente ou no ficheiro `application.properties`.

2. **Clone o repositório:**
   ```bash
   git clone [https://github.com/SEU-USUARIO/eventos-tec.git](https://github.com/SEU-USUARIO/eventos-tec.git)
   cd eventos-tec

    Configure as variáveis de ambiente / application.properties:
    Certifique-se de configurar a string de conexão com o seu banco RDS e as chaves de acesso ao S3 (aws.bucket.name, etc.).

    Execute a aplicação:
    Bash

    mvn spring-boot:run

📌 Endpoints Principais

    POST /api/event - Cria um novo evento (com suporte a multipart/form-data para imagens)   
    PNG+ 1

    GET /api/event - Lista os próximos eventos de forma paginada

    GET /api/event/{eventId} - Detalhes de um evento específico e seus cupons

    POST /api/coupon/event/{eventId} - Adiciona um cupom de desconto a um evento

Desenvolvido por [Seu Nome/Matheus].


---

## 2. Post para o LinkedIn

Pode copiar este texto, adicionar as capturas de tela (prints do Postman com o `200 OK` e da estrutura a funcionar) e publicar para mostrar a sua evolução técnica:

> 🚀 **Projeto Concluído: API RESTful com Spring Boot, AWS RDS e AWS S3!**[cite: 4]
> 
> Nas últimas semanas, dediquei-me ao desenvolvimento e integração do **eventos-tec**, uma aplicação backend robusta focada na gestão completa de eventos, endereços e cupons de desconto[cite: 1, 4].
> 
> O grande diferencial deste projeto foi a implementação prática de um ecossistema real de nuvem e persistência:
> ✅ **Java & Spring Boot:** Arquitetura limpa utilizando Records, Spring Data JPA e mapeamento avançado[cite: 1].
> ✅ **AWS RDS (PostgreSQL):** Conexão segura em nuvem, migrações controladas via Flyway e tratamento de restrições de integridade[cite: 1, 2, 4].
> ✅ **AWS S3:** Gestão e upload de ficheiros multimédia (imagens de capa dos eventos) diretamente para o bucket na nuvem[cite: 1, 4].
> ✅ **Testes de Integração:** Validação completa de endpoints (`POST` e `GET` paginados) utilizando o Postman[cite: 3, 4].
> 
> Desafios como o tratamento de timestamps em milissegundos e o mapeamento correto de parâmetros `form-data` trouxeram ótimos aprendizados de depuração e performance. 
> 
> O código já está estruturado e documentado no meu GitHub! 💻🔥
> 
> #Java #SpringBoot #AWS #PostgreSQL #Backend #CleanCode #DesenvolvimentoDeSoftware
