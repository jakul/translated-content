---
title: itemref
slug: Web/HTML/Global_attributes/itemref
translation_of: Web/HTML/Global_attributes/itemref
original_slug: Web/HTML/Atributos_Globales/itemref
---
## Resumen

Las propiedades que no son descendientes de un elemento con el atributo `itemscope` pueden ser asociadas con el elemento usando un **itemref** . **Itemref** provee una lista de ids de los elementos (no `itemids`) con propiedades adicionales en otras partes dentro del documento .

El atributo itemref puede ser solo especificado en elementos que tienen un atributo itemscope especificado .

> **Nota:** el atributo itemref no es parte del modelo de micro datos . Es solamente un constructor sintáctico que ayuda a los autores en el ingreso de anotaciones a las páginas donde los datos que se van a anotar no siguen una estructura de arbol conveniente . Por ejemplo , permite a los autores marcar los datos en una tabla para que cada columna defina un item separado mientras se mantienen las propiedades en las celdas .

## Ejemplo
### HTML
```html
<div itemscope id="amanda" itemref="a b"></div>
<p id="a">Name: <span itemprop="name">Amanda</span> </p>
<div id="b" itemprop="band" itemscope itemref="c"></div>
<div id="c">
    <p>Band: <span itemprop="name">Jazz Band</span> </p>
    <p>Size: <span itemprop="size">12</span> players</p>
</div>
```

### Datos estructurados
<table class="standard-table"><tbody><tr><th>id's</th><th>itemscope</th><th>itemref</th><th></th><th>(nombre de itemprop )</th><th>(valor de itemprop)</th></tr><tr><td>id=amanda</td><td>itemscope</td><td>itemref=a,b</td><td></td><td></td><td></td></tr><tr><td>id=a</td><td></td><td></td><td>itemprop</td><td>name</td><td><span>Amanda</span></td></tr><tr><td>id=b</td><td>itemscope</td><td>itemref=c</td><td></td><td>band</td><td></td></tr><tr><td colspan="1" rowspan="2">id=c</td><td></td><td></td><td>itemprop</td><td>Band</td><td><span>Jazz Band</span></td></tr><tr><td></td><td></td><td>itemprop</td><td>Size</td><td><span>12</span></td></tr></tbody></table><h3 id="Resultado">Resultado</h3><p>{{ EmbedLiveSample('Example', '', '', '', 'Web/HTML/Global_attributes/itemref') }}</p><h2 id="EspecificaciónEditEdit">Especificación<a class="only-icon button section-edit new" href="https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant-alternates$edit#Specifications"><span>Edit</span></a><a class="only-icon button section-edit new" href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemid$edit#SpecificationsEdit"><span>Edit</span></a></h2><table class="standard-table" style="height: 105px; width: 490px;"><thead><tr><th scope="col">Especificación</th><th scope="col">Estatus</th></tr></thead><tbody><tr><td style="text-align: left; vertical-align: middle;"><a class="external-icon external" href="https://html.spec.whatwg.org/multipage/microdata.html#items">itemref</a></td><td style="text-align: left; vertical-align: middle; white-space: nowrap;">Nota WG - No se encuentra activamente en desarrollo</td></tr></tbody></table>
