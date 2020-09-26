## Domain Services
Quando uma operação é importante ao modelo, mas não pertence necessariamente a nenhuma _Entidade_ ou _Value Object_, um Serviço é normalmente apropriado para a tarefa. Mas é necessário verificar com calma, pois criando sempre um Domain Service, é possivel acabarmos tendo um _Modelo Anemico_.

Normalmente quando precisamos da colaboração de mais uma _Entidade/ValueObject_ utilizamos _Domain Services_.

Eles não podem ser uma parte natural de uma _Entidade/Value Object_, eles devem possuir uma interface e não podem conter estado, mas eventualmente podem ter efeitos colaterais.

<p><img src="https://github.com/matsennin/domain-driven-design/blob/master/images/DomainServices.png" /></p>
