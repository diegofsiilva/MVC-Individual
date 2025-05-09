# Plataforma de Eventos MVC em Node.js com PostgreSQL

Este projeto é uma Plataforma de Eventos (DIEvents) básico para uma aplicação Node.js seguindo o padrão MVC (Model-View-Controller), utilizando PostgreSQL como banco de dados.

## Requisitos

- Node.js (versão 22.13.1)
- PostgreSQL (versão 17.0.0)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/diegofsiilva/MVC-Individual.git
   cd MVC-individual 
```

2. **Instalar as dependências:**
    
```bash
npm init -y
npm install express
```
    
3. **Configurar o arquivo `.env`:**
    
Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.
    

Configuração do Banco de Dados
------------------------------

1. **Criar banco de dados:**
    
    Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.
    
2. **Executar o script SQL de inicialização:**
    
```bash
npm run init-db
```
    
Isso criará a tabela `usuário, ingresso, eventos e notificações` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.
    

Funcionalidades
---------------

* **Padrão MVC:** Estrutura organizada em Model, View e Controller.
* **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
* **UUID:** Utilização de UUID como chave primária na tabela `users`.
* **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
* **Testes:** Inclui estrutura básica para testes automatizados.

Scripts Disponíveis
-------------------

* `npm start`: Inicia o servidor Node.js.
* `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
* `npm run test`: Executa os testes automatizados.
* `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

Estrutura de Diretórios
-----------------------
```bash
meu-projeto/
│
├── assets/                 # Arquivos públicos como imagens e fontes
|   └──favicon.ico
|   └──logointeli.png
├── config/                # Arquivos de configuração (ex: conexão com banco)
│   └── db.js
├── controllers/           # Lógica de controle das requisições
│   └── alunoController.js
|   └── userController.js
├── documentos/            # Descrição do projeto e documentos 
│   └── diagramBD.png
|   └── wad.md
├── models/                # Definição de modelos de dados (estrutura do banco)
│   └── alunos.js
│   └── userModel.js
├── routes/                # Definição das rotas do sistema
│   └── alunos.js
│   └── frontRouter.js
│   └── userRoutes.js
├── scripts/               # Arquivos de JavaScript públicos e criação das tabelas do Banco de Dados
│   └── init.sql
│   └── runSQLScript.js
├── services/              # Serviços auxiliares do sistema
│   └── userService.js
├── tests/                 # Arquivos de testes unitários
│   └── userController.js
│   └── userModel.test.js
│   └── userRoutes.test.js
│   └── userService.test.js
├── views/                 # Arquivos de testes unitários
│   └── alunos/
|        └── index.ejs
│   └── components/
|        └── header.ejs
│   └── css/
|        └── styles.css
│   └── layout/
|        └── main.ejs
│   └── pages/
|        └── page1.ejs
|        └── page2.ejs
├── .gitignore             # Arquivo para ignorar arquivos no      Git (ex: node_modules)
├── app.js              # Arquivo principal que inicializa o servidor
├── jest.config.js         # Arquivo de configuração do Jest
├── package-lock.json      # Gerenciador de dependências do Node.js
├── package.json           # Gerenciador de dependências do Node.js
├── readme.md              # Documentação do projeto (Markdown)
└── rest.http              # Teste de endpoints (opcional)
```

Contribuição
------------

Contribuições são bem-vindas! Sinta-se à vontade para abrir um issue ou enviar um pull request.

Licença
-------

Este projeto está licenciado sob a Licença MIT.

Este README.md fornece uma visão geral clara do boilerplate, incluindo instruções de instalação, configuração do banco de dados, funcionalidades principais, scripts disponíveis, estrutura de diretórios, como contribuir e informações de licença. Certifique-se de personalizar as seções com detalhes específicos do seu projeto conforme necessário.