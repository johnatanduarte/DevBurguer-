# Protótipo de Cardápio Digital - DevBurger

Este projeto é um protótipo de servidor backend para a hamburgueria fictícia "DevBurger". Desenvolvido com **Node.js** e **Express**, o servidor é capaz de servir páginas HTML estáticas, processar formulários e fornecer uma API JSON simples com o cardápio.

## 🚀 Funcionalidades Implementadas

* **Servidor Web:** Utiliza Express para criar e gerenciar o servidor.
* **Serviço de Páginas:** Serve as páginas principais da aplicação (`index.html` e `contato.html`).
* **Processamento de Formulários:**
    * **Sugestão (GET):** Captura dados de sugestão de lanche (nome, ingredientes) enviados via *query string* (`GET /sugestao`) e retorna uma página de agradecimento dinâmica.
    * **Contato (POST):** Captura dados de contato (nome, email, etc.) enviados no corpo da requisição (`POST /contato`) e retorna uma página de confirmação dinâmica.
* **API de Cardápio:** Expõe a rota `GET /api/lanches` que retorna um arquivo JSON estático com a lista de hambúrgueres.
* **Arquivos Estáticos:** Serve arquivos como CSS, imagens e o JSON do cardápio diretamente da pasta `public`.
* **Tratamento de Erro 404:** Exibe uma página de erro personalizada (`404.html`) caso uma rota não seja encontrada.

## 🛠️ Tecnologias Utilizadas

* **Node.js**
* **Express.js**

## 🏁 Como Executar o Projeto

1.  **Clone o repositório** .

2.  **Instale as dependências:**
    Abra o terminal na raiz do projeto e execute:
    ```bash
    npm install
    ```

3.  **Inicie o servidor:**
    ```bash
    npm start
    ```
    Este comando executará o script definido no `package.json`, que por sua vez executa `node server.js`.

4.  **Acesse a aplicação:**
    O servidor estará rodando em `http://localhost:3000`.

## 🗺️ Rotas da Aplicação

O `server.js` define as seguintes rotas:

| Método | Rota | Descrição |
| :--- | :--- | :--- |
| `GET` | `/` | Serve a página principal (`views/index.html`), que contém o formulário de sugestão. |
| `GET` | `/contato` | Serve a página de contato (`views/contato.html`). |
| `GET` | `/sugestao` | **Rota de Processamento.** Recebe dados (`nome`, `ingredientes`) via `req.query` e retorna um HTML de agradecimento. |
| `POST` | `/contato` | **Rota de Processamento.** Recebe dados (`nome`, `email`, etc.) via `req.body` e retorna um HTML de confirmação. |
| `GET` | `/api/lan
