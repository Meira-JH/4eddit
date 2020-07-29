
# 4eddit
<p align="center">
<img src="https://github.com/Meira-JH/4eddit/blob/master/src/img/logo.png"/>
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
<img height="400px" src="https://github.com/Meira-JH/4eddit/blob/master/src/img/localhost_3000_(iPad)%20(4).png"/>
</p>

A página de login possui dois campos de texto: email e senha. O comportamento será o mesmo da página de login feita semana passada. Ao fazer o login, o usuário deverá ser redirecionado para a página de feed.

A página possui também um botão "Cadastrar", que leva o usuário para a página de cadastro.

### Página de cadastro

<p align="center">
<img height="400px" src="https://github.com/Meira-JH/4eddit/blob/master/src/img/localhost_3000_(iPad)%20(2).png"/>
</p>

A página de cadastro possui 3 campos: nome de usuário, email e senha. O endpoint de cadastro retornará as mesmas informações do endpoint de login. Portanto, após cadastrar, o usuário deverá ser redirecionado para a página de feed, já estando logado (ou seja, com o token salvo no LocalStorage).

### Página de feed (lista de posts)

<p align="center">
<img height="400px" src="https://github.com/Meira-JH/4eddit/blob/master/src/img/localhost_3000_(iPad).png"/>
</p>

A página de feed deverá mostrar todos os posts, além de um formulário para a criação de post. O formulário possui apenas o campo de texto. Cada post mostrará o nome de usuário que postou, o texto do post, o número de votos (positivo ou negativo) e o número de comentários. Caso o usuário tenha votado positiva ou negativamente, isso deverá estar indicado. Todas essa informações serão fornecidas pela API.

Quando o usuário clicar em um post, ele deverá ser redirecionado para a página do respectivo post. 

Quando um usuário clicar em votar (positiva ou negativamente), uma requisição deverá ser feita indicando a "direção" do voto. Um voto positivo é indicado com o número `1`. Um voto negativo é indicado com o número `-1`. Para remover um voto, a direção deve ser `0`.

Essa página só pode ser acessada por um usuário logado. Caso o usuário não esteja logado, deverá ser redirecionado para a página de login.

### Página de post

<p align="center">
<img height="400px" src="https://github.com/Meira-JH/4eddit/blob/master/src/img/localhost_3000_feed(iPad).png"/>
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
