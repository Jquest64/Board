# 🏗️ Board de Tarefas

## 🛠️ Sobre o Projeto - Board
Este projeto faz parte de um **desafio de projeto** da plataforma **[DIO](https://www.dio.me/)** e tem como objetivo desenvolver um sistema de **gerenciamento de tarefas**.  

O sistema permite a criação de **boards**, com colunas organizadas de forma configurável, e a movimentação de **cards**, garantindo a **persistência dos dados** em um banco **MySQL**, utilizando **Liquibase** para versionamento e migração.  

A interação ocorre via **menu interativo no terminal**, proporcionando um fluxo simples e eficiente para os usuários.

## 🚀 Tecnologias Utilizadas  
- **Java** – Linguagem principal  
- **MySQL** – Banco de dados relacional  
- **Liquibase** – Migração e versionamento de banco  
- **Flyway** – Alternativa para controle de banco  
- **Gradle** – Gerenciamento de dependências  
- **Lombok** – Redução de boilerplate  

## 📋 Funcionalidades Principais  

### 📂 **Gerenciamento de Boards**  
- Criar, selecionar e excluir **boards**  
- Configuração de colunas padrão e personalizáveis  
- Ordem das colunas configurável (exceto colunas fixas como "Cancelado")  

### 🏷️ **Gerenciamento de Cards**  
- Criar e mover **cards** entre colunas  
- Bloquear/desbloquear **cards** (com justificativa)  
- Cancelamento permitido de qualquer coluna (exceto "Concluído")  

### 🗃️ **Persistência de Dados**  
- Banco de dados **MySQL**  
- Migrações com **Liquibase**  
- Tabelas do sistema: `Boards`, `BoardColumns`, `Cards`, `Blocks`  

### 📊 **Relatórios**  
- Tempo de permanência dos **cards** em cada coluna  
- Histórico de bloqueios e justificativas  

## 🔧 Estrutura do Projeto  

### 🏛️ **Arquitetura**  
- **Persistence:** DAOs (`BoardDAO`, `CardDAO`, `BlockDAO`) + Entidades  
- **Service:** Lógica de negócio (`BoardService`, `CardService`)  
- **UI:** Menus interativos via terminal  

### 🏗️ **Setup Inicial**  
1️⃣ Criar o projeto Gradle  
2️⃣ Configurar conexão com **MySQL** e Liquibase  
3️⃣ Criar migrações (`Boards`, `BoardColumns`, `Cards`, `Blocks`)  

### 🏗️ **Camada de Dados**  
✅ Implementação das entidades (`BoardEntity`, `CardEntity`, `BlockEntity`)  
✅ DAOs com operações **CRUD** e consultas complexas  

### 🎯 **Regras de Negócio**  
🔹 Bloqueio requer motivo  
🔹 Cards não podem ser movidos para colunas inválidas  
🔹 Cancelamento não permitido para cards concluídos  

### 🖥️ **Interface de Usuário (UI)**  
- Menus para criar **boards**, mover **cards**, bloquear/desbloquear, etc.  
- Exibição de detalhes dos cards e histórico de bloqueios  
