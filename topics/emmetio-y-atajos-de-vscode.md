# 2. Emmet.io y Atajos de VSCode

Emmet es un sistema o extensión de atajos similares a los selectores de CSS para la escritura en HTML, y la mayoría de editores de código traen esta extensión

Puedes encontrar su documentación en <a href="https://emmet.io/" target="_blank">Emmet.io</a>.

Aquí tienes una lista de los atajos con sus respectivos ejemplos:

### Elemento

Puedes escribir el nombre de cualquier elemento para generar las etiquetas HTML, aunque puedes escribir cualquier palabra que no sea el nombre de un elemento y al presionar la tecla tabulador para crear una etiqueta con ese nombre.

### Operadores de Anidamiento

#### Hijo <span class="code">&gt;</span>

Se utiliza para añadir un elemento dentro de otro

```html
<!-- Emmet: -->
div>p>span

<!-- Resultado: -->
<div>
  <p>
    <span></span>
  </p>
</div>
```

#### Hermano <span class="code">+</span>

Genera un elemento al lado de otro

```html
<!-- Emmet: -->
div+section

<!-- Resultado: -->
<div></div>
<section></section>
```

#### Ascenso <span class="code">^</span>

Este operador asciende en un nivel del árbol y coloca el elemento que esta después del operador, como hermano del padre del elemento que esta antes del operador.

```html
<!-- Emmet: -->
div>p>span^blockquote

<!-- Resultado: -->
<div>
  <p><span></span></p>
  <blockquote></blockquote>
</div>
```

Puedes usar tantos operadores de ascenso como quieras.

```html
<!-- Emmet: -->
div>p>span^^article

<!-- Resultado: -->
<div>
  <p><span></span></p>
</div>
<article></article>
```

#### Multiplicación <span class="code">*</span>

Define la cantidad de veces que se desea generar un elemento

```html
<!-- Emmet: -->
ul>li*3

<!-- Resultado: -->
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

#### Agrupación <span class="code">()</span>

Se utiliza para agrupar una rama del árbol y que sea independiente de las demás.

```html
<!-- Emmet: -->
section>(header>nav>ul)section

<!-- Resultado: -->
<section>
  <header>
    <nav>
      <ul></ul>
    </nav>
  </header>
  <section></section>
</section>
```

Las siguientes ramas luego del grupo se insertaran el mismo nivel o como hermanos del primer elemento del grupo.

Puedes anidar grupos entre sí y combinarlos con el operador de multiplicación

```html
<!-- Emmet: -->
section>((ul>(li>a)*3)*2)footer>p

<!-- Resultado: -->
<section>
  <ul>
    <li><a href=""></a></li>
    <li><a href=""></a></li>
    <li><a href=""></a></li>
  </ul>
  <ul>
    <li><a href=""></a></li>
    <li><a href=""></a></li>
    <li><a href=""></a></li>
  </ul>
  <footer>
    <p></p>
  </footer>
</section>
```

### Operadores de atributos

#### id <span class="code">#</span> y class <span class="code">.</span>

Para seleccionar un elemento con id específico en CSS se utiliza la <span class="code">#</span> (almohadilla o gatito o numeral) seguido del id y el <span class="code">.</span> (punto) seguido de la clase, y es igual en emmet, para agregar un id al elemento se utiliza la <span class="code">#</span> y para las clases el <span class="code">.</span>

```html
<!-- Emmet: -->
section#section1

<!-- Resultado: -->
<section id="section1"></section>
```

```html
<!-- Emmet: -->
main.container

<!-- Resultado: -->
<main class="container"></main>
```

Puedes agregar tantas clases como desees solamente poniendo una al lado de la otra siempre con el punto antecediendo a cada una.

```html
<!-- Emmet: -->
section.section.active

<!-- Resultado: -->
<section class="section active"></section>
```

#### Atributos personalizados <span class="code">[]</span>

Puedes usar la misma notación de los <span class="code">[...]</span> (Corchetes) que en CSS para añadir los atributos que desees.

```html
<!-- Emmet: -->
a[href="#"]

<!-- Resultado: -->
<a href="#"></a>
```

### Numeración de artículos <span class="code">$</span>

Con el operador de multiplicación puedes generar tantos elemento como desees y en conjunto con este puedes enumerar esos elementos, como por ejemplo que todos tengan el id ítem con el número de iteración de ese elemento.

```html
<!-- Emmet: -->
section#item$*3

<!-- Resultado: -->
<section id="item1"></section>
<section id="item2"></section>
<section id="item3"></section>
```

Puedes usar varios en una fila para rellenar los numero con ceros.

```html
<!-- Emmet: -->
section#item$$$*3

<!-- Resultado: -->
<section id="item001"></section>
<section id="item002"></section>
<section id="item003"></section>
```

Cambio de la base de número y dirección.

Con el modificador <span class="code">@</span> (arroba) seguido de un número <span class="code">@7</span>, puedes cambiar la base de inicio de la numeración donde la base será el número que sigue de la arroba.

```html
<!-- Emmet: -->
article.item$@5*3

<!-- Resultado: -->
<article class="item5"></article>
<article class="item6"></article>
<article class="item7"></article>
```

Juntando con la <span class="code">@</span> con un <span class="code">-</span> guion medio puedes cambiar la dirección de los números en descendente.

```html
<!-- Emmet: -->
div#box$@-*3

<!-- Resultado: -->
<div id="box3"></div>
<div id="box2"></div>
<div id="box1"></div>
```

Juntando los tres puedes crear una numeración descendiente donde el último elemento será el número base que tú escribiste.

```html
<!-- Emmet: -->
a[href="#$@-10"]*3

<!-- Resultado: -->
<a href="#12"></a>
<a href="#11"></a>
<a href="#10"></a>
```

### Mensaje de texto <span class="code">{}</span>

Puedes usar las llaves para agregar texto dentro de un elemento.

```html
<!-- Emmet: -->
button{click me}

<!-- Resultado: -->
<button>click me</button>
```