# 4. Estructura básica de un documento HTML.

HTML (Lenguaje de Marcas de Hipertexto, del inglés HyperText Markup Language) es el componente más básico de la Web. Define el significado y la estructura del contenido web.

La palabra <span class="emphasis">Hiper</span> viene del griego navegar, y si te das cuenta lo que haces al pasar de una página a otra, estás navegando por esas páginas escritas en HTML.

Este es un lenguaje de marcas como su nombre lo dice, así que repito que no es un lenguaje de programación como lo es <span class="code">JS</span> o <span class="code">Java</span>.

Estas marcas son las etiquetas HTML que veremos en los siguientes temas.

Recuerda que para esto necesitas tener el archivo <span class="code">index</span> con la extensión <span class="code">.html</span>

¿Recuerdas a Emmet? Muy bien para crear una estructura básica de html usaremos el atajo <span class="code">!</span> de emmet para que se autocomplete.

Si no te sale las opciones de autocompletado y estas en Visual Studio Code puedes presionar la tecla <span class="code">Ctrl + Space</span> si estas en <span class="emphasis">Windows</span>, o <span class="code">Command + Space</span> si estas en <span class="emphasis">MAC</span>, pero si de igual manera no lo hace puedes copiar y pegar (No te acostumbres) el código de abajo que lo iré explicando en partes.

```html
<!-- Emmet: -->
!

<!-- Resultado: -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>

  </body>
</html>
```

HTML es un lenguaje que no distingues entre mayúsculas y minúsculas, pero de preferencia y como buena práctica se escribe en minúsculas a excepción de la etiqueta <span class="code">&lt;!DOCTYPE></span> ya que es más entendible de esta manera.

Como puedes ver en el código hay algunas etiquetas que están en pares y otra que no, la segunda de las que están en pares tiene una barra diagonal antes del nombre de la etiqueta que está indicando que ahí es donde cierra, y algunas etiquetas tienen más de una palabra con un signo igual y más contenido, estos son los atributos de las etiquetas, pero, todo esto lo veremos mejor en los próximos temas.

Muy bien, seguimos, la etiqueta <span class="code">&lt;html></span> es la etiqueta raíz de un documento HTML aquí es donde se envuelve todo el documento, y este esta dividido en dos partes, el <span class="code">&lt;head> </span>y el <span class="code">&lt;body></span>.

Todo lo que encontramos en la etiqueta <span class="code">&lt;head></span> (La cabecera) es información que se necesitan los navegadores y motores de búsqueda como <span class="emphasis">Google</span> o <span class="emphasis">Bing</span>. Aquí se guarda información necesaria como el título de la página, la descripción del contenido, el o los iconos (<span class="code">favicon</span>), nombre del autor, redes sociales, y muchos datos más. Y también sirve para enlazar al documento <span class="emphasis">Hojas de Estilo CSS</span> y <span class="emphasis">Script de Programación JS</span>.

La cabecera del documento es la parte que no puedes visualizar como usuario a excepción del <span class="emphasis">título</span> y el <span class="emphasis">favicon</span>.

Ahora, el <span class="code">&lt;body></span> (El cuerpo) es el contenedor de todo lo que se verá en la página, ósea lo que el usuario vera al entrar a esta.
Mas adelante veremos que son todas esas etiquetas <span class="code">&lt;meta></span>, <span class="code">&lt;title></span>, etcétera.

Una etiqueta debe abrir y cerrar dentro de su etiqueta contenedora, no puedes abrir una etiqueta <span class="code">&lt;title></span> dentro de <span class="code">&lt;head></span> y cerrarla fuera de esta misma, así que esto sería un error:

```html
<head>
  <title>
</head>
  </title>
```

Sin mucho más que agregar a este tema, te sugiero trabajar siempre de **manera ordenada**.
Si tú notas en el código anterior hay un cierto espaciado entre algunos elementos y el comienzo de la línea, esto se llama <span class="emphasis">indentacion</span>, es una forma de escribir el código de una manera ordenada y nos sirve para que sea más **entendible**.

Para que se te haga más fácil indentar en HTML debes saber esto, cada editor de código tiene un numero de espacios establecidos para **indentar**, en este caso son 2 y en otros son 4, estos espacios se generan presionando la tecla <span class="code">tab</span> (Tabulación).

Ahora que ya sabes esto, lo último que debes saber sobre esto es que cada elemento que está dentro de otro (<span class="emphasis">Hijo</span>) debe iniciar 2 o 4 espacios delante de donde inicio el elemento que contiene este mismo (<span class="emphasis">Padre</span>), veamos un ejemplo:

```html
<head> <!-- Padre -->
  <meta> <!-- Hijo -->
  <title><title> <!-- Hijo -->
</head>
<body>
</body>
```

Como puedes ver las etiquetas <span class="code">&lt;meta></span> y <span class="code">&lt;title></span> inician dos espacios después de la etiqueta <span class="code">&lt;head></span> y, por último, si te fijas bien en la etiqueta <span class="code">&lt;body></span> veras que inicio en la misma línea que <span class="code">&lt;head></span> ya que no esta dentro de ella, si no que es su <span class="emphasis">“hermana”</span>.

Aquí te dejo un último ejemplo:

```html
<section> <!-- Padre -->
  <p> <!-- Hijo de <section> -->
    <span> <!-- Hijo de <p> -->
    </span>
  </p>
<section>
```



