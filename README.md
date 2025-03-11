# Gerenciador de Boards

Este é um projeto Java para gerenciar boards.

## Funcionalidades

- Criar novo board
- Selecionar board
- Excluir board

## Regras de Negócio

**1. Gerenciamento de Boards:**

* **Criação de Boards:**
    * O sistema deve permitir a criação de novos "boards".
    * Cada "board" deve ter um nome (obrigatório) e uma descrição (opcional).
    * As informações do "board" (nome e descrição) devem ser armazenadas em um banco de dados MySQL.
* **Seleção de Boards:**
    * O sistema deve permitir a seleção de "boards" existentes.
    * (Observação: A implementação dessa funcionalidade está pendente no código fornecido).
* **Exclusão de Boards:**
    * O sistema deve permitir a exclusão de "boards" existentes.
    * (Observação: A implementação dessa funcionalidade está pendente no código fornecido).

**2. Interação com o Usuário:**

* **Menu de Opções:**
    * O sistema deve apresentar um menu com as seguintes opções:
        * Criar novo board
        * Selecionar board
        * Excluir board
        * Sair
    * O usuário deve poder escolher uma opção digitando o número correspondente.
* **Validação de Entrada:**
    * O sistema deve verificar se a opção digitada pelo usuário é válida.
    * Se a opção for inválida, o sistema deve exibir uma mensagem de erro.

**3. Persistência de Dados:**

* **Banco de Dados MySQL:**
    * O sistema deve utilizar um banco de dados MySQL para armazenar as informações dos "boards".
    * As informações dos "boards" devem ser armazenadas na tabela "boards", com as colunas "nome" e "descricao".
* **Conexão com o Banco de Dados:**
    * O sistema deve estabelecer uma conexão com o banco de dados MySQL utilizando as credenciais fornecidas (URL, usuário e senha).
    * O sistema deve tratar possíveis erros de conexão com o banco de dados.

**Observações:**

* As funcionalidades de seleção e exclusão de "boards" ainda não foram implementadas no código fornecido.
* As regras de negócios representam as diretrizes de como o sistema deve funcionar. As regras de negocios são muito importantes para o desenvolvimento de software.

```
graph TD
    A[Início] --> B{Exibir Menu};
    B --> C{Opção Escolhida?};
    C -- 1 --> D[Ler Nome e Descrição do Board];
    D --> E[Conectar ao Banco de Dados];
    E --> F[Inserir Dados na Tabela "boards"];
    F --> G[Exibir Mensagem de Sucesso];
    G --> B;
    C -- 2 --> H[Selecionar Board (TODO)];
    H --> B;
    C -- 3 --> I[Excluir Board (TODO)];
    I --> B;
    C -- 0 --> J[Sair];
    C -- Opção Inválida --> K[Exibir Mensagem de Erro];
    K --> B;
    E -- Erro --> L[Exibir Mensagem de Erro de Banco de Dados];
    L --> B;
```
