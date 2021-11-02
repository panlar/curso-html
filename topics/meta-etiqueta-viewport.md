# 9. Meta etiqueta **viewport**

Antes de saber cuál es la función de esta etiqueta hablaremos sobre el **viewport**.

En español viewport significa *ventana gráfica*, en el ámbito de desarrollo web este se refiere al espacio grafico del navegador donde se muestra el contenido del <span class="code">&lt;body></span> de la página, por ejemplo, todo el recuadro visible del contenido de este tema incluyendo este texto que has leído.

<img loading="lazy" src="https://i.postimg.cc/5y3LHKyX/viewport.png" alt="viewport" title="La parte clara es el viewport">

Ahora que ya sabes que es el viewport y lo has visto, tratare de explicarte cual es la función de esta etiqueta, y, si al final de este tema no sientes que no tienes idea de lo que se trata ya que es un tema más complicado de explicar que de entender, puedes ir a este artículo de <a href="https://desarrolloweb.com/articulos/etiqueta-meta-viewport.html" target="_blank"><img src="./img/link.svg"> desarrolloweb.com</a> que esta muy bien explicado.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Muy bien, ahora, debo decir que esta etiqueta es **necesaria y obligatoria** si quieres que el contenido se vea bien en los *dispositivos móviles*, y es que por esa razón fue creada esta misma, al introducir los teléfonos móviles al mundo y el internet, las paginas web no se veían del todo bien en estos ya que tienen una pantalla muy pequeña en comparación con los monitores, que eran el único lugar donde se visualizaban las páginas webs.

Como puedes ver en el valor de la etiqueta hay dos parámetros, el <span class="code">width</span> (<span class="emphasis">ancho</span>) y la <span class="code">initial-scale</span> (<span class="emphasis">escala inicial</span>);

El valor <span class="code">device-width</span> de <span class="emphasis">width</span> le indica al navegador que la pagina será tan ancha como es el ancho del dispositivo, así que si tienes un titulo en una sola línea en el móvil, si ese título es más largo que el ancho del viewport, hará tantos saltos de línea como necesite y así con todo el texto que escribas.

El valor <span class="code">1.0</span> de <span class="emphasis">initial-scale</span> indica que el contenido se visualizara en el tamaño normal, ósea que si cambiamos el valor a <span class="code">2.0</span> el contenido se vera al doble de lo normal.
