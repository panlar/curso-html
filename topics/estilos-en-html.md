# 18. Estilos en HTML

Como te explicaba al inicio de este curso existen más lenguajes además de HTML existen más lenguajes para crear una página web como *CSS* (Estilos) y *JavaScript* (Funcionalidad).

Aunque este no es un curso de CSS te ensenare las tres formas distintas de usar CSS en HTML, pero antes de eso te explicare un poco como va este lenguaje.

Existen dos conceptos importantes o principales en CSS y estos son los **selectores** y **reglas**.

Los <span class="emphasis">selectores</span> son las palabras o combinaciones de ellas con símbolos que se utilizan para seleccionar los elementos o etiquetas HTML a las cuales quieres agregarle los estilos.

Las <span class="emphasis">reglas</span> son los estilos correctamente escritos dentro de una **declaración de estilos**, que se asignaran al elemento, o, a los elementos seleccionados y estos mismos se aplicaran visualmente en el navegador. Estas reglas se dividen en dos partes: propiedad y valor.

La <span class="emphasis">propiedad</span> es el aspecto que cambiara del elemento, por ejemplo: <code>width</code> : ancho, <code>height</code> : alto, <code>background-color</code> : color de fondo, <code>margin</code> : margen, etcétera.

El valor es lo que recibe la propiedad, por ejemplo, un color *hexadecimal* (<code>#0F53A3</code>) o en *ingles* (<code>green</code>), una unidad de medida como *centímetros* (<code>4cm</code>) o *pixeles* (<code>20px</code>), *palabras reservadas* en el lenguaje, etcétera.

<blockquote>
  Cada regla css va separada por un <code>;</code>
</blockquote>

```css
body
{
  background-color: black;
  color: white;
  margin: 20px;
}

/*
body -> selector
{} -> declaración
background-color / color / margin -> propiedad
black / white / 20px -> valor
*/
```

En el código le estaremos diciendo al navegador que el color del fondo del body será color negro y el color de las letras color blanco y que los márgenes a los cuatro lados será de 20px.

Muy bien, ahora que sabemos los conceptos basicos de CSS podemos seguir con el tema.

### 1. Styles Inline / Estilos en línea.

Estos estilos se escriben dentro de las etiquetas utilizando el atributo <code>style</code> y como valor recibe las reglas que se la aplicaran a ese elemento, por lo tanto si quieres ponerles los mismo estilos a las otras etiquetas tendrás que asignárselos una por una.

```html
<h1 style="background-color: #0066FF; color: white;">
  Esto es un encabezado con estilos en línea con un color de fondo azul (#0066FF) y un color de texto blanco (white)
</h1>

<p style="width: 100px; color: red;">
  Este es un párrafo con un ancho de 100px y un color de texto rojo (red)
</p>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/estilos_html.html"></iframe>
</div>

Esta manera, aunque es totalmente valida y funciona, se considera una mala práctica y se recomienda que no se utilice a excepción de casos que si los necesite.

### 2. *style* Tag / Etiqueta *style*

Antes de todo, no confundas esto con el atributo <code>style</code>, el atributo se utiliza dentro de las etiquetas y esta es una etiqueta.

Muy bien, esta etiqueta fue creada para contener estilos CSS dentro de ella y se los aplique al documento. Puedes utilizar la etiqueta dentro del <code><body></code> pero no se recomienda, una buena práctica es utilizarla siempre en el <code><head></code> al final preferiblemente.

```html
<head>
  <style>
    h1 /* Estos estilos se aplicarán a todas las etiquetas <h1> */
    {
      background-color: rgb(239, 101, 42); /* Color de fondo naranja */
      color: white; /* Color de texto blanco */
    }

    p /* Estos estilos se aplicarán a todas las etiquetas <p> */
    {
      margin: 50px; /* Margen a los 4 lados de 50 pixeles */
    }

    h2 /* Estos estilos se aplicarán a todas las etiquetas <h2> */
    {
      margin-left: 30px; /* Margen izquierdo de 30 pixeles */
      color: rgb(239, 101, 42); /* Color de texto naranja */
    }
  </style>
</head>
<body>
  <h1>Styles CSS in HTML / Estilos CSS en HTML</h1>

  <p>
    There are three ways to use styles in HTML / Existen tres formas de utilizar estilos en HTML
  </p>

  <h2>
    1. Styles Inline / Estilos en línea
  </h2>

  <h2>
    2. Style Tag / Etiqueta style
  </h2>

  <h2>
    3. Styles Linked with the link Tag / Estilos enlazados con la etiqueta link
  </h2>
</body>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/estilos_html2.html"></iframe>
</div>

### 3. Styles Linked with the *link* Tag / Estilos enlazados con la etiqueta *link*

Esta es la forma más recomendada y la más utilizada en el desarrollo web, y se trata de crear archivos externos, o sea que ya no serán estilos dentro del documento <code>.html</code> sino que se creara un archivo llamado por convención <code>styles</code> con la extensión <code>.css</code> y dentro de él se escribirá todo el código CSS.

Una convención y buena práctica es crear una carpeta llamada <code>assets</code> y dentro de ella crear todos los recursos de tu página web como las hojas de estilo en este caso, los scripts de programación, las imágenes, videos, audio, etcétera. Incluso puedes crear dentro de estas carpetas llamadas <code>css</code> por si tienes más de un archivo CSS, otra llamada <code>js</code> igualmente, si tienes más de un archivo JS, otra carpeta llamada <code>img</code> para el mismo caso anterior, pero con imágenes.

```text
> carpeta raíz
| > assets
  | - styles.css
| - index.html
```

Bien, luego de crear la carpeta y el archivo vamos a seguir con el siguiente paso, y es aquí donde entra la etiqueta <code><link></code>, esta etiqueta se coloca dentro de <code><head></code> ya que no es algo visible, sino que contendrá la ruta o url de la hoja de estilos que utilizará esa página web.

Esta etiqueta **NO** solo es para la hoja de estilos, tiene varios propósitos como, por ejemplo, indicar cual será el icono que se mostrará en la pestaña de la página (<code>favicon</code>), pero esto lo veremos en próximos capítulos.

Para utilizar esta etiqueta como un enlace de hojas de estilos se debe utilizar el atributo <code>rel</code> y como valor tendrá <code>"stylesheet"</code> que en español significa hoja de estilo, y para indicar la ruta se utiliza el atributo <code>href</code> que es la abreviatura de <em><b>h</b>ypertext <b>ref</b>erence</em> ósea que hace referencia o vincula un documento de hipertexto, pero también vincula una hoja de estilos; este atributo contendrá la ruta relativa o absoluta de la página web. En este caso será una ruta relativa ya que el archivo se encuentra en nuestro dominio o carpeta, si fuera una hoja de estilos que se encuentra en un dominio web como <code>https://www.google.com/assets/styles.css</code> sería una ruta absoluta porque no está en la carpeta de nuestro proyecto.

Bien, ahora sí, para enlazar la hoja CSS tendría que escribir lo siguiente:

```html
<head>
  <!-- Metadata -->
  <link rel="stylesheet" href="./assets/styles.css">
</head>
```

Ahora para comprobar que esto funciona lo que haremos será cortar lo que escribimos en la etiqueta <code><style></code> y lo pegaremos dentro del documento <code>styles.css</code> y eliminaremos esta misma etiqueta, y como puedes ver se aplican los mismos estilos pero ahora desde una hoja externa.

<div class="pagination">
  <a href="#/etiquetas-de-linea-y-bloque" class="pagination-button">< Etiquetas de línea y de bloque</a>
  <a href="#/scripts-en-html" class="pagination-button">Scripst en HTML ></a>
</div>
