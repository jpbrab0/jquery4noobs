# Manipulando atributos de uma tag HTML

Agora que ja sabemos alguns comandos do jquery, vamos ver como manipular atributos de uma tag HTML.

Antes de tudo vamos fazer o HTML para mostrar o como podemos manipular os atributos de um elemento HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Manipulando atributos de uma tag HTML</title>
    <style>
      div.box{
        width:110px;
        height:110px;
        background-color:yellow
      }
    </style>
  </head>
  <body>
    <div class="box"></div>
    <button>Adicionar ou remover cor!</button>
    <!--CDN do jquery-->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script></script>
  </body>
</html>
```

No javascript vamos manipular os atributos:

```js
$("button").click(function() {
  $('.box').toggleClass("blue")
})
```
O código acima ele faz com que, caso o botão seja clicado, a div com a classe "box" ela vai ser adicionada uma caso ainda não contenha  a classe, se ela tiver essa classe vai removida.

Ao inves de fazer esse "toggle", podemos simples mente adicionar uma classe:

```js
$("button").click(function() {
  $('.box').addClass("blue")
})
```


Ou remover ela:

```js
$("button").click(function() {
  $('.box').removeClass("blue")
})
```

Agora, caso a div .box esteja com a classe "blue" ela devera ficar azul.

Para isso podemos utilizar o Css

```css
div.blue{
  background-color:blue;
}
```