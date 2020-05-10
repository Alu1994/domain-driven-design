# Aggregates

## O que são Aggregates?
Aggregates é o agrupamento de Entidades e Value Objects que juntos são uma unidade do negócio, que precisam ser tratados em conjunto para alterações no sistema. E para fazer essas alterações é preciso verificar a consistencia de todos os membros desse Aggregate.

## Aggregate Root
Aggregate Root é o objeto pai de todos os objetos de um determinado Aggregate, assim, todo Aggregate deve ter um Aggregate Root.
- É possível ter somente 1 objeto dentro de um Aggregate, e esse objeto será o pai, o próprio Aggregate Root.
