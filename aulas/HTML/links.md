# HTML - Links

Os links ou hyperlinks permitem "interligar" as páginas na Internet, ou seja, através de links se vai de uma página para
outra com um simples clique do mouse.

## Criar um link

Para a criação de links é utilizada a tag `<a>` conforme  sintaxe abaixo:

```html
<a href="URL"> texto que receberá o link </a>
```

#### Exemplos

Link para uma página da internet

```html
Esse é um link para a página da <a href="http://www.etb.com.br/">
Escola Técnica de Brasília</a>.
```

Link para uma página interna (do próprio site)

```html
<p> 
Esse é um link para uma outra página interna (caminho relativo) 
	<a href="html/outra_pagina_de_links.html">Uma outra página</a>.
</p>
```

## Imagem como link

Pode ser utilizada uma imagem como link, basta incluir a tag `img` entre as tags de abertura `<a>` e fechamento `</a>`

#### Exemplo

```html
Essa imagem é um link: <a href="http://www.etb.com.br/">
<img src="etb.png"></a>
```

## Link com o atributo target

O atributo `TARGET` define a janela do browser onde o endereço referenciado no atributo href será exibido (o "default" é `_self`).

#### Exemplo

```html
<p> 
<a href="http://www.etb.com.br/" target="_blank">Visite o site da Escola Técnica de Brasília!</a>.
</p>
```

|Valores para target| Descrição|
|---|---|
|_blank|    Abre o documento vinculado em uma nova janela ou guia|
|_self|     Abre o documento vinculado na mesma janela ou guia|
|_parent|   Abre o documento vinculado no frame pai|
|_top|      Abre o documento vinculado no corpo inteiro da janela|

## Link para email

Essa forma de link é utilizada para um o envio de email para um destinatário definido.

Para o envio é utilizado o cliente de email instalado na máquina do usuário (por exemplo, o MS Outlook)

#### Exemplo

```html
<p>
    Esse é um link para email:
    <a href="mailto:contato@etb.com.br" target="_top">Enviar email</a>
</p>
```

## Link para um elemento específico da página (Âncora)

As âncoras são links que levam a barra de rolagem da tela do navegador para um elemento específico da página.

Esse elemento é definido por meio do atributo `id` que pode ser associada a uma tag HTML.

As âncoras são muito úteis em páginas muito extensas, onde o cliente HTTP tem que usar a barra de rolagem vertical do browser para visualizar o conteúdo da página.

#### Exemplo

```html
<h1 id=inicio>Links</h1>

...

<a href="#inicio">Início da página</a>
```


## Exercícios práticos

**Questão 01.** Crie uma página HTML (index.html) com os seguintes links:

1. Link para a página do Google

1. Link para uma outra página criada por vocês com o nome pagina.html (coloque qualquer conteúdo)

1. Crie o mesmo link do item 1 utilizando uma figura com a logo do Google e que abra em uma outra página (ou guia)</li>
