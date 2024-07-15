# 🌟 Projeto de Gerenciamento de Sistema Multi-APIs

## 📝 Descrição do Projeto

Este projeto tem como objetivo desenvolver um sistema distribuído com múltiplas APIs, cada uma responsável por uma parte específica do sistema. O projeto está sendo desenvolvido de forma incremental. 

### 🛠️ APIs do Projeto

1. **API de Usuários e Permissões** 🧑‍💻
   - Gerencia usuários e suas permissões, incluindo o login.
   - Funcionalidades principais:
     - Registro de novos usuários.
     - Autenticação e autorização.
     - Gerenciamento de permissões de acesso.

2. **API de Clientes** 🏢
   - Gerencia os dados cadastrais dos clientes e seus endereços.
   - Funcionalidades principais:
     - Cadastro de clientes.
     - Atualização de dados cadastrais.
     - Gerenciamento de múltiplos endereços para cada cliente.
   - Envia mensagens para uma fila quando há qualquer alteração nos dados dos clientes para que outras APIs possam se atualizar.

3. **API de Produtos** 📦
   - Gerencia os produtos e realiza controle de estoque básico.
   - Funcionalidades principais:
     - Cadastro de produtos.
     - Atualização de dados dos produtos.
     - Controle de estoque (quantidade atual, quantidade mínima e quantidade máxima).
   - Envia mensagens para uma fila quando há qualquer alteração nos dados dos produtos para que outras APIs possam se atualizar.

4. **API de Pedidos** 🛒
   - Registra os pedidos realizados pelos clientes.
   - Funcionalidades principais:
     - Registro de novos pedidos.
     - Atualização e consulta de pedidos existentes.
     - Controle de status dos pedidos (aberto, finalizado, cancelado).
     - Gerenciamento de itens de pedido (produto, quantidade, preço unitário, total).
   - Consome atualizações dos dados dos clientes e produtos a partir da fila.

### 🔄 Estrutura de Comunicação

- Cada API possui seu próprio banco de dados, garantindo isolamento e independência dos dados.
- Alterações nos dados de clientes e produtos são comunicadas através de mensagens enviadas para uma fila.
- As APIs consumirão essas mensagens para manter suas bases de dados sincronizadas com as informações atualizadas.

## 🚀 Como Executar o Projeto
EM BREVE...
