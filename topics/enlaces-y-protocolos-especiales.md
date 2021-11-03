# 28. Enlaces y protocolos especiales

Ya vimos como nos sirven los enlaces para navegar entre sitios y paginas y dentro de las paginas, pero sabias que tambien nos sirven para enviar correos electronicos o realizar llamadas, este ultimo claramente en telefonos y laptops modernas en los que puedas hacer llamadas.

Para esto, se utilizan los protocolos <code>mailto</code> seguido de dos puntos y el correo y <code>tel</code> seguido de dos puntos, el codigo del pais y el numero de telefono.

```html
<a href="mailto:correo@mail.com" target="_blank">Enviar un correo a ####</a>
<br>
<a href="tel:50412345678" target="_blank">Realizar llamadas telefonicas</a>
```

<div class="iframe">
<div class="iframe-title">Resultado</div>
<iframe src="./iframes/protocolos.html"></iframe>
</div>

Si tienes una aplicacion de correo en tu computadora o telefono se abrira, sino, este protocolo no funcionara.
Para lo del telefono pues es lo mismo, pero todos los telefonos tiene la aplicacion de **telefono**.

Tambien puedes crear enlaces para enviar mensajes en WhatsApp, Telegram, Messenger, etcetera utilizando los enlaces que nos brindan estas aplicaciones, en este caso veremos un ejemplo para WhatsApp.

Para esto debes colocar la siguiente url en el atributo <code>href</code>:

```text
https://api.whatsapp.com/send?phone=504########&text=Hola, Soy Paul!

? : Indica que ingresaras variables.
phone : es el codigo y numero de telefono al que enviaras el mensaje | Obligatoria
& : Se ingresa para ingresar una nueva variable
text : es el texto que deseas enviar | Opcional
```

<div class="pagination">
  <a href="#/enlaces-internos" class="pagination-button">← Enlaces internos</a>
  <a href="#/elementos-interactivos" class="pagination-button">Elementos interactivos →</a>
</div>