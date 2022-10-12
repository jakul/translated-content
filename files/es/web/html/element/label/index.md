---
title: <label>
slug: Web/HTML/Element/label
translation_of: Web/HTML/Element/label
original_slug: Web/HTML/Elemento/label
---
## Resumen

El\_ \_**Elemento** **HTML** **`<label> `**representa una etiqueta para un elemento en una interfaz de usuario. Este puede estar asociado con un control ya sea mediante la utilizacion del atributo for, o ubicando el control dentro del elemento label. Tal control es llamado "el control etiquetado" del elemento label.

<ul class="htmlelt"><li><dfn><a href="/en-US/docs/Web/HTML/Content_categories">Categorias</a></dfn> <a href="/en-US/docs/Web/HTML/Content_categories#Flow_content">Contenido de flujo</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">contenido de fraseo</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Interactive_content">contenido interactivo</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Form-associated_content">elemento de formulario asociado</a>, contenido palpable.</li><li><dfn>Contenido permitido</dfn> <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">Contenido de fraseo</a>, pero no otros componentes <code>label</code> ni otros elementos etiquetables a parte del de control ya etiquetado.</li><li><dfn>Omision del Tag</dfn> {{no_tag_omission}}</li><li><dfn>Elementos padre permitidos</dfn> Cualquier elemento que acepte el <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">contenido de fraseo</a>.</li><li><dfn>DOM interface</dfn> {{domxref("HTMLLabelElement")}}</li></ul>

## Atributos

Este elemento incluye los [atributos globales](/es/docs/Web/HTML/Global_attributes).

<dl><dt>{{htmlattrdef("accesskey")}} {{HTMLVersionInline("4")}} {{HTMLVersionInline("5")}}</dt><dd>Una tecla de atajo para acceder a este elemento desde el teclado.</dd><dt>{{htmlattrdef("for")}}</dt><dd>El ID del elemento de formulario etiquetable relacionado en el mismo documento que el elemento <span style="font-family: &#x27;Courier New&#x27;,&#x27;Andale Mono&#x27;,monospace; line-height: normal;">label</span><span style="line-height: 1.5;">. El primer elemento en el documento con tal ID que coincida con el dispuesto en el atributo </span><span style="font-family: &#x27;Courier New&#x27;,&#x27;Andale Mono&#x27;,monospace; line-height: normal;">for</span><span style="line-height: 1.5;"> será el control etiquetado para este elemento.</span></dd><dd><div class="note"><strong>Nota:</strong> Un elemento label puede contener ambos; El atributo for y el elemento de control anidado, siempre y cuando el atributo for <span style="line-height: 1.5em;">apunte al mismo elemento.</span></div></dd><dt>{{htmlattrdef("form")}} {{HTMLVersionInline("5")}}</dt><dd>El formulario con el cual el label está asociado (su formulario dueño). El valor de este atributo debe ser un ID del elemento {{HTMLElement("form")}} en el mismo documento. Si este atributo no es especificado, este elemento <code>&#x3C;label></code> deberia ser descendiente de un elemento {{HTMLElement("form")}}. Este atributo permite ubicar el elemento label en cualquier lugar dentro del documento y no solo como descendiente de su respectivo formulario.</dd></dl>

## Ejemplos

```html
<!-- Un simple ejemplo de un label con el atributo for -->
<label for="Name">Click me</label>
<input type="text" id="Name" name="Name" />

<!-- Aun mas simple -->
<label>Click me <input type="text" id="Name" name="Name" /></label>
```

### Resultado

<label>Click me <input></label>

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}

## See also

- Other form-related elements: {{HTMLElement("form")}}, {{HTMLElement("button")}}, {{HTMLElement("datalist")}}, {{HTMLElement("legend")}}, {{HTMLElement("select")}}, {{HTMLElement("optgroup")}}, {{HTMLElement("option")}}, {{HTMLElement("textarea")}}, {{HTMLElement("keygen")}}, {{HTMLElement("fieldset")}}, {{HTMLElement("output")}}, {{HTMLElement("progress")}} and {{HTMLElement("meter")}}.

{{HTMLRef}}
