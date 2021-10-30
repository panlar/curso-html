# 19. Scripts en HTML

Ya que vimos con insertar estilos en html ahora veremos cómo hacer lo mismo, pero con los scripts de programación en el lenguaje **JavaScript** que es el que se utiliza para la web como lo he venido diciendo.

Existen 2 formas de insertar scripts y ambas son utilizando la etiqueta <code><script></code>, esta es una etiqueta de apertura y de cierre ósea que va así: <code><script></script></code>.

### 1. In the *script* tag / Dentro de la etiqueta *script*

Aquí básicamente es lo mismo que la forma 2 de los estilos, el código JS se escribirá dentro de esta etiqueta. Para este ejemplo enviaremos un mensaje a la consola que diga: <span class="emphasis">"Hola Mundo desde scripts dentro de html"</span>

Para estos casos lo mejor es que la etiqueta este antes del cierre de la etiqueta body, ya que el navegador va leyendo y mostrando el contenido del documento en el orden en el que ha sido escrito, por lo que si quisieras manipular un elemento y pones esta etiqueta en el <code><head></code> se cargara antes del elemento y no funcionara lo que desees hacer con este mismo.

```html
<body>
  <!-- Todo el código HTML -->
  <script>
    console.log("Hola Mundo desde scripts dentro de html");
  </script>
</body>
```

Si recargas la página aun no vera nada, pero si entras a la ventada de *herramientas para desarrolladores* desde el menú contextual dando *clic derecho* en la página o desde el *menú del navegador* y entras en la pestaña de la **consola** veras el mensaje que acabamos de escribir, algo así:

```text
Hola Mundo desde scripts dentro de html                     index.html:21
```

El texto <code>index.html:21</code> hace referencia al documento de donde viene el mensaje y la línea en el que está escrita, en mi caso está en la línea 21.

### 2. Scripts linked / Scripst enlazados

Al igual que la tercer forma para los estilos, nos crearemos un nuevo archivo llamada <code>script</code> con la extensión <code>.js</code> dentro de la carpeta <code>assets</code> con lo que la estructura de nuestro proyecto quedaría así:

```text
> carpeta raíz
| > assets
  | - styles.css
  | - script.js
| - index.html
```

Dentro de este documento escribiremos un código que lance a la consola un mensaje que diga: <span class="emphasis">"Hello World desde un script enlazado"</span>

```js
console.log("Hello World desde un script enlazado");
```

Ahora, pondremos otro <code><script></code> pero en este caso, la posición de la etiqueta, en realidad depende mucho de lo que quieras o no hacer, ya que puedes ponerla en el <code><head></code> pero como dije antes, se ejecutara antes de que el contenido se carga, pero, puedes usar un atributo, el cual es <code>defer</code> que le indica al navegador que lo cargue pero no le ejecute aun, sino que, hasta que todo el documento completo se cargue, y también puedes ponerlo al final como en la forma anterior.

Algo que también cambia en este caso es el atributo <code>href</code>, en las etiquetas <code><link></code> era este atributo el que se utilizaba para decirle al navegador donde buscar la hoja de estilos, con esta etiqueta se utiliza el atributo <code>src</code> que es una abreviatura de <span class="emphasis">source</span> que significaría la fuente o recurso de donde obtendrá este script de programación.

Con la primera de manera de posición de la etiqueta quedaría así:

```html
<head>
  <!-- Metadata -->
  <script src="./assets/script.js"></script>
</head>
```

Con la segunda manera quedaría así:

```html
<body>
  <!-- Todo el codigo HTML -->
  <script src="./assets/script.js"></script>
</body>
```

Al final ambas formas funcionan, y como te dije, su posición difiere en que quieres o no hacer con el código.

El resultado en la consola sería el siguiente:

```text
Hello World desde un script enlazado                     script.js:1
```

Como puedes ver, la referencia del mensaje cambia de <code>index.html:21</code> por <code>script.js:1</code> ya que el código se encuentra en la línea uno del archivo que creamos.

<div class="pagination">
  <a href="#/estilos-en-html" class="pagination-button">< Estilos en HTML</a>
  <a href="#/imagenes" class="pagination-button">Imágenes ></a>
</div>
