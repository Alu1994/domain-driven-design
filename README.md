# Domain Driven Design

## O que é DDD?

Domain Driven Design é um conjunto de principios e padrões que nos ajudam a resolver problemas complexos de negócio em softwares bem escritos. Possibilita criar um código claro e testavel que represente um domínio de negócio.

## Visão Geral
- DDD tem como missão não só facilitar a escrita do código, mas muito mais em entender a verdadeira necessidade do cliente para dai então, utilizando desenvolvimento de software como uma ferramenta, resolvermos seus problemas.
- A interação com os **Domain Experts** é extremamente importante para a entrega de um software, especialmente quando utilizamos DDD. Essas são as pessoas que vivem e respiram o negócio e os processos dia a dia, são para elas que nós desenvolvemos os softwares. Ao conversar com um especialista, normalmente utilizamos termos técnicos não relacionados ao domínio de negócio ou até presumimos ações a serem feitas baseados em alguns requisitos de negócio, complicando assim a comunicação e o desenvolvimento correto do projeto.
- Um outro ponto importante é modelar um grande problema em Sub Dominios(**Sub-Domain**), por vezes quando recebemos uma necessidade de desenvolvimento complexa, acabamos atacando os problemas de vez sem antes pensarmos por exemplo, em sub-divisões, o que ao longo do tempo se torna complicado de manter/desenvolver, e o valor para que isso tudo seja mantido será gradualmente mais alto. Então, será que faz sentido tratarmos tudo junto? Não poderiamos tratar assuntos especificos separadamente? Separar esses pequenos assuntos por equipes com suas soluções tecnicas e de negócio especificas para este problema seria muito menos doloroso, realmente dividindo para conquistar.
- Ao implementar Sub-Dominios é importante ter em mente _separation of concerns_ que é você dividir as responsabilidades de forma bem clara, um sub-dominio deve se preocupar somente com aquilo que faz sentido à ele, que são as regras do negócio. Interações com infraestrutura, bases de dados e outros, devem ser tratados separadamente.

## Prós :) e Contras :( em usar DDD
### Prós
- DDD nos ajuda a dividir um super problema em problemas menores(**Sub-Domain**) que facilita o entendimento bem como o seu processo de desenvolvimento, o que o torna também mais flexivel.
- Torna a solução final mais próxima da visão de negócios do cliente. Entregando um caminho para problemas **complexos**.
- Normalmente o código é bem organizado e facilmente testavel.
- A regra de negócio fica somente em um único lugar.
- Mesmo não utilizando totalmente DDD, existem alguns padrões que podem beneficiar o desenvolvimento das nossas aplicações.

### Contras
- Um dos pontos negativos do DDD é o **Tempo e Esforço**, é necessário muitas discussões com _**Domain Experts**_ para entender de fato o Modelo do sistema e todos os problemas à serem resolvidos. Junto a isolar as regras do domínio separando-as de outras partes da aplicação.
- A **curva de aprendizado** é longa, existem muitos principios, padrões e processos que vão exigir estudo, dedicação e muito comprometimento.
- DDD só faz sentido quando o objetivo é solucionar problemas de **negócio** complexos, não apenas CRUD.
- O time tem de estar comprado com a prática de DDD.





## Ubiquitous Language ou Linguagem onipresente
É a criação de termos que normalmente serão usados ao discutir um subdomínio especifico, termos esses que vem dos problemas à serem solucionados, que são do négocio em si e não de questões técnicas, para termos uma comunicação clara entre todos os envolvidos no projeto.

Esses termos devem ser acordados com toda a equipe bem como com o cliente, para que não haja mal entendidos.

É claro que exige um esforço maior para decidir os termos e difundi-los, porém a vantagem é que, por exemplo, não haverá necessidade de tradução entre os termos do cliente e os termos do desenvolvedor.

## Model Driven Design
É uma verificação intensa do problema, esse processo deve ser realizado em conjunto aos **Domains Experts**, para poder identificar o **Core Domain** e os subdomínios.

## Domain Experts
São pessoas que conhecem de fato as necessidades à serem supridas, que conhecem os problemas, e nos auxiliam a entender esses mesmos problemas e trazer eles de forma limpa e coerente para o mundo do software.

## Bounded Context
É a limitação dos subdomínios à serem desenvolvidos, é o foco no desenvolvimento de um subdomínio especifico. Ao identificar um Bonded Context será possível identificar *Entities*, *ValueObjects*, *Aggregates*, *Domain Events*, *Repository* e outros, bem como a interação entre eles.

Tendo sua separação de forma bem clara, não haverá confusão entre outros subdomínios, evitando a sobreposição de atributos, funcionalidades e outros. E evitando também um grande sistema complexo que deverá gerenciar todo o negócio.

## Sub-Domain x Bounded Context

A diferença entre subdominio e bounded context é que:
- O Subdominio é como o problema a ser solucionado foi subdividido.
- Bounded context é como esse mesmo problema foi sulucionado e subdividido em termos de software, tecnicamente falando.
Seria sempre bom que os 2 fossem correspondentes, mas nem sempre isso é atingido. A ideia é que o bounded context seja criado para atender perfeitamente o subdominio.


## Context Maps
Como o nome diz, é o mapeamento dos contextos que devemos fazer para manter a devida organização dos projetos, e os relacionamentos entre si.

Quando trabalhamos com *bounded contexts*, esbarramos por vezes em necessidades que são compartilhadas entre os projetos, como pedaços de uma mesma entidade(Cliente), o que normalmente é feito é criar um super projeto onde temos todos esses contextos juntos e dividindo os mesmos recursos e competindo entre si. 
No DDD eles são separados e tem somente os recursos necessários para cada *bounded context*, e por exemplo, é feito uma consistencia eventual dos dados compartilhados.

Um outro exemplo seria os *Cross Cutting Concerns*, esse tipo de necessidade no DDD é resolvido em um *layer* chamado *Shared Kernel* que é uma parte reservada para o compartilhamento entre vários *bounded contexts*.


## Shared Kernel
É uma parte do modelo compartilhada entre 2 ou mais times que concordam em não alterar-lo sem colaboração.
