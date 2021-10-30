# 15. Etiquetas de formateo

Como bien pudimos ver anteriormente HTML no respeta los espacios en blanco y saltos en línea que escribes, para esos problemas también existe la etiqueta <code><pre></code> que proviene del inglés **pre formating**, y puedes lo que le dice al navegador es que el texto escrito dentro de esta etiqueta *se muestre tal y como esta*.

```html
<pre>
  Lista de elementos
    - Elemento 1
    - Elemento 2
    - Elemento 3
</pre>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/etiquetas_formateo.html"></iframe>
</div>

Como puedes ver, la lista se visualiza de la misma manera que fue escrita en el código, incluso *toma en cuenta los espacios en blanco* y también los formatea, pero como también notaras, existe un cambio de letra o fuente, como <code>monoespaciada</code>, similar a la de los ejemplos de código, y es que esa es una de las características de esta etiqueta al igual que la etiqueta <span class="code">&lt;code></span> que se utiliza para escribir código, que tiene el mismo formato de fuente con esta, pero que no respeta el pre formateado.

Para crear estos ejemplos de código yo utilice estas dos etiquetas en conjunto, pero antes de mostrarte el ejemplo, *¿recuerdas los caracteres especiales del tema atributo <code>charset</code>?* bien como aprendimos en ese tema si el navegador encuentra una o varias palabras dentro de los símbolos lo tomara como si fuera una etiqueta, entonces para eso utilizaremos estos caracteres espaciales;

```html
<pre>
  <code>
    &lt;html&gt;
    &lt;head&gt;
    &lt;/head&gt;
    &lt;body&gt;
    &lt;/body&gt;
    &lt;/html&gt;
  </code>
</pre>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/etiquetas_formateo2.html"></iframe>
</div>

Como puedes ver el texto se escribe tal y como si fuera puro codigo HTML gracias a estos caracteres especiales.
