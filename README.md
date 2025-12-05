# 🏛️ Bidding System API (Gestão de Licitações)

> API RESTful robusta desenvolvida para o gerenciamento de empresas e processos licitatórios (Public Procurement), focada na integridade dos dados e agilidade no cadastro de fornecedores.

![Java Badge](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot Badge](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MySQL Badge](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

---

## 💻 Sobre o Projeto

Este projeto consiste no Back-End de um sistema de licitações públicas. Ele fornece os serviços necessários para o credenciamento de empresas participantes, gerenciando dados críticos como **Acervo Técnico**, **Capital Declarado** e **CNPJ**.

A aplicação foi construída utilizando as versões mais recentes do ecossistema Java (Java 21 LTS e Spring Boot 3), seguindo os padrões de arquitetura REST.

### 🛠️ Tech Stack & Ferramentas

* **Linguagem:** Java 21 (Recursos modernos da linguagem)
* **Framework:** Spring Boot 3.3.0
* **Banco de Dados:** MySQL (Produção) / H2 Database (Memória/Dev)
* **ORM:** Spring Data JPA / Hibernate
* **Produtividade:** Lombok (Redução de boilerplate code)
* **Build:** Maven

---

## ⚙️ Funcionalidades (Endpoints)

A API expõe recursos para a gestão completa do ciclo de vida das empresas licitantes:

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `GET` | `/empresas` | Lista todas as empresas cadastradas no certame. |
| `POST` | `/empresas` | Cadastra uma nova empresa (Requer JSON no corpo). |
| `PUT` | `/empresas/{id}` | Atualiza dados cadastrais (Acervo, Capital, E-mail). |
| `DELETE`| `/empresas/{id}`| Remove uma empresa da base de dados. |

---

## 🚀 Como Executar

### Pré-requisitos
* Java JDK 21 instalado
* Maven instalado
* MySQL (Opcional, pois o projeto está configurado para aceitar H2 em memória se necessário)

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/Welberrr/bidding-system-api.git](https://github.com/Welberrr/bidding-system-api.git)
Configure o Banco de Dados:

O projeto utiliza MySQL por padrão. Certifique-se de ter um banco criado ou altere o arquivo application.properties para usar H2 em memória para testes rápidos.

Execute a aplicação:

Bash

cd bidding-system-api
./mvnw spring-boot:run
Teste a API:

Acesse via Postman ou Insomnia em: http://localhost:8080/empresas

📂 Estrutura do Projeto
Plaintext

src/main/java/com/licitacao/
├── controller/       # Camada de exposição da API (REST Controllers)
├── model/            # Entidades JPA e regras de negócio
├── repository/       # Camada de acesso a dados (Spring Data Repositories)
└── LicitacaoApiApplication.java # Classe Main
