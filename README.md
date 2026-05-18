# BeautyBook

# 💅 BeautyBook 👨‍💻

> Aplicação web para gerenciamento de agendamentos em salões de beleza.  
> Permite que clientes realizem reservas online e que funcionários e administradores gerenciem a agenda, os serviços e os relatórios de atendimento.

-----

## 🚧 Status do Projeto

![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-17-007ec6?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.5-007ec6?style=for-the-badge&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-19.1.1-007ec6?style=for-the-badge&logo=react&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Licença](https://img.shields.io/badge/Licença-MIT-007ec6?style=for-the-badge)

-----

## 📚 Índice

- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Instalação e Execução](#-instalação-e-execução)
- [Deploy](#-deploy)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Testes](#-testes)
- [Documentações Utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

-----

## 🔗 Links Úteis

- 🌐 **Demo Online:** [Acesse a Aplicação Web](https://beautybook.vercel.app)

> 💻 Aplicação hospedada na Vercel (ambiente de produção).

- 📖 **Documentação:** [Leia a Documentação de Projeto](./docs/Documentacao_BeautyBook_v1.0.pdf)

> 📚 Documentação técnica completa com modelos de usuário, diagramas UML e modelos de dados.

-----

## 📝 Sobre o Projeto

O **BeautyBook** é uma aplicação web desenvolvida para modernizar o processo de agendamento em salões de beleza. O sistema surgiu da necessidade de substituir agendamentos manuais (cadernos, ligações telefônicas) por uma plataforma digital centralizada, acessível e fácil de usar.

A aplicação oferece valor para três perfis distintos:

- **Clientes**, que podem reservar serviços de forma autônoma, visualizar seus agendamentos e utilizar cupons de desconto.
- **Funcionários**, que acompanham sua agenda diária e atualizam o status dos atendimentos.
- **Administradores**, que gerenciam o catálogo de serviços, controlam promoções e analisam o desempenho do negócio através de relatórios.

O projeto foi desenvolvido como trabalho acadêmico na disciplina de **Projeto de Software** da PUC Minas, aplicando conceitos de arquitetura em camadas, modelagem UML e boas práticas de engenharia de software.

-----

## ✨ Funcionalidades Principais

- 👤 **Cadastro e Autenticação de Usuários:** Registro de clientes, login seguro e recuperação de senha.
- 📅 **Agendamento Online:** Seleção de serviço, profissional e horário disponível com bloqueio automático da agenda.
- ❌ **Cancelamento de Reservas:** Cancelamento com antecedência mínima de 2 horas, com liberação automática do horário.
- 🏷️ **Cupons de Desconto:** Inserção de códigos promocionais no momento do agendamento.
- 🗓️ **Consulta de Agenda (Funcionário):** Visualização da lista de atendimentos diários por profissional.
- ✅ **Atualização de Status:** Marcação de atendimentos como concluídos para manter o histórico atualizado.
- 🛠️ **Gestão de Catálogo:** Cadastro, edição e remoção de serviços e preços pelo administrador.
- 📊 **Relatórios de Desempenho:** Geração de relatórios de atendimentos e faturamento por período.
- 🎟️ **Gestão de Promoções:** Criação e gerenciamento de campanhas com cupons de desconto.

-----

## 🛠 Tecnologias Utilizadas

### 💻 Front-end

- **Biblioteca:** React 19.1.1
- **Linguagem:** TypeScript
- **Estilização:** Tailwind CSS
- **Gerenciamento de Estado:** Context API
- **Build Tool:** Vite 6.x

### 🖥️ Back-end

- **Linguagem:** Java 17 (JDK)
- **Framework:** Spring Boot 3.3.5
- **Banco de Dados:** PostgreSQL 16
- **ORM:** Hibernate / Spring Data JPA
- **Autenticação:** JWT + Spring Security
- **Comunicação:** REST API (HTTP/JSON)

### ⚙️ Infraestrutura & DevOps

- **Containerização:** Docker + Docker Compose
- **Cloud (Front-end):** Vercel
- **Cloud (Back-end):** Railway
- **CI/CD:** GitHub Actions

-----

## 🏗 Arquitetura

O **BeautyBook** segue uma **Arquitetura em Camadas (Layered Architecture)**, organizada da seguinte forma:

|Camada                  |Responsabilidade                |Tecnologia                |
|------------------------|--------------------------------|--------------------------|
|**Presentation Layer**  |Interface com o usuário         |React (SPA)               |
|**Application Layer**   |Exposição de endpoints REST     |Spring Boot               |
|**Domain Layer**        |Regras de negócio e entidades   |Java (POJOs + Services)   |
|**Infrastructure Layer**|Persistência e serviços externos|PostgreSQL, JavaMailSender|

A comunicação entre o frontend e o backend é feita exclusivamente via **HTTP/JSON**. O banco de dados é acessado somente pela camada de infraestrutura, respeitando o encapsulamento das camadas.

**Padrões adotados:** Repository Pattern, Service Layer, DTO, MVC.

### Exemplos de Diagramas

|Diagrama de Componentes|Diagrama de Implantação                |
|-----------------------|---------------------------------------|
|*(inserir imagem)*     |*(inserir imagem)*                     |
|**Diagrama de Classes**|**Diagrama de Sequência – Agendamento**|
|*(inserir imagem)*     |*(inserir imagem)*                     |


> Os diagramas completos estão disponíveis na pasta `/docs` e na [Documentação de Projeto](./docs/Documentacao_BeautyBook_v1.0.pdf).

-----

## 🔧 Instalação e Execução

### Pré-requisitos

- **Java JDK 17** ou superior
- **Node.js** v18.x ou superior (LTS)
- **npm** ou **yarn**
- **Docker** (recomendado para o banco de dados)

-----

### 🔑 Variáveis de Ambiente

#### Back-end (Spring Boot)

Configure as variáveis de ambiente do sistema ou no arquivo `application.yml`:

|Variável                    |Descrição                                   |Exemplo                                      |
|----------------------------|--------------------------------------------|---------------------------------------------|
|`SERVER_PORT`               |Porta do servidor back-end                  |`8080`                                       |
|`SPRING_DATASOURCE_URL`     |URL JDBC de conexão com o banco             |`jdbc:postgresql://localhost:5432/beautybook`|
|`SPRING_DATASOURCE_USERNAME`|Usuário do banco de dados                   |`postgres`                                   |
|`SPRING_DATASOURCE_PASSWORD`|Senha do banco de dados                     |`senha-segura-123`                           |
|`JWT_SECRET`                |Chave secreta para assinatura dos tokens JWT|`chave_super_segura_base64`                  |
|`MAIL_USERNAME`             |E-mail usado para notificações              |`noreply@beautybook.com`                     |
|`MAIL_PASSWORD`             |Senha do serviço de e-mail                  |`senha_email`                                |

#### Front-end (React + Vite)

Crie o arquivo `.env` na raiz da pasta `/frontend`:

|Variável      |Descrição                  |Exemplo                    |
|--------------|---------------------------|---------------------------|
|`VITE_API_URL`|URL base da API Spring Boot|`http://localhost:8080/api`|

-----

### 📦 Instalação de Dependências

1. **Clone o repositório:**

```bash
git clone https://github.com/alice-salomao/beautybook.git
cd beautybook
```

1. **Instale as dependências do Front-end:**

```bash
cd frontend
npm install
cd ..
```

1. **Instale as dependências do Back-end:**

```bash
cd backend
./mvnw clean install
cd ..
```

-----

### 💾 Inicialização do Banco de Dados (PostgreSQL)

Suba o banco com Docker:

```bash
docker run --name beautybook_db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=senha-segura-123 \
  -e POSTGRES_DB=beautybook \
  -p 5432:5432 \
  -d postgres:16
```

O schema será gerado automaticamente pelo Hibernate no primeiro startup do back-end.

-----

### ⚡ Como Executar a Aplicação

**Terminal 1 – Back-end:**

```bash
cd backend
./mvnw spring-boot:run
```

🚀 API disponível em **http://localhost:8080**

**Terminal 2 – Front-end:**

```bash
cd frontend
npm run dev
```

🎨 Aplicação disponível em **http://localhost:5173**

-----

### 🐳 Execução Completa com Docker Compose

```bash
docker-compose up --build -d
```

Para parar:

```bash
docker-compose down
```

-----

## 🚀 Deploy

```bash
# Build do Front-end
cd frontend
npm run build

# Build do Back-end
cd ../backend
./mvnw clean package
```

- **Front-end:** Deploy automático na **Vercel** via integração com o GitHub.
- **Back-end:** Deploy no **Railway** com variáveis de ambiente configuradas no painel.

-----

## 📂 Estrutura de Pastas

```
beautybook/
├── README.md
├── docker-compose.yml
├── docs/                              # 📚 Documentação de projeto e diagramas UML
│   └── Documentacao_BeautyBook_v1.0.pdf
│
├── frontend/                          # 📁 Aplicação React
│   ├── .env.example
│   ├── Dockerfile
│   ├── package.json
│   └── src/
│       ├── components/                # 🧱 Componentes reutilizáveis
│       ├── pages/                     # 📄 Páginas da aplicação
│       │   ├── Login/
│       │   ├── Agendamento/
│       │   ├── MinhasReservas/
│       │   ├── AgendaFuncionario/
│       │   └── Admin/
│       ├── services/                  # 🔌 Chamadas HTTP à API
│       ├── hooks/                     # 🎣 Hooks customizados
│       ├── context/                   # 🌐 Contextos globais (Auth, etc.)
│       └── utils/                     # 🛠️ Funções utilitárias
│
└── backend/                           # 📁 Aplicação Spring Boot
    ├── .env.example
    ├── Dockerfile
    ├── pom.xml
    └── src/main/java/com/beautybook/
        ├── controller/                # 🎮 Endpoints REST
        ├── service/                   # ⚙️ Regras de negócio
        ├── repository/                # 🗄️ Repositórios JPA
        ├── model/                     # 🧬 Entidades (Cliente, Agendamento, Servico...)
        ├── dto/                       # ✉️ Data Transfer Objects
        ├── config/                    # 🔧 Configurações (CORS, Swagger, etc.)
        ├── exception/                 # 💥 Handlers de exceção
        └── security/                  # 🛡️ JWT e Spring Security
```

-----

## 🎥 Demonstração

### 🌐 Aplicação Web

|Tela                     |Captura de Tela          |
|-------------------------|-------------------------|
|**Tela Inicial / Login** |**Painel do Cliente**    |
|*(inserir screenshot)*   |*(inserir screenshot)*   |
|**Tela de Agendamento**  |**Agenda do Funcionário**|
|*(inserir screenshot)*   |*(inserir screenshot)*   |
|**Painel Administrativo**|**Relatórios**           |
|*(inserir screenshot)*   |*(inserir screenshot)*   |

-----

## 🧪 Testes

### Testes Unitários e de Integração

```bash
# Back-end (JUnit + Mockito)
cd backend
./mvnw test

# Front-end (Vitest)
cd frontend
npm run test
```

### Testes End-to-End (E2E)

```bash
cd frontend
npm run test:e2e
```

*Ferramenta: Cypress*

-----

## 🔗 Documentações Utilizadas

- 📖 **React:** [Documentação Oficial do React](https://react.dev/reference/react)
- 📖 **Vite:** [Guia de Configuração do Vite](https://vitejs.dev/config/)
- 📖 **Spring Boot:** [Documentação Oficial do Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- 📖 **Spring Security + JWT:** [Spring Security Reference](https://docs.spring.io/spring-security/reference/)
- 📖 **Spring Data JPA:** [Spring Data JPA Docs](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)
- 📖 **PostgreSQL:** [Documentação do PostgreSQL](https://www.postgresql.org/docs/)
- 📖 **Docker:** [Documentação Docker](https://docs.docker.com/)
- 📖 **Conventional Commits:** [Padrão de Mensagens de Commit](https://www.conventionalcommits.org/en/v1.0.0/)

-----

## 👥 Autores

|👤 Nome               |🐙 GitHub                                          |💼 LinkedIn                                                            |
|---------------------|--------------------------------------------------|----------------------------------------------------------------------|
|Alice Shikida Salomão|[@alice-salomao](https://github.com/alice-salomao)|[linkedin.com/in/alice-salomao](https://linkedin.com/in/alice-salomao)|

-----

## 🤝 Contribuição

1. Faça um `fork` do projeto.
1. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`).
1. Commit suas mudanças (`git commit -m 'feat: Adiciona nova funcionalidade X'`). (**Utilize [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)**)
1. Faça o `push` para a branch (`git push origin feature/minha-feature`).
1. Abra um **Pull Request**.

-----

## 🙏 Agradecimentos

- [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo suporte institucional e pela formação em boas práticas de engenharia.
- [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos em **Projeto de Software**, **Arquitetura** e **Padrões de Projeto**.

-----

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](./LICENSE)**.
