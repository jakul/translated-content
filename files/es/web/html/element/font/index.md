---
title: font
slug: Web/HTML/Element/font
tags:
  - HTML
  - HTML:Elemento
  - Todas_las_Categorías
translation_of: Web/HTML/Element/font
original_slug: Web/HTML/Elemento/font
---
### Definición

**font** -_fuente_ . Indica el tamaño, color, o fuente del texto que contiene.

<dl><dd><strong>Sus etiquetas son</strong>: &#x3C;font> y &#x3C;/font> (ambas obligatorias).</dd><dd><strong>Está definido como</strong>: Elemento <a href="es/HTML/Elemento/Tipos_de_elementos#desaprobado">desaprobado</a>.<dl><dd>En un doctype transicional está definido como un elemento <a href="es/HTML/Elemento/Tipos_de_elementos#especial">especial</a> y por lo tanto <a href="es/HTML/Elemento/Tipos_de_elementos#enlinea">en línea</a>.</dd></dl></dd></dl>

<dl><dd><strong>Crea una caja</strong>: En línea.</dd><dd><strong>Puede contener</strong>: Texto, y/o cero o más elementos <a href="es/HTML/Elemento/Tipos_de_elementos#enlinea">en línea </a>.</dd></dl>

#### Atributos

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
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-title"
          ><span style="color: green">title</span></a
        >
      </td>
      <td>
        Texto informativo o título del elemento. Suele mostrarse a modo de "tool
        tip".
      </td>
      <td>
        Texto legible por personas. Sensible a
        <abbr title="diferencia entre Mayúsculas y minúsculas">M/m.</abbr>. Por
        defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-id"
          ><span style="color: green">id</span></a
        >
      </td>
      <td>
        Le da un nombre al elemento que lo diferencia de todos los demás del
        documento.
      </td>
      <td>
        Un
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/types.html#type-id"
          >nombre único</a
        >. Sensible a
        <abbr title="diferencia entre Máyusculas y minúsculas">M/m.</abbr> Por
        defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/struct/global.html#adef-class"
          ><span style="color: green">class</span></a
        >
      </td>
      <td>Asigna nombres de clases al elemento. Por defecto, clases CSS.</td>
      <td>
        Lista de clases separadas por espacio en blanco. Sensible a
        <abbr title="diferencia entre Máyusculas y minúsculas">M/m.</abbr> Por
        defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/present/styles.html#adef-style"
          ><span style="color: green">style</span></a
        >
      </td>
      <td>
        Permite especificar
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/present/styles.html"
          >información de estilo</a
        >. Por defecto, estilos CSS.
      </td>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/types.html#type-style"
          >Declaraciones de estilo</a
        >. Por defecto: Lo fija el navegador.
      </td>
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
      <td colspan="3">No tiene</td>
    </tr>
    <tr>
      <th colspan="3">De transición</th>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/present/graphics.html#adef-size-FONT"
          ><span style="color: green">size</span></a
        >
      </td>
      <td>Tamaño de la fuente. Según una tabla del 1 al 7.</td>
      <td>
        Un número entero (ej. 1), o un valor incremental (ej. +1).
        <s>Por defecto:</s> debe indicarlo el autor.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/present/graphics.html#adef-color-FONT"
          ><span style="color: green">color</span></a
        >
      </td>
      <td>El color del texto.</td>
      <td>
        Un
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/types.html#h-6.5"
          >color RGB</a
        >. Por defecto: Lo fija el navegador.
      </td>
    </tr>
    <tr>
      <td>
        <a
          class="external"
          href="http://html.conclase.net/w3c/html401-es/present/graphics.html#adef-face-FONT"
          ><span style="color: green">face</span></a
        >
      </td>
      <td>Especifica la/s fuentes para el texto.</td>
      <td>
        Lista de nombres de fuentes separadas por coma. Por defecto: Lo fija el
        navegador.
      </td>
    </tr>
    <tr>
      <th>atributo</th>
      <th>descripción</th>
      <th>valor</th>
    </tr>
  </tbody>
</table>

### Ejemplos de uso

#### Un ejemplo simple

código:

```
<p>
 Texto normal y ...
 <font size="5" color="#0000ff"> Texto distinto. </font>
</p>
```

Resultado:

Texto normal y ... <font color="#0000ff" size="5">Texto distinto.</font>

### Estilo predeterminado

### Notas

### Referencia

- El elemento [**font** en la especificación](http://html.conclase.net/w3c/html401-es/present/graphics.html#edef-FONT) de html 4.01

### Soporte

Puede consultar esta [comparativa](http://www.webdevout.net/browser_support_html.php#support-html401-font): IE 6 - IE 7 - FF 1.5 - OP 9.

---

> **Nota:** Estamos ampliando este documento, posiblemente contenga defectos y carencias. ¡Estamos en obras!... disculpen las molestias.
>
> ¿Quieres participar en su elaboración? Para saber cómo hacerlo consulta MDC:Como ayudar.

Categoría

interwiki links

automatismos
