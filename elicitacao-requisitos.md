## Elicitação dos Requisitos

### **Sistema:** Sistema de Gerenciamento de Planos de Barbearia

### **Contexto**
Um barbeiro tem um sistema de planos mensal em sua barbearia, onde os clientes podem realizar 4 cortes em um mês pagando um valor fixo. Para saber quem possui um plano, ele tem que consultar em um caderno onde anota tudo a mão, os planos e os cortes realizados. Ele gostaria de poder centralizar toda essa anotação em um sistema que pudesse cadastrar esses planos, armazenar e poder visualizar de forma rápida e fácil.

### Atores do Sistema
* Barbeiro
* Cliente

### Requisitos Funcionais
1. **Autenticação**
   * **RF-001:(Cadastro)** O sistema deve permitir que uma barbearia cadastre suas informações, como o nome do barbeiro responsável, nome da barbearia, localização, email, senha e telefone.
   * **RF-002:(Login)** O sistema deve permitir que o barbeiro realize login no sistema com as credenciais de (e-mail, telefone) e senha.
   * **RF-003:(Recuperação de Senha)** O sistema deve garantir que um barbeiro possa restaurar sua senha solicitando um código de restauração por e-mail.
  
2. **Gestão de Planos**
   * **RF-004:(Cadastro de Planos)**: O sistema deve permitir que o barbeiro responsável realize o cadastro de um plano no aplicativo com as informações de nome do plano, quantidade de cortes e valor.
   * **RF-005:(Editar Planos)**: O sistema deve permitir que o barbeiro realize alterações em um plano cadastrado, mudando informações como o nome do plano, quantidade de cortes e valor.
   * **RF-006:(Excluir Planos)**: O sistema deve permitir que o barbeiro exclua um plano cadastrado no sistena.
   * **RF-007: (Visualizar planos)**: O sistema deve exibir ao barbeiro os planos existentes cadastrados no sistema.
  
3. **Planos ao Cliente**
   * **RF-008: (Vincular Plano ao Cliente)**: O sistema deve permitir que o barbeiro vincule um plano ao cliente, com as informações de nome do cliente, WhatsApp e os dados do plano.
   * **RF-009: (Visualizar Clientes)**: O sistema deve permitir que a barbearia visualize os clientes com planos cadastrados, sejam ativos ou com planos finalizados. Uma aba com um perfil do cliente, como os planos ativos, cortes realizados e um botão para renovar plano.
   * **RF-010: (Registros de Cortes)**: O sistema deve permitir que o barbeiro registre um corte realizado no cliente, diminuindo os cortes disponíveis em seu plano.

### Requisitos Não Funcionais
1. **Usabilidade**
   * **RNF-001**: O sistema deve ter uma interface simples, intuitiva. O barbeiro deverá realizar um cadastro de plano a um usuário em no máximo 3 etapas.
2. **Persistência**
   * **RNF-002**: O sistema deve garantir a integridade dos dados de acesso do login do barbeiro e dos planos ativos do cliente. Garantindo que os dados fiquem salvos e que eles nçao sejam perdidos.
3. **Disponibilidade e Responsabilidade**
   * **RNF-003**: O sistema deve se adaptar a todo o tipo de tela, seja ela desktop, tablet ou mobile.
4. **Segurança**:
   * **RNF-004**: O sistema deve garantir o acesso aos dados persistidos no banco de dados a somente usuários autenticados.
  
### Regras de Negócios
* O sistema deve vincular planos e usuários a um login de barbearia
* Um Babeiro pode cadastrar quantos planos quiser
* Um cliente pode ter mais de 1 plano contratado, porém a utilização será pelo sistema de FILA.
* O sistema não deve permitir o registro de corte a um cliente que não tenha plano ativo.
* O plano não se expira após um mês, ele expira quando o cliente utilizar os 4 cortes ou q quantidade de cortes do plano contratado.
* O sistema deve ficar registrado com o nome da barbearia e qualquer barbeiro pode acessar com o login da barbearia.
* O sistema deve registrar a data que o corte foi realizado.

### Fora do Escopo
* Agendamento pelo sistema será implementado em novas atualizações do sistema.
* Notificações no WhatsApp do cliente sobre informações de seu plano, como quantidades sobrando, novidades, promoções.

### Definições Rápidas
* Plano Cadastrados: São os modelos de planos que a barbearia tem.
* Plano vinculado a um cliente: É quando o barbeiro adiciona ao cliente um plano de sua barbearia.
* FILA: Um cado é usado de acordo com a ordem que foi cadastrado ao cliente.
