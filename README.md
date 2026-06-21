<!-- README adaptado do template oficial da disciplina:
https://github.com/joaopauloaramuni/laboratorio-de-desenvolvimento-de-software/blob/main/TEMPLATES/template_README.md -->

# 🏷️ FoodStack 👨‍💻

<p align="center">
  <img src="assets/readme/foodstack_logo_animado_v4.svg" alt="Apresentação animada do FoodStack" width="88%"/>
</p>

> [!NOTE]
> Projeto acadêmico individual de uma **despensa virtual com recomendação de receitas**. A solução controla estoque e validade, reduz desperdícios e sugere receitas com os alimentos disponíveis.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O FoodStack foi projetado para famílias que desejam organizar alimentos, acompanhar vencimentos e decidir o que cozinhar. Esta entrega contém somente documentação, arquitetura e diagramas, conforme solicitado. Não existe código executável da aplicação.
      </div>
    </td>
    <td>
      <img src="assets/logo-foodstack.png" alt="Logo do FoodStack" width="140px"/>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

### Exemplos de badges básicos:

![Status](https://img.shields.io/badge/status-concluído-2ea44f)
![Versão](https://img.shields.io/badge/versão-1.0.0-blue)
![Licença](https://img.shields.io/badge/licença-MIT-green)
![Documentação](https://img.shields.io/badge/entrega-documentação%20e%20arquitetura-007ec6)

### Outros exemplos de badges:

![PlantUML](https://img.shields.io/badge/PlantUML-obrigatório-F7A81B?style=for-the-badge)
![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

---

## 📚 Índice

- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
  - [Exemplos de diagramas](#exemplos-de-diagramas)
- [Instalação e Execução](#-instalação-e-execução)
  - [Pré-requisitos](#pré-requisitos)
  - [Variáveis de Ambiente](#-variáveis-de-ambiente)
  - [Instalação de Dependências](#-instalação-de-dependências)
  - [Inicialização do Banco de Dados](#-inicialização-do-banco-de-dados-postgresql)
  - [Como Executar a Aplicação](#-como-executar-a-aplicação)
- [Deploy](#-deploy)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Testes](#-testes)
- [Documentações utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🔗 Links Úteis

- **Documento obrigatório:** [FoodStack - Documentação de Projeto.docx](docs/FoodStack%20-%20Documenta%C3%A7%C3%A3o%20de%20Projeto.docx)
- **Códigos PlantUML:** [docs/plantuml](docs/plantuml)
- **Diagramas renderizados:** [docs/diagramas](docs/diagramas)
- **Template de README utilizado:** [template_README.md](https://github.com/joaopauloaramuni/laboratorio-de-desenvolvimento-de-software/blob/main/TEMPLATES/template_README.md)
- **PlantUML:** [plantuml.com](https://plantuml.com/)

> Não há demo online ou aplicativo para download, pois a atividade não exige implementação.

---

## 📝 Sobre o Projeto

O FoodStack nasceu da necessidade de reduzir o desperdício doméstico de alimentos. Muitas famílias perdem produtos por vencimento, compram itens duplicados e têm dificuldade para escolher receitas com o estoque disponível.

A aplicação projetada mantém uma despensa compartilhada, registra quantidades e datas de validade, alerta sobre vencimentos e recomenda receitas. O contexto é acadêmico e todo o comportamento foi especificado por requisitos, regras de negócio, contratos e diagramas UML.

A documentação detalhada está no [arquivo Word preenchido no template obrigatório](docs/FoodStack%20-%20Documenta%C3%A7%C3%A3o%20de%20Projeto.docx).

---

## ✨ Funcionalidades Principais

- **Autenticação:** cadastro, login e recuperação de acesso.
- **Gestão da despensa:** cadastro, consulta, edição e remoção de ingredientes.
- **Controle de validade:** alertas para itens próximos do vencimento.
- **Sugestão de receitas:** recomendações compatíveis com o estoque e restrições alimentares.
- **Baixa automática:** atualização transacional do estoque após o preparo.
- **Lista de compras:** cálculo dos ingredientes ausentes ou insuficientes.
- **Compartilhamento:** papéis de dono, editor e leitor para membros da família.
- **Histórico:** rastreabilidade das alterações de estoque.

---

## 🛠 Tecnologias Utilizadas

> As tecnologias abaixo são **fictícias e planejadas**, conforme solicitado. Não há implementação no repositório.

### 💻 Front-end

- React 19
- TypeScript 5.8
- Vite 7
- Tailwind CSS
- Zustand

### 🖥️ Back-end

- Java 21
- Spring Boot 3.4
- Spring Security com JWT
- Spring Data JPA e Hibernate
- PostgreSQL 16

### 📱 Mobile (Opcional)

- React Native
- Expo
- Firebase Cloud Messaging

### ⚙️ Infraestrutura & DevOps

- Docker e Docker Compose
- GitHub Actions
- AWS ECS Fargate e Amazon RDS
- Redis
- RabbitMQ
- OpenTelemetry, Prometheus e Grafana

---

## 🏗 Arquitetura

O sistema foi projetado como um **monólito modular orientado a domínio**, dividido nas camadas de interface, aplicação, domínio e infraestrutura.

- **Interface:** aplicação web e futuro aplicativo mobile.
- **Aplicação:** orquestra casos de uso, autorização e transações.
- **Domínio:** concentra entidades, políticas e regras de negócio.
- **Infraestrutura:** banco de dados, cache, mensageria e notificações.

Foram planejados os padrões Repository, Service Layer, DTO, Strategy e Observer. A escolha do monólito modular reduz a complexidade operacional e mantém os módulos separados para uma futura evolução.

### Exemplos de diagramas

| Diagrama | Diagrama |
| :---: | :---: |
| **01 - Casos de Uso** | **02 - Componentes** |
| <img src="docs/diagramas/01-casos-de-uso.png" alt="Diagrama de Casos de Uso" width="430px"/> | <img src="docs/diagramas/02-diagrama-componentes.png" alt="Diagrama de Componentes" width="430px"/> |
| **03 - Classes** | **04 - Modelo de Dados / DER** |
| <img src="docs/diagramas/03-diagrama-classes.png" alt="Diagrama de Classes" width="430px"/> | <img src="docs/diagramas/04-modelo-dados-der.png" alt="Modelo de Dados" width="430px"/> |
| **05a - Sequência: Sugestão de Receitas** | **05b - Sequência: Preparo e Baixa de Estoque** |
| <img src="docs/diagramas/05a-sequencia-sugestao-receitas.png" alt="Sequência de Sugestão de Receitas" width="430px"/> | <img src="docs/diagramas/05b-sequencia-preparo-baixa-estoque.png" alt="Sequência de Preparo e Baixa de Estoque" width="430px"/> |
| **05c - Sequência: Lista de Compras** | **05d - Sequência: Alerta de Vencimento** |
| <img src="docs/diagramas/05c-sequencia-lista-compras.png" alt="Sequência de Lista de Compras" width="430px"/> | <img src="docs/diagramas/05d-sequencia-alerta-vencimento.png" alt="Sequência de Alerta de Vencimento" width="430px"/> |
| **06 - Atividade** | **07 - Estados** |
| <img src="docs/diagramas/06-diagrama-atividade-alerta-vencimento.png" alt="Diagrama de Atividade" width="430px"/> | <img src="docs/diagramas/07-diagrama-estados-item-despensa.png" alt="Diagrama de Estados" width="430px"/> |
| **08 - Comunicação** | **09 - Implantação** |
| <img src="docs/diagramas/08-diagrama-comunicacao-lista-compras.png" alt="Diagrama de Comunicação" width="430px"/> | <img src="docs/diagramas/09-diagrama-implantacao.png" alt="Diagrama de Implantação" width="430px"/> |

Cada imagem foi gerada a partir de um arquivo PlantUML versionado em [docs/plantuml](docs/plantuml).

---

## 🔧 Instalação e Execução

> [!IMPORTANT]
> A atividade solicita apenas projeto, diagramação e arquitetura. Os comandos desta seção representam a execução futura da solução fictícia.

### Pré-requisitos

- Java JDK 21
- Maven 3.9
- Node.js 20
- Docker e Docker Compose
- PlantUML e Graphviz

### 🔑 Variáveis de Ambiente

#### 1 Back-end (Spring Boot)

| Variável | Descrição | Exemplo |
|---|---|---|
| `SERVER_PORT` | Porta da API | `8080` |
| `SPRING_DATASOURCE_URL` | Conexão PostgreSQL | `jdbc:postgresql://localhost:5432/foodstack` |
| `SPRING_DATASOURCE_USERNAME` | Usuário do banco | `foodstack` |
| `SPRING_DATASOURCE_PASSWORD` | Senha do banco | `senha-local` |
| `JWT_SECRET` | Assinatura dos tokens | `segredo-ficticio` |

#### 2 Front-end (React, Vite)

| Variável | Descrição | Exemplo |
|---|---|---|
| `VITE_API_URL` | URL da API | `http://localhost:8080/api` |
| `VITE_APP_NAME` | Nome exibido | `FoodStack` |

#### 3. Exemplos de Variáveis de Ambiente na Vercel

##### **Exemplo 1 – Front-end com Next.js usando API externa**

`NEXT_PUBLIC_API_URL=https://api.foodstack.example/api`

##### **Exemplo 2 – Aplicação Full-stack (Next.js + Prisma + PostgreSQL)**

`DATABASE_URL=postgresql://foodstack:senha@db.example:5432/foodstack`

##### **Exemplo 3 – Integração com APIs externas**

`SENDGRID_API_KEY=chave_ficticia`

##### **Exemplo 4 – Frontend com Vite (EmailJS)**

`VITE_EMAILJS_PUBLIC_KEY=chave_publica_ficticia`

> Os valores são apenas exemplos acadêmicos e não representam credenciais reais.

### 📦 Instalação de Dependências

#### Front-end (React)

```bash
cd frontend
npm install
```

#### Back-end (Spring Boot)

```bash
cd backend
./mvnw dependency:resolve
```

### 💾 Inicialização do Banco de Dados (PostgreSQL)

O banco seria iniciado pelo Docker Compose e atualizado pelo Flyway:

```bash
docker compose up -d postgres
./mvnw flyway:migrate
```

### ⚡ Como Executar a Aplicação

#### Terminal 1: Back-end (Spring Boot)

```bash
cd backend
./mvnw spring-boot:run
```

#### Terminal 2: Front-end (React, Vite)

```bash
cd frontend
npm run dev
```

#### 🐳 Execução Local Completa com Docker Compose (Incluindo Banco de Dados)

```bash
docker compose up --build
```

#### 📦 Passos para build, inicialização e execução

1. Configurar as variáveis de ambiente.
2. Iniciar PostgreSQL e Redis.
3. Executar as migrações.
4. Iniciar o back-end.
5. Iniciar o front-end.

> Esses comandos documentam a arquitetura planejada. As respectivas pastas de código não existem nesta entrega.

---

## 🚀 Deploy

O deploy planejado utiliza:

| Camada | Tecnologia |
|---|---|
| Front-end | Vercel |
| API | AWS ECS Fargate |
| Imagens | AWS ECR |
| Banco de dados | Amazon RDS PostgreSQL |
| Cache | Amazon ElastiCache Redis |
| Mensageria | Amazon SQS |
| Monitoramento | CloudWatch e Grafana |
| CI/CD | GitHub Actions |

Não existe ambiente publicado porque a implementação não faz parte do trabalho.

---

## 📂 Estrutura de Pastas

```text
FoodStack-Arquitetura/
├── README.md
├── LICENSE
├── assets/
│   ├── logo-foodstack.png
│   └── readme/
│       ├── foodstack_logo_animado_v4.svg
│       └── foodstack_encerramento_animado.svg
└── docs/
    ├── FoodStack - Documentação de Projeto.docx
    ├── diagramas/
    │   ├── 01-casos-de-uso.png
    │   ├── 02-diagrama-componentes.png
    │   ├── 03-diagrama-classes.png
    │   ├── 04-modelo-dados-der.png
    │   ├── 05a-sequencia-sugestao-receitas.png
    │   ├── 05b-sequencia-preparo-baixa-estoque.png
    │   ├── 05c-sequencia-lista-compras.png
    │   ├── 05d-sequencia-alerta-vencimento.png
    │   ├── 06-diagrama-atividade-alerta-vencimento.png
    │   ├── 07-diagrama-estados-item-despensa.png
    │   ├── 08-diagrama-comunicacao-lista-compras.png
    │   └── 09-diagrama-implantacao.png
    └── plantuml/
        ├── 01-casos-de-uso.puml
        ├── 02-diagrama-componentes.puml
        ├── 03-diagrama-classes.puml
        ├── 04-modelo-dados-der.puml
        ├── 05a-sequencia-sugestao-receitas.puml
        ├── 05b-sequencia-preparo-baixa-estoque.puml
        ├── 05c-sequencia-lista-compras.puml
        ├── 05d-sequencia-alerta-vencimento.puml
        ├── 06-diagrama-atividade-alerta-vencimento.puml
        ├── 07-diagrama-estados-item-despensa.puml
        ├── 08-diagrama-comunicacao-lista-compras.puml
        └── 09-diagrama-implantacao.puml
```

---

## 🎥 Demonstração

A demonstração desta entrega é composta pelo documento e pelos diagramas.

### 📱 Aplicativo Mobile

O aplicativo mobile foi apenas planejado. Seu comportamento está representado nos casos de uso e diagramas de sequência.

### 🌐 Aplicação Web

A aplicação web não foi implementada. A navegação e as responsabilidades estão representadas no diagrama de componentes.

### 💻 Exemplo de Saída no Terminal (para Back-end, API, CLI)

#### 1. Demonstração da API (Exemplo com cURL)

Resposta fictícia planejada para consulta de estoque:

```json
{
  "despensaId": 1,
  "itens": 12,
  "proximosDoVencimento": 3
}
```

#### 2. Demonstração de Execução de CLI/Script

Os arquivos PlantUML podem ser renderizados com:

```bash
java -jar plantuml.jar -tpng docs/plantuml/*.puml -o ../diagramas
```

| Diagrama | Código PlantUML | Imagem |
|---|---|---|
| Casos de uso | [01-casos-de-uso.puml](docs/plantuml/01-casos-de-uso.puml) | [PNG](docs/diagramas/01-casos-de-uso.png) |
| Componentes | [02-diagrama-componentes.puml](docs/plantuml/02-diagrama-componentes.puml) | [PNG](docs/diagramas/02-diagrama-componentes.png) |
| Classes | [03-diagrama-classes.puml](docs/plantuml/03-diagrama-classes.puml) | [PNG](docs/diagramas/03-diagrama-classes.png) |
| Modelo de dados | [04-modelo-dados-der.puml](docs/plantuml/04-modelo-dados-der.puml) | [PNG](docs/diagramas/04-modelo-dados-der.png) |
| Sequência: sugestões | [05a-sequencia-sugestao-receitas.puml](docs/plantuml/05a-sequencia-sugestao-receitas.puml) | [PNG](docs/diagramas/05a-sequencia-sugestao-receitas.png) |
| Sequência: preparo | [05b-sequencia-preparo-baixa-estoque.puml](docs/plantuml/05b-sequencia-preparo-baixa-estoque.puml) | [PNG](docs/diagramas/05b-sequencia-preparo-baixa-estoque.png) |
| Sequência: compras | [05c-sequencia-lista-compras.puml](docs/plantuml/05c-sequencia-lista-compras.puml) | [PNG](docs/diagramas/05c-sequencia-lista-compras.png) |
| Sequência: vencimento | [05d-sequencia-alerta-vencimento.puml](docs/plantuml/05d-sequencia-alerta-vencimento.puml) | [PNG](docs/diagramas/05d-sequencia-alerta-vencimento.png) |
| Atividade | [06-diagrama-atividade-alerta-vencimento.puml](docs/plantuml/06-diagrama-atividade-alerta-vencimento.puml) | [PNG](docs/diagramas/06-diagrama-atividade-alerta-vencimento.png) |
| Estados | [07-diagrama-estados-item-despensa.puml](docs/plantuml/07-diagrama-estados-item-despensa.puml) | [PNG](docs/diagramas/07-diagrama-estados-item-despensa.png) |
| Comunicação | [08-diagrama-comunicacao-lista-compras.puml](docs/plantuml/08-diagrama-comunicacao-lista-compras.puml) | [PNG](docs/diagramas/08-diagrama-comunicacao-lista-compras.png) |
| Implantação | [09-diagrama-implantacao.puml](docs/plantuml/09-diagrama-implantacao.puml) | [PNG](docs/diagramas/09-diagrama-implantacao.png) |

---

## 🧪 Testes

### Testes Unitários e de Integração

Testes planejados para uma futura implementação:

- regras de validade e baixa de estoque;
- permissões de dono, editor e leitor;
- persistência e transações;
- contratos dos endpoints REST.

### Testes End-to-End (E2E)

Cenários planejados:

- cadastrar ingrediente;
- receber alerta de vencimento;
- sugerir e preparar receita;
- gerar lista de compras;
- compartilhar despensa.

Na entrega atual, a validação realizada consiste na renderização dos 12 arquivos PlantUML e na revisão visual do documento Word.

---

## 🔗 Documentações utilizadas

- [Template README da disciplina](https://github.com/joaopauloaramuni/laboratorio-de-desenvolvimento-de-software/blob/main/TEMPLATES/template_README.md)
- [PlantUML](https://plantuml.com/)
- [C4 Model](https://c4model.com/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [React](https://react.dev/)
- [PostgreSQL](https://www.postgresql.org/docs/)
- [Docker](https://docs.docker.com/)

---

## 👥 Autores

| Autor | Responsabilidade |
|---|---|
| Pedro Henrique | Requisitos, arquitetura, documentação e diagramas PlantUML |

---

## 🤝 Contribuição

Este é um trabalho acadêmico individual. Alterações devem preservar o template obrigatório e manter os códigos PlantUML sincronizados com as imagens renderizadas.

---

## 🙏 Agradecimentos

Agradecimento ao Prof. Dr. João Paulo Aramuni pelos templates disponibilizados para a atividade.

---

## 📄 Licença

Distribuído sob a licença MIT. Consulte [LICENSE](LICENSE).

<p align="center">
  <img src="assets/readme/foodstack_encerramento_animado.svg" alt="Encerramento animado do FoodStack" width="88%"/>
</p>
