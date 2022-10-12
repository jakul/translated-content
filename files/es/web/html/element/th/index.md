---
title: <th>
slug: Web/HTML/Element/th
translation_of: Web/HTML/Element/th
original_slug: Web/HTML/Elemento/th
---
El elemento **HTML `<th>` **define una celda como encabezado de un grupo de celdas en una tabla. La naturaleza exacta de este grupo está definida por los atributos {{htmlattrxref("scope", "th")}} y {{htmlattrxref("headers", "th")}}.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/en-US/docs/HTML/Content_categories"
          >Categorías de contenido</a
        >
      </th>
      <td>Ninguno</td>
    </tr>
    <tr>
      <th scope="row">Contenido permitido</th>
      <td>
        <div class="content-models">
          <div id="table-mdls">
            Contenido de flujo, pero sin encabezado, pie de página, contenido de
            seccionamiento, o contenido descendiente de encabezados
          </div>
        </div>
      </td>
    </tr>
    <tr>
      <th scope="row">Omisión de etiqueta</th>
      <td>
        La etiqueta de inicio es obligatoria.<br />La etiqueta de cierre puede
        ser omitida si es inmediatamente seguida por el elemento
        {{HTMLElement("th")}} o {{HTMLElement("td")}} o si no hay
        más datos en su elemento padre.
      </td>
    </tr>
    <tr>
      <th scope="row">Parents permítidos</th>
      <td>Un elemento {{HTMLElement("tr")}}</td>
    </tr>
    <tr>
      <th scope="row">Roles permítdos de ARIA</th>
      <td>Cualquiera</td>
    </tr>
    <tr>
      <th scope="row">Interfaz DOM</th>
      <td>{{domxref("HTMLTableHeaderCellElement")}}</td>
    </tr>
  </tbody>
</table>

## Atributos

Este elemento incluye los [atributos globales](/es/docs/Web/HTML/Global_attributes).

<dl><dt>{{htmlattrdef("abbr")}} {{obsolete_inline}} in {{HTMLVersionInline("5")}}</dt><dd>Este atributo contiene una breve descripción del contenido de las celdas. Algunos agentes de usuario (e.g., a speech reader) pueden presentar esta descripción antes que el propio contenido.</dd><dd><div class="note"><strong>Nota de uso: </strong>No uses este atributo, ya que se ha vuelto obsoleto en el último estandar. Alternativamente, puedes poner la descripción abreviada dentro de la celda y colocarla el largo contenido en el atributo de <strong>title</strong>.</div></dd><dt>{{htmlattrdef("align")}} {{Deprecated_inline}} in {{HTMLVersionInline("4")}}, {{obsolete_inline}} in {{HTMLVersionInline("5")}}</dt><dd>Este atributo enumerado especifica cómo se tratará el alineado horizontal de la celda. Los valores posibles son:<ul><li><code>left</code>: El contenido se alinea a la izquierda de la celda.</li><li><code>center</code>: El contenido se centra en la celda.</li><li><code>right</code>: El contenido se alinea a la derecha de la celda.</li><li><code>justify</code> (solo con texto): El contenido se alarga para ocupar todo el ancho de la celda.</li><li><code>char</code> (solo con texto): El contenido es alineado a un caracter dentro de <code>&#x3C;th></code> con el offset mínimo. Este caracter esta definido por los atributos {{htmlattrxref("char", "th")}} y {{htmlattrxref("charoff", "th")}}.</li></ul><p>El valor por defecto cuando no se especifica este atributo es <code>left</code>.</p><div class="note"><p><strong>Nota: </strong>No usar este atributo, ya que está obsoleto en el último estándar.</p><ul><li>Para lograr el mismo efecto que con los valores <code>left</code>, <code>center</code>, <code>right </code>o <code>justify</code>, aplicar la propiedad CSS {{cssxref("text-align")}} al elemento.</li><li>Para lograr el mismo efecto que con el valor <code>char</code>, dar a la propiedad {{cssxref("text-align")}} el mismo valor que usarías para {{htmlattrxref("char", "th")}}. {{unimplemented_inline}} in CSS3.</li></ul></div></dd><dt>{{htmlattrdef("axis")}} {{obsolete_inline}} in {{HTMLVersionInline("5")}}</dt><dd>Este atributo contiene una lista de cadenas separadas por espacios. Cada cadena es el <code>id</code> de un grupo de celdas a las que se les aplica esta cabecera.<div class="note"><strong>Nota: </strong>Este atributo está obsoleto en el último estándar y no debe usarse. Puedes sustituirlo por {{htmlattrxref("scope", "th")}}.</div></dd><dt>{{htmlattrdef("bgcolor")}} {{Non-standard_inline}}</dt><dd>Este atributo define el color de fondo de cada celda en una columna. Consiste en una código hexadecimal de 6 digitos, con un prefijo '#'. Este atributo puede usarse con uno de los 16 colores predefinidos:<table><tbody><tr><td style="background-color: black; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>black</code> = "#000000"</td><td style="background-color: green; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>green</code> = "#008000"</td></tr><tr><td style="background-color: silver; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>silver</code> = "#C0C0C0"</td><td style="background-color: lime; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>lime</code> = "#00FF00"</td></tr><tr><td style="background-color: gray; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>gray</code> = "#808080"</td><td style="background-color: olive; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>olive</code> = "#808000"</td></tr><tr><td style="background-color: white; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>white</code> = "#FFFFFF"</td><td style="background-color: yellow; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>yellow</code> = "#FFFF00"</td></tr><tr><td style="background-color: maroon; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>maroon</code> = "#800000"</td><td style="background-color: navy; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>navy</code> = "#000080"</td></tr><tr><td style="background-color: red; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>red</code> = "#FF0000"</td><td style="background-color: blue; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>blue</code> = "#0000FF"</td></tr><tr><td style="background-color: purple; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>purple</code> = "#800080"</td><td style="background-color: teal; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>teal</code> = "#008080"</td></tr><tr><td style="background-color: fuchsia; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>fuchsia</code> = "#FF00FF"</td><td style="background-color: aqua; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>aqua</code> = "#00FFFF"</td></tr></tbody></table><div class="note"><strong>Nota:</strong> No usar este atributo, ya que no es un estándar y sólo esta implementado en algunas versiones de Microsoft Internet Explorer. El elemento {{HTMLElement("th")}} debe estilizarse usando <a href="/en-US/docs/CSS">CSS</a>. Para crear un efecto similar usa la propiedad {{cssxref("background-color")}}.</div></dd></dl>

- {{htmlattrdef("char")}} {{Deprecated_inline}} in {{HTMLVersionInline("4")}}, {{obsolete_inline}} in {{HTMLVersionInline("5")}}

  - : El contenido de la celda se alinea con un caracter en el elemento `<th>`. Los valores típicos incluyen un punto (.) para alinear números o valores monetarios. Si no se establece {{htmlattrxref("align", "th")}} como char, el atributo es ignorado.

    > **Nota:** No usar este atributo, ya que no está soportado por el último estándar. Para lograr el mismo efecto, puedes especificar el caracter como el primer valor de la propiedad {{cssxref("text-align")}}, {{unimplemented_inline}} en CSS3.

<!---->

- {{htmlattrdef("charoff")}} {{Deprecated_inline}} in {{HTMLVersionInline("4")}}, {{obsolete_inline}} in {{HTMLVersionInline("5")}}

  - : This attribute is used to shift column data to the right of the character specified by the **char** attribute. Its value specifies the length of this shift.

    > **Nota:** No usar este atributo, ya que no está soportado por el último estándar.

<!---->

- {{htmlattrdef("colspan")}}
  - : This attribute contains a positive integer value that indicates over how many columns a cell is extended. Its default value is `1.` If its value is set to `0`, the cell is extended to the last element of the {{HTMLElement("colgroup")}}. Values higher than 1000 are clipped down to 1000.
- {{htmlattrdef("headers")}}
  - : This attribute contains a list of space-separated strings, each corresponding to the `id` attributes of other {{HTMLElement("th")}} elements that relate to this element.
- {{htmlattrdef("rowspan")}}
  - : This attribute contains a positive integer value that indicates over how many rows a cells is extended. Its default value is `1.` If its value is set to `0`, the cell is extended to the last element of the table sections ({{HTMLElement("thead")}}, {{HTMLElement("tbody")}} or {{HTMLElement("tfoot")}}). Values higher than 65534 are clipped down to 65534.
- {{htmlattrdef("scope")}}

  - : This enumerated attribute defines the cells that the header (defined in the {{HTMLElement("th")}}) element relates to. It may have the following values:

    - `row`: The header relates to all cells of the row it belongs to.
    - `col`: The header relates to all cells of the column it belongs to.
    - `rowgroup`: The header belongs to a rowgroup and relates to all of its cells. These cells can be placed to the right or the left of the header, depending on the value of the [`dir`](/en-US/docs/Web/HTML/Global_attributes/dir) attribute in the {{HTMLElement("table")}} element.
    - `colgroup`: The header belongs to a colgroup and relates to all of its cells.
    - `auto`

- {{htmlattrdef("valign")}} {{Deprecated_inline}} in {{HTMLVersionInline("4")}}, {{obsolete_inline}} in {{HTMLVersionInline("5")}}

  - : This attribute specifies how a text is vertically aligned inside a cell. Possible values for this attribute are:

    - `baseline`: Positions the text near the bottom of the cell and aligns it with the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom. If characters don't descend below the baseline, the baseline value achieves the same effect as `bottom`.
    - `bottom`: Positions the text near the bottom of the cell.
    - `middle`: Centers the text in the cell.
    - and `top`: Positions the text near the top of the cell.

    > **Nota:** **Usage Note:** Do not use this attribute as it is no longer supported by the latest standard: use the CSS {{cssxref("vertical-align")}} property instead.

- {{htmlattrdef("width")}} {{Deprecated_inline}} in {{HTMLVersionInline(4.01)}}

  - : This attribute is used to define a recommended cell width. Additional space can be added with the [cellspacing](/es/docs/Web/API/HTMLTableElement/cellSpacing) and [cellpadding](/es/docs/Web/API/HTMLTableElement/cellPadding) properties and the width of the {{HTMLElement("col")}} element can also create extra width. But, if a column's width is too narrow to show a particular cell properly, it will be widened when displayed.

    > **Nota:** **Usage Note:** Do not use this attribute in the latest standard: use the CSS {{cssxref("width")}} property instead.

## Examples

See {{HTMLElement("table")}} for examples on `<th>`.

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}

## See also

- Other table-related HTML Elements: {{HTMLElement("caption")}}, {{HTMLElement("col")}}, {{HTMLElement("colgroup")}}, {{HTMLElement("table")}}, {{HTMLElement("tbody")}}, {{HTMLElement("td")}}, {{HTMLElement("tfoot")}}, {{HTMLElement("thead")}}, {{HTMLElement("tr")}}.

{{HTMLRef}}
