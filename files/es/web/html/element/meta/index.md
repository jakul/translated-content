---
title: meta
slug: Web/HTML/Element/meta
tags:
  - HTML
  - HTML:Elemento
  - Todas_las_Categorías
translation_of: Web/HTML/Element/meta
original_slug: Web/HTML/Elemento/meta
---
### Definición

**meta** de "metainformation" - metainformación. Sirve para aportar información sobre el documento..

<dl><dd><strong>Sus etiquetas son</strong>: <code>&#x3C;meta></code> (solo tiene una).</dd><dd><strong>Está definido como</strong>: Elemento <a href="es/HTML/Elemento/Tipos_de_elementos#de_cabecera">de cabecera</a>.</dd></dl>

<dl><dd><strong>Crea una caja</strong>: No.</dd><dd><strong>Puede contener</strong>: Nada.</dd><dd><strong>Puede ser contenido por</strong>: Elementos <a href="es/HTML/Elemento/head">head</a></dd></dl>

#### Atributos

~~Por defecto~~: Debe indicarlo el autor.

name = name {{ mediawiki.external('CS') }} Este atributo identifica un nombre de propiedad. Esta especificación no enumera los valores legales para este atributo. content = cdata {{ mediawiki.external('CS') }} Este atributo especifica el valor de una propiedad. Esta especificación no enumera los valores legales para este atributo. scheme = cdata {{ mediawiki.external('CS') }} Este atributo especifica un esquema que se usará para interpretar el valor de la propiedad (véase la sección sobre perfiles para más detalles). http-equiv = name {{ mediawiki.external('CI') }} Este atributo puede utilizarse en lugar del atributo name. Los servidores HTTP utilizan este atributo para obtener información sobre los encabezados del mensaje de respuesta HTTP.

<table class="fullwidth-table standard-table">
  <tbody>
    <tr>
      <th>atributo</th>
      <th>descripción</th>
      <th>valor</th>
    </tr>
    <tr>
      <th colspan="3">Genéricos</th>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/dirlang.html#adef-lang"
          ><span style="color: green">lang</span></a
        >
      </td>
      <td>
        Información sobre el
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/dirlang.html"
          >idioma del contenido</a
        >
        del elemento y del valor de sus atributos.
      </td>
      <td>
        Un
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/types.html#type-langcode"
          >código de idioma</a
        >. Por defecto: "desconocido". Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/dirlang.html#adef-dir"
          ><span style="color: green">dir</span></a
        >
      </td>
      <td>
        Indica la
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/dirlang.html"
          >dirección de texto</a
        >
        y tablas.
      </td>
      <td>
        Uno de los siguientes: <abbr title="Left-to-right">'ltr' </abbr>o
        <abbr title="Right-to-left">'rtl'. </abbr>Por defecto: En castellano
        'ltr'. Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <th colspan="3">Específicos</th>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-name-META"
          ><span style="color: green">name</span></a
        >
      </td>
      <td>Nombre al que se asocia la metainformación</td>
      <td>
        Un 'nombre'. Sensible a
        <abbr title="diferencia entre Mayúsculas y minúsculas">M/m.</abbr> Por
        defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-content"
          ><span style="color: green">content</span></a
        >
      </td>
      <td>
        Los datos que se quieren asociar a
        <code style="color: green">name</code>.
      </td>
      <td>
        Texto. Sensible a
        <abbr title="diferencia entre Mayúsculas y minúsculas">M/m.</abbr>.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-http-equiv"
          ><span style="color: green">http-equiv</span></a
        >
      </td>
      <td>
        Aporta información sobre los encabezado de respuesta HTTP, puede usarse
        en lugar de <code style="color: green">name</code>.
      </td>
      <td>Un 'nombre'. Por defecto: Lo fija el navegador.</td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-scheme"
          ><span style="color: green">scheme</span></a
        >
      </td>
      <td>Indica un esquema de interpretación para los metadatos.</td>
      <td>
        Texto. Sensible a
        <abbr title="diferencia entre Mayúsculas y minúsculas">M/m.</abbr>. Por
        defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <th colspan="3">De transición</th>
    </tr>
    <tr>
      <td colspan="3">No tiene</td>
    </tr>
    <tr>
      <th>atributo</th>
      <th>descripción</th>
      <th>valor</th>
    </tr>
  </tbody>
</table>

### Ejemplos de uso

#### Con name y content

```
<meta name="copyright" content="© 2006 MDC">
```

#### Con http-equiv

```
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
```

### Estilo predeterminado

### Notas

### Referencia

- El elemento [**meta** en la especificación](http://html.conclase.net/w3c/html401-es/struct/global.html#edef-META) de html 4.01

### Soporte

Puede consultar esta [comparativa](http://www.webdevout.net/browser_support_html.php#support-html401-meta): IE 6 - IE 7 - FF 1.5 - OP 9.

---

> **Nota:** Estamos ampliando este documento, posiblemente contenga defectos y carencias. ¡Estamos en obras!... disculpen las molestias.
>
> ¿Quieres participar en su elaboración? Para saber cómo hacerlo consulta MDC:Como ayudar.

Categoría

interwiki links

automatismos
