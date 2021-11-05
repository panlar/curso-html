# 34. Selects, Radios y Checkbox.

Ya vimos la mayoria de los atributos de los <code><input></code>, ahora veremos que mas podemos hacer con el <code><select></code> y como utilizar los <code<input></code> de tipo <code>radio</code> y <code>checkbox</code>.

### Select.

Ya vimos como utilizar un <code><select></code>, que necesita tener internamente las etiquetas <code><option></code>, para que estas etiquetas envien el dato que se selecciono, necesitan tener un valor definido en el atributo <code>value</code>.

Puedes seleccionar varias opciones utilizando el atributo booleano <code>multiple</code>

Tambien puedes tener un elemento seleccionado por defecto asignando el atributo <code>selected</code>. Este atributo es booleano y solo debe existir en una etiqueta <code><option></code> por <code><select></code>, a menos que este tenga el atributo <code>multiple</code>.

Tambien puedes utilizar el atributo <code>required</code> en estos elementos.

```html
<form>
  <label>Selecccione un lenguaje: </label>
  <!-- Utilizando el atributo value -->
  <select name="language">
    <option value="es">Español</option>
    <option value="en">Ingles</option>
    <option value="fr">Frances</option>
    <option value="it">Italiano</option>
  </select>

  <label>Selecccione varios lenguajes: </label>
  <!-- Utilizando el atributo multiple y required -->
  <select name="language" multiple required>
    <option value="es">Español</option>
    <option value="en">Ingles</option>
    <option value="fr">Frances</option>
    <option value="it">Italiano</option>
  </select>

  <label>Selecccione otro lenguaje: </label>
  <!-- Utilizando los atributos selected -->
  <select name="language">
    <option value="es">Español</option>
    <option value="en" selected>Ingles</option>
    <option value="fr">Frances</option>
    <option value="it">Italiano</option>
  </select>
  <input type="submit">
</form>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/src.html"></iframe>
</div>

### Radios

Como se menciono en el tema anterior con el atributo <code>name</code>, al utilizarlo en los controladores de tipo <code>radio</code>, todos estos que pertenezcan a un mismo grupo de opciones necesitan tener el mismo valor en el atributo <code>name</code>, y tener un valor en el atributo <code>value</code>.

Un controlador de este tipo solo muestra el boton, pero no su nombre o valor, para esto se utiliza la etiqueta <code><label></code>, y ya sabemos que para utilizarla tendremos que poner el controlador dentro de esta, y esta es una forma muy buena y rapida, pero tambien existe otra manera, que es utilizando el atributo <code>for</code> y este recibe el <code>id</code> del controlador con el que estara relacionado.

```html
<form>
  <h3>Selecciona un lenguaje Frontend</h3>

  <label>
    <input type="radio" name="language-front" value="html" />
    HTML
  </label>

  <label>
    <input type="radio" name="language-front" value="css" />
    CSS
  </label>

  <label>
    <input type="radio" name="language-front" value="js" />
    JavaScript
  </label>

  <h3>Selecciona un lenguaje Frontend</h3>

  <input type="radio" name="language-back" id="php" value="php" />
  <label for="php">PHP</label>

  <input type="radio" name="language-back" id="python" value="python" />
  <label for="python">Python</label>

  <input type="radio" name="language-back" id="go" value="go" />
  <label for="go">GO</label>
</form>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/src2.html"></iframe>
</div>

### Checkbox

En realidad no hay mucho misterio a la hora de utilizar estos controladores Se utilizan de la misma manera que los anteriores, pero al ser para seleccionar varias opciones deberian tener un <code>name</code> cada una.

```html
<form>
  <h3>Selecciona tus gustos</h3>
  <input type="checkbox" id="programmer" name="programmer" />
  <label for="programmer">Programar</label>
  <input type="checkbox" id="draw" name="draw" />
  <label for="draw">Dibujar</label>
  <label>
    <input type="checkbox" name="sing" />
    Cantar
  </label>
  <label>
    <input type="checkbox" name="run" />
    Correr
  </label>
</form>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/src3.html"></iframe>
</div>

Como ves se pueden utilizar ambas formas de relacionar la etiqueta label con el controlador en estos controladores, al igual que en todos los tipos que existen.

<div class="pagination">
  <a href="#/atributos-de-input-y-formulario" class="pagination-button">← Atributos de input y formulario.</a>
  <a href="#/data-attributes" class="pagination-button">Data Attributes →</a>
</div>