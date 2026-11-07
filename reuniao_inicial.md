## Reunião Inicial

### Partes interessadas - Stakeholders
- *Dono do produto:* Barbeiro.
- *Usuários Finais:* Barbeiro, Cliente. 
- *Time de desenvolvimento:*

### Especialistas do dominio
O proprio barbeiro é o especialista do dominio, ele quem anota todos os planos dos clientes

### Existe algum sistema atual?
O barbeiro utiliza um caderno para notar manualmente os planos do cliente

### O que querem?
Uma aplicação que possa gerenciar o fluxo de anotação de planos de cortes de cabelo de uma barbearia.

### Dores princiais do fluxo atual de trabalho do usuário
- Barbeiro reclamou da dificuldade em gerenciar os planos do cliente, pois atualmente anota tudo em um caderno de forma manual, sem organização. 
- Cliente informa que as vezes esquece de quantos cortes ainda possui em seu plano, já que não recebe nenhum cupom informativo, ficando refêm das anotações do barbeiro.

### O que esperam do sistema
- *Barbeiro:* Quer um sistema em que ele possa cadastrar o tipo de plano de sua barbearia, além de poder gerenciar esses planos, como excluir, editar ou criar novos planos a qualquer momento. Registrar um novo plano para um cliente, registrar corte automatizando a quantidade de cortes atuais e quantos faltam e que possa ficar registrado no sistema o plano do cliente como um histórico. Ele quer também que o sistema informe a quantidade de planos ativos, clientes registrados e algo que possa chamar atenção daquele cliente que ficou um tempo sem cortar. Baebeiro informou que queria algo que pudesse fazer agendamentos de clientes para cortar o cabelo.
- *Cliente:* Quer alguma coisa para mostrar a quantidade de cortes que ainda possui na barbearia


### Restrição e Limitações
- O barbeiro quer uma interface bem simples, intuitiva e sem ser poluida. Algo rápido de ser feito, como registrar um plano e um corte em poucas etapas, que não consuma muito tempo.
- Um sistema de cadastro e login bem simples.
- Anotação e persistência de cliente com dados simples, sem que seja um formulário de cadastro complexo. Ele quer algo simples que possa identificar um cliente único.
- Barbeiro reclamou de outros aplicativos que tem uma interface bem ruim, bastante poluida que dá até sono e preguiça de usar.

### Evidências e Contexto da Coleta
Entrevista de maneira informal pessoalmente com o barbeiro.

### Regras de Negócio e Requisitos de Domínio Preliminares
- Um cliente pode ter mais de um plano, porém na hora da utilização seria utilizado como um sistema de FILA
- Quer que seja registrado a data de cada inicio de plano e de corte realizado
- Um plano deve informar uma confirmação para ser adicionado, pois como é registrado após o cliente pagar e não tem integração com pagamento, é só um sistema para anotar os planos, então um plano só é acrescentado quando um cliente já pagou. Impedir exclução. Informar confirmação quando um cliente ja tiver um plano ativo e permitir editar somente.

### Objetivos de Negócio e Critérios de Sucesso
- Deixar a anotação dos planos de forma mais eficiênte para poupar tempo e não atrapalhar o fluxo principal que é cortar cabelo.