# Aggregates

## O que são Aggregates?
Aggregates é o agrupamento de Entidades e Value Objects que juntos são uma unidade do negócio, que precisam ser tratados em conjunto para alterações no sistema. 
- Para fazer essas alterações é preciso verificar a consistencia de todos os membros desse Aggregate.

## Aggregate Root
Aggregate Root é o objeto pai de todos os objetos de um determinado Aggregate, assim, todo Aggregate deve ter um Aggregate Root.
- É possível ter somente 1 objeto dentro de um Aggregate, e esse objeto será o pai, o próprio Aggregate Root.

## Alterações em um Aggregate
Quando trabalhamos com um Aggregate, as alterações dentro dele devem ser feitas pensando em uma linha de produção de um determinado produto, se esse produto é composto de **_N_** itens, esses itens só fazem sentido juntos, para que assim possam formar o produto final, para que isso seja possível em um software é necessário que essas alterações sejam feitas como uma transação, onde só faz sentido commitar aquela operação, caso todas as peças estejam alinhadas com o necessário para o produto final daquela operação.

Por isso, alterações feitas em um Aggregate devem seguir **_ACID_**:
  - Atomicidade
  - Consistência
  - Isolamento
  - Durabilidade
