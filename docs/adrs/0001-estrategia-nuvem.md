# ADR 0001 – Estratégia de Nuvem e Escalabilidade

## Status

Aceita

## Contexto

A Fintech Wallet executa operações financeiras críticas, como transferências, consultas de saldo e registro de transações. Com o crescimento do número de usuários, torna-se necessário garantir escalabilidade, disponibilidade e facilidade de manutenção.

## Problema Arquitetural

Como garantir crescimento da plataforma sem comprometer desempenho e disponibilidade?

## Alternativas Consideradas

### IaaS

Vantagens:

* Controle total da infraestrutura.

Desvantagens:

* Necessidade de administração dos servidores.
* Maior custo operacional.

### PaaS (Escolhida)

Vantagens:

* Implantação simplificada.
* Escalabilidade automática.
* Menor esforço operacional.

Desvantagens:

* Menor controle sobre a infraestrutura.

### Serverless

Vantagens:

* Pagamento sob demanda.

Desvantagens:

* Possibilidade de Cold Start.
* Menor previsibilidade para sistemas financeiros.

## Decisão

Foi adotada uma estratégia baseada em PaaS com escalabilidade horizontal através de containers.

## Consequências

Benefícios:

* Alta disponibilidade.
* Escalabilidade automática.
* Redução do esforço operacional.

Trade-offs:

* Dependência do provedor de nuvem.
* Menor controle sobre recursos físicos.

## Referências

MARTIN, Robert C. Clean Architecture. 2017.

RICHARDS, Mark. Fundamentals of Software Architecture. 2020.
