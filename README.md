# Comolatti Sales Orchestrator

Plataforma corporativa de orquestracao de vendas B2B do Grupo Comolatti.

Responsavel por integrar canais digitais, inteligencia conversacional, ERP, estoque, pricing, logistica e pagamentos em uma experiencia unica de compra para clientes corporativos.

---

# Visao Estrategica

O Sales Orchestrator atua como camada central de negocio entre os canais de atendimento e os sistemas corporativos, desacoplando regras comerciais dos sistemas legados e permitindo evolucao continua da operacao.

A plataforma foi concebida para suportar:

* Omnichannel Commerce
* Conversational Commerce
* Inteligencia Artificial
* Escalabilidade Horizontal
* Arquitetura Orientada a Eventos
* Integracao com SAP
* Marketplace B2B
* Observabilidade Corporativa

---

# Objetivos de Negocio

* Reduzir atrito na jornada de compra B2B.
* Aumentar conversao de pedidos.
* Melhorar giro de estoque.
* Centralizar regras comerciais.
* Diminuir dependencia de sistemas legados.
* Habilitar canais digitais escalaveis.

---

# Dominios de Negocio

## Identity Domain

Responsavel pela identificacao e contextualizacao do cliente.

### Capacidades

* Identificacao por CNPJ
* Autenticacao
* Carteira de Vendas
* Politica Comercial
* Centro de Distribuicao
* Perfil de Credito

---

## Catalog Domain

Responsavel pela consulta de produtos.

### Capacidades

* Busca por descricao
* Busca por codigo
* Busca multimodal
* Upload de Excel
* Upload de PDF
* Normalizacao de catalogo
* input via foto

---

## Inventory Domain

Responsavel pela disponibilidade.

### Capacidades

* Consulta de estoque
* Reserva de itens
* Distribuicao por CD
* Priorizacao logistica

---

## Pricing Domain

Responsavel pela precificacao.

### Capacidades

* Preco por carteira
* Tabelas comerciais
* Promocoes
* Campanhas
* Cashback

---

## Checkout Domain

Responsavel pela geracao do pedido.

### Capacidades

* PIX
* Boleto
* Credito Comercial
* Cashback
* Garantias

---

## Order Domain

Responsavel pelo ciclo de vida do pedido.

### Capacidades

* Criacao
* Aprovacao
* Faturamento
* Expedicao
* Entrega

---

# Arquitetura Corporativa

```text
Cliente B2B
        |
        v
WhatsApp / App / Portal / Vendedor
        |
        v
API Gateway
        |
        v
Sales Orchestrator
        |
 +------+------+------+------+------+
 |      |      |      |      |
 v      v      v      v      v
Identity Catalog Inventory Pricing Checkout
        |
        v
Event Bus
        |
 +------+-------------+
 |                    |
 v                    v
SAP              Data Lake
```

---

# Principios Arquiteturais

## API First

Toda funcionalidade deve ser disponibilizada atraves de APIs.

## Domain Driven Design (DDD)

Separacao clara dos dominios de negocio.

## Event Driven Architecture

Integracoes desacopladas atraves de eventos.

## Cloud Native

Preparado para execucao em Kubernetes.

## Observability First

Monitoramento desde a origem.

---

# Stack Tecnologica

## Backend

* Node.js
* NestJS
* TypeScript

## Integracao

* REST
* GraphQL
* Webhooks

## Mensageria

* Apache Kafka
* RabbitMQ

## Banco de Dados

* PostgreSQL
* Redis

## Observabilidade

* OpenTelemetry
* Grafana
* Prometheus

## Cloud

* AWS
* Azure

---

# Estrutura do Projeto

```text
src
├── domains
│   ├── identity
│   ├── catalog
│   ├── inventory
│   ├── pricing
│   ├── checkout
│   └── orders
│
├── shared
│
├── integrations
│   ├── sap
│   ├── payments
│   └── logistics
│
├── events
│
└── orchestrator

test
.github
docs
```

---

# Roadmap

## MVP

* Login por CNPJ
* Busca multimodal
* Consulta de estoque
* Checkout PIX
* Checkout Boleto

## Fase 2

* Historico de pedidos
* Rastreamento de entregas
* Cashback
* Credito Comercial

## Fase 3

* IA Conversacional
* Recomendacoes inteligentes
* Cross Sell
* Up Sell
* Agentes de IA

## Fase 4

* Marketplace B2B
* Ecossistema de parceiros
* APIs publicas

---

# Qualidade

Validacoes automaticas executadas em:

* Pull Request
* Merge
* Release

Cobertura minima:

* Unit Tests
* Integration Tests
* Contract Tests

---

# Licenca

Uso interno do Grupo Comolatti.

Todos os direitos reservados.
