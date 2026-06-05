# Fintech Wallet

## Visão Executiva

A Fintech Wallet é uma plataforma financeira digital desenvolvida para gerenciamento de contas, consulta de saldo, realização de transferências e acompanhamento de transações financeiras.

Na Fase 2 do projeto foi adotada a Arquitetura Hexagonal (Ports & Adapters) para garantir o isolamento das regras de negócio. Na Fase 3, a arquitetura evoluiu para um modelo baseado em Microsserviços e Computação em Nuvem, visando escalabilidade, resiliência e alta disponibilidade.

---

## Diagrama C4 - Containers

```mermaid
flowchart LR

User[Usuário]

Gateway[API Gateway]

Account[Account Service]
Wallet[Wallet Service]
Transaction[Transaction Service]
Notification[Notification Service]

DB1[(PostgreSQL Accounts)]
DB2[(PostgreSQL Wallet)]
DB3[(PostgreSQL Transactions)]

RabbitMQ[RabbitMQ]

User --> Gateway

Gateway --> Account
Gateway --> Wallet
Gateway --> Transaction

Account --> DB1
Wallet --> DB2
Transaction --> DB3

Transaction --> RabbitMQ
RabbitMQ --> Notification
```

---

## ADRs

- [ADR 0001 - Estratégia de Nuvem](docs/adrs/0001-estrategia-nuvem.md)
- [ADR 0002 - Padrão de Resiliência](docs/adrs/0002-padrao-resiliencia.md)
- [ADR 0003 - Modelo de Comunicação](docs/adrs/0003-modelo-comunicacao.md)

---

## SAD

- [SAD Fase 3](docs/sad/sad-fase3.md)

---

## Tecnologias

- Java Spring Boot
- PostgreSQL
- Docker
- RabbitMQ
- API Gateway
- REST APIs

---

## Execução do Projeto

```bash
docker-compose up -d
```
