# Repository

## O que é um Repository?
É um Design Pattern que nos auxilia a gerenciar o acesso à leitura, escrita e remoção de dados, independente do tipo de reposório que estejamos lidando (banco de dados, arquivo, cache e etc.).

Assim toda a regra de acesso à dados deve ficar na camada de repositório e não em qualquer outra camada.

## Para que tipo de objeto devo criar um Repository?
Em DDD os repositórios devem ser criados apenas para Aggregate Roots, eles não podem ser criados para simples entidades, pois o foco está no life cycle de uma operação transacional do Aggregate, onde todos os objetos pertencentes à ele só fazem sentido dado um determinado Aggregate Root.


## Prós :) e Contras :( em utilizar uma camada de Repository
### Prós
- O Repository auxilia na separação de responsabilidades, pois é uma camada que tem como atividade principal o acesso à dados, possibilitando que outras camadas cuidem daquilo que fazem sentido à elas, ajudando assim por consequencia, na manutenabilidade do código, bem como em testes de código.

- Repositórios provem uma abstração boa para as complexidades técnicas da persistencia de dados.

- Uma interface de repositório(IRepository<T>) traz o controle daquilo que de fato faz sentido ser exposto para as camadas de negócio e aplicação. 
  
Obs:
  Lembrando que nem todos os casos faz sentido utilizar uma interface com todas as operações basicas de um banco de dados.
  
### Contras
- Exige que todos do time estejam comprados com a ideia de introduzir mais uma camada ao projeto.

- Exige que os integrantes do time saibam como deve ser implementado essa camada, o que pode e o que não pode ser feito nela.
