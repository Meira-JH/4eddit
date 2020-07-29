
# 4eddit
<p align="center">
<img src="https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/logo-future-eats-invert.png"/>
</p>

4eddit is a front-end development project of an imaginary web-desktop-first responsive application, as an activity result of Labenu's full-stack development course. This was a collective effort imagined, executed and revised by [Ana Kempfer](https://github.com/skempfer) and [me](https://github.com/Meira-JH).


## Tools and technologies

![Node.js environment](https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/EnvironmentNodejs.png)

![Languages JS CSS HTML](https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/languages.png)

![React Lib](https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/JSLibReactJS.png)

![Dev tools](https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/tools.png) 

![Layout tools](https://github.com/Meira-JH/futureEats/blob/master/futureEats/src/imgs/layout.png)

## The app

[Deploy]()

[API Documentation](https://documenter.getpostman.com/view/674905/SzYXXKEE?version=latest#08adf102-4d87-4f70-9dc3-b3c321b29739)

### Página de login


<p align="center">
<img height="400px" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c10d6996-4e20-45e8-a4aa-c1d7e4710fea/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200729%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200729T153108Z&X-Amz-Expires=86400&X-Amz-Signature=046745aa808ff18376a8edcde91767f76b9d73dbd2dee61cbcbedd2883e72c05&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22"/>
</p>

A página de login possui dois campos de texto: email e senha. O comportamento será o mesmo da página de login feita semana passada. Ao fazer o login, o usuário deverá ser redirecionado para a página de feed.

A página possui também um botão "Cadastrar", que leva o usuário para a página de cadastro.

### Página de cadastro

<p align="center">
<img height="400px" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/74892eaa-2276-42fc-8a0d-7ad3295f413c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200729%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200729T153044Z&X-Amz-Expires=86400&X-Amz-Signature=44350818f780c9e9cbd3d79e1d7d092fe79f14810316a387b30c2be31750d7f4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22"/>
</p>

A página de cadastro possui 3 campos: nome de usuário, email e senha. O endpoint de cadastro retornará as mesmas informações do endpoint de login. Portanto, após cadastrar, o usuário deverá ser redirecionado para a página de feed, já estando logado (ou seja, com o token salvo no LocalStorage).

### Página de feed (lista de posts)

<p align="center">
<img height="400px" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/38b78c1b-6bb4-4fb7-844b-991ed9f199da/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200729%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200729T152910Z&X-Amz-Expires=86400&X-Amz-Signature=3d896d6c137b0d6440e31200748053ea04382faa36142d130d7b66905f2e23cf&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22"/>
</p>

A página de feed deverá mostrar todos os posts, além de um formulário para a criação de post. O formulário possui apenas o campo de texto. Cada post mostrará o nome de usuário que postou, o texto do post, o número de votos (positivo ou negativo) e o número de comentários. Caso o usuário tenha votado positiva ou negativamente, isso deverá estar indicado. Todas essa informações serão fornecidas pela API.

Quando o usuário clicar em um post, ele deverá ser redirecionado para a página do respectivo post. 

Quando um usuário clicar em votar (positiva ou negativamente), uma requisição deverá ser feita indicando a "direção" do voto. Um voto positivo é indicado com o número `1`. Um voto negativo é indicado com o número `-1`. Para remover um voto, a direção deve ser `0`.

Essa página só pode ser acessada por um usuário logado. Caso o usuário não esteja logado, deverá ser redirecionado para a página de login.

### Página de post

<p align="center">
<img height="400px" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/38b78c1b-6bb4-4fb7-844b-991ed9f199da/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200729%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200729T152910Z&X-Amz-Expires=86400&X-Amz-Signature=3d896d6c137b0d6440e31200748053ea04382faa36142d130d7b66905f2e23cf&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22"/>
</p>

A página de um post mostrará o mesmo card de post da página de feed, com o usuário, texto, curtidas e número de comentários. Abaixo, terá um formulário para criação de comentários e os cards de comentários. A estrutura é muito similar à do post, mas comentários não possuem outros comentários dentro deles. A lógica de votos é a mesma do post.

Essa página só pode ser acessada por um usuário logado. Caso o usuário não esteja logado, deverá ser redirecionado para a página de login.


## Running the app

On your terminal, type:

```
git clone 
```

Install dependencies:
```
npm install
```

Execute the application:
```
npm start 
```

## Contributing
This was a collective effort imagined, executed and revised by [Ana Kempfer](https://github.com/skempfer) and [me](https://github.com/Meira-JH).

<p align="center">
<img src="https://uploads-ssl.webflow.com/5e790d30d198385b09366d8f/5eb17dfd4a07be86d2b8951e_Labenu_principal_slogan.png"/>
</p>

## License
[MIT License](https://choosealicense.com/licenses/mit/)
