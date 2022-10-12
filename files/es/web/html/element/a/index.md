---
title: <a>
slug: Web/HTML/Element/a
tags:
  - Contenido
  - Ejemplo
  - Elemento
  - HTML
  - Principiante
  - Referencia
  - Web
translation_of: Web/HTML/Element/a
original_slug: Web/HTML/Elemento/a
---
{{HTMLRef}}

El _Elemento HTML `Anchor`_ **`<a>`** crea un enlace a otras páginas de internet, archivos o ubicaciones dentro de la misma página, direcciones de correo, o cualquier otra URL.

{{EmbedInteractiveExample("pages/tabbed/a.html")}}

<div class="hidden">The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone <a href="https://github.com/mdn/interactive-examples">https://github.com/mdn/interactive-examples</a> and send us a pull request.</div>

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Categorías de contenido</th>
      <td>
        Contenido de flujo, contenido de párrafo, contenido interactivo,
        contenido palpable
      </td>
    </tr>
    <tr>
      <th scope="row">Contenido permitido</th>
      <td>
        <a
          href="/en-US/docs/HTML/Content_categories#Transparent_content_model"
          title="HTML/Content_categories#Transparent_content_model"
          >Transparente, que contiene contenido de flujo (excluyendo contenido
          interactivo) o contenido de párrafo.</a
        >
      </td>
    </tr>
    <tr>
      <th scope="row">Omisión de etiquetas</th>
      <td>{{no_tag_omission}}</td>
    </tr>
    <tr>
      <th scope="row">Elementos principales permitidos</th>
      <td>
        Cualquier elemento que acepte contenido de párrafo o cualquier elemento
        que acepte contenido de flujo, sin embargo simpre excluyendo los
        elementos &#x3C;a> (de acuerdo con el principio lógico de simetría, si
        una etiqueta &#x3C;a> como padre, no puede contener contenido
        interactivo, entonces el mismo contenido de &#x3C;a> no puede tener una
        etiqueta &#x3C;a> como su padre).
      </td>
    </tr>
    <tr>
      <th scope="row">Roles ARIA permitidos</th>
      <td>
        {{ARIARole("button")}}, {{ARIARole("checkbox")}},
        {{ARIARole("menuitem")}},
        {{ARIARole("menuitemcheckbox")}},
        {{ARIARole("menuitemradio")}}, {{ARIARole("option")}},
        {{ARIARole("radio")}}, {{ARIARole("switch")}},
        {{ARIARole("tab")}}, {{ARIARole("treeitem")}}
      </td>
    </tr>
    <tr>
      <th scope="row">Interfaz DOM</th>
      <td>{{domxref("HTMLAnchorElement")}}</td>
    </tr>
  </tbody>
</table>

## Atributos

Este elemento incluye los [atributos globales](/es/docs/HTML/Global_attributes "HTML/Global attributes").

<dl><dt>{{htmlattrdef("download")}} {{HTMLVersionInline(5)}}</dt><dd>Este atributo, indica descargar a los navegadores una URL en lugar de navegar hacia ella, por lo que el usuario será dirigido para salvarla como un archivo local. Si el atributo tiene un valor, éste se utilizará como nombre de archivo por defecto en el mensaje Guardar que se abre cuando el usuario hace clic en el enlace (sin embargo, el usuario puede cambiar el nombre antes de guardar el archivo). No hay restricciones sobre los valores permitidos, aunque: / y: \ se convertirán en guiones bajos (<em>underscores</em>), lo que evitará sugerencias de ruta específicas. Se debe tener en cuenta que la mayoría de los sistemas de archivos tienen limitaciones con respecto a los símbolos de puntuación admitidos en los nombres de archivo, por lo que los navegadores ajustarán los nombres de los archivos en consecuencia.<div class="note"><strong>Notas:</strong><ul><li>Este atributo sólo funciona para las <a href="https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy">políticas de mismo origen (same-origin URLs)</a>.</li><li>Este atributo puede ser utilizado con <a href="https://developer.mozilla.org/en-US/docs/Web/API/URL.createObjectURL"><code>blob:</code> URLs</a> y <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs"><code>data:</code> URLs</a> para descargar contenido generado por JavaScript, tales como fotografías creadas por una aplicación web de edición de imágenes.</li><li>Si el encabezado (<em>header</em>) HTTP <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Disposition"><code>Content-Disposition:</code></a> proporciona un nombre de archivo diferente al de este atributo, el encabezado HTTP tiene prioridad sobre este atributo.</li><li>Si <code>Content-Disposition:</code> está ajustado a <code>inline</code>, Firefox prioriza <code>Content-Disposition</code>, como en el caso del nombre de archivo, mientras que Chrome prioriza el atributo <code>download</code>.</li></ul></div></dd><dt>{{htmlattrdef("href")}}</dt><dd>Contiene una URL o un fragmento de URL al cual apunta el enlace.</dd><dd>Un fragmento de URL es un nombre ("name") precedido por el símbolo de número (<code>#</code>), el cual especifíca una ubicación interna objetivo (un <a href="https://developer.mozilla.org/en-US/docs/HTML/Global_attributes#attr-id">ID</a> de un elemento HTML) dentro del actual documento. Las URLs no están restringidas sólo a documentos de internet basados en HTTP, sin embargo pueden utilizar cualquier protocolo soportado por el navegador. Por ejemplo, <a class="external external-icon" href="https://en.wikipedia.org/wiki/File_URI_scheme"><code>file:</code></a>, <code>ftp:</code>, and <code>mailto:</code> funcionan en la mayoría de los navegadores.</dd><dd>Este atributo puede ser omitido (a partir de HTML5) para crear un enlace de marcador de posición. Un enlace de marcador de posición se parece a un enlace tradicional, pero que no dirige a algún lugar.<div class="note"><p><strong>Nota:</strong> Puede ser utilizado <code>href="#top"</code> o un fragmento vacío <code>href="#"</code> para enlazar a la parte superior de la página actual. <a href="https://www.w3.org/TR/html5/single-page.html#scroll-to-fragid">Este comportamiento está especficado en HTML5</a>.</p></div></dd><dt>{{htmlattrdef("hreflang")}}</dt><dd>Este atributo indica el lenguaje humano del recurso al que se enlaza. Este es únicamente informativo, sin ninguna funcionalidad incorporada. Los valores permitidos están determinados por <a class="external external-icon" href="https://www.ietf.org/rfc/bcp/bcp47.txt" title="Tags for Identifying Languages">BCP47</a>.</dd><dt>{{htmlattrdef("referrerpolicy")}} {{experimental_inline}}</dt><dd>Indica que <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer">referencia (<em>referer</em>)</a> enviar cuado la URL es recuperada:<ul><li><code>'no-referrer'</code> significa <code>Referer:</code> el encabezado no será enviado.</li><li><code>'no-referrer-when-downgrade'</code> significa sin <code>Referer:</code> el encabezado será enviado cuando se navega a un origen (<code>origin</code>) sin HTTPS. Este es un comportamiento por defecto.</li><li><code>'origin'</code> significa que el "referrer" estará en el <a href="https://developer.mozilla.org/en-US/docs/Glossary/Origin">origen</a> (<code>origin</code>) de la página, no incluye la información posterior al dominio.</li><li><code>'origin-when-cross-origin'</code> significa que la navegación a otros orígenes (<em>origins</em>) será limitada al esquema (<em>scheme</em>), el host y el puerto, mientras que la navegación en el mismo origen (origin) incuirá la trayectoria de referencia (<em>referrer's path</em>).</li><li><code>'unsafe-url'</code> significa que la referencia (<em>referrer</em>) incuirá el origen(<code>origin</code>) y la trayectoria (<em>path</em>), pero no el fragmento, contraseña o nombre de usuario. Esto es inseguro, ya que puede filtrar datos desde una URL segura hacia URLs inseguras.</li></ul></dd><dt>{{htmlattrdef("rel")}}</dt><dd>Especifica la relación del objeto de destino con el objeto de enlace. El valor es una lista separada por espacios de tipos de enlace<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types"> tipos de enlace (link types)</a>.</dd><dt>{{htmlattrdef("target")}}</dt><dd>Especifica en donde desplegar la URL enlazada. Es un nombre (<em>name of</em>), o palabra clave (<em>keyword for</em>), un contexto de navegación <em>(browsing context)</em>: una pestaña, ventana, o <code>&#x3C;iframe></code>. Las siguientes palabras clave (<em>keywords</em>) tienen significado especial:<ul><li><code>_self</code>: Carga la URL en el mismo contexto de navegación que el actual. Este es el comportamiento por defecto.</li><li><code>_blank</code>: Carga la URL en un nuevo contexto de navegación. Usualmente es una pestaña, sin embargo, los usuarios pueden configurar los navegadores para utilizar una ventana nueva en lugar de la pestaña.</li><li><code>_parent</code>: Carga la URL en el contexto de navegación padre (<em>parent</em>) del actual. Si no existe el padre, este se comporta del mismo modo que <code>_self</code>.</li><li><code>_top</code>: Carga la URL en le contexto más alto de navegación (el cual es un ancestro del actual, y no tiene padre (<em>parent</em>)). Si no hay padre (<em>parent</em>), este se comporta del mismo modo que <code>_self</code>.</li></ul><div class="note"><p><strong>Nota:</strong> Cuando se utiliza <code>target</code>, considera agregar <code>rel="noopener noreferrer"</code> para evitar el uso de la API <code>window.opener</code>.</p></div></dd><dt>{{htmlattrdef("type")}}</dt><dd>Especifica el tipo de medio (<em>media type</em>) en la forma de {{Glossary("MIME type")}} para la URL enlazada. Esto es únicamente informativo, sin ninguna funcionalidad incorporada.</dd><dt><h3 id="Obsoleto">Obsoleto</h3></dt><dt>{{htmlattrdef("charset")}} {{obsoleteGeneric("inline","HTML5")}}</dt><dd>Este atributo define la <a href="https://developer.mozilla.org/en-US/docs/Glossary/character_encoding">codificación de caracteres (character encoding)</a> de la URL enlazada. El valor debe de ser una lista delimitada por espacio y/o coma de caracteres definidos en <a class="external external-icon" href="https://tools.ietf.org/html/rfc2045">RFC 2045</a>. El valor por defecto es <code>ISO-8859-1</code>.<div class="note"><p><strong>Nota de uso:</strong> Este atributo es obsoleto en HTML5 y <strong>no debe ser utilizado por autores</strong>. Para lograr su efecto, se debe utilzar el encabezado HTTP <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type"><code>Content-Type:</code></a> en la URL enlazada.</p></div></dd><dt>{{htmlattrdef("coords")}} {{HTMLVersionInline(4)}} only, {{obsoleteGeneric("inline","HTML5")}}</dt><dd>Para utilizar con el siguiente atributo <code>shape</code>, este atributo utiliza una lista de números separada por comas para definir las coordenadas del enlace en la página.</dd><dt>{{htmlattrdef("name")}} {{HTMLVersionInline(4)}} only, {{obsoleteGeneric("inline","HTML5")}}</dt><dd>Este atributo era requerido para anclas (<em>anchors</em>) que definían una posible ubicación dentro de la página. En HTML 4.01, <code>id</code> y <code>name</code> podían ser utilizados simultáneamente en un elemento <code>&#x3C;a></code> simpre y cuando tuvieran valores idénticos.<div class="note"><p><strong>Nota de uso:</strong> Este atributo es obsoleto en HTML5, se utiliza el <a href="https://developer.mozilla.org/en-US/docs/HTML/Global_attributes#attr-id">atributo global <code>id</code></a> en su lugar.</p></div></dd><dt>{{htmlattrdef("rev")}} {{HTMLVersionInline(4)}} only, {{obsoleteGeneric("inline","HTML5")}}</dt><dd>Este atributo especifica un enlace inverso, la relación inversa del atributo <strong>rel</strong>. Fue desechado por ser muy confuso.</dd><dt>{{htmlattrdef("shape")}} {{HTMLVersionInline(4)}} only, {{obsoleteGeneric("inline","HTML5")}}</dt><dd>Este atributo era utilizado para definir una región de enlaces para crear un mapa de imagen. El valore es <code>circle</code>, <code>default</code>, <code>polygon</code>, y <code>rect</code>. El formato del atributo <code>coords</code> depende del valor de la forma geométrica. Para <code>circle</code>, el valor es <code>x,y,r</code> donde <code>x</code> y <code>y</code> son las coordenadas en pixel para el centro del círculo y <code>r</code> es el valor del radio en pixeles. Para <code>rect</code>, el atributo <code>coords</code> debe ser <code>x,y,w,h</code>. Los valores <code>x y y</code> definen la esquina superior izquierda del rectángulo, mientras que <code>w</code> y <code>h</code> definen el ancho y el alto respectivamente. Un valor del <code>polygon</code> para <code>shape</code> requiere los valores <code>x1,y1,x2,y2,...</code>para <code>coords</code>. Cada uno de los pares <code>x,y</code> definen un punto en el polígono, con puntos sucesivos que son unidos por líneas rectas y el útlimo punto se une al primer punto. El valor <code>default</code> para <code>shape</code> Requiere que el área encerrada, típicamente una imágen, sea utilizada.<div class="note"><strong>Nota:</strong> Utilice el <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attr-usemap">atributo <code>usemap</code></a> para el elemento {{HTMLElement("img")}} y el elemento asociado {{HTMLElement("map")}} para definir puntos de acceso (<em>hotspots</em>) en lugar del atributo <code>shape</code>.</div></dd></dl>

##

## Ejemplos

### Enlazando a una ubicación externa

```html
<!-- anclaje a un archivo externo -->
<a href="https://www.mozilla.com/">
Enlace externo
</a>
```

#### Resultado

[Enlace externo](https://www.mozilla.com/)

### Enlazando a otra sección de la misma página

```html
<!-- enlace a un elemento en esta página con id="attr-href" -->
<a href="#attr-href">
Descripción de enlaces de la misma página
</a>
```

#### Resultado

[Descripción de enlaces de la misma página](#attr-href)

### Creando una imagen clicable

Este ejemplo utiliza una imagen que enlaza a la página de inicio de MDN. La página de inicio se abrirá en un contexto de navegación nuevo, esto es, en una nueva página o nueva ventana.

```html
<a href="https://developer.mozilla.org/en-US/" target="_blank">
  <img src="https://mdn.mozillademos.org/files/6851/mdn_logo.png"
       alt="MDN logo" />
</a>
```

#### Resulta

{{EmbedLiveSample("Creating_a_clickable_image", "320", "64")}}

### Creando un enlace de correo

Es común crear enlaces que abren el programa de correo del usuario para permitir enviar un nuevo mensaje. Esto se hace con un enlace `mailto:`. Aquí tenemos un ejemplo:

```html
<a href="mailto:nowhere@mozilla.org">Enviar correo a nowhere</a>
```

#### Resultado

[Envia un correo a: nowhere](mailto:nowhere@mozilla.org)

Para detalles adicionales acerca del esquema de la URL `mailto`, tales como incluir el asunto, el cuerpo u otros contenidos predeterminados, consultar [Enlaces de correo (Email links)](/es/docs/Web/Guide/HTML/Email_links) o {{RFC(6068)}}.

### Creando un enlace a un número de teléfono

Ofrecer enlaces a números de teléfono es muy útil para los ususarios que observan documentos de internet desde computadoras portátiles conectadas a teléfonos o desde teléfonos celulares (móviles)

```html
<a href="tel:+491570156">+49 157 0156</a>
```

Para detalles adicionales acerca del esquema de la URL `tel`, consultar {{RFC(2806)}} y {{RFC(2396)}}.

### Utilizando el atributo `download` para guardar un `<canvas>` como PNG

Si deseas permitir a los usurios descargar una elemento HTML {{HTMLElement("canvas")}} como una imagen, puedes crear un enlace con una atributo `download` y la información canvas como un archivo URL:

```js
var link = document.createElement('a');
link.innerHTML = 'download image';

link.addEventListener('click', function(ev) {
    link.href = canvas.toDataURL();
    link.download = "mypainting.png";
}, false);

document.body.appendChild(link);
```

Puedes ver como funciona en: [jsfiddle.net/codepo8/V6ufG/2/](https://jsfiddle.net/codepo8/V6ufG/2/).

## Notas

HTML 3.2 define sólo los atributos `name`, `href`, `rel`, `rev`, y `title`.

### Recomendaciones de accesibilidad

Se abusa frecuntemente de las etiquetas de ancla (_anchor tags_) con el uso de los eventos `onclick` para crear pseudo-botones ajustando **href** a `"#"` o `"javascript:void(0)"` para prevenir la recarga de la página. Estos valores provocan comportamientos inesperados con los enlaces de copiado/dibujado, la apertura de enlaces en nuevas pestañas/ventanas, el guardado de enlaces (_bookmarking_), y cuando JavaScript está aún descargando, esto arroja errores, o es deshabilitado. Esto tambíen lleva a semánticas (_semantics_) incorrectas para tecnologías de asistencia (p.ej., lectores de pantalla). En estos casos, se recomienda utilizar un {{HTMLElement("button")}} en su lugar. En general, sólo se debe utilizar una ancla (_anchor_) para navegación utilizando una URL adecuada.

### Cliceo y enfoque

Cuando se clicea sobre un {{HTMLElement("a")}} las consecuencias varían de acuerdo al navegador y el sistema operativo.

| Navegadores de escritorio                                                                                                                             | Windows 8.1 | OS X 10.9                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------- |
| Firefox 30.0                                                                                                                                          | Si          | Si                              |
| Chrome ≥39 ([Chromium bug 388666](https://code.google.com/p/chromium/issues/detail?id=388666 "Issue 388666: Focus anchor (A) elements on mousedown")) | Si          | Si                              |
| Safari 7.0.5                                                                                                                                          | N/A         | Sólo cuando tiene un `tabindex` |
| Internet Explorer 11                                                                                                                                  | Si          | N/A                             |
| Presto (Opera 12)                                                                                                                                     | Si          | Si                              |

| Navegadores móviles | iOS 7.1.2                       | Android 4.4.4                   |
| ------------------- | ------------------------------- | ------------------------------- |
| Safari Mobile       | Sólo cuando tiene un `tabindex` | N/A                             |
| Chrome 35           | ???                             | Sólo cuando tiene un `tabindex` |

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}

## Consultar también

- Otros elementos comunicando a nivel semántico de texto [(text-level semantics)](/es/docs/HTML/Text_level_semantics_conveying_elements): {{HTMLElement("abbr")}}, {{HTMLElement("em")}}, {{HTMLElement("strong")}}, {{HTMLElement("small")}}, {{HTMLElement("cite")}}, {{HTMLElement("q")}}, {{HTMLElement("dfn")}}, {{HTMLElement("time")}}, {{HTMLElement("code")}}, {{HTMLElement("var")}}, {{HTMLElement("samp")}}, {{HTMLElement("kbd")}}, {{HTMLElement("sub")}}, {{HTMLElement("sup")}}, {{HTMLElement("b")}}, {{HTMLElement("i")}}, {{HTMLElement("mark")}}, {{HTMLElement("ruby")}}, {{HTMLElement("rp")}}, {{HTMLElement("rt")}}, {{HTMLElement("bdo")}}, {{HTMLElement("span")}}, {{HTMLElement("br")}}, {{HTMLElement("wbr")}}.
