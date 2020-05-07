# Domain

## O que é?
A camada de domínio é o coração do negócio dentro de um sistema, ela é responsável por representar os conceitos do negócio, estado e suas regras. O estado que reflete a regra de negócio é controlada nessa camada, apesar dos detalhes técnicos de guardar esses mesmos dados estarem em uma camada de Repositório.

## Modelos de Dominio _Anemico_ x Modelos de Dominio _Rico_

### Dominio Anemico

Um modelo de dominio anemico tem seu foco nos estados dos objetos, que vai contra as intenções do DDD, nele modelos anemicos são considerados "Anti-Patterns".

Vale dizer que, não há problemas em ter um domínio anemico, principalmente se a intenção for fazer somente um sistema que possui _CRUDs_.

### Dominio Rico

Um dominio rico é a ideia de ter o controle do negócio, e não apenas o estado. Por vezes tiramos essas regras que pertencem ao Domínio e colocamos em serviços externos, enfraquecendo-o e tirando parte de sua responsabilidade.
