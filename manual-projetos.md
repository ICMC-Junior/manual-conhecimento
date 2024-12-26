# Manual de Conhecimento - ICMC Júnior

## Sumário

1.  [1.1 Docker e Containers](#11-docker-e-containers)
    1.  [1.1.1 Docker na Prática](#111-docker-na-pratica)
    2.  [1.1.2 Docker para Desenvolvimento](#112-docker-para-desenvolvimento)
    3.  [1.1.3 Docker para Produção](#113-docker-para-producao)
    4.  [1.1.4 Containers Deep Dive](#114-containers-deep-dive)
2.  [1.2 APIs: Design, REST, gRPC e API Gateway](#12-apis-design-rest-grpc-e-api-gateway)
    1.  [1.2.1 REST e Níveis de Maturidade na Prática](#121-rest-e-niveis-de-maturidade-na-pratica)
    2.  [1.2.2 gRPC](#122-grpc)
    3.  [1.2.3 Design de APIs](#123-design-de-apis)
    4.  [1.2.4 API Gateway](#124-api-gateway)
3.  [1.3 Testes automatizados](#13-testes-automatizados)
    1.  [1.3.1 TDD - Test Driven Development](#131-tdd---test-driven-devolopment)
    2.  [1.3.2 Testes avançados: Padrões, tipos e ferramentas](#132-testes-avancados-padroes-tipos-e-ferramentas)
    3.  [1.3.3 Testcontainers](#133-testcontainers)
4.  [1.4 SOLID e Design Patterns](#14-solid-e-design-patterns)
    1.  [1.4.1 SOLID na Prática - Princípios e Aplicações em Design de Software](#141-solid-na-pratica---principios-e-aplicacoes-em-design-de-software)
    2. [1.4.2 SOLID na Prática - Princípios e Aplicações em Design de Software](#142-solid-na-pratica---principios-e-aplicacoes-em-design-de-software-2)
    3. [1.4.3 Design Patterns na Prática - Gang of Four e Aplicações Reais](#143-design-patterns-na-pratica---gang-of-four-e-aplicacoes-reais)
5.  [1.5 Arquitetura MVC, Hexagonal, Clean Archtecture e MultiTenancy](#15-arquitetura-mvc-hexagonal-clean-archtecture-e-multitenancy)
    1. [1.5.1 Arquitetura em Camadas MVC](#151-arquitetura-em-camadas-mvc)
    2. [1.5.2 Arquitetura Hexagonal e Clean Archtecture](#152-arquitetura-hexagonal-e-clean-archtecture)
    3.  [1.5.3 Arquitetura Multi-Tenancy](#153-arquitetura-multi-tenancy)
6.  [1.6 Domain Driven Design, Microsserviços e mensageria](#16-domain-driven-design-microsservicos-e-mensageria)
    1.  [1.6.1 Domain-Driven Design (DDD)](#161-domain-driven-design-ddd)
    2.  [1.6.2 Domain-Driven Design e Arquitetura baseada em eventos](#162-domain-driven-design-e-arquitetura-baseada-em-eventos)
    3.  [1.6.3 RabbitMQ](#163-rabbitmq)
    4.  [1.6.4 Arquitetura baseada em microsserviços](#164-arquitetura-baseada-em-microsservicos)
    5.  [1.6.5 Apache Kafka](#165-apache-kafka)
7. [1.7 Sistemas legados e monólitos: Modernização e decomposição](#17-sistemas-legados-e-monolitos-modernizacao-e-decomposicao)
    1. [1.7.1 Criação de monolitos modulares](#171-criacao-de-monolitos-modulares)
    2. [1.7.2 Modernização de sistemas legados](#172-modernizacao-de-sistemas-legados)
    3. [1.7.3 Decomposição de sistemas monolíticos para microsserviços](#173-decomposicao-de-sistemas-monoliticos-para-microsservicos)
8. [2. DevOps e SRE](#2-devops-e-sre)
    1. [2.1 Kubernetes, Pipelines CI/CD e Infra as Code](#21-kubernetes-pipelines-cicd-e-infra-as-code)
        1. [2.1.1 Kubernetes](#211-kubernetes)
        2. [2.1.2 Helm](#212-helm)
        3. [2.1.3 Terraform](#213-terraform)
        4. [2.1.4 Pipelines, GitOps e ArgoCD](#214-pipelines-gitops-e-argocd)
    2. [2.2 SRE, Monitoramento e Observabilidade](#22-sre-monitoramento-e-observabilidade)
        1. [2.2.1 Observabilidade](#221-observabilidade)
        2.  [2.2.2 Prometheus e Grafana](#222-prometheus-e-grafana)
        3.  [2.2.3 OpenTelemetry](#223-opentelemetry)
        4.  [2.2.4 Site Reliability Engineering](#224-site-reliability-engineering)
    3. [2.3 DevSecOps na Prática](#23-devsecops-na-pratica)
9.  [3. Banco de dados](#3-banco-de-dados)
    1. [3.1 SQL](#31-sql)
        1. [3.1.1 PosgreeSQL para desenvolvedores](#311-posgreesql-para-desenvolvedores)
        2. [3.1.2 MySQL para desenvolvedores](#312-mysql-para-desenvolvedores)
    2. [3.2 NoSQL](#32-nosql)
        1.  [3.2.1 MongoDB para desenvolvedores](#321-mongodb-para-desenvolvedores)
        2.  [3.2.2 Redis para desenvolvedores](#322-redis-para-desenvolvedores)
10. [4. Segurança](#4-seguranca)
    1. [4.1 Autenticação e autorização: Tokens JWT, ACL e RBAC](#41-autenticacao-e-autorizacao-tokens-jwt-acl-e-rbac)
    2. [4.2 Keycloak: o Auth2, OpenID Connect e Single Sign-On](#42-keycloak-o-auth2-openid-connect-e-single-sign-on)
    3.  [4.3 OWASP 10, Segurança de APIs e Secret Management (Vault)](#43-owasp-10-seguranca-de-apis-e-secret-management-vault)

---
### 1.1 Docker e Containers
<a id="11-docker-e-containers"></a>

### 1.1.1 Docker na Prática
<a id="111-docker-na-pratica"></a>

Este guia detalha o uso prático do Docker para desenvolvimento e orquestração de aplicações. Ele abrange desde os fundamentos até configurações avançadas, com exemplos de comandos e organização de projeto.

### Fundamentos e Configuração do Docker
<a id="fundamentos-e-configuracao-do-docker"></a>

### Conceitos básicos e arquitetura do Docker
-   **Docker Engine:** É o módulo principal do Docker, responsável por criar e gerenciar containers. Ele funciona como o "motor" do sistema de containers.
-   **Docker Images:** São modelos prontos que contêm o sistema operacional e as aplicações necessárias. Servem como base para criar containers.
-   **Containers:** São instâncias de imagens em execução. Eles isolam o ambiente da aplicação, garantindo consistência e independência do sistema hospedeiro.
-   **Docker CE vs Docker Desktop:**
    -   **Docker CE** (Community Edition): Versão voltada para servidores e ambientes Linux. É gratuita e de código aberto, ideal para ambientes de produção e servidores, com foco em linha de comando e configuração manual.
    -   **Docker Desktop:** Versão para desktops (Windows e macOS), com interface gráfica integrada e suporte adicional. Oferece uma experiência mais amigável para desenvolvedores, com recursos como interface gráfica, Kubernetes integrado e atualizações automáticas.

### Instalação do Docker
1.  Baixe e instale o Docker Desktop pelo site oficial ([docker.com](https://www.docker.com/)).
2.  Verifique a instalação:
    ```bash
    docker --version
    ```

### Configuração inicial
1.  Inicie o Docker Desktop.
2.  Configure recursos como CPUs e memória em **Settings > Resources** para ajustar o desempenho conforme o hardware.

### Principais comandos para gerenciamento
-   **Listar containers ativos**: Mostra containers em execução no momento.
    ```bash
    docker ps
    ```
-   **Listar todos os containers**: Inclui containers parados.
    ```bash
    docker ps -a
    ```
-   **Iniciar um container**: Inicia um container previamente criado.
    ```bash
    docker start <container_id>
    ```
-   **Parar um container**: Finaliza a execução de um container.
    ```bash
    docker stop <container_id>
    ```
-   **Remover um container**: Deleta um container.
    ```bash
    docker rm <container_id>
    ```

### Imagens e Build de Containers
<a id="imagens-e-build-de-containers"></a>

### O que são imagens Docker?
As imagens Docker são "blueprints" que contêm tudo o que é necessário para rodar uma aplicação, como bibliotecas, dependências e código-fonte. Elas são imutáveis, garantindo consistência entre ambientes.

### Criação de imagens com Dockerfile
O **Dockerfile** é um arquivo de texto que define os passos para criar uma imagem. Exemplo:
```dockerfile
# Usar uma imagem base
FROM node:16

# Configurar diretório de trabalho
WORKDIR /app

# Copiar arquivos
COPY package*.json ./

# Instalar dependências
RUN npm install

# Copiar código-fonte
COPY . .

# Expõe a porta
EXPOSE 3000

# Comando para iniciar a aplicação
CMD ["npm", "start"]
```
### Comandos e Funções

- **FROM**: Define a imagem base (neste caso, Node.js).
- **WORKDIR**: Define o diretório de trabalho.
- **COPY**: Copia arquivos do host para o container.
- **RUN**: Executa comandos no container durante a construção.
- **EXPOSE**: Declara a porta usada pelo container.
- **CMD**: Define o comando padrão ao iniciar o container.

### Construindo Imagens

```bash
docker build -t minha-imagem:1.0 .
```

- `-t`: Nomeia a imagem.

### Executando um Container

```bash
docker run -d -p 3000:3000 minha-imagem:1.0
```

- `-d`: Executa em segundo plano.
- `-p`: Mapeia portas (host:container).

---

## Multistage Builds

Permite criar imagens menores e mais seguras ao separar as etapas de build e execução.

### Exemplo:

```dockerfile
# Etapa 1: Build
FROM node:16 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Etapa 2: Execução
FROM nginx:alpine
COPY --from=builder /app/build /usr/share/nginx/html
```

- **AS builder**: Define um nome para a etapa.
- **COPY --from=builder**: Copia arquivos da etapa anterior.

---

## Volumes e Redes

### Volumes

Volumes são usados para persistir dados gerados e utilizados pelos containers.

### Criar um Volume

```bash
docker volume create meu-volume
```

### Usar um Volume

```bash
docker run -d -v meu-volume:/dados busybox
```

### Redes

As redes permitem comunicação entre containers ou entre containers e o host.

### Listar Redes

```bash
docker network ls
```

### Criar uma Rede

```bash
docker network create minha-rede
```

### Conectar um Container a uma Rede

```bash
docker network connect minha-rede <container_id>
```

---

## Docker Compose e Orquestração Local

Docker Compose é uma ferramenta para definir e gerenciar aplicações multicontainer.

### Exemplo de Serviço Multicontainer

```yaml
version: '3.8'
services:
  app:
    build: .
    ports:
      - "3000:3000"
    volumes:
      - .:/app
    depends_on:
      - db
  db:
    image: postgres:13
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
      POSTGRES_DB: mydb
    volumes:
      - db_data:/var/lib/postgresql/data
volumes:
  db_data:
```

- **services**: Define os containers e suas configurações.
- **depends_on**: Indica dependências entre serviços.
- **volumes**: Define volumes persistentes.

### Comandos Úteis

- **Subir serviços:**

```bash
docker-compose up
```

- **Subir em segundo plano:**

```bash
docker-compose up -d
```

- **Parar serviços:**

```bash
docker-compose down
```

---

## Publicação e Gerenciamento de Imagens em Registries

Registries são repositórios onde imagens Docker são armazenadas e compartilhadas. O mais comum é o Docker Hub.

### Login no Docker Hub

```bash
docker login
```

### Publicar uma Imagem

```bash
docker tag minha-imagem:1.0 meu-usuario/minha-imagem:1.0
docker push meu-usuario/minha-imagem:1.0
```

### Baixar uma Imagem

```bash
docker pull meu-usuario/minha-imagem:1.0
```

---

## Recursos e Ferramentas Adicionais no Docker Desktop

Permite criar, iniciar ou parar containers diretamente pelo painel do Docker Desktop, simplificando o uso.

### Detectar Vulnerabilidades

```bash
docker scout cves minha-imagem:1.0
```

O Docker Desktop também pode habilitar o Kubernetes para orquestração de containers.

### Ativar Kubernetes

1. Acesse **Settings > Kubernetes**.
2. Verifique o status:

```bash
kubectl get nodes
```

---

## Estrutura de Projeto

Organize seu projeto para facilitar o gerenciamento:

```
projeto/
├── Dockerfile
├── docker-compose.yml
├── src/
│   ├── index.js
│   ├── app.js
├── package.json
├── .env
```

- **Dockerfile**: Define como criar a imagem.
- **docker-compose.yml**: Define serviços.
- **src/**: Código-fonte da aplicação.
- **.env**: Armazena variáveis de ambiente sensíveis.
