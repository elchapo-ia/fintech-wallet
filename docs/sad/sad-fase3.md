# Software Architecture Document (SAD) – Fase 3

## Visão Geral

A Fintech Wallet é uma plataforma financeira digital destinada ao gerenciamento de contas, consultas de saldo, transferências e histórico financeiro.

A arquitetura evoluiu de Arquitetura Hexagonal para uma arquitetura baseada em Microsserviços executados em ambiente de nuvem.

## Objetivos Arquiteturais

* Escalabilidade
* Alta disponibilidade
* Resiliência
* Segurança
* Facilidade de manutenção

## Microsserviços

### Account Service

Responsável por:

* Cadastro de usuários
* Gestão de contas

### Wallet Service

Responsável por:

* Controle de saldo
* Carteira digital

### Transaction Service

Responsável por:

* Transferências
* Extrato financeiro

### Notification Service

Responsável por:

* Envio de notificações
* Confirmações de transações

## Comunicação

Síncrona:

* REST API

Assíncrona:

* RabbitMQ

## Persistência

Cada microsserviço possui seu próprio banco de dados PostgreSQL.

## Segurança

* Autenticação baseada em tokens.
* Comunicação protegida por HTTPS.

## Tecnologias

* Java Spring Boot
* Docker
* PostgreSQL
* RabbitMQ
* API Gateway

## Conclusão

A adoção de Microsserviços e Computação em Nuvem proporciona maior escalabilidade, disponibilidade e resiliência para a Fintech Wallet, mantendo os princípios de isolamento do domínio definidos na Arquitetura Hexagonal da Fase 2.
