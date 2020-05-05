# Domain Driven Design

## O que é DDD?

Domain Driven Design é um conjunto de principios e padrões que nos ajudam a resolver problemas complexos de negócio em softwares bem escritos. Possibilita criar um código claro e testavel que represente um domínio de negócio.

## Visão Geral
- DDD tem como missão não só facilitar a escrita do código, mas muito mais em entender a verdadeira necessidade do cliente para dai então, utilizando desenvolvimento de software como uma ferramenta, resolvermos seus problemas.
- A interação com os **Domain Experts** é extremamente importante para a entrega de um software, especialmente quando utilizamos DDD. Essas são as pessoas que vivem e respiram o negócio e os processos dia a dia, são para elas que nós desenvolvemos os softwares. Ao conversar com um especialista, normalmente utilizamos termos técnicos não relacionados ao domínio de negócio ou até presumimos ações a serem feitas baseados em alguns requisitos de negócio, complicando assim a comunicação e o desenvolvimento correto do projeto.
- Um outro ponto importante é modelar um grande problema em Sub Dominios(**Sub-Domain**), por vezes quando recebemos uma necessidade de desenvolvimento complexa, acabamos atacando os problemas de vez sem antes pensarmos por exemplo, em sub-divisões, o que ao longo do tempo se torna complicado de manter/desenvolver, e o valor para que isso tudo seja mantido será gradualmente mais alto. Então, será que faz sentido tratarmos tudo junto? Não poderiamos tratar assuntos especificos separadamente? Separar esses pequenos assuntos por equipes com suas soluções tecnicas e de negócio especificas para este problema seria muito menos doloroso, realmente dividindo para conquistar.
- Ao implementar Sub-Dominios é importante ter em mente _separation of concerns_ que é você dividir as responsabilidades de forma bem clara, um sub-dominio deve se preocupar somente com aquilo que faz sentido à ele, que são as regras do negócio. Interações com infraestrutura, bases de dados e outros, devem ser tratados separadamente.

## :) Prós e :( Contras do DDD

- DDD nos ajuda a dividir um super problema em problemas menores(**Sub-Domain**) que facilita o entendimento bem como o seu processo de desenvolvimento, o que o torna também mais flexivel.
- Torna a solução final mais próxima da visão de negócios do cliente. Entregando um caminho para problemas **complexos**.
- Normalmente o código é bem organizado e facilmente testavel.
- A regra de negócio fica somente em um único lugar.
- Mesmo não utilizando totalmente DDD, existem alguns padrões que podem beneficiar o desenvolvimento das nossas aplicações.
