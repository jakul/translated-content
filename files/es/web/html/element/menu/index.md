---
title: menu
slug: Web/HTML/Element/menu
tags:
  - HTML
  - HTML:Elemento
  - Todas_las_Categorías
translation_of: Web/HTML/Element/menu
original_slug: Web/HTML/Elemento/menu
---
### Definición

El elemento `menu` (directorio) es un elemento desaprobado. En su origen fue pensado para crear menús, en la actualidad es inutil.

<dl><dd><strong>Sus etiquetas son</strong>: &#x3C;menu> y &#x3C;/menu> (ambas obligatorias).</dd></dl>

<dl><dd><strong>Crea una caja</strong>: <a href="es/HTML/Elemento/Tipos_de_elementos#en_bloque">en bloque</a>.</dd></dl>

<dl><dd><strong>Está definido como</strong>: <a href="es/HTML/Elemento/Tipos_de_elementos#desaprobado">Elemento DESAPROBADO</a>.</dd></dl>

<dl><dd><strong>Puede contener</strong>: uno o más elementos <a href="es/HTML/Elemento/li">li</a></dd><dd><strong>NO puede contener</strong>: <a href="es/HTML/Elemento/Tipos_de_elementos#en_bloque">Elementos en bloque</a></dd></dl>

#### Atributos

<table class="standard-table">
  <tbody>
    <tr>
      <th>Atributo</th>
      <th colspan="2">valor</th>
      <th>descripción</th>
    </tr>
    <tr>
      <th colspan="4">Genericos</th>
    </tr>
    <tr>
      <td><code style="color: green">title</code></td>
      <td>texto</td>
      <td>implícito</td>
      <td>título consultivo del elemento.</td>
    </tr>
    <tr>
      <td><code style="color: green">style</code></td>
      <td>reglas de estilo</td>
      <td>implícito</td>
      <td>información de estilo en línea.</td>
    </tr>
    <tr>
      <td><code style="color: green">id</code></td>
      <td>ID</td>
      <td>implícito</td>
      <td>identificador único a nivel de documento.</td>
    </tr>
    <tr>
      <td><code style="color: green">class</code></td>
      <td>CDATA</td>
      <td>implícito</td>
      <td>
        identificador a nivel de documento, lista de clases separadas por
        espacios.
      </td>
    </tr>
    <tr>
      <td><code style="color: green">dir</code></td>
      <td>(ltr|rtl)</td>
      <td>implícito</td>
      <td>dirección del texto débil/neutral</td>
    </tr>
    <tr>
      <td><code style="color: green">lang</code></td>
      <td>código de idioma</td>
      <td>implícito</td>
      <td>información sobre el idioma</td>
    </tr>
    <tr>
      <td colspan="4">
        <strong>Eventos</strong>:
        <code style="color: green"
          >onclick, ondblclick, onmousedown, onmouseup, onmouseover,
          onmousemove, onmouseout, onkeypress, onkeydown, onkeyup.</code
        >
      </td>
    </tr>
    <tr>
      <th colspan="4">Específicos</th>
    </tr>
    <tr>
      <td colspan="4">No tiene</td>
    </tr>
    <tr>
      <th colspan="4">de transición</th>
    </tr>
    <tr>
      <td><code style="color: green">compact</code></td>
      <td>compact</td>
      <td>implícito</td>
      <td>espacio entre objetos reducido</td>
    </tr>
    <tr>
      <th>Atributo</th>
      <th colspan="2">valor</th>
      <th>descripción</th>
    </tr>
  </tbody>
</table>

### Ejemplos

El siguiente código:

```html
 <menu>
  <li>primer elemento </li>
  <li>segundo elemento </li>
  <li>tercer elemento </li>
 </menu>
```

Se visualiza así:

- primer elemento
- segundo elemento
- tercer elemento

### Comentarios

En el navegador se visualiza (o deberia) igual que una lista desordenada ([ul](es/HTML/Elemento/ul))
