# 📚 Biblioteca Virtual

Este repositório abriga o desenvolvimento de uma Biblioteca Virtual voltada para a organização e disponibilização de um acervo físico real, com foco em simplicidade, leveza e acessibilidade para estudantes.

A proposta é criar um sistema de gerenciamento onde os usuários possam:

- Visualizar livros disponíveis de forma intuitiva, em uma estante interativa
- Acessar informações detalhadas ao passar o mouse ou clicar nos livros
- Consultar disponibilidade em tempo real
- Solicitar empréstimos (em etapas futuras)

O sistema será dividido em:

- **Frontend**: uma interface interativa desenvolvida em React com Vite e TailwindCSS, projetada para funcionar bem mesmo em dispositivos mais modestos.
- **Backend**: uma API REST construída com Node.js (Express), responsável pelo controle dos dados e comunicação com o banco.
- **Banco de Dados**: será utilizado SQLite durante o desenvolvimento e primeiras versões, por sua simplicidade e portabilidade. O banco conterá dados do acervo, usuários (futuramente), histórico de empréstimos, entre outros.

## 🎯 Objetivos do projeto

Até o final do desenvolvimento, pretendemos implementar:

- [ ] Exibição do acervo em formato de estante virtual
- [ ] Backend funcional com banco persistente
- [ ] Interface administrativa para cadastro/edição de livros
- [ ] Login básico para bibliotecários
- [ ] Controle simples de empréstimos
- [ ] Histórico de interações (a depender da demanda)
- [ ] Exportação e backup do banco de dados

O projeto é colaborativo, modular e planejado para ser facilmente mantido por qualquer integrante do curso, mesmo com conhecimentos básicos em programação.

---
## 🚀 Tecnologias

- **Frontend**: React 19 + Vite + Tailwind CSS
- **Backend**: Node.js (Express) + SQLite
- **Infraestrutura**: Docker + Docker Compose
- **Ambiente Dev**: VSCode + DevContainer
- **CI/CD**: GitHub Actions (pronto para configurar)

---

## 🧠 Estrutura do projeto

```
biblioteca-virtual/
├── backend/            # API Express + acesso ao SQLite
├── frontend/           # Interface React + Tailwind
├── database/           # Arquivo SQLite separado
├── .devcontainer/      # Ambiente de desenvolvimento (VSCode)
├── docker-compose.yml  # Orquestra frontend e backend
└── README.md
```

---

## 🛠️ Como rodar o projeto

### 🔁 Clonar o repositório

```bash
git clone <URL>
cd biblioteca-virtual
```

### 🐳 Requisitos

- [Docker](https://www.docker.com/)
- [VSCode](https://code.visualstudio.com/)
- Extensão: **Dev Containers**

---

### ✅ Rodar com Docker

```bash
docker compose up --build
```

- Frontend: http://localhost:5173  
- Backend: http://localhost:3000

---

### 💻 Usar com DevContainer (VSCode)

1. Abra a pasta no VSCode
2. Clique em "Reabrir no Container"
3. Pronto! Ambiente com todas as extensões, dependências e acesso ao banco

---

## 🔐 Variáveis de ambiente

> Configuradas no `backend/.env` (exemplo abaixo):

```env
PORT=3000
DATABASE_PATH=./database/database.sqlite
```

> O container também usa esse caminho por padrão.

---

## 🗂️ Scripts úteis

No **frontend**:

```bash
npm run dev       # inicia o Vite
npm run build     # build de produção
npm run preview   # preview do build
```

No **backend**:

```bash
node index.js     # inicia a API Express
```

---

## 🧹 Gitignore inteligente

O projeto ignora:

- `node_modules/`
- `dist/`, `.vite/`
- Arquivos `.sqlite`
- `.env`, `.log`
- `.vscode/`, `.DS_Store`

---

## 👨‍👩‍👧‍👦 Contribuição

Pull Requests são bem-vindos!

---