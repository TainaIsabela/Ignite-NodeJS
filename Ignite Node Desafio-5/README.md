# Chapter 5 do Ignite Trilha NodeJS

<img alt="Ignite" src="./assets/cover-node.js.png" />

<h3 align="center">
  Chapter 5: Transferências com a FinAPI
</h3>

<p align="center">“É genial festejar o sucesso, mas é mais importante aprender com as lições do fracasso.”</blockquote>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/TainaIsabela/https://github.com/TainaIsabela/Ignite-Node-Desafio-5?style=flat">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Tainá Isabela" src="https://img.shields.io/badge/made%20by-Tainá%20Isabela-orange">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/rocketseat-education/ignite-template-introducao-ao-SOLID/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/rocketseat-education/ignite-template-introducao-ao-SOLID?style=social">
  </a>
</p>


<p align="center">
  <a href="#rocket-sobre-o-desafio">Descrição do desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#keyboard-instalação-e-execução-do-projeto">Instalação e Execução do Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#template-da-aplicação">Template da aplicação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio você irá implementar uma nova funcionalidade na FinAPI, a aplicação que foi testada durante o desafio **[Testes unitários](https://www.notion.so/Desafio-01-Testes-unit-rios-0321db2af07e4b48a85a1e4e360fcd11)**.

A nova funcionalidade deverá permitir a transferência de valores entre contas. Para isso, você pode pensar na melhor forma de construir essa solução mas alguns requisitos deverão ser cumpridos:

- Não deve ser possível transferir valores superiores ao disponível no saldo de uma conta;
- O balance (obtido através da rota `/api/v1/statements/balance`) deverá considerar também todos os valores transferidos ou recebidos através de transferências ao exibir o saldo de um usuário;
- As informações para realizar uma transferência serão:
	```json
	{
		"amount": 100,
		"description": "Descrição da transferência"
	}
	```
	Você pode passar o id do usuário destinatário via parâmetro na rota (exemplo: /api/v1/statements/transfers/:user_id) e o id do usuário remetente poderá ser obtido através do token JWT enviado no header da requisição;

- Ao mostrar o balance de um usuário, operações do tipo `transfer` deverão possuir os seguintes campos:
    
    ```json
    {
      "id": "4d04b6ec-2280-4dc2-9432-8a00f64e7930",
    	"sender_id": "cfd06865-11b9-412a-aa78-f47cc3e52905"
      "amount": 100,
      "description": "Transferência de valor",
      "type": "transfer",
      "created_at": "2021-03-26T21:33:11.370Z",
      "updated_at": "2021-03-26T21:33:11.370Z"
    }
    ```
    
    Observe o campo `sender_id`. Esse deverá ser o `id` do usuário que enviou a transferência.
    O campo `type` também deverá exibir o tipo da operação, que nesse caso é `transfer`.

### :keyboard: Instalação e Execução do Projeto

- Clone este repositório

```
> git clone https://github.com/TainaIsabela/Ignite-Node-Desafio-5.git
```

- Navegue até o diretório principal do projeto

```
> cd Ignite-Node-Desafio-5
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
