 # Diagrama  de Caso de Uso
Este diagrama de caso de uso representa o funcionamento de um sistema de gerenciamento com diferentes tipos de usuários: Sistema, Gerente, Cliente e Funcionário de Estoque. Cada um tem acessos distintos para realizar operações específicas.

### 1. Sistema: Permite criar cadastro, fazer login e gerenciar produtos, clientes e vendas.

- Ações: criar cadastro, fazer login, cadastrar, editar, excluir e consultar produtos e clientes, registrar e cancelar vendas.
### 2. Gerente: Tem permissões amplas para gerenciar produtos, clientes e vendas, similares ao sistema.

- Ações: login, cadastrar, editar, excluir e consultar produtos e clientes, registrar, consultar e cancelar vendas.
### 3. Cliente: Pode realizar operações básicas relacionadas a produtos e compras.

- Ações: criar cadastro, fazer login, consultar e selecionar produtos, realizar e cancelar compras.
### 4. Funcionário de Estoque: Gerencia produtos e consulta vendas.

- Ações: cadastrar, editar, excluir e consultar produtos, além de consultar vendas.


 # Especificação de caso de uso
### Visão Geral dos Casos de Uso
O sistema é composto por uma série de funcionalidades principais que permitem:

Gerenciamento de clientes e autenticação.
Consulta e seleção de produtos.
Processamento de compras e vendas.
Manutenção de estoque.
Gerenciamento de transações por funcionários e gerentes.

### Descrição dos Casos de Uso
 UC01 - Cadastrar Cliente
- Descrição: Permite que o cliente se cadastre no sistema.
- Ator Primário: Cliente
- Pré-condição: O cliente não deve estar registrado no sistema.
- Pós-condição: O cliente é registrado no sistema e pode realizar login.
- Fluxo Principal:
1. O cliente acessa a opção de cadastro.
2. O cliente insere os dados pessoais exigidos (nome, CPF, endereço, login e senha).
3. O sistema verifica se os dados são válidos.
4. O sistema confirma o cadastro do cliente.
- Fluxo Alternativo:
- A1: Se os dados estiverem incompletos ou inválidos, o sistema exibe uma mensagem de erro.
  
  
UC02 - Login do Cliente
- Descrição: Permite que o cliente faça login no sistema.
- Ator Primário: Cliente
- Pré-condição: O cliente já deve estar registrado no sistema.
- Pós-condição: O cliente é autenticado no sistema e pode acessar suas funcionalidades.
- Fluxo Principal:
1. O cliente insere seu login e senha.
2. O sistema valida as credenciais.
3. O cliente é autenticado e redirecionado para a página principal.
- Fluxo Alternativo:
- A1: Se o login ou senha estiverem incorretos, o sistema exibe uma mensagem de erro e permite uma nova tentativa.


UC03 - Consultar Produto
- Descrição: Permite ao cliente consultar produtos disponíveis no sistema.
- Ator Primário: Cliente
- Pré-condição: O cliente deve estar logado no sistema.
- Pós-condição: Os produtos consultados são exibidos ao cliente.
- Fluxo Principal:
1. O cliente acessa a opção de consulta de produtos.
2. O sistema exibe a lista de produtos disponíveis com informações relevantes.


UC04 - Selecionar Produto
- Descrição: Permite ao cliente selecionar um produto para compra.
- Ator Primário: Cliente
- Pré-condição: O cliente deve estar logado no sistema e ter consultado a lista de produtos.
- Pós-condição: O produto é adicionado ao carrinho do cliente.
- Fluxo Principal:
1. O cliente escolhe um produto e seleciona a quantidade desejada.
2. O sistema adiciona o produto ao carrinho do cliente.


UC05 - Realizar Compra
- Descrição: Permite que o cliente finalize a compra dos produtos selecionados.
- Ator Primário: Cliente
- Pré-condição: O cliente deve estar logado e ter produtos no carrinho.
- Pós-condição: A compra é registrada no sistema.
- Fluxo Principal:
1. O cliente acessa o carrinho e seleciona a opção de finalizar compra.
2. O sistema solicita a forma de pagamento e a forma de envio.
3. O cliente escolhe as opções desejadas.
4. O sistema calcula o valor final e registra a compra.


UC06 - Cancelar Compra
- Descrição: Permite ao cliente cancelar uma compra.
- Ator Primário: Cliente
- Pré-condição: O cliente deve ter uma compra realizada no sistema.
- Pós-condição: A compra é cancelada.
- Fluxo Principal:
1. O cliente acessa a área de histórico de compras.
2. O cliente seleciona uma compra e escolhe a opção de cancelamento.
3. O sistema confirma o cancelamento e atualiza o estoque.


UC07 - Atualizar Estoque
- Descrição: Permite ao funcionário de estoque atualizar a quantidade de produtos.
- Ator Primário: FuncionarioEstoque
- Pré-condição: O funcionário deve estar autenticado no sistema.
- Pós-condição: O estoque é atualizado com as novas quantidades.
- Fluxo Principal:
1. O funcionário acessa o gerenciamento de estoque.
2. O funcionário seleciona um produto e define a nova quantidade.
3. O sistema atualiza a quantidade em estoque.


UC08 - Cadastrar Produto (Gerente)
- Descrição: Permite ao gerente cadastrar novos produtos no sistema.
- Ator Primário: Gerente
- Pré-condição: O gerente deve estar autenticado no sistema.
- Pós-condição: O produto é adicionado ao catálogo do sistema.
- Fluxo Principal:
1. O gerente acessa o cadastro de produtos.
2. O gerente insere as informações do produto (nome, preço, descrição, quantidade inicial).
3. O sistema confirma e armazena o novo produto.


UC09 - Registrar Venda (Funcionário)
- Descrição: Permite que o funcionário registre uma venda.
- Ator Primário: Funcionario
- Pré-condição: O funcionário deve estar autenticado no sistema.
- Pós-condição: A venda é registrada e o estoque é atualizado.
- Fluxo Principal:
1. O funcionário acessa a opção de registrar venda.
2. O funcionário seleciona o produto e a quantidade vendida.
3. O sistema registra a venda e atualiza o estoque.


UC10 - Cancelar Venda (Gerente)
- Descrição: Permite que o gerente cancele uma venda.
- Ator Primário: Gerente
- Pré-condição: A venda deve estar registrada no sistema.
- Pós-condição: A venda é cancelada e o estoque é atualizado.
- Fluxo Principal:
1. O gerente acessa o histórico de vendas.
2. O gerente seleciona uma venda e escolhe a opção de cancelamento.
3. O sistema confirma o cancelamento e ajusta o estoque.




 # Diagrama de classe 
O diagrama de classes apresenta a estrutura principal do sistema, detalhando as classes e suas relações.
### Classes Principais
- Cliente: Representa o cliente do sistema, responsável por realizar o cadastro, consultar e comprar produtos.
- Produto: Contém informações sobre os produtos no estoque.
- Compra e Venda: Representam as transações de compra e venda, respectivamente, cada uma com métodos para calcular preço, selecionar forma de envio, entre outros.
- FuncionarioEstoque: Responsável por atualizar o estoque de produtos.
- Gerente: Garante a coordenação geral do sistema, incluindo registro e cancelamento de vendas.
- FormaEnvio: Define as formas de envio dos produtos, com métodos para calcular o frete.

### Relacionamentos
- Cliente realiza compras (Realiza).
- Produtos informam detalhes à Compra e à Venda.
- FuncionarioEstoque atualiza o estoque (Atualiza).
- Gerente realiza e cancela operações de compra e venda.
- Compra e Venda definem a forma de envio (Define).

  
 # Diagrama de sequência 

### 1. Descrição Geral: Fornecer uma visão geral dos diagramas, explicando como eles representam as interações entre os componentes do sistema.
- Atores e Objetos: Listar os principais atores (pessoas ou sistemas que interagem com o sistema) e objetos (entidades do sistema) envolvidos nos diagramas.
- Fluxo Típico: Descrever o fluxo típico de uma ação, como por exemplo, o processo de realizar uma compra, desde a escolha dos produtos até a finalização do pedido.
- Casos de Uso: Destacar os principais casos de uso cobertos pelos diagramas (e.g., cadastro de produtos, realização de vendas, gerenciamento de clientes).

  
### 2. Funcionalidades
- Gerenciamento de Produtos: Detalhar as funcionalidades relacionadas aos produtos, como cadastro, edição, exclusão e consulta.
- Gerenciamento de Clientes: Detalhar as funcionalidades relacionadas aos clientes, como cadastro, edição, exclusão e consulta.
- Processamento de Vendas: Descrever o processo de venda, incluindo cálculo de preços, formas de pagamento, envio e acompanhamento de pedidos.
- Outras Funcionalidades: Listar outras funcionalidades importantes, como geração de relatórios, integrações com outros sistemas, etc.

Os diagramas de sequência apresentados ilustram as interações entre os atores (cliente, gerente) e os objetos (produto, pedido) durante o processo de compra. Eles detalham o fluxo de uma venda, desde a escolha dos produtos até a finalização do pedido, incluindo o cálculo do frete e a atualização do estoque.


# Diagrama de Atividade

