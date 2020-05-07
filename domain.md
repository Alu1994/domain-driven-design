# Domain

## O que é?
A camada de domínio é o coração do negócio dentro de um sistema, ela é responsável por representar os conceitos do negócio, estado e suas regras. O estado que reflete a regra de negócio é controlada nessa camada, apesar dos detalhes técnicos de guardar esses mesmos dados estarem em uma camada de Repositório.

## Modelos de Dominio _Anemico_ x Modelos de Dominio _Rico_

### Dominio Anemico
Um modelo de dominio anemico tem seu foco nos estados dos objetos, que vai contra as intenções do DDD, nele modelos anemicos são considerados "Anti-Patterns".

Vale dizer que, não há problemas em ter um domínio anemico, principalmente se a intenção for fazer somente um sistema que possui _CRUDs_.

### Dominio Rico
Um dominio rico é a ideia de ter o controle do negócio, e não apenas o estado. Por vezes tiramos essas regras que pertencem ao Domínio e colocamos em serviços externos, enfraquecendo-o e tirando parte de sua responsabilidade.


## Entities
No DDD temos 2 tipos de objetos, aqueles que são definidos por seus Valores, e aqueles definidos por sua Identidade. Esses objetos definidos por sua identidade são chamados de **Entidades**.

Uma Entidade é algo que precisamos rastrear, localizar, recuperar e armazenar, fazemos isso com um ID.

As propriedades que compõem uma entidade podem mudar portanto não podemos usar essas mesmas propriedades para identificar essa entidade, pora isso usamos seu ID.

Em DDD normalmente os IDs são _Guids_, para facilitar testes e implementações, porém int's não ferem nenhum principio de DDD, apenas tornam as coisas um pouco mais dificeis.

### Entity & SRP (Single Responsability Principle)
É importante termos uma entidade que possua sim seus comportamentos, porém é importante levarmos em consideração a quantidade de responsabilidades e se todas fazem mesmo parte de uma determinada entidade.

Segundo Eric Evans, as responsabilidades de uma entidade são a sua identidade e seu ciclo de vida. Mas mesmo nesses casos, quando sua regra fica muito complexa, talvez seja interessante delegar essas responsabilidades para serviços ou até mesmo _Value Objects_.

### Entity & Equality Comparer
Quando falamos sobre entidades, normalmente não faz muito sentido termos um comparador (Equals), pois comparar duas entidades é mais complexo do que comparar 2 _Value Objects_. Precisamos de muitas informações para de fato cravarmos que uma entidade se assemelha ou é de fato a mesma, e também se realmente essa pergunta faz sentido, será que precisamos realmente saber se 2 entidades são iguais ou se assemelham? Isso pode variar dependendo da situação, mas normalmente não faz muito sentido.

## Relationships
Normalmente quando definimos relacionamentos, pensamos de forma bidirecional, por exemplo:
  - 1 Carro tem 1 Dono
  - 1 Dono possui 1 Carro

Não está errado pensar assim, mas quando implementamos essa regra no código, normalmente as coisas ficam um pouco mais complexas, fora que normalmente leva-nos a pensar que, um objeto dentro de um sistema não existe ou não faz sentido sem o outro, o que não é a verdade.

