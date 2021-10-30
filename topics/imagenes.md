# 20. Imagenes

Talvez ya hayas visto que en muchas paginas web hay imagenes y hasta gif animados, y por si no, pues debes saber que si, en html no solo puedes usar texto, tambien puedes utilizar la multimedia.

En este tema veremos como insertar imagenes, que en realidad es muy sencillo, y en temas posteriores veremos como insertar videos y audio.

Para insertar una imagen en HTML se utiliza la etiqueta <code><img></code> que es una etiqueta que se cierra sola, osea no tiene etiqueta de cierre ya que con contendra ningun texto u otro contenido dentro.

Esta etiqueta tiene debe tener siempre dos atributos muy importantes que son <code>src</code> que al igual que en la etiqueta <code><script></code> contendra la ruta de donde se encuentra la imagen, y el atributo <code>alt</code> que esta etiqueta es muy importante y se puede decir obligatoria ya que funciona para la accesibilidad de personas con discpacidad visual, o cuando la imagen no pueda cargar por cualquier inconveniente, esta etiqueta contendra la informacion o descripcion de lo que se puede ver en la imagen.

La sintaxis de una etiqueta <code><img></code> seria la siguiente:

```html
<img src="ruta_de_la_imagen" alt="texto_alternativo_que_describe_la_imagen">
```

Los navegadores soportan mucho formatos de imagen, los mas comunes son <code>.png</code>, <code>.jpg</code>, <code>.gif</code>, <code>.svg</code>

En este tema probaremos los 4 formatos, para ello crearemos una nueva carpeta dentro de <code>assets</code> llamada <code>img</code> o <code>images</code> como tu prefieras, puedes llamarla como desees.

Dentro de ella guardaremos estas cuatro imagenes que puedes descargar dando clic en los siguientes enlaces.

- <a download href="./anochecer.png"><img src="./download-arrow.svg"> anochecer.png</a>
- <a download href="./perro.jpg"><img src="./download-arrow.svg"> perro.jpg</a>
- <a download href="./web_development_meme.gif"><img src="./download-arrow.svg"> web-development-meme.gif</a>
- <a download href="./logo_html.svg"><img src="./download-arrow.svg"> logo_html.svg</a>

Con lo que la estructura quedaria asi:

```text
> carpeta raíz
| > assets
  | > img
    | - anochecer.png
    | - logo_html.svg
    | - perro.jpg
    | - web_development_meme.gif
  | - styles.css
  | - script.js
| - index.html
```

Y nuestro codigo quedaria asi:

```html
<img src="./assets/img/anochecer.png" alt="anochecer">
<img src="./assets/img/perro.jpg" alt="perro negro">
<img src="./assets/img/web-development-meme.gif" alt="meme de desarrollo web">
<img src="./assets/img/logo_html.svg" alt="logo de html">
```

Y como puedes ver se muestran todas las imagenes, unas mas grandes que las otras, porque el navegador poner por defecto el ancho que tiene la imagen, pero a diferencia de las demas puedes notar que el ultimo tiene como ancho el 100% del contenedor, ya que este es un formato especial llamado <code>SVG</code> que son las siglas del ingles <span class="emphasis">Scalable Vectors Graphic</span> del cual hablaremos en el siguiente tema.

Para mejorar esta pagina y que todas las imagenes tengan un ancho del 100% utilizaremos una regla css para las imagenes, puedes colocarla en el archivo externo o con la etiqueta <code><style></code>.

```css
img {
  max-width: 100%;
  height: auto;
}

/*
  Con esta regla estamos indicando que las imagenes tendran
  un ancho del 100% y el maximo sera ese 100% y el alto sera
  automatico para que no se deforme la imagen.
*/
```