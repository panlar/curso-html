# 32. Elementos de Formularios

Los formularios son otro tema de interactividad del usuario, y uno de los mas extensos e interesantes, ya que hay muchas cosas que se pueden hacer con sus elementos. En este tema veremos solo los elementos y en proximos temas los atributos y la variedad de opciones que hay.

Para definir un formualario se utiliza la etiqueta <code><form></form></code> y los elementos pues iran dentro de esta, aunque tambien pueden ir fuera, esto lo veremos en el proximo tema.

Los elementos de los formulario son los siguientes:


<code><input></code> : Crea una cajita para introducir datos, y existen de varios tipos que se definen con el atributo <code>type</code>, el valor por defecto es <code>text</code> y pues puedes escribir cualquier caracter, osea texto.

Recuerda que estas son etiquetas en linea por lo que necesitaras colocar un <code><br></code> para mostrarlos hacia abajo.

```html
<form>
  <input type="button" />
  <!--
    al igual que la etiqueta <button> crea un boton.
    - El texto del boton va dentro del atributo value.
  -->

  <input type="checkbox" />
  <!-- control que crea una casilla de selecion. -->

  <input type="color" />
  <!-- control que muestra una pequeña interfaz para seleccionar un color. -->

  <input type="date" />
  <!-- control para introducir una fecha (año, mes y día, sin tiempo). -->

  <input type="datetime" />
  <!-- control para introducir fecha y hora personalizada. -->

  <input type="email" />
  <!-- 
    control para introducir una dirección de correo electrónico.
    - el valor introducido se valida para que contenga una dirección de correo válida antes de enviarse.
   -->

  <input type="file" />
  <!-- control que permite al usuario seleccionar un archivo. -->

  <input type="hidden" />
  <!-- control que no es mostrado en pantalla, pero cuyo valor es enviado al servidor. -->

  <input type="image" />
  <!-- control de envío de formulario con una imagen. -->

  <input type="month" />
  <!-- control para introducir un mes y año. -->

  <input type="number" />
  <!-- control para introducir un número negativo o positivo. -->

  <input type="password" />
  <!-- control para introducir una contraseña -->

  <input type="radio" />
  <!-- control para seleccion unica de alguna opcion. -->

  <input type="range" />
  <!-- control para introducir un rango entre X y Y numero. -->

  <input type="reset" />
  <!-- control que restaura los elementos de un formulario a sus valores predeterminados. -->

  <input type="search" />
  <!-- cuadro de texto para búsquedas, incluye una x para borrar el texto introducido. -->

  <input type="submit" />
  <!-- control que envía el formulario. -->

  <input type="tel" />
  <!-- control para introducir un número telefónico. -->

  <input type="text" />
  <!-- campo de texto. -->

  <input type="time" />
  <!-- control para introducir una hora sin zona horaria específica. -->

  <input type="url" />
  <!--
    control para introducir una url.
    - el valor introducido se valida para que contenga una dirección url antes de enviarse.
  -->

  <input type="week" />
  <!-- control para introducir una semana del año. -->
</form>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios.html"></iframe>
</div>

<code><fieldset></fieldset></code> : <span class="emphasis">Campo</span> | Crea un cuadro contenedor de las secciones de un formulario.

<code><legend></legend></code> : <span class="emphasis">Legenda</span> | Se utiliza dentro de la etiqueta <code><fieldset></code> y sera el titulo de ese seccion del formulario.

```html
<fieldset>
  <legend>Seccion 1</legend>
</fieldset>
<fieldset>
  <legend>Seccion 2</legend>
</fieldset>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios2.html"></iframe>
</div>

<code><label></label></code> : <span class="emphasis">Rotulo</span> | Contiene el titulo de los elementos, y al darle click coloca el cursor en el elemento, y este debe estar dentro de esta etiqueta.

```html
<label>
  Nombre
  <input type="text" />
</label>
<label>
  Contraseña
  <input type="password" />
</label>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios3.html"></iframe>
</div>

<code><select></select></code> : <span class="emphasis">Seleccion</span> | Crea una lista de seleccion, cada elemento se define dentro de una etiqueta <code><option></code>.

<code><datalist></datalist></code> : <span class="emphasis">Lista de Datos</span> | Al igual que el anterior define una lista con la etiqueta <code><option></code> pero esta lista se usa junto con un <code><input></code> colocando un <code>id</code> a esta etiqueta y colocando en el atributo <code>list</code> el id de esta lista.

```html
<label>
  Seleccione un lenguaje:
  <select>
    <option></option>
    <option>HTML</option>
    <option>CSS</option>
    <option>JavaScript</option>
  </select>
</label>

<label>
  Seleccione un lenguaje:
  <input type="text" list="languages" />
  <datalist id="languages">
    <option>HTML</option>
    <option>CSS</option>
    <option>JavaScript</option>
  </datalist>
</label>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios4.html"></iframe>
</div>

<code><optgroup></optgroup</code> : <span class="emphasis">Grupo de Opciones</span> | Se utiliza para agrupar las opciones y puedes colocarle un titulo con el atributo <code>label</code>.

```html
<label>
  Selecciona un Lenguaje:
  <select>
    <optgroup label="Frontend">
      <option>HTML</option>
      <option>CSS</option>
      <option>JavaScript</option>
    </optgroup>
    <optgroup label="Backend">
      <option>PHP</option>
      <option>Python</option>
      <option>GO</option>
    </optgroup>
  </select>
</label>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios5.html"></iframe>
</div>

<code><textarea></textarea</code> : <span class="emphasis">Area de Texto</span> | Es una caja de texto pero multilinea a diferencia de los input que son de una sola linea. Esta caja se puede redimensionar

```html
<textarea></textarea>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios6.html"></iframe>
</div>

<code><output></output></code> : <span class="emphasis">Salida</span> | Se utiliza para mostrar el resultado de una operacion que ha hecho el usuario con la interaccion con los demas elementos, como una suma.

Para este ejemplo utilizaremos un poco de codigo JS en el codigo, asi que puedes copiarlo, y te explico como funciona.

```html
<form oninput="c.value = parseInt(a.value) + parseInt(b.value)">
  <input type="number" name="a" value="0" />
  +
  <input type="number" name="b" value="0" />
  =
  <output name="c">0</output>
</form>
```

```text
oninput="c.value = parseInt(a.value) + parseInt(b.value)"
```

Con este codigo le estamos diciendo que el <code>value</code> (*valor*) del elemento **c** que es el <code><output></code> con el <code>name="c"</code> sea igual a la suma de los valores de los elementos **a** y **b** que son los <code><input></code> con esos <code>name</code> Y que este valor cambie cada vez que entre un dato, osea cada vez que cambian los numeros, y, el atributo <code>value</code> se utiliza para definir un valor por defecto en el elemento.

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios7.html"></iframe>
</div>

<code><progress></progress></code> : <span class="emphasis">Progreso</span> | Se utiliza para ver el progreso de una tarea.

```html
<progress max="100" value="50"></progress>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/formularios8.html"></iframe>
</div>

<div class="pagination">
  <a href="#/iframes" class="pagination-button">← Iframes</a>
  <a href="#/atributos-de-input-y-formulario" class="pagination-button">Atributos de input y formulario →</a>
</div>