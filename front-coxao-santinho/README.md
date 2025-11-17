


---

# 🧦 Frontend - Sistema de Estoque “coxão do santinho” (React + Axios)

Este é o frontend em React para o sistema de controle de estoque da empresa **“coxão do santinho”**, que auxilia na gestão de produtos (utensílios de academia) e nos empréstimos realizadas pelos **usuários**.

A aplicação utiliza **Axios** para consumir o backend REST (Node + Express + PostgreSQL) e **Vite** para o ambiente de desenvolvimento rápido e simples.

---

## 🚀 Tecnologias

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-264de4?style=for-the-badge&logo=css3&logoColor=white)

---

## 🎯 Funcionalidades

- Login de divulgadores com autenticação simples
- Cadastro, edição e exclusão de produtos (modelos de meia)
- Busca dinâmica de produtos (`/produtos?q=nome`)
- Registro de movimentações de **entrada** e **saída** de produtos
- Alerta automático de **estoque abaixo do mínimo**
- Listagem alfabética de produtos com indicação de estoque baixo
- Interface única e intuitiva (SPA)

---

## 🛠️ Pré-requisitos

- **Node.js** instalado
- **Backend** da “meia meia meia” em execução (porta padrão: `http://localhost:3000`)
  - Backend sugerido: Node + Express + PostgreSQL  
  - Banco: `saep_db`  
  - Tabelas: `usuarios`, `produtos`, `movimentacoes`

---

## 📦 Instalação e execução

```bash
git clone https://github.com/seu-usuario/meia-meia-meia-estoque.git
cd meia-meia-meia-estoque
npm install
npm run dev
````

O frontend será iniciado em **[http://localhost:5173](http://localhost:5173)** (padrão do Vite).

---

## 🧪 Estrutura de diretórios

```
src/
├── App.jsx         # Componente principal (SPA) com todas as interfaces da prova
├── App.css         # Estilização da aplicação
├── index.css       # Estilo global
├── main.jsx        # Entrada da aplicação
```

---

## 🔗 Rotas esperadas no backend

O frontend consome o backend em `http://localhost:3000` com as seguintes rotas REST:

### 🔐 Autenticação

* `POST /auth/login` — Login de divulgadores

### 👥 Usuários

* `POST /usuarios` — Cadastro de novo divulgador

### 🧦 Produtos

* `GET /produtos` — Lista todos os produtos
* `GET /produtos?q=nome` — Busca por nome (sem `unaccent`)
* `POST /produtos` — Cadastra novo produto
* `PUT /produtos/:id` — Atualiza produto existente
* `DELETE /produtos/:id` — Remove produto

### 🔄 Movimentações

* `POST /movimentacoes` — Registra entrada/saída e atualiza o saldo
* `GET /movimentacoes?produto_id=` — Lista histórico geral ou filtrado

---

## 💡 Dica para alunos

Toda a prova prática pode ser resolvida **com apenas uma página React** (`App.jsx`), alternando seções com `useState`.
Isso simplifica a manutenção e permite evoluir o projeto facilmente depois, caso se queira separar as telas.

---

## 📄 Licença

Este projeto está sob a licença MIT.

---

Feito com 🖤 por [rafaellindemann](https://github.com/rafaellindemann)

---


