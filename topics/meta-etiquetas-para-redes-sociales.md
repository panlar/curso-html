# 36. Meta etiquetas para redes sociales.

Talvez ya hayas visto en algunas redes sociales como Facebook o Twitter que al publicar un enlace a veces sale como una tarjetita de ese sitio web, algo asi:

<img src="https://i.postimg.cc/DfbQKJc3/social-card.png" loading="lazy">

Esto se debe a estas maravillosas etiquetas que en lo personal a mi me gustan mucho. Estas existen gracias a un protocolo especial llamado Open Graph que fue hecho con el fin de enriquecer a la vista la comparticion de los enlaces. Existen muchas opciones para estas etiquetas y puedes verlas todas en la pagina oficial de <a href="https://ogp.me" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> Open Graph</a>.

En este tema veremos las cuatro opciones basicas que son:
 - <code>og:title</code> : Titulo de la pagina.
 - <code>og:description</code> : Descripcion de la pagina.
 - <code>og:image</code> : url de la imagen que se vera en la tarjeta del enlace, esta ruta debe ser absoluta, si es relativa no funcionara.
 - <code>og:url</code> : Recibe la url de la pagina web.

Estos valores van como valor del atributo <code>property</code> a diferencia de las otras que hemos visto que van en el atributo <code>name</code>.

```html
<meta property="og:title" content="Curso HTML">
<meta property="og:description" content="Aprende desde cero HTML con PanLar">
<meta property="og:image" content="https://panlarweb.com/curso-html/img/poster.jpg">
<meta property="og:url" content="https://panlarweb.com/curso-html">
```

<div class="pagination">
  <a href="#/meta-etiquetas-para-seo-y-moviles" class="pagination-button">← Meta etiquetas para SEO y moviles</a>
  <a href="#/accesibilidad-web" class="pagination-button"> Accesibildad web →</a>
</div>