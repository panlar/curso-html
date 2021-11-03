# 26. Enlaces

Los enlaces son textos o imagenes que nos permitiran ir a otras paginas dentro de nuestro sitio web, a diferenctes secciones dentro de la misma pagina y tambien a otros sitios webs y paginas que no sean nuestras.

Los enlaces se definen dentro de la etiqueta <code><a></a></code> que es una **etiqueta de linea** y tienen el atributo <code>href</code> que es el mismo que utiliza la etiqueta <code><link></code> y pues como te lo estaras imaginando, recibira como valor la ruta o direccion relativa o absoluta de la pagina a la cual queremos dirigirnos.

Para este ejemplo crearemos un nuevo documento html en la carpeta raiz llamado <code>acerca.html</code> que contendra el titulo **Acerca**.

```text
▼ carpeta raiz
| > assets
| - acerca.html
| - index.html
```

Y dentro del <code>index</code> escribiremos un enlace que nos llevara a esta pagina con el texto *Ir Acerca*

```html
<a href="./acerca.html">Ir Acerca</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/enlaces.html"></iframe>
</div>

Como ves, este enlace nos muestra en la pantalla la otra pagina, incluso puedes ver que cambio el ultimo texto en las barras de direcciones donde se agrego el nombre del documento.

Ahora para regresarnos desde esa pagina al inicio agregaremos un enlace con el texto **Ir a Inicio* simplemente cambiando la ruta y el nombre del archivo.

```html
<a href="./index.html">Ir a Inicio</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/enlaces2.html"></iframe>
</div>

Tambien podemos agregar enlaces externos, osea que nos lleven a otros sitios o paginas web, por ejemplo la pagina de busqueda de google, para ello solo tenemos que poner esa ruta. En este ejemplo utilizare como ejemplo la pagina de mi blog, pero tu puedes usar la ruta que desees, siempre y cuando exista.

```html
<a href="https://panlar.github.io/blog">Ir a PanLar Blog</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/enlaces3.html"></iframe>
</div>

Como puedes ver, el resultado si es el esperado, pero acabamos de abrir la pagina dentro de la pagina de nuestro ejercicio, y esto puede que lo queramos asi cuando nos lleve a una pagina que este dentro de nuestro sitio web como la de *Acerca* pero que pasa cuando es una pagina externa? Para eso existe el atributo <code>target</code> que en español es objetivo y como valor recibe unas palabras especiales que indica si abrir la pagina dentro de la misma pestaña o en otra.

```text
Valores para el atributo target de los enlaces:
_self : Abre la pagina dentro de la misma pestaña | Valor por defecto.
_blank : Abre la pagina en otra pestaña.
```

```html
<a href="https://panlar.github.io/blog" target="_self">
  Ir a PanLar Blog con atributo _self
</a>
<br>
<a href="https://panlar.github.io/blog" target="_blank">
  Ir a PanLar Blog con atributo _blank
</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/enlaces4.html"></iframe>
</div>

Existe otro atributo llamada <code>rel</code> que tambien lo tiene la etiqueta <code><link></code> y pues tienen un proposito similar.

Los robots de los buscadores, cuando buscan en tus paginas los elementos tambien buscan los enlaces y tambien ratrean el contenido de esa url, osea lo que tiene la pagina. Este atributo en los enlaces nos sirve para indicarle a esos robots si deben rastrear esos enlaces o no, pero tambien existen otros valores.

```text
Valores para el atributo rel en los enlaces:
nofollow : valor utilizado para indicar que no rastree ese enlace.
noreferrer : valor utilizado para que la pagina a la que iremos no sepa desde que direccion se accedio a esa pagina, osea para que no sepan que presionamos ese enlace en la pagina que lo hicimos.
```

El valor <code>nofollow</code> se recomienda que se utilice cuando la pagina a la que se dirige no tenga que ver con nuestro contenido o identidad.

Como dije al inicio tambien puedes utilizar imagenes e incluso vectores como enlaces, simplemente los tienes que color dentro de los enlaces.

Crearemos dos enlaces, uno que nos lleve a la imagen del perro cliqueando la imagen del perro y otro que nos lleve a este curso cliqueando el logo de HTML5.

```html
<a href="./assets/img/perro.jpg" target="_blank">
  <img src="./assets/img/perro.jpg" alt="Ver perro negro"/>
</a>
<a href="https://panlar.github.io/curso-html" target="_blank">
  <img src="./assets/img/logo_html.svg" alt="Ir al curso de HTML" />
</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/enlaces5.html"></iframe>
</div>

Por ultimo, pudiste ver que los enlaces tienen un estilo diferete al demas texto, ya que por defecto vienen subrayados y de un color azul, u morado y que al colocar el cursor del mouse cambia su estilo de una flecha a una manita lo cual indica que esto es un enlace o elemento cliqueable.

Cuando tu no has visitado la url de los enlaces, el color de este mismo es azul en la mayoria de navegadores y cuando la url ya es visitada, cambia su color a morado para indicar que estos enlaces ya han sido visitados.

<div class="pagination">
  <a href="#/tablas" class="pagination-button">← Tablas</a>
  <a href="#/enlaces-internos" class="pagination-button">Enlaces Internos →</a>
</div>