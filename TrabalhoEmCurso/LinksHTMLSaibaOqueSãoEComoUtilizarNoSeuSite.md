# Links HTML: saiba o que são e como utilizar no seu site

Neste artigo, vamos entender o que são os links HTML, como surgiram, sua sintaxe e algumas formas de aplicação. Além disso, veremos diversos exemplos práticos, para você praticar e utilizar em suas páginas HTML.

Este artigo possui os seguintes tópicos:

- [O que são os links HTML](https://www.homehost.com.br/blog/tutoriais/links-html/#topico1)
- [O surgimento dos links HTML](https://www.homehost.com.br/blog/tutoriais/links-html/#topico2)
- [Como fazer um link em HTML](https://www.homehost.com.br/blog/tutoriais/links-html/#topico3)
- [Estilizando o link](https://www.homehost.com.br/blog/tutoriais/links-html/#topico4)
- [O atributo href](https://www.homehost.com.br/blog/tutoriais/links-html/#topico5)
- [O atributo target](https://www.homehost.com.br/blog/tutoriais/links-html/#topico6)
- [O atributo title](https://www.homehost.com.br/blog/tutoriais/links-html/#topico7)
- [Criando âncoras com os links HTML](https://www.homehost.com.br/blog/tutoriais/links-html/#topico8)
- [Link HTML para enviar um e-mail](https://www.homehost.com.br/blog/tutoriais/links-html/#topico9)
- [Link HTML para download de um arquivo](https://www.homehost.com.br/blog/tutoriais/links-html/#topico10)
- [Base link](https://www.homehost.com.br/blog/tutoriais/links-html/#topico11)
- [Links HTML em imagens](https://www.homehost.com.br/blog/tutoriais/links-html/#topico12)
- [Pratique você mesmo](https://www.homehost.com.br/blog/tutoriais/links-html/#topico13)



## O que são os links HTML

Desde a origem da internet, o que torna a web o que ela é hoje é justamente a possibilidade de vincular um documento a qualquer outro documento ou recurso. Essa função é chamada de hiperlink ou link. Mas afinal de contas, o que são os links HTML?

O link [HTML, nada mais é que uma função do HTML que permite inserir](https://www.homehost.com.br/blog/criar-sites/html-div/) os hiperlinks em diversos elementos, como textos e imagens. Um link precisa sempre apontar para uma URL (endereço) existente em seu site. Caso contrário, você poderá obter uma mensagem de [erro 404](https://www.homehost.com.br/blog/internet/erro-404-not-found/).

A [tag link do HTML](https://www.homehost.com.br/blog/criar-sites/tags-html/) está presente desde a primeira versão, criada por Tim Berners-Lee.

## O surgimento dos links HTML

Em 1980 o Fisico Britâncio [*Tim Berners-Lee*](https://www.internethalloffame.org//official-biography-tim-berners-lee) iniciou um projeto baseado no conceito de hipertexto denominado Enquire, desenvolvido inicialmente em linguagem Pascal. Anos mais tarde, Tim Berners-Lee e Robert Cailliau conseguiram implementar a primeira comunicação entre um cliente e um [servidor através](https://www.homehost.com.br/blog/criar-sites/servidor-web/) da internet, o protocolo HTTP. Em 1989, surgia então a World Wide Web (www).

Em conjunto à implementação da World Wide Web, Tim Berners-Lee lançou a linguagem HTML (HyperText Markup Language). A versão inicial do HTML foi baseada na SGML, uma linguagem de estruturação de documentos. Foi dele que o [HTML herdou diversas tags](https://www.homehost.com.br/blog/criar-sites/tags-html/) como as de título (<h1> a <h6>), de parágrafos (<p>) e a de cabeçalho (<head>). A maior diferença entre essas duas linguagens de marcação é que o HTML implementava a tag <a>, surgindo então o link HTML, que permitia a ligação de uma página a outra.

Certamente esse conceito de ligação entre um documento a outro é o grande diferencial e principal conceito que define a base do funcionamento da web.

## Como fazer um link em HTML

No HTML, os links são definidos pela tag <a>. Dentro dessa tag incluímos o atributo href (Hypertext Reference), que é o endereço de destino do link. Dentro do conteúdo da tag <a>, incluímos então o texto ou elemento que servirá como redirecionador, ou seja, que ao ser clicado, executará a função de redirecionar para o endereço dentro do atributo href.

Dessa forma, a sintaxe [básica do HTML](https://www.homehost.com.br/blog/criar-sites/html-basico/) link é:

```
<a href="url">Exemplo</a>
```

A tag <a> pode ser [utilizada dentro ou fora dos demais elementos do HTML](https://www.homehost.com.br/blog/criar-sites/html-css/), como no exemplo abaixo onde criamos um parágrafo, e dentro dele, apenas a palavra HomeHost contém um hiperlink para a página inicial da HomeHost:

```
<p>Seja redirecionado à página da 
<a href="https://www.homehost.com.br/">HomeHost</a></p>
```

Como resultado, teremos:

Seja redirecionado a página da [HomeHost](https://www.homehost.com.br/)

Viu como é simples?

## Estilizando o link

Por padrão, a tag <a> traz consigo o estilo próprio com o texto sublinhado e na cor azul, para links ainda não visitados, roxo para links visitados e vermelho para links ativos. Porém, podemos estilizar diretamente os links através do estilos inline ou dentro do elemento <style>. Dessa forma, podemos reiniciar o estilo da tag apenas aplicando “text-decoration:none”. Também podemos utilizar as pseudo classes do CSS. Você pode aprender mais neste outro artigo sobre a [tabela de cores HTML](https://www.homehost.com.br/blog/tutoriais/tabela-de-cores-html/).

Vejamos um exemplo de estilização CSS:

```
<style>
/*Link não visitado */
a:link {
  color: green;
  text-decoration: none;
}

/*Link já visitado*/
a:visited {
  color: blue;
  text-decoration: none;
}

/*Quando o mouse passa por cima*/
a:hover {
  color: pink;
  text-decoration: none;
}

/*Link ativo/selecionado*/
a:active {
  color: yellow;
  text-decoration: none;
}
</style>
```

Também poderíamos atribuir um estilo único para o elemento <a>, fazendo com que, independente da condição, ele receberia o mesmo estilo. Veja o exemplo a seguir:

```
<!DOCTYPE html>
<html>
<head>
<style>
    a{
        text-decoration: none;
        background-color: yellow;
        color: red;
        border: 1px solid blue
        padding:3px 5px;
    }
</style>
</head>

<body>
    <a href="">
        Meu link personalizado
    </a>
</body>
<html>
```

Com o código acima, aplicamos uma borda azul, um fundo na cor amarela e a cor vermelha para o texto. Aplicamos também um *padding* (espaçamento). Portanto, perceba que poderíamos aplicar qualquer propriedade para a tag <a>. Isso acontece pois o mesmo tem como padrão de display bloco. Portanto, vejamos resultado do código acima:

[Meu link personalizado](https://www.homehost.com.br/#)

## O atributo href

Através do atributo principal da tag <a>, o href=””, podemos redirecionar o usuário a outro documento ou recurso. Existem três diferentes tipos de links utilizados para redirecionamento dentro do href. Um link pode ser:

- interno: redireciona para um elemento existente dentro da mesma página;
- local: utilizados para páginas contendo o mesmo domínio, ou seja, entre páginas do mesmo site;
- global: utilizados para páginas de outros domínios, ou seja, fora do site.

Veja abaixo alguns exemplos de como podem ser utilizados:

```
Interno - <a href="#contato">Contato</a>
Redirecionará ao elemento âncora contato.

Local - <a href="../pages/pagina2.html">Pagina 2</a>
Redirecionará ao arquivo pagina2.html pertencente à pasta pages.

Global - <a href="http://www.google.com/">Google</a>
Redirecionará à pagina inicial do Google
```



## O atributo target

Além do atributo href, também podemos incluir o atributo target dentro da tag <a>. Esse atributo informa ao navegador como o redirecionamento deverá ocorrer, abrindo a página na mesma janela/aba do navegador ou abrindo uma nova janela/aba.

Os atributos target são:

- _blank: abre a página em uma nova janela/aba;
- _self: abre a página na mesma janela;
- _parent: abre a página na mesma janela do link;
- _top: cancela todos os demais frames e abre a nova página no mesmo navegador.

Com isso, veja o exemplo a seguir onde ao clicar no link, abrirá uma nova aba do navegador com a página inicial da HomeHost:

```
<a href="https://www.homehost.com.br/" target="_blank">
Página inicial da HomeHost</a>
```

Nesse exemplo temos o resultado:

[Página inicial da HomeHost](https://www.homehost.com.br/)



## O atributo title

O atributo title permite escrever um texto que aparecerá apenas quando passarmos o mouse por cima do link. Portanto, é um atributo importante que nos permite digitar informações úteis suplementares sobre o link, como o tipo de informação que a página contém ou avisos.

Veja um exemplo de como podemos utilizar esse atributo.

```
<a href="" title="Exemplo de como funciona o atributo title">
Confira como funciona o atributo title!
</a>
```

Com esse código, nosso resultado será:

Confira como funciona o atributo title!



## Criando âncoras com os links HTML

Conforme o que foi explicado no tópico “O atributo href”, uma das possibilidades de utilizar o link HTML é através do redirecionamento interno, processo que também é conhecido como âncora. Para isso, utilizamos a tag <a> para linkar duas seções da mesma página. Além disso, podemos nomear a seção ou atribuir um ID a um determinado elemento, e assim, através da âncora, acontecerá o redirecionamento ao elemento.

Um ótimo exemplo de utilização desse processo, se encontra no inicio desse artigo: ao clicar nos links de qualquer um dos tópicos, você é redirecionado para essa posição! Este recurso também é muito utilizado dentro de menus de páginas únicas e landing pages.

Confira o exemplo a seguir, utilizando como base o seguinte código:

```
<h1>Texto 1 de exemplo<a name="text1"></a></h1>
<h2>Texto 2 de exemplo<a name="text2"></a></h2>
<h2>Texto 3 de exemplo<a name="text3"></a></h2>
```

Agora vamos criar os links que ao serem clicados realizarão o redirecionamento para a posição do text1, do text2 e do text3:

```
<a href="#text1">Esse link leva ao Texto 1 de exemplo</a>
<a href="#text2">Esse link leva ao Texto 2 de exemplo</a>
<a href="#text3">Esse link leva ao Texto 3 de exemplo</a>
```

Confira os exemplos que deixamos para você testar essa funcionalidade:

[Redirecionar para o topo do artigo](https://www.homehost.com.br/blog/tutoriais/links-html/#topo)
[Redirecionar para o final do artigo](https://www.homehost.com.br/blog/tutoriais/links-html/#final)

## Link HTML de e-mail

Atualmente, o HTML é capaz de criar um link que redireciona para o envio de e-mail. [Para criar](https://www.homehost.com.br/blog/criar-sites/4-motivos-para-criar-site-com-homehost/) essa função, basta colocar dentro do atributo href o “mailto:” e separados por uma interrogação “?”, o “subject=”. O “mailto” deve conter o endereço ao qual será enviado o e-mail, o “subject=” nada mais é que o assunto. Vejamos então o exemplo abaixo:

```
<p><a href="mailto:exemplo@examplo.com?subject=Assunto" >Clique aqui</a>
para enviar um e-mail.</p>
```

O resultado dessa linha de código é:

[Clique aqui](mailto:exemplo@examplo.com?subject=Assunto) para enviar um e-mail.

Posteriormente, ainda podemos acrescentar um texto pré-estabelecido para o corpo do e-mail. Para isso acrescentamos ao código o “body=”

```
<p><a href="mailto:exemplo@examplo.com?subject=Assunto&body=Digite sua mensagem">
Clique aqui</a> para enviar um e-mail.</p>
```

Dessa forma, o resultado fica da seguinte forma:

[Clique aqui](mailto:exemplo@examplo.com?subject=Assunto&body=Digite sua mensagem) para enviar um e-mail.

No exemplo utilizado anteriormente, incluímos a função de link em texto, porém, essa função é muito bem aproveitada quando [inserida em imagens](https://www.homehost.com.br/blog/criar-sites/html-img/) ou ícones. Atenção, para que essa forma de link funcione, é necessário ter um [software de e-mail configurado](https://www.homehost.com.br/blog/contas-de-email/outlook-configurar-email-iphone-android/) em seu PC ou celular.

## Link HTML e o atributo download



Anteriormente, vimos que é possível utilizar dentro do href uma url global, e com isso temos diversas possibilidades de utilizar os hiperlinks. Uma dessas possibilidades é utilizar uma url que redirecione para o download de um arquivo. Apenas com o atributo href, o download irá abrir normalmente, porém é muito recomendável utilizar o atributo download. Com esse atributo, podemos definir um nome padrão para o arquivo que será baixado.

Vejamos o exemplo a seguir:

```
<a href="urldodownload"
   download="nomedoarquivo.exe">
  Faça o download do Firefox 39 para Windows
</a>
```

Separamos o seguinte exemplo para vocês, o nome do download está como padrão exemplo.zip:
[Faça o download aqui](https://www.homehost.com.br/blog/wp-content/uploads/2019/07/teste.zip)

## Base link

Caso algum link utilizado possua um destino que não existe mais ou não funcione, podemos utilizar um base link para redirecionar o usuário a um endereço específico. Com este objetivo, acrescente a tag <base> no interior do elemento <head> do seu HTML. Posteriormente adicione dentro da tag <base> o atributo href contendo o endereço que servirá como base link. Dessa forma, caso o link não funcione, o mesmo será redirecionado para a url contida na tag <base>. Geralmente, utiliza-se a própria página inicial como base.

Vejamos o exemplo a seguir de como inserir um base link no seu código HTML:

```
<head>
  <base href="https://www.homehost.com.br/">
</head>
```

Assim, caso haja algum link que não funcione no site, o mesmo será redirecionado para a página inicial da [HomeHost.](https://www.homehost.com.br/)

Certamente, esse elemento é um grande diferencial ao site, pois evita que o usuário tenha uma má experiência ao clicar num link defeituoso.

## Links HTML em imagens

Já ficou claro que o a tag <a> permite sua utilização de diversas formas. Uma das formais mais exploradas atualmente é a de links em blocos. Ou seja: uma vez que o elemento <a> não possui nenhum impedimento com a inserção de blocos dentro dele, podemos inserir um link numa imagem, para toda uma <div> ou até mesmo para uma seção inteira de um site.

Portanto, vejamos o exemplo a seguir, onde vamos inserir uma imagem para um link:

```
<a href="https://www.homehost.com.br/" target="_blank">
    <img width="100" height="100" src="images/homehost.png">
</a>
```

Teremos como resultado o seguinte:

[![Link Html Aplicado a Logo da Home Host](https://www.homehost.com.br/blog/wp-content/uploads/2016/05/homehost-logo.jpg)](https://www.homehost.com.br/)

Perceba que no exemplo anterior, utilizamos os atributos para alterar o tamanho da imagem normalmente. Portanto, a utilização da tag link não impede a estilização do elemento. A mesma regra vale para elementos de blocos, como no exemplo a seguir:

```
<a href="https://www.homehost.com.br/" target="_blank">
    <div height="100" style="background-color: blue;line-height: 100px;text-align: center;">
        <p style="color: white">Meu link em uma Div</p>
    </div>
</a>
```

Da mesma forma que utilizamos atributos de estilo inline normalmente, estamos agora aplicando um link para uma div inteira. Portanto, teste abaixo clicar em qualquer parte do bloco azul:

Meu link em uma Div

 

Além disso, há infinitas possibilidades de estilização e utilização do elemento link.

## Pratique você mesmo

Após a leitura e estudo do conteúdo desse artigo, recomenda-se praticar! Por isso, faça testes com seus códigos, utilizando links externos, internos, locais e globais. Siga as sugestões abaixo e certamente você estará apto a utilizar as funcionalidades do link HTML em qualquer situação.

Então, seguem algumas sugestões para treinamento:

- Comece fazendo o básico, aplicando link a algumas partes do texto;
- Estilize o elemento link, tente deixá-lo com diversos estilos diferentes;
- Crie um link que tenha o formato de um botão, com cores de fundo, e cor de fonte diferente da padrão;
- Criem uma lista <ul> e para cada <li> inclua um link, como um menu;
- Façam um menu que levem a determinada parte do site;
- Utilize links dentro de imagens;
- Utilize link de um download com um nome padrão do arquivo;
- Experimente utilizar link dentro de uma *div* completa, estilize e brinque com essa *div,* aproveite para treinar seu CSS.