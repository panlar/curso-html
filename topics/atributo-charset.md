# 8. Atributo **charset**

Este atributo es el indicador de la **codificación de caracteres** de la página.

```html
<meta charset="UTF-8">
```

Como ves el valor del atributo charset es <span class="code">“UTF-8”</span> esto quiere decir que el navegador tiene que mostrar todos los caracteres que existen en la codificación <a href="https://es.wikipedia.org/wiki/Unicode" target="_blank"><img src="./img/link.svg"> Unicode</a>
 e <a href="https://es.wikipedia.org/wiki/ISO/IEC_10646" target="_blank"><img src="./img/link.svg"> ISO 10646</a>.

Antes esta etiqueta era obligatoria y necesaria si querías escribir una página en lenguaje español ya que si no estaba no iba a mostrar caracteres como la <span class="emphasis">ñ</span>, la *tilde* (<span class="emphasis">´</span>), la *diéresis* (<span class="emphasis">¨</span>) y otros caracteres del español, y aunque ahora ya no es necesaria gracias a que los navegadores se han ido actualizando y no necesitan de esta etiqueta para mostrar estos caracteres, se considera una buena práctica añadirla siempre.

Puedes encontrar información mas detallada de esta etiqueta en este enlace, aunque con lo que ya sabes es suficiente 😄

- <a href="https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#la_codificaci%C3%B3n_de_caracteres_de_tu_documento" target="_blank"><img src="./img/link.svg"> meta charset</a>