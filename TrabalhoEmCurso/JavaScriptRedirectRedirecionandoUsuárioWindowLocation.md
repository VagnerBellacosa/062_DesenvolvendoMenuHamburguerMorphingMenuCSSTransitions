
Artigo[Invista em você! Saiba como a DevMedia pode ajudar sua carreira.](https://www.devmedia.com.br/javascript-redirect-redirecionando-o-usuario-com-window-location/39809#modulo-mvp)

# JavaScript redirect: Redirecionando o usuário com window.location

## Nesta documentação aprenderemos como redirecionar o usuário em JavaScript utilizando window.location.

- 

[Artigos](https://www.devmedia.com.br/artigos/)[JavaScript](https://www.devmedia.com.br/artigos/javascript)JavaScript redirect: Redirecionando o usuário com window.location



### JavaScript redirect

Nesta **documentação de JavaScript** veremos como redirecionar o usuário utilizando window.location.href, assign() e replace().

Apresentaremos aqui como redirecionar o usuário em JavaScript.

##### JavaScript redirect: Na prática

### Como funciona o redirecionamento

**O redirecionamento faz com que o usuário saia da página atual para outra página**. Quando precisar redirecionar o usuário para páginas diferentes com JavaScript, essa é a linha de código a ser utilizada. Considerando o seguinte código:

```
window.location.href = "http://www.devmedia.com.br";
```

Assim que essa linha de código é executada o **usuário é redirecionado** da página em que se encontra para a página principal da DevMedia, conforme a **Figura 1**.

![Funcionamento do redirecionamento](https://arquivo.devmedia.com.br/naoexclusivo/EduardoSpinola/Documentacao/redirect/redirecionamento.png)
**Figura 1**. Funcionamento do redirecionamento

```
1- window.location.assign("http://www.devmedia.com.br"); 2- window.location.replace("http://www.devmedia.com.br");
```

Os métodos assign() e replace() também são utilizados para redirecionar o usuário. A diferença entre eles é que o método replace() redireciona o usuário, mas não mantém a página anterior no histórico. Dessa forma o usuário não conseguirá utilizar o botão voltar no browser para acessar a página que estava em exibição.

### Sintaxe

```
window.location.href = “URL a ser acessada”
```

##### Ação executada

Assim que esse código é executado pelo browser, o endereço especificado na string à direita é acessado e renderizado.

```
window.location.assign(url)
```

##### Parâmetro

url é uma string contendo o endereço da página a ser exibida.

### Exemplos de redirect

##### Exemplo 1

No exemplo a seguir demonstramos como redirecionar o usuário para uma página qualquer assim que o usuário acessar o endereço responsável por exibir o HTML abaixo:

`<html>  <head>    <title>Pagina 1</title>    <meta charset="utf-8">  </head>  <body>    Pagina exemplo 1     <script>        window.location.href = "http://www.devmedia.com.br/";    </script>  </body> </html>`Ao acessar a página 1 o usuário é redirecionado para a página da DevMedia assim que a página 1 é renderizada. Outra opção é chamar apenas window.location, ao invés de window.location.href.



##### Exemplo 2

No exemplo a seguir temos um código semelhante ao anterior. No entanto, o redirecionamento foi definido dentro do <head>.

```
<html>  <head>    <script>        window.location.href = "http://www.devmedia.com.br/";    </script>    <meta charset="utf-8">  </head>  <body>    Pagina exemplo 1  </body> </html>
```

Ao acessar a página 1 o usuário é redirecionado imediatamente para a página da DevMedia. Outra opção é chamar apenas window.location, ao invés de window.location.href.

##### Exemplo 3

No exemplo a seguir demonstramos como redirecionar o usuário para outra página após determinado período de tempo, neste caso, cinco segundos.

```
<html>  <head>    <title>Pagina 2</title>    <meta charset="utf-8">  </head>  <body>    Pagina exemplo 2     <script>        setTimeout(function() {            window.location.href = "http://www.devmedia.com.br/";        }, 5000);    </script>  </body> </html>
```

Ao acessar a página 2, apenas após cinco segundos o usuário será redirecionado para a página da DevMedia. Diferentemente do exemplo anterior, dessa forma o usuário consegue visualizar o conteúdo da atual por determinado período.

##### Exemplo 4

No exemplo a seguir demonstramos como redirecionar o usuário para outra página de acordo com alguma condição.

```
<html>  <head>    <title>Pagina 3</title>    <meta charset="utf-8">  </head>  <body>    Pagina exemplo 3     <script>        statusUsuario = "Ativo";         if (statusUsuario == "Ativo") {            window.location.href = "http://www.devmedia.com.br/";        }    </script>  </body> </html>
```

Ao acessar a página 3 o usuário será redirecionado para a página da DevMedia apenas se statusUsuario for “Ativo”; como neste exemplo. Caso não seja, o usuário não será redirecionado.

##### Exemplo 5

No exemplo a seguir demonstramos como redirecionar o usuário para outra página com o método assign().

```
<html>  <head>    <title>Home</title>    <meta charset="utf-8">  </head>  <body>    Home comum     <script>        window.location.assign("http://www.devmedia.com.br/guia/javascript/34372");    </script>  </body> </html>
```

Ao acessar essa página o usuário é redirecionado para o Guia JavaScript da DevMedia.

##### Exemplo 6

No exemplo a seguir demonstramos como redirecionar o usuário para outra página com o método replace().

```
<html> <head>   <title>Home</title>   <meta charset="utf-8"> </head> <body>  Home comum   <script>   window.location.replace("http://www.devmedia.com.br/guia/javascript/34372");  </script> </body> </html>
```

Ao acessar essa página o usuário é redirecionado para a página da DevMedia. O método replace() evita que o usuário volte para a página anterior através do botão voltar do navegador. Ele substitui, no histórico, o registro da última página acessada pela página que o usuário passará a visualizar.

##### Exemplo 7

No exemplo a seguir demonstramos como redirecionar o usuário quando este clica em um botão.

```
<html>  <head>    <title>Home</title>    <meta charset="utf-8">  </head>  <body>    Home comum    <button onclick="redirecionar()">Acessar DevMedia</button>     <script>       function redirecionar() {          window.location.href = "http://www.devmedia.com.br";       }    </script>  </body> </html>
```

Ao acessar a página home o usuário será redirecionado para a página da DevMedia após clicar em um botão.

### Compatibilidade entre navegadores

A propriedade window.location.href e os métodos assign() e replace() são suportados por todos os browsers apresentados **Tabela 1**.

|                      | Chrome | Firefox | IE   | Edge | Safari | Opera |
| -------------------- | ------ | ------- | ---- | ---- | ------ | ----- |
| window.location.href | Sim    | Sim     | Sim  | Sim  | Sim    | Sim   |
| assign()             | Sim    | Sim     | Sim  | Sim  | Sim    | Sim   |
| replace()            | Sim    | Sim     | Sim  | Sim  | Sim    | Sim   |

**Tabela 1**. Compatibilidade do método x browsers.

### Mais sobre JavaScript

- [JavaScript if/else: Criando scripts com estruturas condicionais](https://www.devmedia.com.br/javascript-if-else-criando-scripts-com-estruturas-condicionais/39686)

- [Curso de Introdução ao JavaScript](https://www.devmedia.com.br/curso/curso-de-javascript-completo/388)