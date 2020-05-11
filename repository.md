# Repository

## O que é Repository?
É um Design Pattern que nos auxilia a gerenciar o acesso à leitura, escrita e remoção de dados, independente do tipo de reposório que estejamos lidando. (banco de dados, arquivo, cache e etc.)

Esses repositórios devem ser criados apenas para Aggregate Roots, eles não podem ser criados para simples entidades, pois o foco dos Repositórios no DDD são os Aggregate Roots.

Toda a regra de acesso à dados deve ficar na camada de repositório e não em qualquer outra camada.

Repositórios provem uma abstração boa para as complexidades técnicas da persistencia dos dados.

Auxilia na separação de responsabilidades, pois é uma camada que tem responsabilidade direta no acesso à dados, possibilitando que outras camadas cuidem daquilo que fazem sentido à elas, ajudando assim, por consequencia na manutenabilidade do código, bem como também em teste de código.

Uma interface de repositório(IRepository<T>) traz o controle daquilo que de fato faz sentido ser exposto para as camadas de negócio e aplicação. Lembrando que nem todos os casos faz sentido utilizar uma interface com todas as operações basicas de um banco de dados.
