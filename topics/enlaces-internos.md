# 27. Enlaces Internos

Los enlaces internos o anclas, son enlaces como los anteriores pero no nos llevan a otra pagina sino que a una seccion dentro de la misma pagina, pensemos en una pagina de inicio de una tienda o un portafolio web, tienen su secciones como **Sobre Nosotros**, **Nuestros Productos**, **Servicios**, **Contacto**, etcetera y hay un menu en la cabecera o al lado que nos lleva a esas secciones, pues esos son los enlaces internos.

Para que un enlace interno funcione se necesita que la seccion a la que queremos ir tenga el atributo <code>id</code> en el mismo elemento contenedor o en el titulo y pues este debe ser un nombre unico, osea que si tienes mas de uno, no debes repetir su valor en nigun otro, y en el atributo <code>href</code> del enlace se debe colocar el simbolo <code>#</code> seguido del nombre del <code>id</code>.

Utilizaremos este ejemplo para crear una pagina de inicio de una tienda como te mencione al inicio, con un texto de prueba solo para tener contenido y haya espacio entre las secciones.

Aqui te dejo el texto para que lo pegues dentro de cada seccion o puedes utilizar el atajo <code>lorem</code> de <span class="emphasis">Emmet</span>. Si solo utilizas el atajo asi se escribira un texto un poco largo, pero puedes poner el numero de palabras que quieres que se escriban seguido de esta palabra, de esta forma: <code>lorem20</code> o <code>lorem100</code>

```text
TEXTO LOREM

Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere officia
iusto blanditiis aliquid maxime inventore deserunt libero atque velit.
Laboriosam accusamus id commodi quas ducimus doloribus autem itaque
iusto sequi vero, perspiciatis ipsam sunt dolorum quam tempore voluptas
veritatis. Earum, animi quae. Commodi ullam minus veritatis cupiditate
consequuntur cum sunt nulla amet at autem iure deserunt laboriosam earum
reprehenderit soluta, ducimus consequatur quas illo minima dolorem
animi, eius voluptatum. Accusamus quibusdam suscipit omnis. Laboriosam
nobis doloremque pariatur facilis cum, dolorum necessitatibus sequi
praesentium ipsam obcaecati totam dolore illum accusamus dicta, eos ipsa
repellendus dolorem odio voluptatum voluptates odit! Consequatur,
aliquam?
```

```html
<h1>Tienda Online</h1>
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#acerca">Acerca De</a></li>
    <li><a href="#servicios">Nuestros Servicios</a></li>
    <li><a href="#productos">Nuestros Productos</a></li>
    <li><a href="#contacto">Contactanos</a></li>
  </ul>
</nav>
<section id="inicio">
  <h2>Inicio</h2>
  <p>
    <!-- TEXTO LOREM -->
  </p>
</section>
<section id="acerca">
  <h2>Acerca De</h2>
  <p>
    <!-- TEXTO LOREM -->
  </p>
</section>
<section id="servicios">
  <h2>Nuestros Servicios</h2>
  <p>
    <!-- TEXTO LOREM -->
  </p>
</section>
<section id="productos">
  <h2>Nuestros Productos</h2>
  <p>
    <!-- TEXTO LOREM -->
  </p>
</section>
<section id="contacto">
  <h2>Contactanos</h2>
  <p>
    <!-- TEXTO LOREM -->
  </p>
</section>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/internos.html"></iframe>
</div>

Como puedes ver, al darle click nos lleva a la seccion que nosotros cliqueamos y en la barra de direcciones se agrega el texto del atributo <code>href</code>, este parte de la direccion url se llama <span class="emphasis">hash</code> y pues esa es su principal funcion.

Tambien puedes utilizar esta tecnica para ir a enlaces internos dentro de algunas paginas, por ejemplo si tu quieres ir a la seccion que explica el atributo <code>href</code> de la documentacion de *MDN* puedes hacerlo agregando el **hash** a la direccion de esta manera:

```html
<a
  href="https://developer.mozilla.org/es/docs/Web/HTML/Element/a#attr-href"
  target="_blank"
>
  Atributo <code>href</code> en MDN
</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/internos2.html"></iframe>
</div>

<div class="pagination">
  <a href="#/enlaces" class="pagination-button">← Enlaces</a>
  <a href="#/enlaces-y-protocolos-especiales" class="pagination-button">Enlaces y protocolos especiales →</a>
</div>