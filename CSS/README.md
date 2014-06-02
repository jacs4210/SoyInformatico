# CSS

CSS significa hoja de estilos en cascada y sirve para darle estilo y formato a la estructura de un proyecto escrito en un lenguaje de marcado, ejemplo: HTML.

## Tabla de contenido

- Propiedades en CSS
 - [Over flow](#propiedad-overflow)
 - [Border radius](#propiedad-border-radius)
 - [Float](#propiedad-float)
 - [Display](#propiedad-display)
 - [Position](#propiedad-position)
 - [Box shadown](#propiedad-boxshadown)
 - [Min y Max](#propiedades-min-o-max)
 - [@Font face](#propiedad-font-face)
- [Pseudo elementos](#pseudo-elementos-en-css)
 - [first-child](#first-child)
 - [last-child](#last-child)
 - [nth-child](#nth-child)
 - [after](#after)
 - [before](#before)
- [Valores de herencia](#valores-de-herencia)
 - [Inherit](#inherit)
 - [Initial](#initial)
 - [Unset](#unset)
- FAQs

## Propiedad Overflow

Permite que se recorte el contenido de una capa, para mostrar únicamente el contenido que quepa, según sus dimensiones.

**Sintaxis**:

```css

#objeto 
{
	overflow: hidden|visible|auto|scroll;
}

```

**Valores**:

visible: Muestra todo el contenido de la capa así no quepa en ella.

hidden: Para ocultar el contenido que sobrepasa el alto y ancho que tiene asignado la capa.

auto: Muestra un scroll en la capa para poder mostrar contenido que sea mayor al tamaño de dicha capa.

scroll: Muestra un scroll en la capa así el contenido no sea mayor al tamaño de dicha capa.

**Gráficamente se vería así**:

![valores overflow](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/CSS/Images/overflow-values.jpg)

Fuente:

http://www.desarrolloweb.com/articulos/atributo-overflow-css.html


## Propiedad border radius

Permite darle estilos redondeados a las esquinas de las cajas. Esta propiedad nace en la versión CSS3.

**Sintaxis**:

```css

#objeto 
{
	border-radius: 1-4 length|% / 1-4 length|%|initial|inherit;
}

```
**Ejemplo 1**:

```css

border-radius:2em;

// is equivalent to:

border-top-left-radius:2em;
border-top-right-radius:2em;
border-bottom-right-radius:2em;
border-bottom-left-radius:2em;

```

**Ejemplo 2**:

```css

border-radius: 2em 1em 4em / 0.5em 3em;

// is equivalent to:

border-top-left-radius: 2em 0.5em;
border-top-right-radius: 1em 3em;
border-bottom-right-radius: 4em 0.5em;
border-bottom-left-radius: 1em 3em;

```

Los valores 0.5 y 3em del ejemplo 2, aproxima el grado de redondeo al eje x de la caja, ejemplo:

`border-top-left-radius: 10em;` produce lo siguiente:

![ejemplo border radius](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/CSS/Images/border-radius-one-values.jpg)

Ahora con dos valores:

`border-top-left-radius: 10em 5em;` produce lo siguiente:

![Ejemplo de border radius con dos valores](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/CSS/Images/border-radius-two-values.jpg)


## Propiedad float

Las propiedades display, float y position se usan de igual importancia en CSS3 y sirve para ajustar las cajas de información del sitio web. Con la propiedad float podemos colocar un objeto a la derecha o a la izquierda.

**Sintaxis*

```css
#objeto 
{
	float:left|right|intial|inherit;
}
```

>Elementos posicionados absolutamente ignora la propiedad float.

## Propiedad display

Display es la propiedad más importante para estructurar los objetos de nuestro sitio web. Cada elemento tiene un valor de display por defecto dependiendo de qué tipo de elemento sea. El valor por defecto para la mayoría de los elementos es usualmente block (de bloque) o inline (en línea). Un elemento que es block es comúnmente llamado elemento block-level. Un elemento inline siempre es llamado elemento inline.

**Sintaxis**

```css
#objeto
{
	display: block|inline|inline-block|none…;
}
```

**Tipos de display**

**Block**: `div` Es el elemento block-level estándar. Un elemento block-level comienza en una nueva línea y se estira hasta la derecha e izquierda tan lejos como pueda. Otros elementos block-level muy comunes son `p` y `form`, y algunos nuevos en HTML5 son `header`, `footer` y `section`.

**Inline**: El `span` es el elemento inline estándar. Un elemento inline puede contener algo de texto dentro de un párrafo `<span> como esto </span>` sin interrumpir el flujo del párrafo. El elemento `<a>` es el elemento inline más común, ya que se usa para links.

**Inline-block**: Permite tener varios bloques de elementos en una sola línea. Útil para la maquetación de la información.

**None**: Otro valor común de display es none. Algunos elementos especializados como script usan este por defecto. Es comúnmente usado en JavaScript para ocultar o mostrar elementos sin eliminarlos ni recrearlos. Esto es diferente de visibility. Usar `display: none` no dejará espacio donde el elemento se encontraba, pero `visibility: hidden;` dejará un espacio vacío.

**Fuente**: 

http://es.learnlayout.com/display.html

**Descripción gráfica del display**:

![Decripción gráfica de la propiedad display](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/CSS/Images/representacion-grafica-display.jpg)
>Imagen sacada del curso de Diseño Web de Mejorando.la

## Propiedad position

La propiedad position ofrece reglas alternativas para el posicionamiento de elementos.

**Sintaxis**

```css
#objeto
{
	position: static|absolute|fixed|relative|initial|inherit;
}
```

**Static**: Es el valor por defecto. Un elemento con `position: static;` no está posicionado en ninguna forma en específico y se ubicará según el flujo normal que tenga el HTML o en otras palabras, no tendra en cuenta los valores top, right, bottom y left que si aparecen con el atributo `position: relative;`.


**Relative**: Se comporta de la misma manera que static a menos que le agregues otras propiedades. La propiedad relative me genera 4 nuevos atributos: top, left, bottom, right.. Al darle valores a los nuevos atributos esto causará que la posición actual del objeto se reajuste.

**Fixed**: Un elemento fixed (fijo) se posiciona a la ventana del navegador de manera relativa, lo que significa que se mantendrá en el mismo lugar incluso después de hacer scroll en la página. Al igual que con relative, las propiedades top, right, bottom, y left también son usadas.

**Absolute**: Se comporta como fixed pero es relativo a su ancestro posicionado más cercano en lugar de ser relativo a la ventana del navegador, significa que, toma la posición (0,0) de la posición relativa más cercana. Si un elemento con `position: absolute;` no tiene ancestros posicionados, usará el elemento body del documento, y se seguirá moviendo al hacer scroll en la página. 

>Recuerda, un elemento "posicionado" es aquel cuyo valor es cualquiera excepto static.

**Fuente**:

http://es.learnlayout.com/position.html

**Ejemplos de position**:

http://www.w3schools.com/cssref/playit.asp?filename=playcss_position


## Propiedad box-shadown

Sirve para darle sombra a los elementos en CSS3.

**Sintaxis**

```css
#objeto
{
box-shadow: none|h-shadow v-shadow blur spread color |inset|initial|inherit;
}
```

Existe varias formas de representar sombras en los elementos por CSS3, por ejemplo:

**Ejemplo 1**:

```css
#objeto
{
	box-shadow: rgba(0,0,0,0.5) 5px 5px 20px
}
```

>Los primeros tres ceros del ejemplo hacen referencia al color en hexadecimal. El 0.5 hace referencia al % de transparencia (esto se debe a que el color RGBA añade un canal de transparencia). Los valores 5px 5px hacen referencia a los ejex (X,Y) y el valor 20px hace referencia al % de difuminación.


**Ejemplo 2**:

```css
#objeto
{
box-shadow: 10px 10px 5px #888888;
}
```

>Los dos valores de 10px del ejemplo 2 hace referencia a la posición de la sombra (se puede dar valores negativos para representar el otro lado del elemento a sombrear), el valor 5px hace referencia la longitud de radio de desenfoque de la sombra y el valor hexadecimal #888888 hace referencia al color de la sombra.


**Ejemplo 3**: Varias sombras.

```css
#bojeto
{
	box-shadow: 0 0 20px black, 0 10px 20px yellow;
}
```

>Puedo colocar varias sombras en un elemento con solo separar los valores por comas.

## Propiedades min o max

Es una propiedad adicional que se les puede dar a las otras propiedades como `width` y `height` y sirven para tener un límite de minimo o máximo de valor, dependiendo de la propiedad que uses.

**Sintaxis**

```css
#objeto
{
	min|max-height|width: valor;
}
```

## Propiedad @font-face

Sirve para especificar un tipo de fuente y la url donde se encuentra alojado el archivo. Ideal para utilizarlo con fuentes externas como las que ofrece el servicio [Google Fonts](https://www.google.com/fonts).

**Sintaxis**

```css
@font-face
{
font-family: 'NombreDeLaFuente';
src: url(sansation_light.woff);
}
```

## Pseudo elementos en CSS

Se utilizan para añadir efectos especiales a algunos selectores y/o etiquetas.

**Sintaxis**

```css
selector:pseudo-element 
{
	property:value;
}
```

También se puede poner selectores de clases e id's:

```css
selector.class:pseudo-element 
{
	property:value;
}
```

**Estos son algunos de los pseudo-elementos más utilizados**:


### first-child

La función first-child va a busca la primera etiqueta `<p>` que este dentro del objeto de nuestro interés y le agrega el estilo que definamos.

**Ejemplo**:

```css
footer p: first-child
{
	atributo: valor;
}
```

### last-child

Hará lo contrario a first-child, buscará el último `<p>` definido en el objeto para agregar algún estilo.

**Ejemplo**:

```css
footer p: last-child
{
	atributo: valor;
}
```

### nth-child

Atributo que sirve para darle estilo a una etiqueta `<p>` especifica de varias `<p>` que se encuentren en un contendedor. En otras palabras, si la caja de elementos tiene más de dos `<p>` se usa este atributo.

>Si no quieres complicarte con este atributo, simplemente usa un class para identificar la etiqueta la cual se desea darle estilo.

**Ejemplo**:

```css
p:nth-child(3)
{
	background:#ff0000;
}
```

### nth-child(odd)

Toma todos los elementos `<p>` pares de una caja.

**Ejemplo**:

```css
p:nth-child(odd)
{
	background:#ff0000;
}
```

### nth-child(even)

Toma todos los elementos `<p>` impares de una caja.

**Ejemplo**:

```css
p:nth-child(even)
{
	background:#ff0000;
}
```

### after

Inserta contenido después de un bloque `<p>`.

**Ejemplo 1**:

```css
p:after
{ 
	content:"- Remember this";
}
```

**Ejemplo 2**:

```css
footer p:last-child:after
{
	content: " -";
}
```

>En el ejemplo 2 vemos cómo se puede combinar dos pseudo-elementos. Tomará la última etiqueta `<p>` y le agregará después el " -".

### before

Inserta contenido antes de una etiqueta `<p>`

**Ejemplo 1**:

```css
p:before
{
	content:"Read this -";
}
```

**Ejemplo 2**:

```css
p:first-child:before
{
	content:"Read this -";
}
```

## Valores de herencia

Una de las características principales de CSS es la herencia de los estilos definidos para los elementos. Cuando se establece el valor de una propiedad CSS en un elemento, sus elementos descendientes heredan de forma automática el valor de esa propiedad.

Fuente:

http://librosweb.es/css/capitulo_2/herencia.html

A continuación, veremos algunos valores que permiten hacer herencia con base al valor que tenga sus elementos padres o valores predefinidos por los navegadores:

### inherit

Este es un valor que especifica que a la propiedad que se la apliquemos  debe de heredar los valores de su elemento padre. Podemos decir que la palabra Inherit significa  **Usa el valor de mi padre**, si el elemento padre no tiene definido dicho valor, el navegador seguirá el DOM hasta que encuentre un elemento superior que lo contenga, y en última instancia de no tenerlo ningún elemento superior, se aplicara el valor por defecto.

**Ejemplo**: Si tenemos el siguiente código HTML

```css
<div id="padre">
      <p>Hola soy el parrafo hijo del div con id padre</p>
</div>
```
y aplicamos el siguiente CSS:

```css
#padre {
     margin: 10px;
     border: 1px solid #000;
     color: blue;
}
#padre p{
     padding: inherit;
     border: inherit;
     color: inherit;
}
```

El elemento párrafo obtendrá el estilo del border y del color de su padre inmediato, que el `#padre` y el padding como no está definido en el padre inmediato, lo tomara de un elemento superior de acuerdo al árbol DOM.

### initial

Este valor pertenece a la especificación CSS3 y cuando aplicamos a una propiedad el valor initial estamos dando el valor inicial y predefinido por el navegador en cuestión. 

**Ejemplo**:

```css
body{
    font-size: 0.5em;
}
p{
    font-size: initial;
}
```

En este caso aunque tengamos un valor de tipografía definido para el cuerpo del documento, los párrafos tendrán un tamaño de fuente predefinida y por defecto, que general y normalmente es 1em, que por defecto es 16px.

>Los navegadores no tienen el mismo valor por defecto para ciertas propiedades.

### unset

Este valor unset es una combinación entre inherit e initial, cuando utilizamos este valor en una propiedad tratara de heredar el valor de su elemento padre si este está disponible, de no ser así este valor colocará el valor de la propiedad en su valor inicial, como si usáramos inherit e initial juntamente.

Fuente:

http://www.tutosytips.com/valores-de-herencia-en-css3-con-inherit-initial-unset/#sthash.yVJmDxDG.dpuf

