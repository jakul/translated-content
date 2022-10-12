---
title: '<progress>: Elemento indicador de progreso'
slug: Web/HTML/Element/progress
translation_of: Web/HTML/Element/progress
original_slug: Web/HTML/Elemento/progress
---
{{HTMLRef}}

La etiqueta **HTML\_ \_`<progress>`** se utiliza para visualizar el progreso de una tarea. Aunque los detalles de como se muestran depende directamente del navegador que utiliza el cliente, aunque básicamente aparece una barra de progreso.

{{EmbedInteractiveExample("pages/tabbed/progress.html", "tabbed-standard")}}

<p class="hidden">The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone <a href="https://github.com/mdn/interactive-examples">https://github.com/mdn/interactive-examples </a>and send us a pull request.</p>

<ul class="htmlelt"><li><dfn><a href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Flujo_de_contenido" title="HTML/Content_categories">Categorias de contenido </a></dfn><a href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Flujo_de_contenido" title="HTML/Content_categories">Flujo de contenido</a><span>, </span><a href="/es/docs/Web/Guide/HTML/categorias_de_contenido#Contenido_de_redacci%C3%B3n">contenido de redacción</a><span style="font-style: normal; line-height: 1.5em;">, contenido etiquetable, contenido palpable.</span></li><li><dfn>Contenido permitido</dfn> <a href="/en-US/docs/HTML/Content_categories#Phrasing_content" title="HTML/Content_categories#Phrasing_content">Contenido de redacción</a>, pero no debe haber ningún elemento de progreso entre sus descendientes</li><li><dfn>Etiquetas por omisión</dfn> {{no_tag_omission}}</li><li><dfn>Elementos padres permitidos</dfn> Cualquier elemento que acepte <a href="/en-US/docs/HTML/Content_categories#Phrasing_content" title="HTML/Content_categories#Phrasing_content">contenido de redacción</a>.</li><li><dfn>DOM interfaz</dfn> {{domxref("HTMLProgressElement")}}</li></ul>

## Atributos

Este elemento incluye [Atributos Globales](/es/docs/HTML/Global_attributes).

- {{ htmlattrdef("max") }}
  - : Este atributo indica la cantidad de trabajo que demorá la carga, se define en el elemento `progress`. Por ejemplo max="100".
- {{ htmlattrdef("value") }}

  - : Este atributo indica que parte de la tarea ya se ha completado o cargado. Debe especificarse un valor entre 0 y `max`, o entre 0 y 1.0 si `max` está omitido. Si al atributo `value` no se le especifica ningún valor, se estara llevando a cabo la tarea sin que el elemento mueste funcionamiento alguno. Por ejemplo si la carga está al 50% será de 0.5 el valor, en el caso de no especificar max.

Puedes usar la propiedad CSS {{ cssxref("orient") }} permite especificar la orientacion de la barra de progreso (horizontal o vertical) con horizontal por defecto. La pseudo-clase {{ cssxref(":indeterminate") }} se puede utiliza para hacer que coincida con las barras de progreso indeterminadas.

## Ejemplo

```html
<progress value="70" max="100">70 %</progress>
```

### Resultado

{{EmbedInteractiveExample("pages/tabbed/progress.html", "tabbed-standard")}}

En Mac OS X, Se vería como esto:

![progress-1.png](/@api/deki/files/4946/=progress-1.png)

En Windows, el resultante sería este:

![progress-firefox.JPG](/@api/deki/files/6031/=progress-firefox.JPG)

## Especificaciones

{{Specifications}}

## Compatibilidad con navegadores

{{Compat}}

## Véase también

- {{htmlelement("meter")}}
- {{ cssxref(":indeterminate") }}
- {{ cssxref("-moz-orient") }}
- {{ cssxref("::-moz-progress-bar") }}
- {{ cssxref("::-ms-fill") }}
- {{ cssxref("::-webkit-progress-bar") }}
- {{ cssxref("::-webkit-progress-value") }}
- {{ cssxref("::-webkit-progress-inner-element") }}
