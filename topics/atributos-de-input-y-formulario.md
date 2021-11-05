# 33. Atributos de input y formulario.

En esta seccion veremos los atributos mas utilizados e importantes en os elementos <code><input></code> y <code><form></code>.

### Atributos de **form**

1. <code>action</code> : Recibe la url a la que se desean enviar los datos del formulario. Aunque en la actualidad estos envios se manejan con programacion en JS, si funciona y ya lo veremos en un ejemplo. Si el formulario no tiene este atributo procesa los datos dentro de la misma pagina
1. <code>autocomplete</code> : Recibe dos valores que son <code>on</code> y <code>off</code> y este indica si se deben mostrarse las opciones de autocompletado los campos del formulario, el valor por defecto es <code>on</code>.
1. <code>method</code> : Recibe dos valores, los cuales son <code>GET</code> y <code>POST</code>, el primero adjunta los valores del formulario a la **url** y el segundo envia estos datos de forma oculta en el cuerpo de la peticion.
1. <code>target</code> : Tiene el mismo proposito y valores que en la etiqueta <code><a></code> y se utiliza cuando envias el formulario sin programacion en JS.

```html
<h2>Formulario con el <code>method="GET"</code></h2>
<form action="https://panlar.github.io/blog" target="_blank" method="GET">
  <input type="hidden" name="text" value="hola" />
  <input type="submit" />
</form>

<h2>Formulario con el <code>method="POST"</code></h2>
<form action="https://panlar.github.io/blog" target="_blank" method="POST">
  <input type="hidden" name="text" value="hola" />
  <input type="submit" />
</form>

<h2>Formulario con el <code>method="GET"</code> sin <code>action</code></h2>
<form method="GET">
  <input type="hidden" name="text" value="hola" />
  <input type="submit" />
</form>

<h2>Formulario con el <code>method="POST"</code> sin <code>action</code></h2>
<form method="POST">
  <input type="hidden" name="text" value="hola" />
  <input type="submit" />
</form>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/atributos_formulario.html"></iframe>
</div>

Si pruebas cada ejemplo veras que el primer ejemplo te enviara a mi blog pero adjuntado esta cadena: <code>?text=hola</code>, que como señale en el capitulo de <a href="#/enlaces-y-prtocolos-especiales">Enlaces y Protocolos especiales</a> el simbolo <code>?</code> indica que pasaremos unas variables a la url, y lo mismo pasa en el tercer ejemplo pero esta vez adjunta esta cadena a la url de nuestro servidor local.

En el segundo y cuarto ejemplo, utilizando el metodo <code>POST</code> puedes ver que nos envia a las url del blog y en la que estamos trabajando pero ambas paginas nos lanzan un error 405, esto debido a que no hemos programado nada para que muestre algo en pantalla, pero si puedes apreciar que no se adjunta nada a la url.

### Atributos de **input**

Existe una cantidad muy grande de atributos para los <code><input></code> debido a su gran variedad de tipos pero aqui veremos los mas importantes y usados.

<blockquote>
  Los atributos que tambien puedan ser utilizados en un <code>textarea</code> estaran marcados con un asterisco, asi: <code>required*</code>
</blockquote>

- <code>accept</code> : este atributo se utiliza con el tipo <code>file</code> y su valor es una lista de archivos que aceptara, por ejemplo <code>.jpg,.png,.mp3</code> que solo aceptara esos tipos de archivos o tambien puedes usar valores como <code>audio</code> o <code>images</code> que solo acepataran archivos de audio e imagenes respectivamente.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-accept" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>accept</code></a>


- <code>autocomplete*</code> : Al igual que en el elemento <code><form></code> muestra u oculta una lista para autocompletar los campos, pero en estos elementos puedes personalizarlo para que te muestre solo la listas de nombres, telefonos, correos, etcetera que has utilizado. Esta lista de valores se encuentra en la siguiente documentacion:
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-autocomplete" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>autocomplete</code></a>


- <code>autofocus*</code> : Este atributo es booleano y debe ser unico en una pagina, osea que solo puede existir en una vez, y su funcion es colocar el cursor en el elemento que se lo asignas al momento de cargar la pagina.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-autofocus" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>autofocus</code></a>


- <code>checked</code> : Es un atributo booleano y se utiliza en los tipos <code>radio</code> y <code>checkbox</code> y su presencia señala que esos elementos estaran seleccionados al cargar la pagina.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-checked" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>checked</code></a>


- <code>disabled*</code> : Se utiliza para desabilitar cualquier elemento, y este mismo lo hace mas opaco.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-disabled" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>disabled</code></a>


- <code>form*</code> : este atributo se utiliza en cualquier elemento, y su uso es para cuando el elemento no se encuentra dentro de la etiqueta <code><form></code> y recibe como valor el <code>id</code> del formulario al que esta asociado.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-form" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>form</code></a>


- <code>list</code> : Este atributo se utiliza para mostrar una lista de opciones predefinidas en una etiqueta <code><datalist></code> y recibe como valor el <code>id</code> de esta lista. Solo puede ser utilizado en los controles de escritura.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-list" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>list</code></a>


- <code>max</code> : Determina el numero | fecha-hora maximo que se puede ingresar en uno de tipo <code>number</code>, <code>date</code>, <code>time</code>, <code>week</code>, <code>month</code> y <code>range</code>.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-max" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>max</code></a>


- <code>maxlength*</code> : Determina la longitud maxima de una cadena de caracteres, al igual que el <code>list</code> solo funciona en controles de escritura.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-maxlength" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>maxlength</code></a>


- <code>min</code> : misma funcionalidad del atributo <code>max</code> pero ahora seria el minimo numero | hora-fecha.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-min" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>min</code></a>


- <code>minlength*</code> : misma funcionalidad del atributo <code>maxlenght</code> pero seria la longitud minima.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-minlength" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>minlength</code></a>


- <code>multiple</code>: atributo booleano que valida si pueden haber mas de un elemento en controles de tipo <code>email</code> y <code>file</code>.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-multiple" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>multiple</code></a>


- <code>name*</code> : es el nombre que recibe el controlador, y este nombre sera el de la variable que se envie al procesar la variable. Cuando es un grupo de controladores de tipo <code>radio</code> el nombre debe ser igual en todos los controladores de ese grupo para evitar que se seleccione mas de uno.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-name" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>name</code></a>


- <code>pattern</code> : Recibe una expresion regular para validar el contenido escrito en el controlador de escritura. Si el contenido no es valido mostrara una alerta que el contenido no coincide con el formato valido.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-pattern" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>pattern</code></a>
- <a href="https://es.wikipedia.org/wiki/Expresi%C3%B3n_regular" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>expresiones regulares</code></a>

- <code>placeholder*</code> : Muestra una pista o patron en el controlador de escritura para guiar al usuario que debe introducir en el campo.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-placeholder" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>placeholder</code></a>

- <code>readonly*</code> : establece que el controlador solo sea de lectura. Este atributo es booleano.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-readonly" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>readonly</code></a>

- <code>required*</code> : Este atributo valida que el controlador tenga un valor, de lo contrarion no sera enviado el formulario, y mostrara una alerta de que necesitas completarlo.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-required" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>required</code></a>

- <code>spellcheck*</code> : Si este atributo tiene el valor de <code>true</code> comprobara la ortografia y gramatica del controlador.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-spellcheck" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>spellcheck</code></a>

- <code>src</code> : toma como valor la ruta de la imagen para el controlador de tipo <code>image</code>
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-src" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>src</code></a>

- <code>step</code> : funciona en los mismo controladores del atributo <code>max</code> y recibe como valor un numero el cual sera el incremento o decremento de ese controlador.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-step" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>step</code></a>

- <code>value</code> : El valor inicial del control. Este atributo es opcional, excepto cuando el controlador es de tipo <code>radio</code> y <code>checkbox</code>.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/input#attr-value" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>value</code></a>.

### Mas Atributos de **textarea**

- <code>cols</code> : Indica el numero de caracteres que seran visibles en el eje horizontal.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/textarea#attr-cols" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>cols</code></a>

- <code>rows</code> : Misma funcion que el anterior pero esta vez en el eje vertical.
- <a href="https://developer.mozilla.org/es/docs/Web/HTML/Element/textarea#attr-rows" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Mas sobre <code>rows</code></a>.

<div class="pagination">
  <a href="#/elementos-de-formularios" class="pagination-button">← Elementos de formularios</a>
  <a href="#/selects-radios-y-checkbox" class="pagination-button">Selects, radios y checkbox →</a>
</div>