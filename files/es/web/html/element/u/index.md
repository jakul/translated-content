---
title: u
slug: Web/HTML/Element/u
tags:
  - HTML
  - HTML:Elemento
  - Todas_las_Categorías
translation_of: Web/HTML/Element/u
original_slug: Web/HTML/Elemento/u
---
### Definición

Muestra el texto subrayado.

<dl><dd><strong>Sus etiquetas son</strong>: &#x3C;u> y &#x3C;/u> (Ambas obligatorias)</dd></dl>

<dl><dd><strong>Crea una caja</strong>: <a href="es/HTML/Elemento/Tipos_de_elementos#en_linea">en linea</a>.</dd></dl>

<dl><dd><strong>Está definido como</strong><dl><dd><a href="es/HTML/Elemento/Tipos_de_elementos#de_estilo_de_fuente">de estilo de fuente</a>.</dd><dd><a href="es/HTML/Elemento/Tipos_de_elementos#Desaprobado">Desaprobado</a></dd></dl></dd></dl>

<dl><dd><strong>Puede contener</strong>: cero o más elementos <a href="es/HTML/Elemento/Tipos_de_elementos#en_linea">en linea</a></dd></dl>

##### Atributos Genéricos

- title (título del elemento)
- style (información de estilo en línea)

<dl><dd><strong>Identificadores</strong>: id, class (identificadores a nivel de documento)</dd><dd><strong>Idioma</strong>: lang (información sobre el idioma), dir (dirección del texto)</dd><dd><strong>Eventos</strong>: onclick, ondblclick, onmousedown, onmouseup, onmouseover, onmousemove, onmouseout, onkeypress, onkeydown, onkeyup.</dd></dl>

##### Atributos Específicos - No tiene

##### Atributos Transicionales - No tiene

### Ejemplos

Uso de u:

```html
  <p>
       Texto normal y... <u>Texto subrayado</u>
  </p>
```

Uso de CSS:

```html
  <p>
       Texto normal y... <span style='text-decoration: underline'>Texto subrayado</span>
  </p>
```

### Comentarios

Para obtener el mismo resultado puede usarse La propiedad CSS text-decoration: underline;

Si por algún motivo necesita usar elementos desaprobados como u, recuerde que debe declarar un DOCTYPE transicional.

> **Advertencia:** DESAPROBADO

de momento no funciona
