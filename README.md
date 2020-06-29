# Labenu | Full-Stack Web Development Bootcamp
Desenvolvimento de aplicações completas, incluindo frontend Web com React e backend com Node.js.

![Screenshot_1](https://user-images.githubusercontent.com/45580434/79641791-06e1c100-8170-11ea-8ecf-b6c889805d55.png)
<br>

## Projeto: 4eddit

Site do projeto: [link](http://4eddit-sagan3.surge.sh/)

Documentação da API: [link](https://documenter.getpostman.com/view/674905/SzYXXKEE?version=latest#08adf102-4d87-4f70-9dc3-b3c321b29739)


**Versão Web**
<p align="center">
<img  height='400' src='https://user-images.githubusercontent.com/45580434/78464868-deb08780-76c4-11ea-853a-ad3b7c050ee0.gif'>
</p>


**Versão mobile**
<p align="center">
  <img  height='400' src='https://user-images.githubusercontent.com/45580434/78464747-77de9e80-76c3-11ea-9329-1e083568e5b1.gif'>
</p>

<br>

## Escopo

Iremos implementar um rede social realmente funcional (com cadastro, login, posts, likes e comentários) baseada no **[reddit.com](https://reddit.com).**

_OBS_: A disposição dos elementos nos wireframes abaixo é só uma sugestão. Vocês podem fazer o layout e organização como bem entenderem.

A rede social terá 4 páginas:

<br>

### Página de login

<p align="center">
<img  height='400' src='https://user-images.githubusercontent.com/3521896/77802249-3ada3280-7059-11ea-9da7-5762c6daf97d.png'>
</p>

A página de login possui dois campos de texto: email e senha. Comportamento esperado: ao fazer o login, o usuário deverá ser redirecionado para a página de feed.

A página possui também um botão "Cadastrar", que leva o usuário para a página de cadastro.

<br>

### Página de cadastro

<p align="center">
<img  height='400' src='https://user-images.githubusercontent.com/3521896/77802253-3ca3f600-7059-11ea-8bc9-e43db687e62c.png'>
</p>

A página de cadastro possui 3 campos: nome de usuário, email e senha. O endpoint de cadastro retornará as mesmas informações do endpoint de login. Portanto, após cadastrar, o usuário deverá ser redirecionado para a página de feed, já estando logado (ou seja, com o token salvo no LocalStorage).

<br>

### Página de feed (lista de posts)

<p align="center">
<img  height='400' src='https://user-images.githubusercontent.com/3521896/77802257-3e6db980-7059-11ea-9978-cc4612e444a1.png'>
</p>

A página de feed deverá mostrar todos os posts, além de um formulário para a criação de post. O formulário possui apenas o campo de texto. Cada post mostrará o nome de usuário que postou, o texto do post, o número de votos (positivo ou negativo) e o número de comentários. Caso o usuário tenha votado positiva ou negativamente, isso deverá estar indicado. Todas essa informações serão fornecidas pela API.

Quando o usuário clicar em um post, ele deverá ser redirecionado para a página do respectivo post. 

Quando um usuário clicar em votar (positiva ou negativamente), uma requisição deverá ser feita indicando a "direção" do voto. Um voto positivo é indicado com o número `1`. Um voto negativo é indicado com o número `-1`. Para remover um voto, a direção deve ser `0`.

Essa página só pode ser acessada por um usuário logado. Caso o usuário não esteja logado, deverá ser redirecionado para a página de login.

<br>

### Página de post

<p align="center">
<img  height='400' src='https://user-images.githubusercontent.com/3521896/77802261-40377d00-7059-11ea-8f65-2b305bf5e6f8.png'>
</p>

A página de um post mostrará o mesmo card de post da página de feed, com o usuário, texto, curtidas e número de comentários. Abaixo, terá um formulário para criação de comentários e os cards de comentários. A estrutura é muito similar à do post, mas comentários não possuem outros comentários dentro deles. A lógica de votos é a mesma do post.

Essa página só pode ser acessada por um usuário logado. Caso o usuário não esteja logado, deverá ser redirecionado para a página de login.


## Desafios

1. Garantir responsividade em todas as páginas, usar media queries, comparar a como o Reddit de verdade se comporta. Fazer deploy no surge e usar os celulares de verdade para testar as páginas.

2. Implementar funcionalidade de Logout.

3. Implementar funcionalidade de "Compartilhar", que permite mandar o post para outra rede social.

4. Implementar busca por nome/texto do post no feed.

5. Implementar loading em todas as páginas que esperam dados da API (lista de posts, detalhe de post, criação de post)

_OBS_: Todos os desafios foram implementados. 