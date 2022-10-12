---
title: <pre>
slug: Web/HTML/Element/pre
translation_of: Web/HTML/Element/pre
original_slug: Web/HTML/Elemento/pre
---
## Sumario

El **Elemento** **HTML \<pre>** (o _Texto HTML Preformateado_) representa texto preformateado. El texto en este elemento típicamente se muestra en una fuente fija, no proporcional, exactamente como es mostrado en el archivo. Los espacios dentro de este elemento también son mostrados como están escritos.

<ul class="htmlelt"><li><dfn><a href="/en-US/docs/HTML/Content_categories" title="HTML/Content_categories">Content categories</a></dfn> {{todo}}<a href="/en-US/docs/HTML/Content_categories#Flowing_content" title="HTML/Content_categories#Phrasing_content">Flow content</a>, palpable content.</li><li><dfn>Permitted content</dfn> <a href="/en-US/docs/HTML/Content_categories#Phrasing_content" title="/en-US/docs/HTML/Content_categories#Phrasing_content">Phrasing content</a>.</li><li><dfn>Tag omission</dfn> {{no_tag_omission}}</li><li><dfn>Permitted parent elements</dfn> Any element that accepts <a href="/en-US/docs/HTML/Content_categories#flow_content" title="HTML/Content categories#flow content">flow content</a>.</li><li><dfn>DOM interface</dfn> {{domxref("HTMLPreElement")}}</li></ul>

## Atributos

Este elemento solo incluye los [atributos globales](/es/docs/HTML/Global_attributes "/en-US/docs/").

## Ejemplos

```html
<!-- Un poco de codigo CSS -->
<pre>
body{
  color:  red;
}
a   {
  color:green;
}
</pre>
```

### Resultado

```html
body{
  color:  red;
}
a   {
  color:green;
}
```

## Especificaciones

| Epecificación                                                                                                    | Estado                           | Comentarios |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | ----------- |
| {{SpecName('HTML WHATWG', 'grouping-content.html#the-pre-element', '&lt;pre&gt;')}} | {{Spec2('HTML WHATWG')}} |             |
| {{SpecName('HTML5 W3C', 'the-pre-element.html#the-pre-element', '&lt;pre&gt;')}}     | {{Spec2('HTML5 W3C')}}     |             |
| {{SpecName('HTML4.01', 'text.html#h-9.3.4', '&lt;dl&gt;')}}                                 | {{Spec2('HTML4.01')}}     |             |

## Compatibilidad con exploradores

{{Compat("html.elements.pre")}}

## Véase también

- CSS: {{ Cssxref('white-space') }}, {{ Cssxref('word-break') }}
