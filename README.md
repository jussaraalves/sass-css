# sass-css (CSS com superpoderes)

Curso iniciando com SASS no Front-end.

O SASS é uma linguagem de extensão do CSS, que nos permite fazer coisas muito além das que estamos acostumados a fazer normalmente. Tendo como objetivo tornar o processo de desenvolvimento mais simples e eficiente, Com ele, podemos criar variáveis, separar o nosso CSS em módulos, criar funções, implementar lógica de programação, e muito mais.

## Pré-processando
Uma vez instalado o Sass, você pode compilar seu Sass para CSS usando o comando sass. Você precisará informar ao Sass de qual arquivo construir e para onde enviar o CSS.
- sass input.scss output.css

O --watch diz ao Sass para monitorar seus arquivos de origem quanto a alterações e recompilar o CSS toda vez que você salvar seu Sass. para isso basta adicionar o watch ao seu comando, assim:
- sass --watch input.scss:output.css

## Nesting (Aninhamento)
O Sass permitirá que você alinhe e organize seus seletores CSS de uma forma que siga a mesma hierarquia visual do seu HTML, e o Sass trás esse aninhamento de forma a facilitar a sua visão sobre o código.

pensando nisso segue abaixo um exemplo de organizacao scss:

```Sass
  nav {
    ul {
      margin: 0;
      padding: 0;
      list-style: none;
    }

    li { display: inline-block; }

    a {
      display: block;
      padding: 6px 12px;
      text-decoration: none;
    }
}
```
