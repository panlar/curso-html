# 14. Etiquetas de salto

Como vimos en los dos temas anteriores existen etiquetas de *línea* de y de *bloque*, la diferencia entre una y la otra es una abarca solo el contenido que tiene y la otra abarca el 100% del ancho del contenedor, pero que pasa si quiero escribir una lista de elementos uno debajo del otro en un párrafo, podrías pensar en hacer esto

```html
<p>
Lista de elementos
  - Elemento 1
  - Elemento 2
  - Elemento 3
</p>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/etiquetas_salto.html"></iframe>
</div>

Pues bien, si lo ves, no nos da el resultado que deseamos, y para eso existen las **etiquetas de salto**, que son solo dos, <span class="code">&lt;br></span> y <span class="code">&lt;hr></span> que, a diferencia de las etiquetas que hasta ahora hemos visto que tienen una apertura p y un cierre /p estas solo tienen la de apertura ya que no necesitan tener ningún contenido dentro de ellas y algo opcional que antes era obligatorio es que estas etiquetas pueden o no, llevar una barra diagonal antes del cierre de la etiqueta, o sea que sería lo mismo escribir <span class="code">&lt;br></span> y <span class="code">&lt;br/></span> no hay ningún problema.

Y, la diferencia entre estas es que, <span class="code">&lt;br></span> define un salto de línea normal, como si tu presionaras enter al escribir, y <span class="code">&lt;hr></span> define un salto semántico, esto quiere decir que al usar esta etiqueta estas definiendo que ahí acabas un tema y empiezas uno diferente o el siguiente, y esta última se representa visualmente como una línea horizontal.

```html
<p>
  Lista de elementos
  <br>
  - Elemento 1
  <br>
  - Elemento 2
  <br>
  - Elemento 3
</p>

<p>
  <h2>Tema 1</h2>
  Esto es un salto
  <br>
  de linea
  <br>
  <br>
  Hice dos saltos de linea 😄
  <br>
  Aqui termino un tema
</p>

<hr>

<p>
  <h2>Tema 2</h2>
  Aqui estoy entrando al segundo tema
</p>

<hr>

<p>
  <h2>Tema 3</h2>
  Aqui estoy entrando al segundo tema
</p>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/etiquetas_salto2.html"></iframe>
</div>

Como pudiste ver, puedo colocar tantos salto de linea como sean necesarios.
