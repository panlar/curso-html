# 23. Listas Ordenadas

Las listas no tiene mucha historia en realidad, son simples listas como las que ya conocemos, y existen tres tipos, en este tema veremos las **listas ordenadas** y se llaman asi porque van enumeradas por numeros, letras o numeros romanos lo que indica el orden.

La etiqueta para declarar estas listas es <code><ol></ol></code> que es la abreviatura de <span class="emphasis">Ordered List</span> (*Lista Ordenada*) y para definir elementos dentro de las listas se utiliza la etiqueta <code><li></li></code> que es la abreviatura de <span class="emphasis">List Item</span> (*Elemento de Lista*).

```html
<h3>Lenguajes de la Web</h3>
<ol>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ol1.html"></iframe>
</div>

Como puedes ver el resultado es una lista enumerada del 1 al 3.

Existen ciertos atributos para manipular el orden y la enumeracion de las listas ordenadas y estos son:

- <code>start</code> : recibe un valor numerico que indica desde que posicion inciara la lista.

```html
<h3>Lenguajes de la Web</h3>
<ol start="3">
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ol2.html"></iframe>
</div>

- <code>reversed</code> : es un atributo booleano, osea que si existe en la etiqueta se aplicara, y si no pues no sera asi. y lo que hace este atributo lo que hace es darle la vuelta (reversa) a la numeracion de la lista pero los elementos estan en el mismo orden en el que fueron declarados.

```html
<h3>Tecnologias Frontend JavaScript</h3>
<ol reversed>
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ol4.html"></iframe>
</div>

- <code>type</code> : recibe como valores una lista de caracteres que les indican que tipo de numeracion llevara la lista.

```text
Valores para el atributo type en listas ordenadas:
- 1 : Numeracion numerica | Valor por defecto
- A : Numeracion Alfabetica Mayuscula
- a : Numeracion Alfabetica Minuscula
- I : Numeracion Romana Mayuscula
- i : Numeracion Romana Minuscula
```

```html
<h3>Tecnologias Frontend JavaScript</h3>
<ol type="1">
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>

<ol type="A">
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>

<ol type="a">
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>

<ol type="I">
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>

<ol type="i">
  <li>Angular</li>
  <li>Vue</li>
  <li>React</li>
  <li>Svelte</li>
</ol>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/ol4.html"></iframe>
</div>

<div class="pagination">
  <a href="#/figuras" class="pagination-button">← Figuras</a>
  <a href="#/listas-desordenadas" class="pagination-button">Listas Desordenadas →</a>
</div>