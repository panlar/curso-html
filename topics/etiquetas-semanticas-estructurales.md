# 16. Etiquetas Semánticas Estructurales

En este tema veremos una de las partes más importantes del lenguaje HTML.

En temas anteriores vimos algunas etiquetas *semánticas para los textos* como <span class="code">&lt;strong></span> para texto importantes, <span class="code">&lt;code></span> para fragmentos de código, y, como puedes leer en el titulo de este tema veremos las **etiquetas semánticas estructurales** que como su nombre lo dice, nos sirven para estructurar nuestra pagina web de una forma semántica, ósea que tenga un significado esa estructura.

Como ejemplo te pondré una infraestructura como una escuela, para empezar, sabemos que una escuela tiene una entrada, como un lobby de un hotel, también tiene aulas, tiene una cafetería, la dirección, el comedor, el patio de juegos, los baños, etcétera. Cada una de estas secciones de una escuela tiene una función específica, así mismo es en HTML, cada una de las etiquetas funciona para algo o, mejor dicho, para representar algo y estas también cuentan con unas reglas.

Las etiquetas semánticas estructurales son:

```html
<div></div>
<!--
  div : divisor
  Esta es una etiqueta contenedora que no tiene semántica.
  Se utilizan cuando queremos hacer alguna división de contenidos o,
  cuando definimos algo que no tiene semántica por sí solo.
-->

<main></main>
<!--
  main : principal
  Es el bloque de contenido principal de una página, dentro de ella puede
  haber todas las etiquetas, y al igual que el <h1> solo puede haber un main
  en toda la página.
-->

<header></header>
<!--
  !No confundir con head
  header : cabecera
  Esta etiqueta se utiliza para definir la cabecera de tu página o,
  de una o varias secciones, artículos, etcétera.
  Puedes usar header dentro de <section>, <article>, <aside>, <main>.
-->

<nav></nav>
<!--
  nav : abreviatura de navigation : navegación
  Se utiliza para definir un bloque que contendrá los enlaces para
  navegar por la página o sitio web.
-->

<section></section>
<!--
  section : seccion
  Como su nombre lo dice define una sección de la página o, de uno o mas
  artículos, etcétera.
  Puedes utilizar <section> dentro de <main>, <aside>, <article>.
-->

<article></article>
<!--
  article : articulo
  Define un bloque autocontenido, esto quiere decir que se explica
  por si solo y no necesita del contexto general para ser entendido.
  Esto puede ser como un artículo de un blog.
-->

<aside></aside>
<!--
  aside : al lado / aparte
  Es un bloque de contenido que aparte del contenido principal.
  Los mayores casos de uso son para barras laterales donde se muestran anuncios,
  pero puedes mostrar cualquier contenido que no tenga relación con el
  contexto principal de la página.
-->

<footer></footer>
<!--
  footer : pie de pagina
  Aunque su significado se pie de página, también se puede usar para ser el pie
  de un <section>, <article>, <aside>, <main>.
  Su mayor utilización se da para contener enlaces a más secciones o redes sociales,
  el copyright, el autor, etcétera.
-->
```

Antes de la versión 5 de HTML no existían estas etiquetas, solo el <span class="code">&lt;div></span>, y este era el que se utilizaba para definir los contenidos y para saber que parte de la página era se utilizaba el atributo <span class="code">class</span> o <span class="code">id</span>, y aunque esto era totalmente valido, había un problema y es que al momento de haber demasiadas <span class="code">&lt;div></span> dentro o al lado de otras, podía ser confuso leer el código ya que no era tan fácil encontrar donde abría o cerraba una etiqueta.
Pero desde HTML5 este problema se solucionó con estas etiquetas, aquí un ejemplo de ambos casos:

<img loading="lazy" src="https://i.postimg.cc/85vhrPcG/etiquetas-semanticas-estructurales.png" alt="viewport" title="HTML1-4 VS HTML5">

En código esto sería así:

```html
<!-- Antes de HTML 5-->
<div id="header"></div>
<div id="menu"></div>
<div class="post"></div>
<div class="post"></div>
<div id="footer"></div>

<!-- Despues de HTML 5-->
<header></header>
<nav></nav>
<article></article>
<article></article>
<footer></footer>
```

Como puedes ver, mucho mejor y más descriptivo.

Aquí hay otro ejemplo de una estructura en HTML5

```html
<header></header>

<nav></nav>

<main>
  <header></header>
  
  <section>
    <article></article>
    <article></article>
  </section>
  
  <footer></footer>
</main>

<aside></aside>

<footer></footer>
```

Como puedes ver en el ejemplo hay dos etiquetas <span class="code">&lt;header></span> y <span class="code">&lt;footer></span>, unas son para la página y las otras son para el contenido principal