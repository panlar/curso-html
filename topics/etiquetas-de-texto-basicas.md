# 12. Etiquetas de texto básicas

Estas son etiquetas para escribir texto con un cierto estilo como en **negritas**, *cursiva*, <u>subrayadas</u>, etcétera, y aquí está la lista de todas ellas:

```html
<!-- Etiqueta para parrafos -->
<p>Esto es un parrafo de texto</p>

<!-- Etiqueta para negritas -->
<b>Esto es un texto en negrita</b>

<!-- Etiqueta para cursiva o italica -->
<i>Esto es un texto en cursiva</i>

<!-- 
  Etiqueta para subrayados
  No se recomiendo su uso ya que es mejor dar este esilo con CSS
  -->
<u>Eston es un texto subrayado</u>

<!-- Etiqueta para subindices -->
Esto es un subindice: H<sub>2</sub>O

<!-- Etiqueta para superindices -->
Esto es un superindice: 2<sup>3</sup>

<!-- Etiqueta para letras pequeñas -->
<small>Esto es un texto pequeño</small>

<!-- Etiqueta para marcados -->
<mark>Esto es un texto marcado</mark>
```
<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/texto_basicas.html"></iframe>
</div>

Como podrás ver en el resultado anterior todos los textos a excepción del párrafo están uno a lado del otro y es porque estas etiquetas son etiquetas de <span class="emphasis">línea</span>, esto quiere decir que solo abarcan el espacio de su contenido, ósea lo que tienen escrito dentro de ellas, y es por eso que cada una empieza donde acaba la anterior. Y la etiqueta <span class="code">&lt;p></span> abarca todo el ancho de su contenedor en este caso el <span class="code">&lt;body></span> aunque su contenido no lo necesite y es, porque esta es una etiqueta de <span class="emphasis">bloque</span>.

Esto lo veremos mas a fondo en unos temas mas.