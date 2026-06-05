# ADR 0003 – Modelo de Comunicação

## Status

Aceita

## Contexto

A Fintech Wallet possui operações que exigem resposta imediata e outras que podem ocorrer em segundo plano.

## Problema Arquitetural

Qual modelo de comunicação oferece melhor equilíbrio entre desempenho e desacoplamento?

## Alternativas Consideradas

### Apenas REST

Vantagens:

* Simplicidade.

Desvantagens:

* Forte acoplamento entre serviços.

### Apenas Mensageria

Vantagens:

* Alto desacoplamento.

Desvantagens:

* Maior complexidade.

### Modelo Híbrido (Escolhida)

Vantagens:

* Equilíbrio entre desempenho e escalabilidade.

## Decisão

Utilizar REST para operações síncronas e RabbitMQ para processamento assíncrono.

## Consequências

Benefícios:

* Resposta rápida ao usuário.
* Melhor escalabilidade.

Trade-offs:

* Maior complexidade de implementação.

## Referências

NEWMAN, Sam. Building Microservices. 2021.
