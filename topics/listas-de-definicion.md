# 25. Listas de Definicion

Estas lista cambian un poco con las anteriores ya que son un tipo especial de listas que como su nombre lo dice son para definir algo, su mayor uso y en realidad muy escaso ya que no se suelen utilizar son en glosarios o diccionarios web.

Estas listas constan de tres etiquetas o elementos y son
- <code>dl</code> del ingles <span class="emphasis">Definition List</span> (*Lista de Definicion*) y es el contenedor de la lista.
- <code>dt</code> de <span class="emphasis">Definition Term</span> (*Termino de Definicion*) que contendra el termino que queremos definir valga la redundancia.
- <code>dd</code> de <span class="emphasis">Definition Data</span> (*Datos de Definicion*) y pues contendra el significado o datos del termino.

```html
<h3>Algunos terminos de HTML son:</h3>
<dl>
  <dt>Etiquetas</dt>
  <dd>Son marcas contenedoras de los elementos en HTML.</dd>
  <dt>Atributos</dt>
  <dd>
    Propiedades de las etiquetas que manipulas ciertas caracteristicas y dan
    cierta funcionalidad.
  </dd>
</dl>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/dl.html"></iframe>
</div>

Como puedes ver es una lista con una indentacion o tabulacion luego del termino, esta etiqueta como te dije, es muy escaso su uso, pero es util para la semantica en el documento.

<div class="pagination">
  <a href="#/listas-desordenadas" class="pagination-button">← Listas Desordenadas</a>
  <a href="#/tablas" class="pagination-button">Tablas →</a>
</div>