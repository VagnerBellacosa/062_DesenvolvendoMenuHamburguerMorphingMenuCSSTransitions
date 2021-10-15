 [HOME](https://www.htmlecsspro.com/) [CSS](https://www.htmlecsspro.com/artigos/css) Efeito Menu Hamburger com CSS3

# Efeito Menu Hamburger com CSS3

[ CSS](https://www.htmlecsspro.com/artigos/css) Luiz Augusto Vieira  03/02/2018

![Efeito Menu Hamburger com CSS3](https://www.htmlecsspro.com/uploads/images/2018/03/efeito-menu-hamburger-com-css3-1522117178.png)

- **COMPARTILHE** ESSE POST
- [![Compartilhar no Facebook](https://www.htmlecsspro.com/_cdn/widgets/share/icons/facebook.png)00](https://www.facebook.com/sharer/sharer.php?u=https://www.htmlecsspro.com/artigo/efeito-menu-hamburger-com-css3)
- [![Compartilhar no Google Plus](https://www.htmlecsspro.com/_cdn/widgets/share/icons/googleplus.png)00](https://plus.google.com/share?url=https://www.htmlecsspro.com/artigo/efeito-menu-hamburger-com-css3)
- [![Compartilhar no Twitter](https://www.htmlecsspro.com/_cdn/widgets/share/icons/twitter.png)](https://twitter.com/intent/tweet?hashtags=BoraCodificar&url=https://www.htmlecsspro.com/artigo/efeito-menu-hamburger-com-css3&text=Efeito Menu Hamburger com CSS3)



Vamos ver neste post o poder do **CSS3** e como ele facilita nossa vida.

No nosso exemplo, vamos criar um efeito de um menu hamburger usando algumas propriedades do **CSS3**.

**1° Passo:**

```
.container{ position: relative;
 width: 60px;
 margin: 20px auto;
}
```

Criamos uma classe ( .container ) que envolverá todo o nosso conteúdo. Somente para centralizamos na tela do browser.

**2° Passo:**

```
.btn {
 position: absolute;
 width: 60px;
 height: 60px; top: 0; left: 0px;cursor: pointer;
}
```

Criamos uma classe ( .btn ) que será o nosso botão.

**3° Passo:**

```
.btn-left {
 background-color: #333;
 position: absolute;
 height: 8px;
 width: 30px;
 top: 30px;
 left: 0px;
 -webkit-transition-duration: 0.5s;
 transition-duration: 0.5s;
}
```

Criamos uma classe ( .btn-left ) e definimos a largura ( width ) com 30px, ou seja a metade da nossa classe ( .btn ).

**4° Passo:**

```
.btn-right {
  background-color: #333;
  position: absolute;
  height: 8px;
  width: 30px;
  top: 30px;
  left: 30px;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
```

Criamos uma classe ( .btn-right ) e definimos a largura ( width ) com 30px, ou seja a metade da nossa classe ( .btn ) e deslocamos ela para a direita no ( left ) de 30px para ocupar o espaço faltante.

**5° Passo:**

```
.btn-left:before {
  background-color: #333;
  position: absolute;
  width: 30px;
  height: 8px;
  content: "";
  top: -20px;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
```

Criamos uma classe com as mesmas características da classe ( .btn-left ) utilizando o Pseudo Elementos ( :before ) e definimos o ( top: -20px ), isso vai deixar nossa classe 20px acima da classe ( .btn-left ) formando uma barra de com a largura de 30px.

**6° Passo:**

```
.btn-left:after {
  background-color: #333;
  position: absolute;
  width: 30px;
  height: 8px;
  content: "";
  top: 20px;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
```

Criamos uma classe com as mesmas características da classe ( .btn-left ) utilizando o Pseudo Elementos ( :after ) e definimos o ( top: 20px ), isso vai deixar nossa classe 20px abaixo da classe ( .btn-left ) formando uma barra de com a largura de 30px.

**7° Passo:**

```
.btn-right:before {
  background-color: #333;
  position: absolute;
  width: 30px;
  height: 8px;
  content: "";
  top: -20px;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
```

Criamos uma classe com as mesmas características da classe ( .btn-right ) utilizando o Pseudo Elementos ( :before ) e definimos o ( top: -20px ), isso vai deixar nossa classe 20px acima da classe ( .btn-right ) formando uma barra de com a largura de 30px.

**8° Passo:**

```
.btn-right:after {
  background-color: #333;
  position: absolute;
  width: 30px;
  height: 8px;
  content: "";
  top: 20px;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
```

Criamos uma classe com as mesmas características da classe ( .btn-right ) utilizando o Pseudo Elementos ( :after ) e definimos o ( top: 20px ), isso vai deixar nossa classe 20px abaixo da classe ( .btn-right ) formando uma barra de com a largura de 30px.

**9° Passo:**

```
.active .btn-left {
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
  background: transparent;
}
```

Perceba que agora temos uma classe chamada de ( .active ) pois ela será adicionado ao nosso **HTML** via jQuery ( veremos mais a frente ), assim que essa classe é inserida, ela vai invocar os comandos acima e tirar a cor de fundo da classe ( .btn-left ), deixando a mesma invisível na tela.

**10° Passo:**

```
.active .btn-left:before {
  -webkit-transform: rotateZ(45deg) scaleX(1.4) translate(4px, 4px);
  transform: rotateZ(45deg) scaleX(1.4) translate(4px, 4px);
}
```

Aqui vamos atacar a nossa classe criada com o Pseudo Elementos ( :before ) com a propriedade ( transform: ) do **CSS3**.

rotateZ(45deg) – Define uma rotação 3D ao longo do eixo Z;
scaleX(1.4) – Define uma transformação de escala, dando um valor para o eixo X;
translate(4px, -4px) – Define uma tradução em 2D, vai posicionar a classe nas posições ( top e left ).

**11° Passo:**

```
.active .btn-left:after {
  -webkit-transform: rotateZ(-45deg) scaleX(1.4) translate(4px, -4px);
  transform: rotateZ(-45deg) scaleX(1.4) translate(4px, -4px);
}
```

Atacamos agora a nossa classe criada com o Pseudo Elementos ( :after ) com a propriedade ( transform: ) do **CSS3**.

Perceba que mudamos apenas dois valores ( rotateZ(-45deg) ) e ( translate(4px, -4px) ), agora precisamos colocar valores negativos para termos um efeito ao contrário.

**12° Passo:**

```
.active .btn-right {
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
  background: transparent;
}
```

Nessa parte faremos o mesmo processo do 9° Passo, vamos invocar os comandos acima e tirar a cor de fundo da classe ( .btn-right ), deixando a mesma invisível na tela.

**13° Passo:**

```
.active .btn-right:before {
  -webkit-transform: rotateZ(-45deg) scaleX(1.4) translate(-4px, 4px);
  transform: rotateZ(-45deg) scaleX(1.4) translate(-4px, 4px);
}
```

Vamos atacar o Pseudo Elementos ( :before ) para fazer os efeitos.

**14° Passo:**

```
.active .btn-right:after {
  -webkit-transform: rotateZ(45deg) scaleX(1.4) translate(-4px, -4px);
  transform: rotateZ(45deg) scaleX(1.4) translate(-4px, -4px);
}
```

Vamos atacar o Pseudo Elementos ( :after ), mudamos apenas os velores de ( rotateZ ) e ( translate ).

**15° Passo:**

```
<!DOCTYPE html>
<html>
  <head>
    <title>Efeito Menu Hamburger com CSS3</title>
  </head>
 
  <body>
 
    <div class="container">
      <div class="btn">
        <div class="btn-left"></div>
        <div class="btn-right"></div>
      </div>
    </div>
 
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
 
  </body>
</html>
```

Acima está nosso **HTML** para o exemplo. Foi incluída a biblioteca do **jQuery**, pois vamos utilizá-los para incluir a classe ( .active ) responsável pelos efeitos.

**16° Passo:**

```
$('.btn').click(function () {
  $(this).toggleClass('active');
});
```

Acima está nosso **jQuery**, ele que vai adicionar e remover nossa classe ( .active ) ao clicar no botão.

Veja o resultado final: