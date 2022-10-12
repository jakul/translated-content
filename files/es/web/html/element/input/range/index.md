---
title: <input type="range">
slug: Web/HTML/Element/input/range
tags:
  - Elementos
  - Formulários HTML
  - HTML etiqueta input
  - Input
  - Range
  - Rango
  - Referencia
  - Web
  - deslizador
  - formulários
  - slider
translation_of: Web/HTML/Element/input/range
original_slug: Web/HTML/Elemento/input/range
---
{{HTMLRef}}

El elemento {{HTMLElement("input")}} del tipo **`"range"`** permite que el usuario especifique un valor numérico comprendido entre un valor mínimo y máximo. El valor exacto, sin embargo, no se considera importante. Se repesenta típicamente como un "tirador" o un control deslizante en lugar de un campo de texto como otros tipos de {{HTMLElement("input")}}. Como este tipo de widget es bastante inmpreciso, no debe utilizarse normalmente a menos que el valor exacto del control no sea importante.

```html
<input type="range">
```

{{EmbedLiveSample("summary_sample1", 600, 40)}}

Si el navegador del usuario no soporta el tipo `"range"`, será tratado como un input de tipo [`"text"`](/en-US/docs/Web/HTML/Element/input/text).

<table class="properties">
  <tbody>
    <tr>
      <td>
        <strong><a href="#value">Value</a></strong>
      </td>
      <td>
        Un {{domxref("DOMString")}} que contiene la cadena que
        representa el valor numérico seleccionado; use
        {{domxref("HTMLInputElement.valueAsNumber", "valueAsNumber")}}
        to get the value as a {{jsxref("Number")}}.
      </td>
    </tr>
    <tr>
      <td><strong>Eventos</strong></td>
      <td>{{event("change")}} e {{event("input")}}</td>
    </tr>
    <tr>
      <td><strong>Atributos comunes soportados</strong></td>
      <td>
        {{htmlattrxref("autocomplete", "input")}},
        {{htmlattrxref("list", "input")}},
        {{htmlattrxref("max", "input")}},
        {{htmlattrxref("min", "input")}} y
        {{htmlattrxref("step", "input")}}
      </td>
    </tr>
    <tr>
      <td><strong>Atributos IDL</strong></td>
      <td>
        <code>list</code>, <code>value</code> y <code>valueAsNumber</code>
      </td>
    </tr>
    <tr>
      <td><strong>Metodos</strong></td>
      <td>
        {{domxref("HTMLInputElement.stepDown", "stepDown()")}}
        y {{domxref("HTMLInputElement.stepUp", "stepUp()")}}
      </td>
    </tr>
  </tbody>
</table>

## Value

El atributo {{htmlattrxref("value", "input")}} contiene un {{domxref("DOMString")}} que es la representación de tipo cadena del número seleccionado. El valor nunca es una cadena vacía (`""`). El valor por defecto es el punto intermedio entre los valores mínimo y máximo especificados, a menos que el valor máximo sea menor que el valor mínimo, en cuyo caso el valor por defecto será el valor del atributo `min`. El algoritmo de determina el valor por defecto es:

```js
defaultValue = (rangeElem.max < rangeElem.min) ? rangeElem.min
               : rangeElem.min + (rangeElem.max - rangeElem.min)/2;
```

Si se intenta establecer un valor inferior al mínimo definido, el valor será igual al mínimo. De manera similar, un intento de establecer un valor superior al máximo da como resultado el valor máximo.

## Usando inputs range

El input de tipo `"number"` permite al usuario introducir un número y, opcionalmente, forzarle a que dicho valor se encuentre entre un mínimo y un máximo, pero le obliga a introducir un valor específico. El input de tipo `"range"` pide al usuario que indique el valor en un rango numérico sin que tenga que preocuparse qué valor numérico específico está seleccionado.

Los ejemplos títpicos de situaciones en las que se pueden usar inputs de tipo rango suelen ser:

- Controles de audio (volumen o balance) o controles de filtro.
- Configuración de color, como canales, transparencia, brillo, etc.
- Controles de configuración de juegos, como dificultad, distancia de visibilidad, tamaño del nunodGame configuration controls such as difficulty, visibility distance, world size, etc.
- Longitud de contraseñas para un gestor de contraseñas generadas.

Como regla general, si el usuario está más interesado en la distancia entre un mínimo y un máximo más que en el propio valor en sí mismo, el input de tipo rango es el candidato perfecto. Por ejemplo, en el caso del control del volumen de un equipo estéreo, el usuario normalmente piensa "pon el volumen a la midad" en lugar de "pon el volumen al 0,5".

### Especificar los valores mínimo y máximo

Por defecto, el valor mínimo es 0 y el máximo es 100. Si es necesario modificar dichos valores, podemos usar los atributos {{htmlattrxref("min", "input")}} y/o {{htmlattrxref("max", "input")}}. Podemos usar cualquier valor de coma flotante.

Por ejemplo, para usar un rango entre -10 y 10, usaremos:

```html
<input type="range" min="-10" max="10">
```

{{EmbedLiveSample("Specifying_the_minimum_and_maximum", 600, 40)}}

### Definir el tamaño de los saltos

Por defecto, cada salto tiene valor 1, es decir el valor será siempre un número entero. Podemos cambiarlo mediante el atributo {{htmlattrxref("step")}}. Si necesitas, por ejemplo, un valor entre 5 y 10 con una precisión de dos decimales, debes indicar que el valor de `step` es 0.01:

```html
<input type="range" min="5" max="10" step="0.01">
```

{{EmbedLiveSample("Granularity_sample1", 600, 40)}}

Si quieres aceptar cualquier valor independientemente de la cantidad de decimales, puede especificar un valor de `"any"` al atrtibuto {{htmlattrxref("step", "input")}}:

```html
<input type="range" min="0" max="3.14" step="any">
```

{{EmbedLiveSample("Granularity_sample2", 600, 40)}}

En el ejemplo, permitimos al usuario seleccionar cualquier valor entre 0 y π sin restricciones en la parte decimal del número seleccionado.

### Añadir marcas y etiquetas

La especificación HTML permite a los navegadores cierta flexibilidad sobre cómo presentar el control range. En ningún sitio es más notoria dicha flexibilidad como a la hora de representar las marcas y las etiquetas de un rango. La especificación describe cómo añadir puntos personalizados al control range usando el atributo {{htmlattrxref("list", "input")}} y el elemento {{HTMLElement("datalist")}}, pero no hay requisitos o recomendaciones de estandarizar las marcas a lo largo del control.

#### Mockups del control range

Como los navegadores tienen esta flexibilidad, y hasta la fecha ninguno admite todas las funciones que HTML define para los controles range, a continuación mostramos algunas maquetas que permiten conocer lo que puede visualizarse en macOS en un navegador que las admita.

##### El control rango sin adornos

Cuando no especificas un atributo {{htmlattrxref("list", "input")}} al input range, un navegador que lo soporte mostrará lo siguie.

<table class="fullwidth standard-table">
  <tbody>
    <tr>
      <th>HTML</th>
      <th>Captura de pantalla</th>
    </tr>
    <tr>
      <td><pre class="brush: html">&#x3C;input type="range"></pre></td>
      <td>
        <img
          alt="Screenshot of a plain slider control on macOS"
          src="https://mdn.mozillademos.org/files/14989/macslider-plain.png"
          style="height: 28px; width: 184px"
        />
      </td>
    </tr>
  </tbody>
</table>

##### Un control rango con marcas

El siguiente rango utiliza el atributo `list` (al cual le especificamos el ID del elemento {{HTMLElement("datalist")}}) para definir la serie de marcas del rango. Hay once marcas, cada una de ellas mide un 10%, representadas por el {{htmlattrxref("value", "option")}} de cada elemento {{HTMLElement("option")}}.

<table class="fullwidth standard-table">
  <tbody>
    <tr>
      <th>HTML</th>
      <th>Captura de pantalla</th>
    </tr>
    <tr>
      <td>
        <pre class="brush: html">
&#x3C;input type="range" list="tickmarks">

&#x3C;datalist id="tickmarks">
&#x3C;option value="0">
&#x3C;option value="10">
&#x3C;option value="20">
&#x3C;option value="30">
&#x3C;option value="40">
&#x3C;option value="50">
&#x3C;option value="60">
&#x3C;option value="70">
&#x3C;option value="80">
&#x3C;option value="90">
&#x3C;option value="100">
&#x3C;/datalist>

</pre
        >
      </td>
      <td>
        <img
          alt="Screenshot of a plain slider control on macOS"
          src="https://mdn.mozillademos.org/files/14991/macslider-ticks.png"
          style="height: 28px; width: 184px"
        />
      </td>
    </tr>
  </tbody>
</table>

##### Un control rango con marcas y etiquetas

Puedes añadir etiquetas a tu control range usando el atributo {{htmlattrxref("label", "option")}} al elemento {{HTMLElement("option")}} correspondiente a cada marca que desees etiquetar.

<table class="fullwidth standard-table">
  <tbody>
    <tr>
      <th>HTML</th>
      <th>Captura de pantalla</th>
    </tr>
    <tr>
      <td>
        <pre class="brush: html">
&#x3C;input type="range" list="tickmarks">

&#x3C;datalist id="tickmarks">
&#x3C;option value="0" label="0%">
&#x3C;option value="10">
&#x3C;option value="20">
&#x3C;option value="30">
&#x3C;option value="40">
&#x3C;option value="50" label="50%">
&#x3C;option value="60">
&#x3C;option value="70">
&#x3C;option value="80">
&#x3C;option value="90">
&#x3C;option value="100" label="100%">
&#x3C;/datalist>

</pre
        >
      </td>
      <td>
        <img
          alt="Screenshot of a plain slider control on macOS"
          src="https://mdn.mozillademos.org/files/14993/macslider-labels.png"
          style="height: 44px; width: 184px"
        />
      </td>
    </tr>
  </tbody>
</table>

> **Nota:** Actualmente, ningún navegador soporta todas estas características. Firefox no soporta ni marcas ni etiquetas, mientras que Chrome soporta las marcas pero no las etiquetas.

### Cambiar la orientación

<div class="hidden"><p>Por defecto, si un navegador renderiza un input range, lo mostrará como un "slider" (deslizador) que se desliza hacia la izquierda y hacia la derecha. By default, if a browser renders a range input as a slider, it will render it so that the knob slides left and right. Sin embargo puedes cambiar esto fácilmente para que se deslice hacia arriba y hacia abajo simplemente usando CSS</p><div class="note"><p><strong>Nota</strong>: Esto aún no está implementado por los principales navegadores. This is not actually implemented yet by any of the major browsers. See Firefox {{bug(981916)}}, <a href="https://bugs.chromium.org/p/chromium/issues/detail?id=341071">Chrome bug 341071</a>.</p></div><p>Si tenemos el siguiente control range:</p><div id="Orientation_sample1"><pre class="brush: html">&#x3C;input type="range" id="volume" min="0" max="11" value="7" step="1"></pre></div><p>{{EmbedLiveSample("Orientation_sample1", 200, 200, "https://mdn.mozillademos.org/files/14983/Orientation_sample1.png")}}</p><p>Dicho control se muestra en horizontal (al menos en los principales navegadores, o otros puede variar). Presentarlo en vertical es tan simple como añadir CSS para cambiar las dimensiones del control, de la siguiente manera:</p><div id="Orientation_sample2"><h4 id="CSS">CSS</h4><pre class="brush: css">#volume {
  height: 150px;
  width: 50px;
}</pre><h4 id="HTML">HTML</h4><pre class="brush: html">&#x3C;input type="range" id="volume" min="0" max="11" value="7" step="1"></pre><h4 id="Result">Result</h4><p>{{EmbedLiveSample("Orientation_sample2", 200, 200, "https://mdn.mozillademos.org/files/14985/Orientation_sample2.png")}}</p><p><strong>En la actualidad, ninguno de los navegadores principales soporta la creación de inputs range usando este CSS, incluso a perar de que la especificación recomienda que lo hagan.</strong></p></div></div>

La especificación HTML recomienda que los navegadores cambien la orientación del range si el ancho especificado es menor que el alto. Desafortunadamente, ninguno de los principales navegadores soportar controles range verticales directamente. Para conseguir un range vertical, la forma más fácil es usar CSS, aplicando {{cssxref("transform")}} para rotar el elemento y mostrarlo en vertical. Veamos cómo.

#### HTML

El HTML necesita que el elemento {{HTMLElement("input")}} esté dentro de un elemento {{HTMLElement("div")}} :

```html
<div class="slider-wrapper">
  <input type="range" min="0" max="11" value="7" step="1">
</div>
```

#### CSS

Ahora necesitamos un poco de CSS. Primero escribimos el CSS del div contenedor; especificamos el modo de display y el tamaño que queremos que tenga, reservando un área en la página para el "slider" que vamos a rotar.

```css
.slider-wrapper {
  display: inline-block;
  width: 20px;
  height: 150px;
  padding: 0;
}
```

Después ponemos la información para el elemento `<input>`:

```css
.slider-wrapper input {
  width: 150px;
  height: 20px;
  margin: 0;
  transform-origin: 75px 75px;
  transform: rotate(-90deg);
}
```

El tamaño del range es 150 pixeles de ancho por 20 pixeles de alto. Ponemos los márgenes a 0 y con {{cssxref("transform-origin")}} cambiamos centro que usaremos para rotar el range. Como el input mide 150 pixeles de ancho y largo, girará en una cuadrado de 150 pixeles de lado. Colocamos el centro de giro a 75px horizontal y verticalmente y, finalmente, rotamos 90º en sentido contrario a las agujas del reloj. El resultado final es un input range que ha girado y cuyo valor máximo está en la parte superior y el valor mínimo en la parte inferior.

#### Result

{{EmbedLiveSample("Orientation_sample3", 200, 200, "https://mdn.mozillademos.org/files/14987/Orientation_sample3.png")}}

## Validación

<div class="g-unit" id="gt-res-c"><div id="gt-res-p"><div id="gt-res-data"><div id="gt-res-wrap"><div id="gt-res-content"><div class="trans-verified-button-small" dir="ltr" id="gt-res-dir-ctr"><div id="tts_button"></div><span id="result_box" lang="es"><span>No hay un patrón de validación</span></span><span lang="es"><span> disponible;</span> <span>sin embargo, se realizan las siguientes formas de validación automática:</span></span></div></div></div></div></div></div>

- Si el {{htmlattrxref("value", "input")}} está configurado con un valor que no se puede convertir en un número de coma flotante válido, la validación falla porque recibe una entrada incorrecta.
- El valor no puede ser menor que el valor de {{htmlattrxref("min", "input")}}. Por defecto es 0.
- El valor no puede ser mayor que el {{htmlattrxref("max", "input")}}. Por defecto es 100.
- El valor será un múltiplo del valor de {{htmlattrxref("step", "input")}}. Por defecto es 1.

## Ejemplos

Además de los ejemplos anteriores, encontrarás más ejemplos en los siguientes artículos:

- [Controlling multiple parameters with ConstantSourceNode](/es/docs/Web/API/Web_Audio_API/Controlling_multiple_parameters_with_ConstantSourceNode)

## Especificaciones

| Especificación                                                                                                                   | Estatus                          | Comentario         |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------ |
| {{SpecName('HTML WHATWG', 'forms.html#range-state-(type=range)', '&lt;input type="range"&gt;')}} | {{Spec2('HTML WHATWG')}} | Definición inicial |
| {{SpecName('HTML5.1', 'sec-forms.html#range-state-typerange', '&lt;input type="range"&gt;')}}     | {{Spec2('HTML5.1')}}     | Definición inicial |

## Compatibilidad en navegadores

{{Compat("html.elements.input.input-range")}}

## Ver también

- [HTML Forms](/es/docs/Learn/HTML/Forms)
- {{HTMLElement("input")}} and the {{domxref("HTMLInputElement")}} interface it's based upon
- [`<input type="number">`](/en-US/docs/Web/HTML/Element/input/number)
