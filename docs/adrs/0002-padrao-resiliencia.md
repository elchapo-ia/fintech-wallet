# ADR 0002 – Padrões de Resiliência

## Status

Aceita

## Contexto

A Fintech Wallet depende de APIs bancárias, serviços de autenticação e gateways de pagamento externos.

## Problema Arquitetural

Como evitar que falhas externas comprometam todo o sistema?

## Alternativas Consideradas

### Retry Simples

Vantagens:

* Fácil implementação.

Desvantagens:

* Pode aumentar a sobrecarga dos serviços.

### Circuit Breaker (Escolhida)

Vantagens:

* Evita chamadas repetidas para serviços indisponíveis.
* Impede propagação de falhas.

Desvantagens:

* Maior complexidade arquitetural.

## Decisão

Implementar API Gateway e Circuit Breaker para aumentar a resiliência do sistema.

## Consequências

Benefícios:

* Maior disponibilidade.
* Melhor tolerância a falhas.

Trade-offs:

* Necessidade de monitoramento.
* Complexidade adicional.

## Referências

NYGARD, Michael. Release It! 2018.
