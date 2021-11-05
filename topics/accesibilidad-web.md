# 37. Accesibildad Web.

Este es un tema muy importante en el desarrollo web, pero al momento de produccion a la mayoria de los desarrolladores se nos olvida o no le tomamos mucha importancia, y es que talvez recuerdes que te hable en el tema de las <a href="#/imagenes">Imagenes</a> sobre el atributo <code>alt</code> que nos servia para mostrar el texto en caso de que la imagen no se pueda visualizar ya sea por la conexion a internet o por que sea una persona con discapacidad visual que este navegando, y es en este ultimo caso donde entra la accesibilidad. Que pasaria si tenemos a una persona ciega o que tenga problemas en la vista, si selecciona un enlace y quiere saber hacia donde ira el enlaces pues puede que no lo sepa, y para eso existen atributos especiales para indicar que es, que hara, que contiene ese elemento.

Estos atributos son los <code>role</code> y <code>aria-attr</code>, del cual este ultimo es una larga lista de ellos.

### Role

El atributo <code>role</code> recibe un termino especial de una larga lista de valores que puede existir, y pues en español significa rol, osea que indicia cual es el rol o la funcion de ese elemento, como puede ser un <code>button</code>, <code>link</code>, <code>img</code>, etcetera.

```html
<button role="button">Abrir Menu</button>
<nav role="menu">
  <ul role="list">
    <li role="listitem">
      <a role="link">Link 1</a>
    </li>
    <li role="listitem">
      <a role="link">Link 2</a>
    </li>
  </ul>
</nav>
```

Como puedes ver existen varios valores, y pues estos lo que hacen es ayudar al usuario con discapacidad, a identificar que es cada elemento con sus opciones de accesibildad de cada dispositivo. Puedes leer mas sobre este atributo en <a href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> MDN <code>ARIA - Roles</code></a>

### ARIA

Las siglas ARIA vienen del nombre en ingles Accesible Rich Internet Applications que significa Aplicaciones de Internet Accesibles y Enriquecidas, y pues fueron creadas con ese proposito, basicamente mejorar las aplicaciones web.

Existen una larga lista de atributos <code>aria</code>, en este caso veremos solo una, pero puedes ver todos en <a href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#states_and_properties" target="_blank" rel="noreferrer nofollow"><img src="img/link.svg"> MDN <code>ARIA - States and Properties</code></a>

<code>aria-label</code> : Este atributo recibe un rotulo, etiqueta o titulo del elemento para que al momento de presionar el elemento el narrador de accesibildad le indique al usuario que hara, que es, o lo que tu desees o creas importante que deba saber el usuario.

```html
<a
  href="https://panlarweb.com/curso-html"
  aria-label="Este enlace te llevara al curso de HTML de PanLar"
>
  Curso HTML
</a>
```

<div class="pagination">
  <a href="#/meta-etiquetas-para-redes-sociales" class="pagination-button">← Meta etiquetas para redes sociales</a>
</div>