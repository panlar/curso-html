# 13. Etiquetas de texto semánticas

*¿Qué es la semántica?*
Si recuerdas bien los temas del español talvez ya lo sepas, y si no, pues la semántica es la parte de la lingüística que *estudia el significado* de las expresiones lingüísticas (Las palabras);

En HTML esta *se refiere al significado de algunas etiquetas*, si bien es cierto, pues una etiqueta <span class="code">&lt;b></span> representa un texto en **negrita**, la etiqueta <span class="code">&lt;i></span>, un texto en *cursiva*, pero hasta ahí no hay nada más que agregar, y pues es aquí donde entran este tipo de etiquetas, y es que, digamos que tú quieres escribir un texto más **importante** que el resto, pues para eso existe <span class="code">&lt;strong></span>, que es una etiqueta que visualmente hace lo mismo que <span class="code">&lt;b></span>, pero a nivel 
<span class="emphasis">semántico en HTML</span> y a nivel de 
<span class="emphasis">SEO</span> hace una diferencia, ya que los robots o arañas identifican este texto como representativo y una parte importante de la página.

Ahora te lo explico con otro ejemplo, digamos que tú quieres hacer *énfasis* en algún texto, énfasis es la fuerza de entonación con la que se dice alguna palabra o frase para que sobresalga del resto de la oración, entonces para eso también tenemos la etiqueta <span class="code">&lt;em></span>, que visualmente hace lo mismo que <span class="code">&lt;i></span>, pero como lo dije anteriormente, tiene diferencia en la 
<span class="emphasis">semántica HTML</span> y el 
<span class="emphasis">SEO</span>.

Y bien, ahora que ya sabes esto, aquí está la lista de *etiquetas semánticas para los textos*, ya que existen también **etiquetas semánticas estructurales**, pero las veremos en unos temas más.

```html
Al usar este sitio <em>estás de acuerdo</em> con <strong>Nuestros Términos y Condiciones</strong>.

<blockquote>
  Este texto es una cita en bloque donde puedes insertar un frase popular o conmemorativa
</blockquote>

<cite>
  Marca una referencia a una fuente, o el autor de un texto citado
</cite>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/etiquetas_semanticas_texto.html"></iframe>
</div>