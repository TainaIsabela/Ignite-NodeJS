# Chapter 6 do Ignite Trilha NodeJS

<img alt="Ignite" src="./assets/cover-node.js.png" />

<h3 align="center">
  Chapter 06: Construindo com serveless
</h3>

<p align="center">“Você pode criar qualquer coisa: basta escrever”</blockquote>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/TainaIsabela/https://github.com/TainaIsabela/Ignite-Node-Desafio-6?style=flat">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Tainá Isabela" src="https://img.shields.io/badge/made%20by-Tainá%20Isabela-orange">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/rocketseat-education/ignite-nodejs-serverless/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/rocketseat-education/ignite-nodejs-serverless?style=social">
  </a>
</p>


<p align="center">
  <a href="#Tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-sobre-o-desafio">Descrição do desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Sobre-as-rotas">Sobre as rotas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#keyboard-instalação-e-execução-do-projeto">Instalação e Execução do Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#template-da-aplicação">Template da aplicação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## ✨ Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [Node.js](https://nodejs.org/en/)
- [Typescript](https://www.typescriptlang.org/)
- [Serverless Framework](serverless.com/)
- [Amazon Lambda](https://aws.amazon.com/pt/lambda/)



## :rocket: Sobre o desafio

Nesse desafio você irá recriar uma parte da API de *todos* que foi desenvolvida no desafio [Conceitos do Node.js](https://www.notion.so/Desafio-01-Conceitos-do-Node-js-59ccb235aecd43a6a06bf09a24e7ede8) mas dessa vez deverá ser usado o framework [Serverless](https://www.serverless.com/).

Cada funcionalidade deverá ser criada em um arquivo de função separada de acordo com o que foi visto nesse último módulo.
As rotas que deverão existir são:

**POST -** `/todos/{userid}`

**GET-** `/todos/{userid}`

O projeto tem como responsabilidade gerar um certificado para um usuário e a possibilidade de pesquisar a validade de um certificado.

## Sobre as rotas

- **POST -** `/todos/{userid}`
    
    Essa rota deve receber o `id` de um usuário pelo `pathParameters` (você pode criar esse id manualmente apenas para preencher o campo) e os seguintes campos no corpo da requisição: `title` e `deadline`, onde `deadline` é a data limite para o *todo*.
    
    O *todo* deverá ser salvo com os seguintes campos no DynamoDB:
    
    ```json
    { 
    	id: 'uuid', // id gerado para garantir um único todo com o mesmo id
    	user_id: 'uuid' // id do usuário recebido no pathParameters
    	title: 'Nome da tarefa',
    	done: false, // inicie sempre como false
    	deadline: new Date(deadline)
    }
    ```
    
- **GET-** `/todos/{userid}`
    
    Essa rota deve receber o `id` de um usuário pelo `pathParameters` (o mesmo id que foi usado para criar algum *todo*).
    
    A rota deve retornar os *todos* que possuírem o `user_id` igual ao `id` recebido pelos parâmetros.

### :keyboard: Instalação e Execução do Projeto

- Clone este repositório

```
> git clone https://github.com/TainaIsabela/Ignite-Node-Desafio-4.git
```

- Navegue até o diretório principal do projeto

```
> cd ignite-template-corrigindo-o-codigo
```

- Instale as dependências com o Yarn

```
yarn
```

### Template da aplicação

Foi utilizado um modelo de template que possui o esqueleto do projeto.

O template pode ser encontrado na seguinte url: **[Acessar Template](https://github.com/rocketseat-education/ignite-template-corrigindo-o-codigo)**

> **Dica**: Caso não saiba utilizar repositórios do Github como template, utilize o guia em **[nosso FAQ](https://www.notion.so/ddd8fcdf2339436a816a0d9e45767664).**

Agora navegue até a pasta criada e abra no Visual Studio Code, lembre-se de executar o comando `yarn` no seu terminal para instalar todas as dependências.



## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](https://github.com/git/git-scm.com/blob/master/MIT-LICENSE.txt) para mais detalhes.

---

Feito com 💜 by <a href="https://www.linkedin.com/in/taina-isabela/">Tainá Isabela</a> :wave:
