<img src="../assets/logointeli.png">

# Web Application Document (WAD) - Plataforma de Eventos

**Versão**: 1.0  
**Data**: 09 de Maio de 2025  
**Autor**: Diego Figueiredo Silva
**Curso**: Ciência da Computação  

## 1. Introdução
    A era digital transformou a forma como nos conectamos, compartilhamos 
    experiências e organizamos momentos significativos. Nesse contexto, a Plataforma de 
    Eventos surge como um projeto "visionário"(PONDERADA), desenvolvido no âmbito acadêmico, para 
    facilitar a criação e participação em eventos, unindo tecnologia, inovação e usabilidade. 
    Este Web Application Document (WAD) apresenta a essência de uma aplicação web que não apenas 
    atende às necessidades de organizadores e participantes, mas também reflete o compromisso 
    com o aprendizado prático e a aplicação de conceitos fundamentais de desenvolvimento de software.

### 1.1 Objetivo
A criação de uma Plataforma de Eventos, uma aplicação web para criar, gerenciar e participar de eventos, desenvolvida como projeto da semana 2 - INTELI.

### 1.2 Escopo
- Cadastro e login de usuários.
- Criação e gerenciamento de eventos.
- Busca e inscrição em eventos.
- Interface simples e responsiva.

## 2. Arquitetura

### 2.1 Visão Geral
Arquitetura com modelo MVC. O frontend exibe a interface (Por enquanto não desenvolvido), e o backend gerencia dados e lógica.

### 2.2 Tecnologias
- **Frontend**: EJS, CSS, JavaScript.
- **Backend**: Node.js com Express.
- **Banco de Dados**: PostgreSQL.
- **Hospedagem**: Supabase.
- **Ferramentas**: Git/GitHub.

### 2.3 Diagrama do Banco de Dados

<img src="/documentos/diagramaBD.png">


## 3. Funcionalidades

### 3.1 Módulos
1. **Usuários**: Cadastro, login.
2. **Eventos**: Criar, editar, excluir eventos; listar e buscar eventos.
3. **Ingresso**: Inscrever-se ou cancelar inscrição em eventos.
4. **Notificações**: Alertas de inscrição (e-mail do comprador).

## 4. Modelo de Dados

### 4.1 Entidades
- **Usuário**: id, nome, cpf, e-mail, data_nascimento.
- **Evento**: id, nomeEvento, data, localizacao.
- **Ingresso**: id, evento_id, userID, precoID, transacao.
- **Notificação:** id, nomeEventoID, userID, precoID, transacao.

### 4.2 Relacionamentos
- Na tabela Notificações: "userID" referência "id" da tabela "usuario".
- Na tabela Notificações: "nomeEventoID" referência "id" da tabela "eventos".
- Na tabela Ingresso: "userID" referência "id" da tabela "usuario".
- Na tabela Ingresso: "eventoID" referência "id" da tabela "eventos".

