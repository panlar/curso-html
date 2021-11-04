# 31. Iframes

Los iframes son contenedores en linea, se utilizan para cargar contenido externos como archivos <code>pdfs</code>, mapas de **Google Maps**, **Video de YouTube**, incluso otras paginas, como ha sido el caso en todos los resultados de cada ejemplo de codigo en los temas.

Este elemento se define con la etiqueta de linea <code><iframe></iframe></code> y su atributo <code>src</code> recibe la url del contenido que queremos mostrar.


En el primer ejemplo mostraremos este archivo pdf que es una Cheat Sheet osea una Hoja de atajos de Emmet.

- <a download href="./media/cheatsheet-emmet.pdf"><img src="img/download-arrow.svg"> cheatsheet-emmet.pdf</a>

```text
▼ carpeta raiz
| ▼ assets
  | > img
  | ▼ media
    | cheatsheet-emmet.pdf
    | HiFi.mp4
    | Plain-Folks.mp3
| acerca.html
| index.html
```

```html
<iframe src="./assets/media/cheatsheet-emmet.pdf"></iframe>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/iframes.html"></iframe>
</div>

Como puedes ver se carga el archivo en un recuadro pequeño ya que este el tamaño por defecto que traen los iframes, pero puedes cambiar esto utilizando los estilos CSS o con los atributo <code>width</code> y <code>height</code>

En este caso utilizare esta regla para los siguientes ejemplos:

```css
iframe {
  width: 100%
  height: 500px;
}
```

Ahora puedes ir a Google Maps y YouTube, y buscar en las opciones de insertar este codigo en tu web y veras que te daran un codigo htm, ya con la etiqueta <code><iframe></code> para que solo tengas que pegarla, de igual manera te dejo aquiel codigo para que lo copies y pegues.

El video de Youtube es el video de este curso del maestro JonMircha.

```html
<h2>Google Maps</h2>
<iframe
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3942300.6512684277!2d-88.45427850389456!3d15.218474934064501!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8f6a751a73b731cf%3A0x7ed1de82b6fb8264!2sHonduras!5e0!3m2!1sen!2shn!4v1635970346081!5m2!1sen!2shn"
  width="600"
  height="450"
  style="border:0;"
  allowfullscreen
  loading="lazy"
></iframe>

<h2>Youtube Video/h2>
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/videoseries?list=PLvq-jIkSeTUZYcX9SYwVe7f66afwd9qk_" title="YouTube video player"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen
></iframe>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/iframes2.html"></iframe>
</div>

Como puedes ver el resultado es el deseado, y asi como estos, hay muchos sitios que te ofrecen estos servicios, como Instagram, Facebook, etcetera.

Pero que pasa si queremos introducir otra pagina, pues tambien puedes hacerlo pero no con todas, porque hay sitios que rechazan estas conexiones, osea que no dejan que puedes meter sus paginas webs dentro de la tuya, empresas como Google o Facebook, como dije anteriormente, puedes introducir servicios de Facebook, pero como los comentarios que son servicios para desarrolladores pero no puedes meter la pagina principal, que es **https://facebook.com**.

Algunas paginas que puedes usar para este ejemplo, es mi blog o la pagina de jonmircha, que son las que usaremos en este ejemplo.

Y tambien veremos un ejemplo con la pagina de Facebook para que veas el resultado.

```html
<h2>PanLar Blog</h2>
<iframe src="https://panlar.github.io/blog"></iframe>
<h2>jonmircha.com</h2>
<iframe src="https://jonmircha.com"></iframe>
<h2>Facebook</h2>
<iframe src="https://facebook.com"></iframe>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/iframes3.html"></iframe>
</div>

<div class="pagination">
  <a href="#/audio-y-video" class="pagination-button">← Audio y Video </a>
  <a href="#/elementos-de-formulario" class="pagination-button">Elementos de Formulario →</a>
</div>