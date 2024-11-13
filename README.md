**Nome do Projeto:** **StockMaster**  
Um sistema de inventário robusto e escalável para gestão de produtos, categorias e fornecedores, ideal para pequenas empresas acompanharem seus estoques e tomarem decisões estratégicas.

---

## 📋 Descrição

**StockMaster** é um sistema de inventário projetado para pequenas empresas gerenciarem eficientemente seu estoque. Com ele, os usuários podem cadastrar produtos, acompanhar o nível de estoque, registrar movimentações e receber alertas de produtos com estoque baixo. O sistema foi projetado com uma arquitetura escalável que permite a adição de novas funcionalidades e integração com APIs de fornecedores ou de logística.

---

## 🚀 Funcionalidades

**Etapa Básica:**
- Cadastro de Produtos com CRUD completo.
- Cadastro e gerenciamento de Categorias.
- Controle de Estoque com adição e remoção de produtos.
  
**Etapa Intermediária:**
- Alerta de Estoque Baixo via e-mail.
- Histórico de Movimentação de Estoque.
- Relatórios básicos de produtos e estoque.

**Etapa Avançada:**
- Cadastro de Fornecedores com vinculação a produtos.
- Integração com APIs de Logística para atualização de pedidos.
- Dashboard com gráficos e análises.
- Sistema de Permissões de Usuário (Admin e Colaborador).

---

## 🛠️ Tecnologias Utilizadas

- **Backend**: Node.js, Express
- **Banco de Dados**: MongoDB
- **Notificações**: Nodemailer para envio de e-mails
- **Logs**: Winston para registro de logs de movimentação
- **Frontend**: HTML, CSS e JavaScript
- **Dashboard** (Etapa Avançada): Chart.js ou similar para gráficos

---

## 📁 Estrutura de Pastas

```
/stockmaster
|-- /backend                # API e servidor backend
|   |-- /config             # Configuração de banco de dados e variáveis de ambiente
|   |-- /controllers        # Lógica de controle para produtos, categorias, etc.
|   |-- /models             # Modelos de dados (Produto, Categoria, etc.)
|   |-- /routes             # Rotas da API para cada funcionalidade
|   |-- /middleware         # Middlewares para autenticação, etc.
|   |-- /utils              # Utilitários, como envio de e-mail e logs
|-- /frontend               # Interface HTML/CSS/JS
|   |-- /css                # Estilos da interface
|   |-- /js                 # Scripts de JavaScript
|   |-- /pages              # Páginas HTML
|-- README.md               # Documentação do projeto
|-- .env                    # Variáveis de ambiente (não incluir no Git)
|-- package.json            # Dependências e scripts npm
```

---

## 📌 Pré-requisitos

- **Node.js** e **npm** instalados
- **MongoDB** (local ou MongoDB Atlas)
- Configuração de variáveis de ambiente (`.env`) para conexões e dados de e-mail.

---

## 📦 Instalação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/sua-conta/stockmaster.git
   cd stockmaster
   ```

2. **Instale as dependências do backend:**
   ```bash
   cd backend
   npm install
   ```

3. **Configure as variáveis de ambiente no arquivo `.env`:**
   ```plaintext
   DB_URI=mongodb://seu_banco_de_dados
   EMAIL_USER=seu_email_para_envio
   EMAIL_PASS=sua_senha_do_email
   ```

4. **Inicie o servidor:**
   ```bash
   npm start
   ```

5. **Abra o frontend** no navegador, acessando os arquivos HTML diretamente ou via um servidor local.

---

## 🎯 Endpoints da API

- **Produtos**
  - `POST /api/produtos` - Adicionar novo produto
  - `GET /api/produtos` - Listar todos os produtos
  - `PUT /api/produtos/:id` - Atualizar um produto
  - `DELETE /api/produtos/:id` - Excluir um produto

- **Categorias**
  - `POST /api/categorias` - Adicionar nova categoria
  - `GET /api/categorias` - Listar todas as categorias
  - `PUT /api/categorias/:id` - Atualizar uma categoria
  - `DELETE /api/categorias/:id` - Excluir uma categoria

- **Movimentações de Estoque**
  - `POST /api/movimentacoes` - Registrar entrada/saída de estoque
  - `GET /api/movimentacoes` - Listar movimentações

---

## ⚙️ Funcionalidades Futura (Roadmap)

- Integração com serviços de pagamento e APIs de fornecedores.
- Dashboard avançado com gráficos e relatórios.
- Exportação de dados em PDF ou CSV.
