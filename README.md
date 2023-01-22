# sass-css (CSS com superpoderes)

Curso iniciando com SASS no Front-end.

O SASS é uma linguagem de extensão do CSS, que nos permite fazer coisas muito além das que estamos acostumados a fazer normalmente. Tendo como objetivo tornar o processo de desenvolvimento mais simples e eficiente, Com ele, podemos criar variáveis, separar o nosso CSS em módulos, criar funções, implementar lógica de programação, e muito mais.

## Instalação do Sass
Será necessário que você tenha o Node.Js e o npm instalados em sua maquina, mas se você já usa Node.js, poderá instalar Sass executando o seguinte comando:
  
 ``` 
  npm install -g sass
 ```
 
Para saber a versão do Sass, basta digitar:

```
  sass --version
```

## Pré-processando
Uma vez instalado o Sass, você pode compilar seu Sass para CSS usando o comando sass. Você precisará informar ao Sass de qual arquivo construir e para onde enviar o CSS.
- sass input.scss output.css

O watch diz ao Sass para monitorar seus arquivos de origem quanto à alterações e recompilar o CSS toda vez que você salvar seu Sass. para isso basta adicionar o watch ao seu comando, assim:
- sass --watch input.scss:output.css

Você também poderá compilar todos os arquivos de uma só vez usando o comando:
- sass --watch .

## Nesting (Aninhamento)
O Sass permitirá que você alinhe e organize seus seletores CSS de uma forma que siga a mesma hierarquia visual do seu HTML, e o Sass trás esse aninhamento de forma a facilitar a sua visão sobre o código.

pensando nisso, segue abaixo um exemplo de código de estilização mais organizado em scss:

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
## Herança/Extend
Usar @extend permite compartilhar um conjunto de propriedades CSS de um seletor para outro.

```Sass
.btn{
    width: 200px;
    padding: 10px 0;
    background: none;
    border: 0;
    border-radius: 10px; 
    box-shadow: 2px 2px 3px rgba(0, 0, 0, 0.472); 
}

.btn-laranja{
    @extend .btn;
    font-family: 'Courier New', Courier, monospace;
    font-size: 17px;
    font-weight: 600;
    font-style: normal;
    color: #fff;
    background: orange;   
}
```
Observe como o seletor .btn tem suas características herdadas facilmente. Com CSS puro, geralmente nessa situação o .btn-laranja não herda as características do .btn. Ele só define as suas próprias características. Por isso, no HTML precisaria usar as duas classes (.btn e .btn-laranja). Usando a herança do Sass, só é preciso colocar a classe .btn-laranja. Isso deixa a marcação mais limpa.
