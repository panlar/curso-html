# 30. Audio y Video

Como pudimos ver, se pueden insertar archivos multimedia como las imagenes en las paginas web, si tu eres muy joven talvez no te hayas dado cuenta de que antes de que existiera HTML5, se utilizaba una tecnologia llamada *Flash* para mostar audio y videos en estas paginas web.

HTML5 ademas de algunas etiquetas anteriores, tambien introdujo las etiquetas <code><audio></audio></code> y <code><video></video></code> que pues como su nombre los dice son utilizadas para agregar estos elementos. Ambas etiquetas son de **linea** y al igual que la etiqueta <code><img></code> utilizan el atributo <code>src</code> para definir la ruta de estos archivos.

Estas dos etiquetas comparten algunos atributos propios de ellas, que ademos son atributos booleanos, los cuales son:

- <code>controls</code> : Si este atributo no existe, el el caso del audio no se veran los controles de reproduccion, entonces no se podra escuchar nada, y en el caso del video, se vera el primer fotograma, osea el segundo 0 del video, pero no podras reproducir el video. Entonces este atributo es para mostrar los controles de reproduccion.
- <code>autoplay</code> : Este atributo es para que al momento de cargar el recurso o archivo se empieza a reproducir, **PERO** esto solo funcionara si la pagina ya tiene los permisos para reproducir estos, osea que si es primera vez que entras en la pagina tendras que darle estos permisos.
- <code>muted</code> : Al momento de iniciar a reproducir el audio o video estos empezara pero sin sonido, osea mudo y tendras que quitarlo con los controles.
- <code>preload</code> : Al momento de cargar los recursos, se carga la etiqueta pero no el archivo, sino que lo hace hasta el momento de reproducirlo, y este atributo lo que hace es que se <span class="emphasis">pre cargue</span> para que al momento de reproducir ya este todo o alguna parte cargada dependiendo de la velocidad de descarga de tu red.

Tambien existe otro atributo para los videos, la cual es <code>poster</code> y recibe como valor la url de la imagen que tu quieras que se visualice antes de reproducir el video, asi como las miniatura de YouTube.

Para este ejemplo utilizaremos estos dos archivos los cuales guardare en una carpeta llamada <code>media</code> dentro de <code>assets</code>.

- <a download href="./media/Plain-Folks.mp3"><img src="img/download-arrow.svg"> Plain-Folks.mp3</a>
- <a download href="./media/HiFi.mp4"><img src="img/download-arrow.svg"> HiFi.mp4</a>

```text
▼ carpeta raiz
| ▼ assets
  | > img
  | ▼ media
    | HiFi.mp4
    | Plain-Folks.mp3
| acerca.html
| index.html
```

Con <code>controls</code>

```html
<audio src="./assets/media/Plain-Folks.mp3" controls></audio>
<video src="./assets/media/HiFi.mp4" controls></video>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/audiovideo.html"></iframe>
</div>

Con <code>autoplay</code>, pero por razones para no molestar en este ejemplo no coloque ese atributo, pero tu puedes hacerlo y comprobarlo.

```html
<audio src="./assets/media/Plain-Folks.mp3" controls autoplay></audio>
<video src="./assets/media/HiFi.mp4" controls autoplay></video>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/audiovideo2.html"></iframe>
</div>

Con <code>muted</code>

```html
<audio src="./assets/media/Plain-Folks.mp3" controls muted></audio>
<video src="./assets/media/HiFi.mp4" controls muted></video>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/audiovideo3.html"></iframe>
</div>

Con <code>preload</code>

```html
<audio src="./assets/media/Plain-Folks.mp3" controls preload></audio>
<video src="./assets/media/HiFi.mp4" controls preload></video>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/audiovideo4.html"></iframe>
</div>

Con <code>poster</code>

```html
<video
  src="./assets/media/HiFi.mp4"
  poster="./assets/img/perro.jpg"
  controls
  preload
></video>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/audiovideo5.html"></iframe>
</div>

Como puedes ver por defecto, al igual que las imagenes el ancho pues el de su tamaño real pero puedes añadir la regla CSS que utilizamos en las imagenes, puedes añadir los mismos estilos a varias etiquetas separando estas por una coma, asi:

```css
img,
video {
  width: 100%;
  max-width: 100%;
  height: auto;
}
```

<div class="pagination">
  <a href="#/elementos-interactivos" class="pagination-button">← Elementos Interactivos</a>
  <a href="#/iframes" class="pagination-button">Iframes →</a>
</div>