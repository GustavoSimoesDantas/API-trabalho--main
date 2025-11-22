# Projeto Loja - API

## 📌 Nome do Projeto

API LOJA

---

## 🛠 Tecnologias Utilizadas

- **Node.js**
- **Express.js**
- **MongoDB**
- **Mongoose**
- **Nodemon** (ambiente de desenvolvimento)
- **Insomnia/Postman** (testes de API)

---

## 📝 Explicação e Descrição do Sistema

Esta API foi desenvolvida para gerenciar uma loja, permitindo o controle de produtos, clientes, pedidos e outras entidades relacionadas. O sistema segue a arquitetura REST e utiliza o MongoDB como banco de dados NoSQL.

O objetivo é oferecer um conjunto de endpoints que possibilitam o CRUD completo das collections, mantendo uma estrutura organizada, escalável e fácil de manter.

---

## ✨ Funcionalidades Implementadas

- Cadastro, listagem, atualização e remoção de **produtos**.
- Cadastro, listagem, atualização e remoção de **clientes**.
- Cadastro e gerenciamento de **pedidos**.
- Relacionamento entre collections, como associação de pedidos aos clientes e produtos.
- Validações básicas dos dados recebidos.

---

## 📡 Endpoints da API (com exemplos)

### 🔹 Produtos

#### **GET /produtos**

Retorna todos os produtos.

**Resposta:**

```json
[
  {
    "_id": "123",
    "nome": "Camiseta",
    "preco": 49.9,
    "estoque": 10
  }
]
```

#### **POST /produtos**

**Requisição:**

```json
{
  "nome": "Camiseta",
  "preco": 49.9,
  "estoque": 10
}
```

**Resposta:**

```json
{
  "mensagem": "Produto criado com sucesso"
}
```

### 🔹 Clientes

#### **GET /clientes**

Retorna todos os clientes.

### 🔹 Pedidos

#### **POST /pedidos**

Cria um pedido associando cliente e produtos.

---

## 🧩 Diagrama de Modelagem

*(Inserir aqui a imagem do diagrama — adicione usando markdown quando disponível)*

Exemplo:

```
![Diagrama](./diagram.png)
```

---

## 🗂 Collections e Relacionamentos

### **Produtos**

- Campos: nome, preço, estoque

### **Clientes**

- Campos: nome, email, telefone

### **Pedidos**

- Campos: clienteId (referência), lista de produtos, data
- Relacionamento: Um cliente pode ter vários pedidos; cada pedido contém vários produtos.

---

## ⚙ Instalação, Configuração e Execução

### 1️⃣ Clonar o repositório

```
git clone https://github.com/Alexiesb/API-trabalho-
```

### 2️⃣ Instalar dependências

```
npm install
```

### 3️⃣ Configurar variáveis de ambiente

Criar um arquivo `.env` com:

```
MONGO_URI=sua-string-de-conexao
PORT=3000
```

### 4️⃣ Executar o servidor

```
npm run dev
```

---

## 🗄 Comunicação com o Banco de Dados

A conexão utiliza **Mongoose**:

```js
mongoose.connect(process.env.MONGO_URI)
  .then(() => console.log("MongoDB conectado"))
  .catch(err => console.log(err));
```

Operações CRUD são feitas através dos models definidos no diretório `src/models`.

---

## 👥 Integrantes

- Alexandre souza mendonça
- Denys wenceslau 
- Gabriel Ataides de sousa
- Gustavo simões dantas

---

## 🐙 Usuários do GitHub

- [**Alexiesb**](https://github.com/Alexiesb)
- GustavoSimoesDantas
- denyswenceslau1
- [**ataidesgabrielsousa-cyber**](https://github.com/ataidesgabrielsousa-cyber)

---

## 📌 Contribuições de Cada Membro

### 👤 Gabriel Ataides

- Controllers
- Readme

### 👤 Alexandre Souza

- Models
- Docs

### 👤 Gustavo Simões

- Routes

- Postman

### 👤 Denys Wenceslau

- Issues
- Validators




