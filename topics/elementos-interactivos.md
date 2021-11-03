# 29. Elementos Interactivos

Como su nombre lo dice, estos elementos nos dan cierta interactividad en la interfaz, hasta ahora solo hemos visto como hacer elementos estaticos, osea que no se mueven ni tienen algo mas que hacer que informar y mortrar, a excepcion de los enlaces, pero pues aunque si es interactivo, era mejor tratarlo en temas individuales ya que es un tema mas extenso.

El primer elemento es <code><button></button></code> que como te imaginaras es un boton. En realidad este elemento por si solo no tiene ninguna interactividad, necesita de JavaScript para funcionar, y este pues no es un curso de JS, pero te enseñare algo muy basico y necesario para que me entiendas el ejemplo.

Hay ciertos atributos que se utilizan para manejar los eventos que recreamos en la interaccion con la pagina y sus elementos, por ejemplo cuando damos clic en algo, cuando desplazamos la pagina o escribimos algo, esos son eventos, y existen muchos mas. Estos atributos se definen utilizando la palabra <code>on</code> seguido del evento en ingles, como <code>onclick</code> para reaccionar al dar click, o <code>onscroll</code> para reaccionar al desplazar la pagina.

Estos atributos reciben codigo JS como valor, por ejemplo, enviar un mensaje a la consola (<code>console.log()</code>) o enviar una alerta en la pagina (<code>alert()</code>)

En este caso utilizaremos el <code>onclick</code> en el boton para lanzar una alerta de que hemos hecho click en el, el codigo quedaria de la siguiente manera:

```html
<button onclick="alert('Has dado clic en el boton')">
  Boton Cliqueable
</button>
```

<blockquote>
  Ten cuidado con las comillas dobles y sencillas, ya que no puedes colocar comillas dobles dentro de los valores de estos atributos.
</blockquote>

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/interactivos.html"></iframe>
</div>

El siguiente elemento es uno que recientemente salio en HTML5 y es como acordion, los que tu puedes abrir y cerrar presionadolo. Este elemento es <code><details></details></code> y dentro de el iran dos elementos, el titulo dentro de la etiqueta <code><summary></summary></code> y una etiqueta contenedora osea de bloque, por ejemplo un <code><div></code> que es donde ira todo el contenido que colapsara.

```html
<details>
  <summary>Lenguajes para la web</summary>
  <div>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </div>
</details>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/interactivos2.html"></iframe>
</div>

Como puedes ver la interactividad si funciona y podemos y abrirlo con solo un clic, sin nada de programacion.

Si tu deseas que un acordion este abierto al iniciar la pagina puedes ponerle por defecto el *atributo  booleano* <code>open</code> que pues indica que ese acordio esta abierto. Y este mismo atributo es el que tiene al abrirlo nosotros con el clic y se le quita al cerrarlo.

Otro elemento interactivo es <code><dialog></dialog></code>, que es una caja de dialogo, mas popularmente llamada **ventana modal** entre los desarrolladores, estas ventanas son elementos que su sobreponen en los demas.

Ventana Modal:
<img src="https://i.postimg.cc/bJRt27vJ/ventana-modal.png" alt="Ventana Modal" title="Ventana Modal">

Esta etiqueta en realidad es una etiqueta experimental, osea que no es soportada por todos los navegadores. Y su uso no es recomendable hasta que por fin sea soportada por todos, pero de igual manera veamos un ejemplo practico.

Recuerda que si no se muestra en tu navegador puede ser porque no la soporta, puedes ver en que navegadores esta soportada y en que no en la pagina de <a href="https://caniuse.com/?search=dialog" target="_blank" rel="nofollow"><img src="./img/link.svg">Can I Use</a>.

Por defecto estos dialogo estan ocultos y para mostrarlo necesitan tener el atributo <code>open</code> al igual que <code><details></code>.

```html
<dialog open>Esta es una ventana de dialogo</dialog>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/interactivos3.html"></iframe>
</div>

Como puedes ver, pues es una simple caja centrada y con un border, como mencione antes, es experimental y no se recomienda su uso aun, es preferible hacerlo con los otros elementos HTML y CSS, ya que puedes hacer muchas cosas mas.

<div class="pagination">
  <a href="#/enlaces-y-protocolos-especiales" class="pagination-button">← Enlaces y protocolos especiales</a>
  <a href="#/audio-y-video" class="pagination-button">Audio y video →</a>
</div>