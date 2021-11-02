# 22. Figuras

Pensemos en los libros de texto de las escuelas o cuentos, fabulas, ecetera, recuerdas que en algunas paginas venian imagenes con un titulo o leyenda en la parte inferior explicando que tema era o que representaba, algunos venian con el titulo similar a este: *"figura 1.1"*. En HTML las figuras son los mismo, son elementos como imagenes, pero tambien pueden ser videos que pueden estar relacionado con el tema, pero tambien no lo pueden estar ya que al igual que el <code><article></code> son elementos semanticos que pueden ser autocontenido, o sea, que se explica solo.

Para añadir figuras en html se utiliza la etiqueta <code><figure></figure></code> y para el titulo o pie de foto de la figura se utiliza <code><figcaption></figcaption></code>

Como dije anteriormente esta es una etiqueta de proposito semantico y es una muy buena practica utilizarla en todas o las mayoria de imagenes que lo necesites.

```html
<figure>
  <img src="./assets/img/anochecer/png" alt="anochecer" />
  <figcaption>Figura 22.1 Tema: Figuras</figcaption>
</figure>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/figuras.html"></iframe>
</div>

<div class="pagination">
  <a href="#/vectores" class="pagination-button">← Vectores</a>
  <a href="#/listas-ordenadas" class="pagination-button"> Listas Ordenadas →</a>
</div>