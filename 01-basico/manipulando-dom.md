# Manipulando DOM com o jquery

Com o jquery, é bem mais prático manipular a DOM do que com JavaScript Vanilla.

Vamos ver como podemos capturar eventos no jquery.

No html vamos fazer um cubo com um texto dentro, e vamos estiliza-lo dentro do html mesmo:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Manipulando a DOM com Jquery!</title>
    <style type="text/css">
      .box{
        width:100px;
        height:100px;
        background-color:blue;
      }
    </style>

  </head>
  <body>
    <div class="box">
      <p>Passa o mouse aqui!</p>
    </div>
    <!--CDN do jquery-->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script></script>
  </body>
</html>
```

Agora você vai dar seus primeiros comandos com jquery!

```js
<script>
	$('.box').hover(() => {
		$('p').text('O mouse está em cima da caixa!')
	});
	$( ".box" ).mouseleave(() => {
		$('p').text('Passe o mouse aqui!');
	});
</script>

```

Caso não tenha entendido nada desse código, calma que agora vou esplicar!


Para você pegar uma classe, tag, ou id do HTML no jquery, utilizamos o $ que seria basicamente um:

```js
document.querySelector(".box")
```

Depois de pegarmos a classe chamamos uma função do jquery, o hover. Que seria basicamente quando o mouse estiver em cima do elemento.
```js
$('.box').hover(() => {
	$('p').text('O mouse está em cima da caixa!')
});
```

Fizemos uma arrow function e retornamos outra função do jquery, a text.

A função text, ela pode mudar o texto de um elemento.

Fizemos a mesma coisa com o techo de código abaixo:

```js
$( ".box" ).mouseleave(() => {
	$('p').text('Passe o mouse aqui!');
});
```
Neste segundo trecho de código, mudamos a função hover para afunção mouseleave, que é quando o mouse está fora de um elemento.

---

Caso tenha alguma duvida você pode acessar a -> [documentação oficial do jquery](https://api.jquery.com/category/events/mouse-events/) <-
