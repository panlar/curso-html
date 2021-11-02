# 24. Listas Desordenadas

Estas listas a diferencia de las ordenadas no estan enumeradas con caracteres como los numeros, letras o numeros romanos, solamente por unas viñetas, la cuales se cambian con el atributo <code>type</code> y a diferencia de las anteriores, estas listas solo aceptan este atributo ya que al no estar ordenadas no se puede dar reversa a la numeracion ni decir desde donde inicia a enumerarse.

ra definir una lista ordenada se utiliza la etiqueta <code><ul></ul></code> de <span class="emphasis">Unordered List</span> (*Lista Desordenada*) y tambien utiliza la etiqueta <code><li></code> para sus elementos.

```html
<h3>Tareas por hacer</h3>
<ul>
  <li>Terminar los ultimos temas del curso</li>
  <li>Tomar el curso de CSS</li>
  <li>Tomar el curso de JavaScript</li>
  <li>Tomar el curso de React.js</li>
</ul>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ul1.html"></iframe>
</div>

Como puedes ver, es una lista viñetada por discos de color negro, y como dije puede cambiarse con el atributo <code>type</code>.

```text
Valores para el atributo type en listas desordenadas:
- disk : Disco o circulo relleno | Valor por defecto.
- circle : Circulo sin relleno.
- square : Cuadrado relleno.
```

```html
<h3>Tareas por hacer</h3>
<ul type="disc">
  <li>Terminar los ultimos temas del curso</li>
  <li>Tomar el curso de CSS</li>
  <li>Tomar el curso de JavaScript</li>
  <li>Tomar el curso de React.js</li>
</ul>

<ul type="circle">
  <li>Terminar los ultimos temas del curso</li>
  <li>Tomar el curso de CSS</li>
  <li>Tomar el curso de JavaScript</li>
  <li>Tomar el curso de React.js</li>
</ul>

<ul type="square">
  <li>Terminar los ultimos temas del curso</li>
  <li>Tomar el curso de CSS</li>
  <li>Tomar el curso de JavaScript</li>
  <li>Tomar el curso de React.js</li>
</ul>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ul2.html"></iframe>
</div>

<div class="pagination">
  <a href="#/listas-ordenadas" class="pagination-button">← Listas Ordenadas</a>
  <a href="#/listas-de-definicion" class="pagination-button">Listas de Definicion →</a>
</div>