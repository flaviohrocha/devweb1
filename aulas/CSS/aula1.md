# CSS - Cascading Style Sheets

Folhas de estilo em cascata é um mecanismo simples para adicionar estilos (por exemplo: fontes, cores, espaçamentos) aos documentos web. 

- Segundo os idealizadores da WEB, não cabe à HTML fornecer informações a apresentação dos elementos. 
Por exemplo: cores de fontes, tamanho de textos, posicionamento e todo o aspecto visual de um documento não deve ser função da HTML. 

- Cabem às CSS todas as funções de apresentação de um documento. Sendo assim, um website é formado por HTML + CSS. 

- Entre as vantagens de se utilizar CSS merece destacar:

  - Facilidade de manutenção: definição de estilos que se apliquem a toda página ou website. As mudanças são feitas de forma centralizada

  - Novas possibilidades de apresentação visual: muitas funcionalidades permitidas pela CSS não são suportadas pelo HTML

  - Diminuição do tempo de download: não é necessário incluir tags de formatação na página de forma que a leitura do código fonte fica mais fácil.

## Regras da sintaxe CSS

- Uma regra CSS é uma declaração que segue uma sintaxe própria e que define como será aplicado estilo a um ou mais elementos HTML . 

- Um conjunto de regras CSS formam uma Folha de Estilos. 

- Uma regra CSS, na sua forma mais elementar, compõe-se de três partes: um seletor, uma propriedade e um valor e tem a sintaxe conforme mostrado abaixo:

```
seletor {propriedade: valor;}
```

- Seletor: é o elemento HTML identificado por sua tag, ou por uma classe, ou por uma ID e para o qual a regra será válida (por exemplo: \<p>, \<h1>, \<div>, .minhaclasse, etc.);

- Propriedade: é o atributo do elemento HTML ao qual será aplicada a regra (por exemplo: font, color, background, etc.);

- Valor: é a característica específica a ser assumida pela propriedade (por exemplo: letra tipo arial, cor azul, fundo verde, etc.). Se o valor for uma palavra composta, deverá estar entre aspas duplas \", ou simples \'.


> #### Exemplo 1

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>Exemplo 1</title>
        <style type="text/css">
            h1 {font-size: 50px; font-family: arial;}
            
            h2 {font-size: 30px; font-family: courier;}
            
            p {font-size: 20px; font-family: "Comic Sans MS"; text-align: left;}

            h3, h4, h5, h6 {
            color: #00FF00;
            }
            body {
            color: #FFFFFF;
            background: #0000CC;
            font-weight: bold;
            }
        </style>
    </head>
    <body>
        <h1>Minha primeira página CSS</h1>
        <h2>Bem vindo à minha primeira página CSS</h2>
        <p>Aqui você verá como funciona CSS</p>
    </body>
</html>
```

- Para maior legibilidade das folhas de estilo, é uma boa prática escrever cada declaração (propriedade e valor) em linhas distintas. 

- Uma regra CSS pode ser aplicada a vários seletores ao mesmo tempo. Para isso separe cada seletor com uma vírgula.

- Seletores CSS não estão restritos às tags, e podem ser diversas entidades da marcação ou a combinação delas. 

- Seletores podem ser atributos do HTML e seus valores, combinações de tags, entre outros.

### Classes

- Em um site com CSS é comum criar um objeto chamado classe e definir as regras CSS independente de uma tag HTML.

- O objetivo de criar uma classe é aplicar uma regra comum a somente alguns tipos em diferentes seletores. 

- As classes podem ser aplicadas a qualquer elemento HTML.

- Podemos ainda aplicar estilos diferentes para o mesmo tipo de elemento do HTML, usando classes diferentes para cada um deles.

- No CSS a sintaxe consiste na combinação do sinal de ponto (.) imediatamente seguido do nome da classe.

- No código HTML deverá ser criado um atributo para a classe (class)

- Pode-se ainda usar o nome do elemento HTML para completar a grafia do seletor.

A sintaxe de uma classe é representada da seguinte forma:

```css
.nome_da_classe {propriedade: valor;}
```
Ou:

```css
elemento_html.nome_da_classe {propriedade: valor;}
```

> #### Exemplo 2


```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />    
        <title>Exemplo 2</title>
        <style type="text/css">
            .formatacao1 {
            color:#0099FF;
            }
            
            .formatacao2 {
            color:#99CC33;
            }

            h4.formatacao2 {
            color:#99AAFF;
            }  
        </style>
    </head>
    <body>
        <p class="formatacao1"> este é o parágrafo com a primeira formatação.</p>

        <p class="formatacao2"> este parágrafo com a segunda formatação. </p>

        <h4 class="formatacao2"> este cabeçalho com a segunda formatação. </h4>
    </body>
</html>
```


### ID

- Este seletor difere do seletor de classe, por ser ÚNICO. 

- Um seletor ID deve ser aplicado a UM e somente UM elemento HTML dentro do documento.

- A sintaxe do seletor ID é semelhante a do seletor classe, a diferença é que usamos o sinal de “#” ao invés do “.”

Veja a sintaxe abaixo:

```css
#nome_do_id {propriedade: valor;}
```

> #### Exemplo 3

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />    
        <title>Exemplo 3</title>
        <style type="text/css">
            
            #esporte {
            color:#0099FF;
            }
            
            #tecnologia {
            color:#99CC33;
            }

        </style>
    </head>
    <body>
        <p id="esporte"> Parágrafos relativo a esportes.</p>
        <p id="tecnologia"> Parágrafos relativo a tecnologia.</p>
    </body>
</html>
```

### Comentários

- Para adicionar comentários ao código CSS utilizamos a seguinte sintaxe:

```css
/* COMENTÁRIOS DE UMA LINHA */

/* COMENTÁRIOS
DE MÚLTIPLAS
LINHAS */
```

## Métodos de vinculação do CSS ao HTML

- As folhas de estilos são vinculadas no documento HTML de três formas.

  - Estilo Externo (linkadas ou importadas);
  - Estilo Interno;
  - Estilo Inline.

### Externa

- Uma folha de estilo é dita externa, quando as regras CSS estão declaradas em um documento a parte do documento HTML. 

- A folha de estilo é um arquivo separado do arquivo html e que tem a extensão .css

- Uma folha de estilo externa é ideal para ser aplicada a várias páginas. Com uma folha de estilo externa, podemos alterar a aparência de um site inteiro mudando um arquivo apenas (o arquivo da folha de estilo). 

- Para incluir um arquivo externo .css a um documento html, usamos a tag <link> entre as tags <head> </head> de acordo com a seguinte sintaxe:

```html
<head>
<link href="estilo.css“ rel="stylesheet" type="text/css" />
</head>
```

### Interna

- Uma folha de estilo é dita interna, quando as regras CSS estão declaradas no próprio documento HTML.

- Uma folha de estilo interna, é ideal para ser aplicada a uma única página, dessa forma podemos alterar a aparência de somente um documento.

- No estilo interno as regras são declaradas na seção \<head> do documento com a tag de estilo \<style> e são aplicadas no documento inteiro.

Veja a sintaxe abaixo:

```html
<head>
<style type="text/css">
p{
color:#993366;
}
</style>
</head>
```

### Inline

- Uma folha de estilo é dita inline, quando as regras CSS estão declaradas dentro da tag do elemento HTML. 

- No estilo inline as regras são aplicadas diretamente nas tags html e modifica os atributos de uma tag específica no documento, com isto ele perde muitas das vantagens de folhas de estilo pois mistura o conteúdo com a apresentação. 

Veja exemplo:

```html
<p style="color:#0066CC;font-size:20px">
Regilan Meira
</p>
```

### Precedência

Como as definições de estilo podem ser feita de formas por métodos diferentes, podem existir situações onde os estilos são conflitantes. 
Neste caso existe uma prevalência nos métodos segundo a regra abaixo:

- Prevalência em métodos de especificação:

  1. Externo
  2. Interno
  3. Inline

- Prevalência na seleção de métodos:

  1. Seletor
  2. Class
  3. ID

> #### Exemplo 4

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />    
        <title>Exemplo 4</title>
        <link href="estilo.css" rel="stylesheet" type="text/css" />
        <!--style type="text/css">
            p {
            color:#0055FF;
            font-size: 100px;
            }

            .classe {
            color:#0099FF;
            font-size: 50px;
            }

            #identificador {
            color:#99CC33;
            font-size: 20px;
            }
        </style-->
    </head>
    <body>
        <p> Precedência </p>
    </body>
</html>
```

## Propriedades de fontes e background


### Fontes

As propriedades para as fontes, definem as características das letras que constituem os textos dentro dos elementos HTML. 

Elas são representadas de acordo com a relação abaixo:

- font-style: efeito de inclinação; ex.: normal, italic;

- font-variant: transforma letras minúsculas em letras maiúsculas; onde as anteriormente em maiúsculo ficarão um pouco maiores das que estavam em minúsculo; ex.: normal, small-caps;

- font-weight: intensidade (espessura) da fonte; ex.: 100..900,normal, bold, bolder lighter, normal, bold, bolder, lighter.

- font-size: tamanho da fonte; ex.: small, medium, large, smaller, larger, 10, 10%;

- font-family – lista com os nomes da fontes que devem ser utilizadas nos textos por ordem de preferência, começando da mais desejada; ex.: serif, Verdana, Arial, “Times New Roman”;

- font: atalho para especificar as propriedades anteriores em um único local.

Exemplos:
```css
h4 {
 font-style: italic; }
h2 {
 font-variant: small-caps; }
body
 { font-weight: bold; }
h1 {
 font-size: 15pt; }
p {
 font-family: serif; }
h6 {
 font-family: Arial, Verdana, Helvetica; }
h5 {
 font: italic normal bold 14pt Arial; }
```

### Background

A propriedade background define as características do fundo dos elementos HTML. 

Elas são representadas de acordo com a relação abaixo:

- color : cor do texto;

- background-color : cor de fundo; ex.: cor, transparent;

- background-image : imagem que será utilizada como fundo do elemento; e as propriedades a seguir poderão ser usadas;

- background-attachment: define se a imagem ficará fixa ou se acompanhará a rolagem da área de apresentação; ex.: fixed,scroll;

- background-repeat: como a imagem será repetida se o tamanho dela for menor que a área de apresentação; ex.: no-repeat, repeat, repeat-x, repeat-y;

- background-position: posição inicial da imagem na área de apresentação; ex.: 10% 20%, 100 200, left, center, right, top,center, bottom;

- background: atalho para especificar as propriedades anteriores em um único local.

> #### Exemplo 6

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />    
        <title>Exemplo 6</title>
        <style type="text/css">
            a {
            color: #24A836;
            background-color: #FFFF00;
            }
            
            body {
            background-image: url(etb.png);
            background-repeat: no-repeat;
            background-attachment: fixed;
            background-position: center top;
            }

            h3 {
            position: absolute;
            left: 100px;
            top: 150px;
            background-color: #6EC279;
            }
        </style>
    </head>
    <body>
        <h3>Escola Técnica de Brasília</h3>
        <p>Acesse o site da <a href="http://www.etb.com.br">ETB</a></p>
    </body>
</html>
```

## Exercícios práticos

**Questão 01.** Criar uma regra CSS para formatação de parágrafo abaixo com as seguintes configurações:

- Cor da fonte Amarela
- Espessura da fonte: 900
- Estilo Itálico
- Tipo de fonte Arial
- Cor de fundo verde

Para a regra acima você deverá criá-la utilizando as três formas vistas em aula:

a. Método externo

b. Método interno

c. Método inline


**Questão 02.** Em relação às propriedades de background, criar uma classe para cada regra CSS abaixo:

- Cor de fundo de uma página azul claro
- Cor de fundo de um parágrafo em verde claro
- Colocar uma imagem de fundo que permita a repetição em qualquer estilo e que não acompanhe o deslocamento da página
- Colocar uma imagem de fundo e repeti-la na vertical
- Colocar uma imagem de fundo e não repeti-la
- Colocar uma imagem de fundo sem repeti-la e centralizada
- Formatar o fundo de uma página na cor amarela, uma figura de fundo, sem repetição, centralizada e que acompanhe o deslocamento da página

Ao final crie uma página HTML com vários elementos (cabeçalho ou parágrafos) para testar cada uma das regras acima.

**Questão 03.** Em relação às propriedades de fonte, criar um id para cada uma das regras CSS abaixo:

- Tipo de letra Arial e cor vermelha
- Tipo de letra Times, com tamanho 22 e na cor verde
- Tipo de letra Comic Sans Serif, com tamanho 20, na cor azul e estilo itálico
- Formatar a fonte de uma página na cor amarela, em negrito, de tamanho 14, com espessura média e tipo de letra Verdana
- Ao final crie uma página HTML com vários elementos (cabeçalho ou parágrafos) para testar cada uma das regras acima.