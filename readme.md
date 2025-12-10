<p align="center">
  <img width="30%" src="logo eric hiroshi.png" alt="Logo do Projeto">
</p>

<h3 align="center">Desafio DIO - CI&T - Backend com Java & AWS

Gerenciador de Boards — Aplicação Console (Java + Gradle)</h3>

<p align="center">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">
  <img alt="Language" src="https://img.shields.io/badge/language-Java%2025-blue">
  <img alt="Build Tool" src="https://img.shields.io/badge/build-Gradle%209.1.0-success">
  <img alt="Database" src="https://img.shields.io/badge/database-MySQL%208-blue">
  <img alt="Gradle Wrapper" src="https://img.shields.io/badge/Gradle-Wrapper-6DDC4B">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-available-2496ED">
  <img alt="Liquibase" src="https://img.shields.io/badge/Liquibase-4.29.1-8A2BE2">
</p>

---

## 🧭 Visão Geral

Este projeto implementa um **gerenciador de boards de tarefas** executado totalmente via **terminal**.  
O usuário pode criar boards, gerenciar colunas, criar cards, mover tarefas, bloquear/desbloquear atividades e obter relatórios. Desenvolvido durante o bootcamp CI&T - Backend com Java & AWS em parceria com a DIO.

---

## 📚 Sumário
- [🧭 Visão Geral](#-visão-geral)
- [📚 Sumário](#-sumário)
- [⚙️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [🗂️ Estrutura do Board (resumo)](#️-estrutura-do-board-resumo)
- [🚀 Execução do Projeto](#-execução-do-projeto)
  - [✅ Pré-requisitos](#-pré-requisitos)
  - [📥 Clonar o repositório](#-clonar-o-repositório)
  - [🐳 Subir MySQL + phpMyAdmin](#-subir-mysql--phpmyadmin)
  - [▶️ Build](#️-build)
  - [▶️ Executar](#️-executar)
- [💬 Menus e Interações (texto exato usado pelo projeto)](#-menus-e-interações-texto-exato-usado-pelo-projeto)
  - [Menu inicial](#menu-inicial)
  - [Menu do board selecionado](#menu-do-board-selecionado)
- [🤝 Contribuições](#-contribuições)
- [🔗 Referências e Créditos](#-referências-e-créditos)

---

## ⚙️ Tecnologias Utilizadas

| Tecnologia | Finalidade |
|-------------|-------------|
| ☕ **Java 25** | Linguagem principal |
| 🧰 **Lombok** | Redução de boilerplate |
| 🐬 **MySQL Connector/J** | Driver JDBC para MySQL |
| 🐳 **Docker** | Containerização do ambiente |
| 🐘 **Gradle** | Sistema de automação de build |
| 🗄️ **Liquibase** | Versionamento de banco de dados |

---

## 🗂️ Estrutura do Board (resumo)

- **Board**: id, nome, lista ordenada de colunas
- **Coluna**: id, nome, tipo (INICIAL, PENDENTE, FINAL, CANCELAMENTO), ordem
- **Card**: id, título, descrição, bloqueado(Boolean), histórico de movimentos

**Regras principais** (resumidas):
- Um board tem ao menos 3 colunas: INICIAL (primeira), FINAL (penúltima) e CANCELAMENTO (última).
- Apenas 1 coluna de cada tipo especial (INICIAL, FINAL, CANCELAMENTO).
- Cards andam na ordem das colunas e não podem pular etapas. Podem ir direto para CANCELAMENTO.
- Cards bloqueados não se movem; bloqueio/desbloqueio exigem justificativa.

---

## 🚀 Execução do Projeto

### ✅ Pré-requisitos
- Java 25+
- Docker & Docker Compose (para MySQL + phpMyAdmin)
- Git

### 📥 Clonar o repositório

```bash
git clone https://github.com/erichiroshi/board-dio.git
cd board-dio
```

### 🐳 Subir MySQL + phpMyAdmin

No diretório `raiz/` (ou onde está o docker-compose.yml):

```bash
docker compose up -d
```

Acesse phpMyAdmin em `http://localhost:8081` (credenciais conforme seu docker-compose).

### ▶️ Build

```bash
./gradlew clean build
```

### ▶️ Executar

Via Gradle (entrada interativa garantida):

```bash
./gradlew run
```

> Dica: se usar PowerShell, antes execute:
> ```powershell
> [Console]::OutputEncoding = [System.Text.UTF8Encoding]::new()
> $OutputEncoding = [System.Text.UTF8Encoding]::new()
> chcp 65001
> ```

---

## 💬 Menus e Interações (texto exato usado pelo projeto)

### Menu inicial

```
1 - Criar um novo board
2 - Selecionar um board existente
3 - Excluir um board
4 - Sair
```

### Menu do board selecionado

```
1 - Criar um card
2 - Mover um card
3 - Bloquear um card
4 - Desbloquear um card
5 - Cancelar um card
6 - Ver board
7 - Ver coluna com cards
8 - Ver card
9 - Voltar ao menu anterior
10 - Sair
```

---

## 🤝 Contribuições

Contribuições são sempre bem-vindas!  
Para contribuir:

1. Crie um fork do repositório.  
2. Crie uma branch de feature:  
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. Commit suas mudanças:  
   ```bash
   git commit -m "feat: nova funcionalidade"
   ```
4. Envie um Pull Request.  

📜 **Boas práticas**
- Adicione testes unitários.  
- Documente suas alterações no código.  
- Use mensagens de commit seguindo o padrão **Conventional Commits**.

---

## 🔗 Referências e Créditos

- Desafio original: [digitalinnovationone - DIO](https://github.com/digitalinnovationone/board)
- Desenvolvido por [**Eric Hiroshi**](https://github.com/erichiroshi)
- Licença: [MIT](LICENSE)

---

<p align="center">
  <em>“Simplicidade, clareza e intenção: a base de qualquer software bem construído.”</em>
</p>
