---
title: form
slug: Web/HTML/Element/form
translation_of: Web/HTML/Element/form
original_slug: Web/HTML/Elemento/form
---
## Resumen

El elemento HTML form (`<form>`) representa una sección de un documento que contiene controles interactivos que permiten a un usuario enviar información a un servidor web.

Es posible usar las pseudo-clasess de CSS [`:valid`](/es/CSS/%3Avalid) e [`:invalid`](/es/CSS/%3Ainvalid) para darle estilos a un elemento form.

## Contexto de uso

| Categorías de contenido | [Contenido dinámico](/en/HTML/Content_categories#flow_content)                                                                                                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Contenido permitido     | [Contenido dinámico](/en/HTML/Content_categories#flow_content), pero sin contener elementos `<form>`                                                                                  |
| Omisión de etiquetas    | Ninguna, ambas, la etiqueta de apertura y cierre deben estar presentes                                                                                                                |
| Normative document      | [HTML5, section 4.10.3](http://www.w3.org/TR/html5/forms.html#the-form-element) ([HTML4.01, section 17.3](http://www.w3.org/TR/1999/REC-html401-19991224/interact/forms.html#h-17.3)) |

## Atributos

Como cualquier otro elemento HTML, este elemento soporta [atributos globales](/en/HTML/Global_attributes)

<dl><dt>{{ htmlattrdef("accept") }} {{ HTMLVersionInline(4) }} {{ obsolete_inline() }}</dt><dd>Una lista separada por comas de los tipos de contenido que el servidor acepta.<br><div class="note"><p><strong>Nota de uso: </strong>este atributo ha sido removido en HTML5 y no debe ser usado. En su lugar, usar el atributo <strong><a href="/es/HTML/Element/Input#attr-accept" title="/en/HTML/Element/Input#attr-accept">accept</a></strong> del elemento específico {{ HTMLElement("input") }}.</p></div></dd><dt>{{ htmlattrdef("accept-charset") }}</dt><dd>Una lista de codificación de caracteres que el servidor acepta. La lista puede ser delimitada por espacios o comas. El navegador los usa en el orden en que cada uno son listados. Los valores por defecto es la cadena reservada "UNKNOWN", en tal caso la codificación corresponde a la codificación del documento conteniendo el elemento form.<br><p>HTML 4: En versiones anteriores de HTML, las diferentes codificaciones de caracteres pueden ser delimitadas por espacios o comas. Este no es más el caso en HTML5, donde sólo los espacios son correctos.</p></dd><dt>{{ htmlattrdef("action") }}</dt><dd>La URI de un programa que procesa la información enviada por medio del formulario. Este valor puede ser sobreescrito por un atributo {{ htmlattrxref("formaction", "button") }} en un {{ HTMLElement("button") }} o en el elemento{{ HTMLElement("input") }}.</dd><dt>{{ htmlattrdef("autocomplete") }} {{ HTMLVersionInline(5) }}</dt><dd>Indica cuales de los controles en este formulario puede tener sus valores automáticamente completados por el navegador. Esta configuración puede ser sobreescrita por un atributo <code>autocomplete</code> en un elemento que pertenezca al formulario:<ul><li><span style="font-family: Courier New;">off</span>: El usuario debe ingresar explicitamente cada valor dentro de cada campo por cada uso, o el documento provee su propio método de autocompletado; el navegador no autocompleta las entradas.</li><li><span style="font-family: Courier New;">on</span>: El navegador puede completar automáticamente valores basados en lo que el usuario ha ingresado durante entradas previas al formulario.</li></ul><div class="note"><p><strong>Nota:</strong> si se establece <code>autocomplete</code> a un valor de <code>off</code> en un formulario porque el documento provee su propio auto-completado entonces también se debería establecer <code>autocomplete</code> al valor <code>off</code> para cada uno de los elementos de formulario <code>input</code> que el documento pueda autocompletar <a href="#notas_para_google_chrome">Notas para Google Chrome</a>.</p></div></dd><dt>{{ htmlattrdef("enctype") }}</dt><dd>Cuando el valor del atributo <code>method</code> es <span style="font-family: Courier New;">post</span>, este atributo es el <a href="http://en.wikipedia.org/wiki/Mime_type">tipo MIME</a> del contenido que es usado para enviar el formulario al servidor.</dd><dd>Los posibles valores son:<ul><li><span style="font-family: Courier New;">application/x-www-form-urlencoded</span>: El valor por defecto si un atributo no está especificado.</li><li><span style="font-family: Courier New;">multipart/form-data</span>: Usar este valor si se está usando el elemento {{ HTMLElement("input") }} con el atributo <code>type</code> ajustado a "file".</li><li><span style="font-family: Courier New;">text/plain (HTML5)</span></li></ul><p>Este valor puede ser sobreescrito por un atributo{{ htmlattrxref("formenctype", "button") }}en un {{ HTMLElement("button") }} o un elemento {{ HTMLElement("input") }}.</p></dd><dt>{{ htmlattrdef("method") }}</dt><dd>El método <a class="external" href="http://www.w3.org/Protocols/rfc2616/rfc2616.html">HTTP</a> que el navegador usa para enviar el formulario. Valores posibles son:<ul><li><span style="font-family: Courier New;">post</span>: Corresponde al <a href="http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.5">método POST</a> HTTP ; los datos del formulario son incluidos en el cuerpo del formulario y son enviados al servidor.</li><li><span style="font-family: Courier New;">get</span>: Corresponde al <a href="http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.3">método GET</a> HTTP; los datos del formulario son adjuntados a la URI del atributo <code>action</code> , con un '?' como separador, y la URI resultante es enviada al servidor. Use este método cuando el formulario no tiene efectos secundarios y contiene solo caracteres ASCII.</li></ul><p>Este valor puede ser sobreescrito por un atributo {{ htmlattrxref("formmethod", "button") }} en un {{ HTMLElement("button") }} o elemento {{ HTMLElement("input") }}.</p></dd><dt>{{ htmlattrdef("name") }}</dt><dd>El nombre del formulario. En HTML4 ha quedado en desuso (debe usarse un <span style="font-family: Courier New;">id</span> en su lugar). Debe ser único entre los formularios en un documento y no una cadena vacia en HTML5.</dd><dt>{{ htmlattrdef("novalidate") }} {{ HTMLVersionInline(5) }}</dt><dd>Este atributo booleano indica que el formulario no es validado cuando es enviado. Si el atributo no existe {{ htmlattrxref("formnovalidate", "button") }} en un {{ HTMLElement("button") }} o en un elemento {{ HTMLElement("input") }} que pertenece al formulario.</dd><dt>{{ htmlattrdef("target") }}</dt><dd>Un nombre o keyword indicando donde mostrar la respuesta que es recibida después de enviar el formulario. En HTML 4, este es el nombre de, o una palabra clave, para un marco. En HTML5, es un nombre de, o palabra clave para, un contexto de navegación (por ejemplo, tab, window o marco en línea). Las siguientes palabras clave tienen significados especiales:<ul><li><span style="font-family: Courier New;">_self</span>: Carga la respuesta dentro del mismo frame HTML 4 (o en HTML5, contexto de navegación) como el marco actual. Este valor es por defecto si el atributo no es especificado.</li><li><span style="font-family: Courier New;">_blank</span>: Carga la respuesta dentro de una nueva ventana sin nombre en HTML 4 o un contexto de navegación en HTML5.</li><li><span style="font-family: Courier New;">_parent</span>: Carga la respuesta en el marco padre del marco actual en HTML 4 o en el contexto de navegación padre del marco actual en HTML5. Si no hay marco padre, esta opción se comporta de la misma manera que <span style="font-family: Courier New;">_self</span>.</li><li><span style="font-family: Courier New;">_top</span>: HTML 4: Carga la respuesta en toda la ventana original, cancelando otros marcos. HTML5: Carga la respuesta en el contexto de navegación de más alto nivel (esto es, el contexto de navegación que es ancestro del actual, y no tiene padre). Si no hay padre, esta opción se comporta igual que <span style="font-family: Courier New;">_self</span>.</li></ul><p>HTML5: Este valor puede ser sobreescrito por un atributo {{ htmlattrxref("formtarget", "button") }} en un elemento {{ HTMLElement("button") }} o{{ HTMLElement("input") }}.</p></dd></dl>

## Interfaz DOM

Este elemento implementa la interfaz [`HTMLFormElement`](/es/DOM/HTMLFormElement "en/DOM/form").

## Ejemplos

```html
<!-- Formulario simple que enviará una petición GET -->
<form action="">
  <label for="GET-name">Nombre:</label>
  <input id="GET-name" type="text" name="name">
  <input type="submit" value="Save">
</form>

<!-- Formulario simple que enviará una petición POST -->
<form action="" method="post">
  <label for="POST-name">Nombre:</label>
  <input id="POST-name" type="text" name="name">
  <input type="submit" value="Save">
</form>

<!-- Formulario con conjunto de campos, leyenda y etiqueta -->
<form action="" method="post">
  <fieldset>
    <legend>Título</legend>
    <input type="radio" name="radio" id="radio"> <label for="radio">Clic aquí</label>
  </fieldset>
</form>
```

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}

## Véase también

Otros elementos que son usados para crear formularios: {{ HTMLElement("button") }}, {{ HTMLElement("datalist") }}, {{ HTMLElement("fieldset") }}, {{ HTMLElement("input") }},{{ HTMLElement("keygen") }}, {{ HTMLElement("label") }}, {{ HTMLElement("legend") }}, {{ HTMLElement("meter") }}, {{ HTMLElement("optgroup") }}, {{ HTMLElement("option") }}, {{ HTMLElement("output") }}, {{ HTMLElement("progress") }}, {{ HTMLElement("select") }}, {{ HTMLElement("textarea") }}.

{{ languages( { "fr": "fr/HTML/Element/Form" } ) }}
