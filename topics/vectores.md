# 21. Vectores

Como te hable en el tema anterior los Vectores o SVG por sus siglas en ingles (<code>Scalable Vector Graphics</code>) son un lenguaje de marcado asi como HTML, creado por la **W3C** para crear graficos (dibujos y textos) y que los navegadores los puedan interpretar y mostrar.

Los SVG's son por decirlo de una manera facil, imagenes conformadas de formas basicas (Lineas, circulos, rectangulos, poligonos, curvas, etcetera), estas formas se definen en un lenguaje casi identico a HTML, que en realidad se llama XML (Extensible Markup Language) creado tambien por la **W3C**, que es un lenguaje para proposito general, osea que puede tener varios usos.

Los Vectores existen desde hace muchos años pero a pesar de eso no son muy conocidos como los formatos <code>png</code> o <code>jpg</code> ya que son mas utilizados por los diseñadores y desarrolladores, a diferencia de estos dos que la mayoria de las personas los conocen. Este formato es muy util ya que a diferencia de los otros, al tener un tamaño ya definido, si se escalan a mayores proporciones las imagenes pierden calidad, en cambio estos graficos, como su nombre lo dice, son escalables, ya que al estar hechos con codigos, el navegador los compila al tamano necesario y sin perder calidad. 

En el avance de los años. aunque es realidad que estos elementos fueron creados en XML han ido evolucionando y combinandose con el lenguaje HTML por lo que ahora puedes usar las mismas y mas caracteristicas en los vectores como aplicarles estilos con el atributo style, utilizar JavaScript con los eventos, etcetera.

Estos elementos en realidad son dificiles de manejar con codigo ya que entre mas elaborado es el grafico que deseemos, sera mucho mas codigo, coordenadas, etcetera, por lo que existen programas especiales para la creacion de estos con interfaces graficas y sin o poco codigo, programas como Adobe Illustratot e Inkspace que son los mas famosos, pero existen mucho mas.

En esta seccion del curso veremos lo basico de los SVG, como crear un cuadrado, un circulo y una linea y algunos atributos. Para crear un SVG pues se utiliza las etiquetas con el mismo nombre: <code><svg></svg></code> y dentro de ella iran los elementos.

```html
<svg
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
  width="100"
  height="100"
  viewBox="0 0 100 100"
>
</svg>
```

Como puedes ver esta etiqueta trae nuevos atributos:

<ol>
  <li><code>version:</code> Es la version de SVG que se esta utilizando.</li>
  <li>
    <code>xlmns:</code> Es el espacio de nombres utilizados en el dibujo, este
    atributo es obligatorio cuando esta en un archivo aparte y es utilizado
    con la etiqueta <code>img</code> como en el tema anterior de las
    imagenes, pero es opcional cuando lo introducimos como codigo dentro del
    documento html. El valor de este atributo siempre sera
    <b>"http://www.w3.org/2000/svg"</b>
  </li>
  <li><code>width:</code> Es el ancho en pixeles que tendra el grafico.</li>
  <li><code>height:</code> Es el alto en pixeles que tendra el grafico.</li>
  <li>
    <code>viewBox:</code> Es un conjunto de 4 numeros que indican en que
    coordenadas del eje X y Y y el ancho y alto del plano, significando cada
    uno lo siguiente:
    <ul>
      <li>
        Primer valor: Coordenada en el eje <b>X</b> u
        <b>horizontal</b> donde iniciara el plano de dibujo.
      </li>
      <li>
        Segundo valor: Coordenada en el eje <b>Y</b> u <b>vertical</b> donde
        iniciara el plano de dibujo.
      </li>
      <li>Tercer valor: Ancho en pixeles del plano de dibujo.</li>
      <li>Cuarto valor: Alto en pixeles del plano de dibujo.</li>
    </ul>
    Asi que esto quiere decir que la etiqueta <code>svg</code> solo
    representa el contenedor y que ahi hay un vector y el
    <code>viewBox</code> representa el plano en donde se dibujara el
    grafico, pero si por alguna razon este atributo no se declara el svg se
    toma como el mismo plano siendo el eje X y y el inicio del svg y el
    ancho y alto respectivamente.
  </li>
</ol>

<blockquote>
  Si el ancho y el alto del <code>svg</code> es 200 el <code>viewBox</code> anque tenga como ancho y alto 100, lo que hara este es escalarse al doble, osea que si por ejemplo dibujamos un cuadrado de <code>10px × 10px</code> ese cuadrado medira <code>20px × 20px</code>
</blockquote>

Si vemos el codigo anterior en el navegador no se vera nada ya que solo hemos declarado el contenedor pero no el contenido, para que podamos ver algo antes de iniciar a dibujar le agregaremos un color de fondo con el atributo <code><style></code>.

```html
<svg
  style="background-color: gray;"
>
</svg>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/vectores1.html"></iframe>
</div>

Ahora podras ver un cuadrado de color gris y de 100px de alto y ancho.

Ahora empezaremos dibujando un rectangulo que empiece a dibujarse 10px en eje X y 30px en el eje Y y que tenga un alto de 40px y un ancho de 70px utilizando la etiqueta <code><rect></code> dentro del <code><svg></code> como todo lo demas que haremos.

```html
<rect x="10" y="30" width="70" height="40" />
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/vectores2.html"></iframe>
</div>

Como puedes ver en el navegador se dibuja un rectangulo de color negro en la posicion que nosotros definimos y en del tamaño que definimos. y este tiene dos nuevos atributos que son <code>x</code> - <code>y</code> que al igual que los dos primeros valores de <code>viewBox</code> representan las coordernadas donde se dibujara el rectangulo.

existen muchos atributos para estos elementos pero veremos 3 mas que son:

1. <code>fill</code>: es el color (en formato hexadecimal <code>#000000</code> obligatoriamente) de relleno de la figura.
2. <code>stroke</code>: el color pero del trazo o borde igual en formato hexadecimal.
3. <code>stroke-width</code>: es el ancho del trazo.

Ahora haremos que ese rectangulo tenga un color blanco (<code>#FFFFFF</code>) de fondo, un azul (<code>#0066FF</code>) de trazo y un ancho de 5px;

```html
<rect
  fill="#FFFFFF"
  stroke="#0066FF"
  stroke-width="5"
/>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/vectores3.html"></iframe>
</div>

Como puedes ver hasta ahora todo ha funcionado correctamente, ahora lo que haremos sera un circulo, asi que utilizaremos la etiqueta <code><circle></code> y por ahora comentaremos la etiqueta del rectangulo para que nuestros dibujos no se revuelvan;

```html
<circle
  cx="50"
  cy="50"
  r="25"
  fill="#FFFFFF"
  stroke="#0066FF"
/>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/vectores4.html"></iframe>
</div>

Como puedes ver ahora se dibuja un circulo al centro del cuadrado gris y han cambiado algunos atributos como <code>x</code> por <code>cx</code> y <code>y</code> por <code>cy</code> ademas que ahora agregamos el atributo <code>r</code>

1. <code>cx</code>: este atributo es especial ya que lo que le dice al navegador es donde se colocara el centro del circulo en el eje X o vertical, a diferencia del rectangulo que dice donde se colocara la esquina superior izquierda.
2. <code>cy</code>: al igual que el anterior pero en el eje Y u horizontal.
3. <code>r</code>: Es la abreviatura de <span class="emphasis">radius</span> y pues indica eso, el radio del circulo.

Por ultimo dibujaremos dos trazos o lineas que formaran una X, y para esto se utiliza la etiqueta <code><path></code> asi que haremos lo mismo que lo anterior de comentar la etiqueta <code><circle></code>

```html
<path
  d="M 0,0 L 100,100 M 100,0 L 0,100"
  stroke="black"
/>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/vectores5.html"></iframe>
</div>

Si vemos el resultado del codigo anterior veremos que se forma una x perfecta en el cuadrado, pero talvex te cueste entender los valores, y esta es una de las razones por la cual utilizamos programas graficos en vez de escribir el codigo a mano. Pero te explicaremos esto que en realidad no es muy dificil.

El atributo <code>d</code> viene de la palabra <span class="emphasis">drawn</span> que español significaria dibujo o grafico y su valor es una cadena de comandos para dibujar estos trazos, los dos mas basicos son <code>M</code> y <code>L</code> que significan <span class="emphasis">MoveTo</span> y <span class="emphasis">LineTo</span> respectivamente, y los dos numeros son coordenadas en los dos ejes, X y Y respectivamente.

- <code>M</code> : Le estamos indicando al navegador que mueva el inicio del trazo a las coordenadas que le indicamos.
- <code>L</code> : Ahora le indicamos que dibuje un trazo desde la coordenadas que lo movimos anteriormente hasta las coordenadas que le indicamos seguidamente.

```text
M 0,0
El punto inicial de coloca a 0px en el eje X y Y (Esquina superior izquierda)

L 100,100
Se crea una linea o trazo a 100px en el eje X y Y (Esquina inferior derecha)

M 100,0
Se mueve el siguiente trazo hasta 100px en el eje X y 0px en el eje Y (Esquina superior derecha)

L 0,100
Se crea un nuevo trazo hasta 0px en el eje X y 100px en el eje Y (Esquina inferior izquierda)
```

Como ves, los svg se tratan de codigo y mucho mas codigo entre mas elaborado es el trazo, pero espero que esta introduccion te haya ayudado y ya sepas defenderte en lo basico de los graficos vectoriales.

<div class="pagination">
  <a href="#/imagenes" class="pagination-button">← Imagenes</a>
  <a href="#/figuras" class="pagination-button">Figuras →</a>
</div>