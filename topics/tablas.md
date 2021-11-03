# 25. Tablas

Es momento de hablar de una de las primeras formas de maquetacion que tuvo HTML, y esas son las tablas, antes de que existieran algunas funcionalidades de maquetacion de CSS, las tablas eran utilizadas para maquetar sitios webs, y aunque su uso en la actualidad es muy escaso, es un tema importante y en algunos casos util, pero no se recomienda su uso, solo en casos especificos que si lo requieran.

Las tablas en html pues estan conformadas de filas y columnas, si conoces MS Office Excel&reg; o las tablas de Word&reg; ya estaras familiarizad@ con estos conceptos.

```
                         Columnas
                _________________________
                ↓           ↓           ↓
          -------------------------------------
      | → |           |           |           |
      |   -------------------------------------
Filas | → |           |   Celda   |           |
      |   -------------------------------------
      | → |           |           |           |
          -------------------------------------
```

Los espacios horizontales son las filas y los verticales son las columnas  y cada interseccion de estas dos se llama celda.

Para definir una tabla se utiliza la etiqueta <code><table></table></code>

Para definir las filas se utiliza la etiqueta <code><tr></tr></code>, abreviatura de <span class="emphasis">table row</span> (*Fila de Tabla*)

Para definir las celdas de las filas se utiliza: <code><td></td></code>

En este primer ejemplo crearemos una tabla con la tematica de Marvel&reg; donde crearemos dos columnas, una para los Vengadores y otra para los Guardianes de la Galaxia, y por cada fila ira una heroe.

En estos ejemplos utilizaremos un atributo que ya **NO debe ser usado** ya que se considera una mala practica manipular el estilo de los elementos con HTML, pero para que veas la separacion y te hagas una idea, lo utilizaremos, este atributo es <code>border</code> y recibe un valor en numeros, y ese numero es la cantidad de pixeles que tendran los bordes de las celdas y de la tabla.

```html
<table border="1">
  <tr>
    <td>Los Vengadores</td>
    <td>Los Guardianes de la Galaxia</td>
  </tr>
  <tr>
    <td>Capitan America</td>
    <td>Stard Lord</td>
  </tr>
  <tr>
    <td>Iron Man</td>
    <td>Groot</td>
  </tr>
  <tr>
    <td>Viuda Negra</td>
    <td>Gamora</td>
  </tr>
  <tr>
    <td>Hulk</td>
    <td>Rocket</td>
  </tr>
  <tr>
    <td>Hawkeye</td>
    <td>Drax</td>
  </tr>
  <tr>
    <td>Thor</td>
  </tr>
</table>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/tablas1.html"></iframe>
</div>

Como pueds ver la tabla tiene la estructura que queriamos, bajo el titulo de cada grupo de heroes estan sus integrantes, y para que esto suceda como ves en el codigo, todas las celdas de una fila pues deben estar dentro de la fila y en su acumulacion van formando las columnas.

Existen otros elementos o etiquetas para las tablas y estos tienen fines semanticos, osea que la tabla tambien tendra un significado interno, estas etiquetas son:

- <code><thead></thead></code> : <span class="emphasis">Table Head</span> que significa cabeza de la tabla y aqui van pues los titulos de esta misma, y para completar cuentan con una etiqueta que es <code><th></th></code> : <span class="emphasis">Table Heading</span> que significa encabezado de tabla y transforman el texto dentro de ellos en negritas como las etiquetas <code><h1> - <h6></code>. Estas etiquetas se utilizan en lugar de la <code><td></code>.
- <code><tbody></tbody></code> : <span class="emphasis">Table Body</span> osea el cuerpo de la tabla y pues dentro de ella va todo el demas contenido principal de la tabla.
- <code><tfoot></tfoot></code> : <span class="emphasis">Table Foot</span> como podras ya estarlo pensando, se refiere al pie de la tabla y pues al igual que la etiqueta <code><footer></code> puedes poner enlaces, referencias de la tabla, etcetera.

Utilizaremos el ejemplo anterior pero cambiaremos ahora los nombres de los equipos para que esten en la cabecera de la tabla y sean encabezados y el pie de pagina lo utilizaremos para escribir la fuente de donde extraimos la informacion.

```html
<table border="1">
  <thead>
    <th>Los Vengadores</th>
    <th>Los Guardianes de la Galaxia</th>
  </thead>
  <tbody>
    <tr>
      <td>Capitan America</td>
      <td>Stard Lord</td>
    </tr>
    <tr>
      <td>Iron Man</td>
      <td>Groot</td>
    </tr>
    <tr>
      <td>Viuda Negra</td>
      <td>Gamora</td>
    </tr>
    <tr>
      <td>Hulk</td>
      <td>Rocket</td>
    </tr>
    <tr>
      <td>Hawkeye</td>
      <td>Drax</td>
    </tr>
    <tr>
      <td>Thor</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>
        Fuente:
        <cite>MARVEL&reg;</cite>
      </td>
    </tr>
  </tfoot>
</table>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/tablas2.html"></iframe>
</div>

Como puedes ver el proposito fue cumplido, incluso utilizamos una de las etiquetas semanticas para darle mas significado a la tabla.

Existen dos atributos para la etiqueta <code><td></code> los cuales son:

- <code>rowspan</code> : <span class="emphasis">Row Span</span>, recibe como valor un numero entero el cual idica cuantas filas ocupara la celda, puedes verlo como la funcion combinar celdas en Excel y Word.
- <code>colspan</code> : <span class="emphasis">Column Span</span>, hace lo mismo que el anterior pero con las columnas.

Veamos un ejemplo: Digamos que ahora queremos la misma tabla pero al reves.

```html
<table border="1">
  <tr>
    <th rowspan="6">Vengadores</th>
    <td>Captain America</td>
    <td rowspan="11">Info de <cite>MARVEL&reg;</cite></td>
  </tr>
  <tr>
    <td>Iron Man</td>
  </tr>
  <tr>
    <td>Black Widow</td>
  </tr>
  <tr>
    <td>Hulk</td>
  </tr>
  <tr>
    <td>Hawkeye</td>
  </tr>
  <tr>
    <td>Thor</td>
  </tr>
  <tr>
    <th rowspan="5">Guardianes de la Galaxia</th>
    <td>Stard Lord</td>
  </tr>
  <tr>
    <td>Groot</td>
  </tr>
  <tr>
    <td>Gamora</td>
  </tr>
  <tr>
    <td>Rocket</td>
  </tr>
  <tr>
    <td>Drax</td>
  </tr>
</table>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/tablas3.html"></iframe>
</div>

<div class="pagination">
  <a href="#/listas-de-definicion" class="pagination-button">← Listas de Definicion</a>
  <a href="#/enlaces" class="pagination-button">Enlaces →</a>
</div>