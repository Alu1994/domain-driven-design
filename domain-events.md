# Domain Events
Ele é um padrão que serve para desacoplar comunicações internas do projeto, disponibilizando eventos para descrever as atividades ou mudanças de estado que podem ocorrer no sistema. Assim outras partes do domínio podem responder à esses eventos de uma forma fracamente acoplada, sem saber de onde esses eventos vieram, tão pouco seus invocadores saberem quais processos responderam à esses eventos.
  - Domain Events podem ser usados ao comunicar para fora do domínio.
  - Domain Events fazem parte da Ubiquitous Language do projeto, pois Domain Experts sabem quais os eventos que devem ocorrer em cada cenário da aplicação.
  - Domain Events representam coisas que já aconteceram no sistema, sendo assim, eles devem ser imutáveis.
  - Domain Events só devem ser usados caso realmente algum evento **externo** deva ser acionado dado uma regra de negócio. (Quando dizemos externo, pode ser um processamento que deva ser feito por simplesmente uma outra entidade no domínio.)
  
## Como identificar Domain Events?
  - Ex: **Quando** o cliente fechar uma compra, **então** ele deverá receber uma notificação via e-mail com os dados da compra.

## Dicas de como criar um Domain Event:
  - Cada evento é sua própria Classe.
  - É interessante saber quando o evento foi acionado. Podendo ter uma simples propriedade *TimeOccurred*.
  - Os campos do eventos devem ser inicializados em seu Construtor.
  - Não podem ter comportamentos ou efeitos colaterais.
  - Classes de Eventos devem sempre que possível ser leves, com somente as informações necessárias para sua execução ou possível re-execução.

