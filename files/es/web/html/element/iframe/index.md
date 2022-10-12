---
title: '<iframe>: el elemento Inline Frame'
slug: Web/HTML/Element/iframe
tags:
  - Contenido
  - Contenido incrustado
  - Elemento
  - Embebido
  - HTML
  - Incrustado
  - Marcos
  - Web
  - iframe
translation_of: Web/HTML/Element/iframe
original_slug: Web/HTML/Elemento/iframe
---
{{HTMLRef}}

El **elemento HTML `<iframe>`** (de inline frame) representa un {{Glossary("contexto de navegación")}} anidado, el cual permite incrustrar otra página HTML en la página actual.

{{EmbedInteractiveExample("pages/tabbed/iframe.html", "tabbed-standard")}}

Cada elemento `<iframe>` tiene su propio [historial de sesión](/es/docs/Web/API/History) y su propio objeto [Documento](/es/docs/Web/API/Document). El contexto de navegación que incluye el contenido implícito se llama _contexto de navegación principal_. El contexto de navegación de nivel superior (que no tiene padre) es típicamente la ventana del navegador, representado por el objeto {{domxref("Window")}}.

> **Advertencia:** Debido a que cada contexto de navegación es un entorno de documento completo, cada `<iframe>` en una página requiere más memoria y otros recursos informáticos. Aunque teóricamente puede utilizar tantos `<iframe>` como desee, compruebe si hay problemas de rendimiento.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/es/docs/Web/Guide/HTML/categorias_de_contenido"
          >Categorías de contenidos</a
        >
      </th>
      <td>
        <a
          href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Contenido_dinámico"
          >Contenido dinámico</a
        >,
        <a
          href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Contenido_textual_o_estático"
          >contenido textual o estático</a
        >, contenido incrustado, contenido interactivo,
        <a
          href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Contenido_tangible"
          >contenido tangible</a
        >.
      </td>
    </tr>
    <tr>
      <th scope="row">Contenido permitido</th>
      <td>
        Contenido alternativo que normalmente no se renderiza para los
        navegadores que no son compatibles con el elemento
        <code>&#x3C;iframe></code>.
      </td>
    </tr>
    <tr>
      <th scope="row">Omisión de etiqueta</th>
      <td>{{no_tag_omission}}</td>
    </tr>
    <tr>
      <th scope="row">Elementos padres permitidos</th>
      <td>Cualquier elemento que acepte contenido incrustado.</td>
    </tr>
    <tr>
      <th scope="row">Roles ARIA permitidos</th>
      <td>
        {{ARIARole("application")}}, {{ARIARole("document")}},
        {{ARIARole("img")}}
      </td>
    </tr>
    <tr>
      <th scope="row">Interfaz DOM</th>
      <td>{{domxref("HTMLIFrameElement")}}</td>
    </tr>
  </tbody>
</table>

## Atributos

Este elemento admite [atributos globales](/es/docs/Web/HTML/Atributos_Globales).

- En el atributo `target` de los elementos {{HTMLElement("a")}}, {{HTMLElement("from")}} y {{HTMLElement("base")}}.
- En el atributo `formtarget` de los elementos {{HTMLElement("input")}} y {{HTMLElement("button")}}
- En el parámetro `windowName` en el método {{domxref("Window.open()","window.open()")}}.

<dl><dt>{{htmlattrdef("allow")}}</dt><dd>Especifíca una <a href="/en-US/docs/Web/HTTP/Feature_Policy">política de características</a> para el <code>&#x3C;iframe></code>. Vea el articulo <a href="/en-US/docs/Web/Privacy">Privacy, permissions, and information security</a> para detalles en temas de seguridad y como <code>&#x3C;iframe></code> funciona con las Politicas de Herramientas para mantener los sistemas seguros.</dd><dt>{{htmlattrdef("allowfullscreen")}}</dt><dd>Definido como <code>true</code> si el <code>&#x3C;iframe></code> puede activar el modo a pantalla completa llamando al método {{domxref("Element.requestFullscreen", "requestFullscreen()")}}.</dd><dd><div class="blockIndicator note"><p>Se considera un atributo heredado y se redefine como <code>allow="fullscreen"</code>.</p></div></dd><dt>{{htmlattrdef("allowpaymentrequest")}}</dt><dd>Definido como <code>true</code> si se debe permitir que un <code>&#x3C;iframe></code> de origen cruzado pueda invocar el <a href="/en-US/docs/Web/API/Payment_Request_API">API de solicitud de pago</a>.</dd><dd><div class="blockIndicator note"><p>Se considera un atributo heredado y se redefine como <code>allow="payment"</code>.</p></div></dd><dt>{{htmlattrdef("csp")}} {{experimental_inline}}</dt><dd>Una <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP">Politica de Seguridad del Contenido</a> aplicada para el recurso incrustado. Vea {{domxref("HTMLIFrameElement.csp")}} para detalles.</dd><dt>{{ htmlattrdef("height") }}</dt><dd>Indica la altura del frame {{ HTMLVersionInline(5) }}en píxeles CSS, o {{ HTMLVersionInline(4.01) }} en píxeles o como un porcentaje.</dd><dt id="name-attribute">{{htmlattrdef("importance")}} {{experimental_inline}}</dt><dd>La prioridad de descarga en el recurso para el atributo <code>src</code> del <code>&#x3C;iframe></code>. Valores permitidos:<ul><li><code>auto</code>: (default) Sin preferencia. El buscador utiliza sus propias heurísticas para decidir la prioridad del recurso.</li><li><code>high</code>: El recurso debe ser descargado antes que otros recursos de baja-prioridad de los recursos de la página.</li><li><code>low</code>: El recurso debe ser descargado después de otros recursos de alta-prioridad de los recursos de la página.</li></ul><dl></dl></dd><dt>{{ htmlattrdef("name") }}</dt><dd>Nombre objetivo para el contexto de navegación incrustado. Se puede utilizar:<ul><li>En el atributo target de los elementos {{HTMLElement("a")}}, {{HTMLElement("from")}} y {{HTMLElement("base")}}.</li><li>En el atributo formtarget de los elementos {{HTMLElement("input")}} y {{HTMLElement("button")}}</li><li>En el parámetro windowName en el método {{domxref("Window.open()","window.open()")}}.</li></ul></dd><dt id="attr-referrer">{{htmlattrdef("referrerpolicy")}}</dt><dd>Indicates which <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/referrer">referrer</a> to send when fetching the frame's resource:<ul><li><code>no-referrer</code>: The {{HTTPHeader("Referer")}} header will not be sent.</li><li><code>no-referrer-when-downgrade</code> (default): The {{HTTPHeader("Referer")}} header will not be sent to {{Glossary("origin")}}s without {{Glossary("TLS")}} ({{Glossary("HTTPS")}}).</li><li><code>origin</code>: The sent referrer will be limited to the origin of the referring page: its <a href="https://developer.mozilla.org/en-US/docs/Archive/Mozilla/URIScheme">scheme</a>, {{Glossary("host")}}, and {{Glossary("port")}}.</li><li><code>origin-when-cross-origin</code>: The referrer sent to other origins will be limited to the scheme, the host, and the port. Navigations on the same origin will still include the path.</li><li><code>same-origin</code>: A referrer will be sent for {{Glossary("Same-origin policy", "same origin")}}, but cross-origin requests will contain no referrer information.</li><li><code>strict-origin</code>: Only send the origin of the document as the referrer when the protocol security level stays the same (HTTPS→HTTPS), but don't send it to a less secure destination (HTTPS→HTTP).</li><li><code>strict-origin-when-cross-origin</code>: Send a full URL when performing a same-origin request, only send the origin when the protocol security level stays the same (HTTPS→HTTPS), and send no header to a less secure destination (HTTPS→HTTP).</li><li><code>unsafe-url</code>: The referrer will include the origin <em>and</em> the path (but not the <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/hash">fragment</a>, <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/password">password</a>, or <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/username">username</a>). <strong>This value is unsafe</strong>, because it leaks origins and paths from TLS-protected resources to insecure origins.</li></ul></dd><dd><ul></ul></dd><dt>{{htmlattrdef("sandbox")}}</dt><dd>Applies extra restrictions to the content in the frame. The value of the attribute can either be empty to apply all restrictions, or space-separated tokens to lift particular restrictions:<ul><li><code>allow-forms</code>: Allows the resource to submit forms. If this keyword is not used, form submission is blocked.</li><li><code>allow-modals</code>: Lets the resource <a href="https://html.spec.whatwg.org/multipage/origin.html#sandboxed-modals-flag">open modal windows</a>.</li><li><code>allow-orientation-lock</code>: Lets the resource <a href="https://developer.mozilla.org/en-US/docs/Web/API/Screen/lockOrientation">lock the screen orientation</a>.</li><li><code>allow-pointer-lock</code>: Lets the resource use the <a href="https://developer.mozilla.org/en-US/docs/WebAPI/Pointer_Lock">Pointer Lock API</a>.</li><li><code>allow-popups</code>: Allows popups (such as <code>window.open()</code>, <code>target="_blank"</code>, or <code>showModalDialog()</code>). If this keyword is not used, the popup will silently fail to open.</li><li><code>allow-popups-to-escape-sandbox</code>: Lets the sandboxed document open new windows without those windows inheriting the sandboxing. For example, this can safely sandbox an advertisement without forcing the same restrictions upon the page the ad links to.</li><li><code>allow-presentation</code>: Lets the resource start a <a href="https://developer.mozilla.org/en-US/docs/Web/API/PresentationRequest">presentation session</a>.</li><li><code>allow-same-origin</code>: If this token is not used, the resource is treated as being from a special origin that always fails the {{Glossary("same-origin policy")}}.</li><li><code>allow-scripts</code>: Lets the resource run scripts (but not create popup windows).</li><li><code>allow-storage-access-by-user-activation</code> {{experimental_inline}}: Lets the resource request access to the parent's storage capabilities with the <a href="https://developer.mozilla.org/en-US/docs/Web/API/Storage_Access_API">Storage Access API</a>.</li><li><code>allow-top-navigation</code>: Lets the resource navigate the top-level browsing context (the one named <code>_top</code>).</li><li><code>allow-top-navigation-by-user-activation</code>: Lets the resource navigate the top-level browsing context, but only if initiated by a user gesture.</li></ul><div class="note"><strong>Notes about sandboxing:</strong><ul><li>When the embedded document has the same origin as the embedding page, it is <strong>strongly discouraged</strong> to use both <code>allow-scripts</code> and <code>allow-same-origin</code>, as that lets the embedded document remove the <code>sandbox</code> attribute — making it no more secure than not using the <code>sandbox</code> attribute at all.</li><li>Sandboxing is useless if the attacker can display content outside a sandboxed <code>iframe</code> — such as if the viewer opens the frame in a new tab. Such content should be also served from a <em>separate origin</em> to limit potential damage.</li><li>The <code>sandbox</code> attribute is unsupported in Internet Explorer 9 and earlier.</li></ul></div></dd><dt>{{ htmlattrdef("seamless") }}</dt><dd>This Boolean attribute indicates that the browser should render the inline frame in a way that makes it appear to be part of the containing document, for example by applying CSS styles that apply to the <code>&#x3C;iframe></code> to the contained document before styles specified in that document, and by opening links in the contained documents in the parent browsing context (unless another setting prevents this).</dd><dt>{{ htmlattrdef("src") }}</dt><dd>The URL of the page to embed.</dd><dt>{{ htmlattrdef("srcdoc") }}</dt><dd>The content of the page that the embedded context is to contain.</dd><dt>{{ htmlattrdef("width") }}</dt><dd>Indicates the width of the frame {{ HTMLVersionInline(5) }} in CSS pixels, or {{ HTMLVersionInline(4.01) }} in pixels or as a percentage.</dd></dl>

### Atributos obsoletos

Estos atributos están obsoletos y es posible que ya no sean compatibles con todos los agentes de usuario. No debe utilizarlos en contenido nuevo y tratar de eliminarlos del contenido existente.

- {{htmlattrdef("align")}} {{deprecated_inline("html4.01")}}, {{obsolete_inline("html5")}}
  - : La alineación de este elemento con respecto al contexto que lo rodea.
- {{ htmlattrdef("frameborder") }} {{ obsolete_inline("html5")}}

  - : El valor 1 (por defecto) indica al navegador establecer una frontera entre este marco y todo otro marco.&#x20;

    <span class="long_text" id="result_box" lang="es"><span class="gt-trans-draggable hps">El valor 0</span> <span class="gt-trans-draggable hps">indica</span> <span class="gt-trans-draggable hps">que el navegador no</span> establece<span class="gt-trans-draggable hps"> una</span> <span class="gt-trans-draggable hps">frontera</span> <span class="gt-trans-draggable hps">entre este marco y</span> <span class="gt-trans-draggable hps">otros marcos.</span></span>

- {{ htmlattrdef("longdesc") }} {{ obsolete_inline("html5")}}
  - : Una URI de una descripción larga del marco. Debido al mal uso generalizado, esto no es útil para navegadores no visuales.
- {{ htmlattrdef("marginheight") }} {{ obsolete_inline("html5") }}
  - : La cantidad de espacio en píxeles entre el contenido del marco y sus márgenes superior e inferior.
- {{ htmlattrdef("marginwidth") }} {{ obsolete_inline("html5") }}
  - : La cantidad de espacio en píxeles entre el contenido del marco y sus márgenes izquierdo y derecho.
- {{ htmlattrdef("scrolling") }} {{ obsolete_inline("html5") }}

  - : Indica cuándo el navegador debe proporcionar una barra de desplazamiento para el marco:

    - `auto`: Sólo cuando el contenido del marco es mayor que sus dimensiones.
    - `yes`: Muestra siempre una barra de desplazamiento.
    - `no`: No muestr la barra de desplazamiento nunca.

### Atributos no estándar

- {{htmlattrdef("mozbrowser")}} {{non-standard_inline}}

  - :&#x20;

    > **Nota:** See {{bug(1318532)}} for exposing this to WebExtensions in Firefox.

    Makes the `<iframe>` act like a top-level browser window. See [Browser API](/es/docs/Mozilla/Gecko/Chrome/API/Browser_API) for details.
    **Available only to [WebExtensions](/es/docs/Mozilla/Add-ons/WebExtensions).**

- {{ htmlattrdef("mozallowfullscreen") }} {{ non-standard_inline() }}
  - : In Gecko 9.0 or later, this attribute can be set to `true` if the frame is allowed to be placed into full screen mode by calling its {{ domxref("element.mozRequestFullScreen()") }} method. If this isn't set, the element can't be placed into full screen mode.
- {{ htmlattrdef("webkitallowfullscreen") }} {{ non-standard_inline() }}
  - : In Chrome 17 or later (and maybe earlier), this attribute can be set to `true` if the frame is allowed to be placed into full screen mode by calling its {{ domxref("element.webkitRequestFullScreen()") }} method. If this isn't set, the element can't be placed into full screen mode.
- {{ htmlattrdef("mozapp") }} {{ non-standard_inline() }}
  - : For frames hosting an [open web app](/en/Apps "https://developer.mozilla.org/en/OpenWebApps"), this specifies the URL of the [app manifest](/en/Apps/Manifest "https://developer.mozilla.org/en/Apps/Manifest"). This ensures that the app is loaded with the right permissions. See [Using the Browser API](/en/DOM/Using_the_Browser_API "https://developer.mozilla.org/en/DOM/Using_the_Browser_API") for details. Available in Gecko 13.0 and later.
- {{ htmlattrdef("remote") }} {{ non-standard_inline() }}
  - : Load the frame's page in a separate content process.

## Secuencia de comandos

Inline frames, like {{HTMLElement("frame")}} elements, are included in the {{domxref("window.frames")}} pseudo-array.

With the DOM {{domxref("HTMLIFrameElement")}} object, scripts can access the {{domxref("window")}} object of the framed resource via the {{domxref("HTMLIFrameElement.contentWindow", "contentWindow")}} property. The {{domxref("HTMLIFrameElement.contentDocument", "contentDocument")}} property refers to the `document` inside the `<iframe>`, same as `contentWindow.document`.

From the inside of a frame, a script can get a reference to its parent window with {{domxref("window.parent")}}.

Script access to a frame's content is subject to the {{Glossary("same-origin policy")}}. Scripts cannot access most properties in other `window` objects if the script was loaded from a different origin, including scripts inside a frame accessing the frame's parent. Cross-origin communication can be achieved using {{domxref("Window.postMessage()")}}.

## Ejemplos

### Un \<iframe> simple

Un `<iframe>` en acción. Después de crear el marco, cuando el usuario hace clic en un botón, su título se muestra en una alerta.

#### HTML

```html
<iframe src="https://mdn-samples.mozilla.org/snippets/html/iframe-simple-contents.html" title="iframe Example 1" width="400" height="300">
  <p>Your browser does not support iframes.</p>
</iframe>
```

#### Resultado

{{ EmbedLiveSample('Example1', 640,400)}}

### Abrir un enlace en un \<iframe> en otra pestaña

En este ejemplo, se muestra un mapa de Google en un marco.

#### HTML

```html
<iframe id="Example2"
    title="iframe Example 2"
    width="400" height="300"
    style="border:none"
    src="https://maps.google.com/maps?f=q&source=s_q&q=buenos+aires&sll=37.0625,-95.677068&sspn=38.638819,80.859375&t=h&hnear=Buenos+Aires,+Argentina&z=11&ll=-34.603723,-58.381593&output=embed">
</iframe>
```

#### Resultado

{{ EmbedLiveSample('Example2', 640, 400)}}

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}
