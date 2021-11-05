# 35. Meta etiquetas para SEO y moviles.

Al inicio de este curso, en el capitulo 2 de **Informacion HTML** vimos algunas meta etiquetas como la <code>description</code> o la de <code>viewport</code>. En este caso veremos algunas mas que nos seran utiles para el SEO y para dispositivos moviles.

### Canonical

Esta palabra proviene de **canon** que significa o representa la version oficial u original de algo.

Pensemos en un sitio o tienda online, que al entrar al link proporcionado por un anuncion de descuento o promocion, puede ser una url con variables como vimos en el formulario, los motores de busqueda, identifican cada una de estas urls como diferentes, aunque te lleven al mismo sitio, pero debido a estas variables es qeu se toman de estas manera, y pues esto era sancionado por estos buscadores, y por esa razon se creo esta etiqueta que contendra como valor la url raiz u oficial del sitio, para que los buscadores sepan que se estan refiriendo a esa url.

```html
<meta name="canonical" content="https://tudominio.com">
```

### Favicon / Icon

Esta etiqueta recibe la url de la imagen que se mostrara en la pestaña del navegador y en los accesos directos de los dispositivos moviles y tablets. Para estas se utiliza la etiqueta <code><link></code>.

```html
<!-- Para los navegadores -->
<link rel="icon" href="./assets/img/logo_html.svg">

<!-- Para los dispositivos Moviles, Android & IOS -->
<link rel="apple-touch-icon" href="./assets/img/logo_html.svg">
```

### Color del Tema

Esta etiqueta se utiliza para colocar un color a la barra de direcciones de los navegadores moviles de *Chrome* e *Internet Samsung* y reciben un color en formato hexadecimal o en ingles.

```html
<meta name="theme-color" content="black">
<meta name="theme-color" content="#ff6600">
```
<div class="pagination">
  <a href="#/data-attributes" class="pagination-button">← Data attributes</a>
  <a href="#/meta-etiquetas-para-redes-sociales" class="pagination-button">Meta etiquetas para redes sociales →</a>
</div>
