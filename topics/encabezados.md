# 11. Encabezados

Las Etiquetas de encabezados o <span class="emphasis">heading tags</span> en ingles se utilizan para definir los **títulos y subtítulos** de la página.

Existen *6 niveles de encabezado* iniciando desde el <span class="emphasis">1</span> como el nivel más alto hasta el <span class="emphasis">6</span> que es el más bajo, y se definen con esta etiqueta.

```html
<h1>Encabezado 1</h1>
<h2>Encabezado 2</h2>
<h3>Encabezado 3</h3>
<h4>Encabezado 4</h4>
<h5>Encabezado 5</h5>
<h6>Encabezado 6</h6>
```

Recuerda que todo el código visual de la página ira dentro de la etiqueta <span class="code">&lt;body></span>

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/encabezados.html"></iframe>
</div>

Un dato importante es que en este lenguaje existe una regla, y está relacionada con el SEO. Esta regla es que solo debe haber un solo encabezado de primer nivel (<span class="code">&lt;h1></span>) ya que este debería contener el tema principal, entonces los arañas o robots de los motores de búsqueda al revisar tu página identifican ese título y si existe más de uno entonces no sabrá exactamente de qué se trata tu página.