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

### (Gerente)
### 1. Diagrama de Cadastro e Gestão de Produtos:
- Foco: Operações relacionadas ao cadastro, atualização e exclusão de produtos.
- Funcionalidades: Permite ao usuário adicionar novos produtos, modificar informações existentes e remover produtos do sistema.
- Fluxo: O diagrama detalha o processo de cadastro, incluindo a verificação da existência do produto e a exibição de mensagens de sucesso ou erro.

### 2. Diagrama de Gestão de Clientes:
- Foco: Operações relacionadas ao cadastro, atualização, exclusão e pesquisa de clientes.
- Funcionalidades: Permite ao usuário adicionar novos clientes, modificar informações de clientes existentes, remover clientes do sistema e realizar buscas por clientes com base em critérios específicos.
- Fluxo: O diagrama detalha o processo de cadastro de clientes, incluindo a verificação da existência do cliente e a exibição de mensagens de sucesso ou erro.

### 3. Diagrama de Processo de Venda
- Foco: Processo de realização de uma venda, desde a escolha dos produtos até a finalização da transação.
- Funcionalidades: Permite ao usuário selecionar produtos, calcular o valor total da compra e finalizar a venda.
- Fluxo: O diagrama detalha as etapas envolvidas em uma venda, como a adição de itens ao carrinho, o cálculo do valor total e a geração do pedido.

### 4. Diagrama de Login 
- Foco: Processo de autenticação dos usuários para acessar o sistema.
- Funcionalidades: Permite aos usuários se autenticarem no sistema utilizando suas credenciais.
- Fluxo: O diagrama detalha o processo de verificação das credenciais e a concessão ou negação do acesso ao sistema.


## (Funcionário_Estoque)
- Login: Verificação das credenciais do funcionário para acesso ao sistema.
- Consulta de estoque: Pesquisa de produtos em estoque, verificação de quantidade e localização.
- Realização de inventário: Contagem física dos produtos em estoque e atualização do sistema.
- Registro de entrada de produtos: Cadastro de novos produtos no estoque, incluindo informações como quantidade, fornecedor e data de validade.
- Registro de saída de produtos: Registro da saída de produtos do estoque, geralmente associada a pedidos de venda ou outros processos.
- Geração de relatórios: Criação de relatórios sobre o estoque, como nível de estoque, produtos mais vendidos, etc.

- Atendimento a pedidos: O funcionário recebe um pedido, verifica a disponibilidade dos produtos em estoque, separa os itens e registra a saída dos produtos.
- Realização de inventário periódico: O funcionário realiza a contagem física dos produtos em estoque em intervalos regulares e compara os resultados com os dados do sistema.
- Gerenciamento de produtos próximos ao vencimento: O sistema alerta o funcionário sobre produtos com data de validade próxima, permitindo que ele tome as devidas providências (ex: promoção, descarte).
- Controle de qualidade: O funcionário pode realizar inspeções nos produtos recebidos ou armazenados para verificar a qualidade e identificar possíveis problemas.


## (Funcionário)
- Sistema de Gestão de Vendas: O funcionário pode ser um vendedor que consulta informações sobre produtos para atender a um cliente, e o cadastro de clientes é parte do processo de venda.
- Sistema de Atendimento ao Cliente: O funcionário pode ser um atendente que consulta informações sobre produtos para responder a dúvidas de clientes e cadastra novos clientes.
- Sistema de Gestão de Estoque: O funcionário pode ser um responsável por estoque que consulta a disponibilidade de produtos e cadastra novos itens.
### Fluxo 
### 1. Consulta de Produto:

- O funcionário seleciona a opção de consultar um produto.
- O sistema apresenta uma interface para o funcionário inserir os dados do produto (código, nome, etc.).
- O sistema busca as informações do produto no banco de dados e as apresenta ao funcionário.

### 2. Cadastro de Cliente:

- O funcionário inicia o processo de cadastro.
- O sistema apresenta um formulário para o funcionário preencher os dados do cliente (nome, endereço, contato, etc.).
- O sistema verifica se já existe um cliente com os mesmos dados (por exemplo, CPF ou CNPJ).
- Se o cliente já existir, o sistema pode apresentar uma mensagem de erro ou permitir que o funcionário atualize as informações.
- Se o cliente não existir, o sistema salva as informações do novo cliente no banco de dados.

## (Cliente)
### 1. Tentativa de Login: O usuário inicia o processo tentando fazer login no sistema, inserindo suas credenciais (usuário e senha).

### 2. Verificação de Credenciais: O sistema verifica se as credenciais fornecidas são válidas.

### 3. Autenticação:
 - Sucesso: Se as credenciais forem válidas, o usuário é autenticado e pode acessar as funcionalidades do sistema.
- Falha: Se as credenciais forem inválidas, o usuário é direcionado para uma tela de opções.
  
### 4. Opções após Falha de Autenticação:
- Tentar Novamente: O usuário pode tentar fazer login novamente, inserindo as credenciais corretas.
- Criar Cadastro: Se o usuário ainda não possui uma conta, ele pode criar uma nova, fornecendo as informações solicitadas.
  
### 5. Cadastro: O usuário preenche um formulário com seus dados pessoais para criar uma nova conta.

### 6. Verificação de Cadastro: O sistema verifica se o cadastro foi realizado com sucesso.

### 7. Login Após Cadastro: Após o cadastro bem-sucedido, o usuário é direcionado para a tela de login para inserir suas novas credenciais.
