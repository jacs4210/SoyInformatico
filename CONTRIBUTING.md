# Colabora con el repositorio

La mejor formar de asegurar nuestro conocimiento es documentando todo lo que aprendemos. Es una buena practica que a muchos se les dificulta, pero nosotros ya hicimos lo más dificil, que es dar el primer paso, ahora solo requerimos de tu ayuda para complementarlo y/o mejorarlo.

## Tabla de contenido

- [Ventajas](#ventajas).
- [FAQs](#faqs).
	- [¿Como empiezo a contribuir?](#como-empiezo-a-contribuir).
	- [Me da mucha pereza documentar ¿Que me recomiendan?](#me-da-mucha-pereza-documentar-que-me-recomiendan).
	- [¿El proyecto tiene sitio web?](#el-proyecto-tiene-sitio-web).
	- [¿Que debo tener en cuenta a la hora de contribuir con una categoría?](#que-debo-tener-en-cuenta-a-la-hora-de-contribuir-con-una-categor%C3%ADa).
	- [No existe la categoría que deseo documentar ¿Que hago?](#no-existe-la-categor%C3%ADa-que-deseo-documentar-que-hago).
	- [¿Como le doy formato o estilo a los archivos README.md?](#como-le-doy-formato-o-estilo-a-los-archivos-readmemd).
		- [Insertar HN](#insertar-hn).
		- [Cursivas](#cursivas).
		- [Negrilla](#negrilla).
		- [Viñetas para tablas de contenido](#vi%C3%B1etas).
		- [insertar imágenes](#insertar-im%C3%A1genes).
		- [Insertar enlaces](#insertar-enlaces).
		- [Hacer anclaje](#hacer-anclaje).
		- [Insertar una línea de código](#insertar-una-l%C3%ADnea-de-c%C3%B3digo).
		- [Insertar un bloque de código](#insertar-un-bloque-de-c%C3%B3digo).
		- [Resaltar el código](#resaltar-el-c%C3%B3digo).
		- [Insertar tablas](#insertar-tablas).
		- [Otras referencias sobre Markdown](#Otras-referencias-sobre-Markdown).

## Ventajas

- Tener tus propios apuntes y de otros para preservar tu conocimiento por siempre, ya sea en la nube o localmente.
- Depender cada vez menos de la información de sitios de terceros. Recuerda que en GitHub puedes hacer clon de este repositorio en tu cuenta y hasta en tu Pc, lo que aseguras que la información nunca se perdera.
- Poder recordar algo de tu carrera de manera más eficiente cuando lo necesites.
- Documentando te ayuda a practicar lo aprendido, porque te obliga a la investigación y la redacción, dos habilidades que necesitas como profesional.
- Fomenta la retroalimentación por el trabajo colectivo que permite la plataforma GitHub.

## FAQs

### ¿Como empiezo a contribuir?

Utiliza las opciones de GitHub como **Pull Request** o un **Fork** para colaborar con el repositorio. El **Fork** te permite hacer un clon de este repositorio en tu cuenta de GitHub. Teniendo un clon podrás hacer todas las modificaciones que ayuden a mejorar el repositorio. Luego, con la opción **Pull Request** envía las sugerencias de cambio al repositorio original y si son aceptadas por el **master**, se fucionan los cambios y el repositorio del proyecto queda actualizado.

### Me da mucha pereza documentar. ¿Que me recomiendan?

Empieza documentando lo que más te guste o lo más reciente que hayas aprendido de la carrera de Ingeniería Informática. No es necesario que realices todo un manual porque seguramente te cansarás antes de terminar y sentiras que el tiempo no te alcanza para otras actividades de interés, pero si das el primer paso documentando los temas que te gusten, probablemente el resto de la comunidad ayude a terminarlo a su tiempo. Recuerda que es un beneficio colectivo a gran escala.

### ¿El proyecto tiene sitio web?

Se esta creando un sitio web por ahora con el único objetivo de dar a conocer lo que estamos haciendo aquí en GitHub para que estudiantes, profesionales y entusiastas de la Informática se unan. El enlace del sitio web es http://wwww.soyinformatico.org

### ¿Que debo tener en cuenta a la hora de contribuir con una categoría?

La documentación está por carpetas, lo que hace referencia a la categoría de temas. Cada carpeta tiene un archivo `README.md` y una carpeta `Images`. En el archivo `README.md irá toda la documentación compartida acerca de la categoría en cuestión y tiene una estructura definida, la cual, es la siguiente:

- Título de la categoría y definición.
- Tabla de contenido.
  - Tema 1.
  .
  .
  .
  - Tema N.
  - FAQs
    - Pregunta frecuente 1.
      .
      .
      - Pregunta frecuente N.
   - Referencias: los enlaces externos que lleven a la fuente de la información [si aplica].

>Cada item de la tabla de contenido debe tener enlace de anclaje al tema en cuestión.

La carpeta `Images` servirá para guardar las imagenes que necesites insertar en la documentación.

### No existe la categoría que deseo documentar ¿Que hago?

De ser así, te invitamos a dar el primer paso creandola y arrancando, que entre todos lo terminamos ;) Ya sabes que, haciendo **Fork** del repositorio podrás crear las categorías o temas que desees.

### ¿Como le doy formato o estilo a los archivos README.md?

Aquí te dejamos algunos tips, pero recuerda que también puedes ver el código fuente de los README.md ya existentes del repositorio como guía:

Los archivos README.md tienen formato de lenguaje de marcado `markdown` que es mucho más sencillo que el lenguaje `HTML`. Veamos algunos ejemplo:

#### Insertar HN

```plain
# Esto es un H1
## Esto es un H2
### Esto es un H3
#### Esto es un H4

```

#### Cursivas

`*Esto es cursiva*`

#### Negrilla

`**Esto es negrilla**`

#### Viñetas

```plain

- Esto es viñeta 1.
  - Viñeta 1.1 con sangria.
  - Viñeta N.
  
```

#### Insertar imágenes

`![texto cualquiera por si no carga la imagen](url completa de la imagen)`

#### Insertar enlaces

`[texto a mostrar](url completa)`

#### Hacer anclaje

Usar los títulos con la almohadilla `#` y para anclar el título a una tabla de contenido, ponemos lo siguiente:

`[texto a mostrar](#mi-titulo-a-anclar)`

#### Insertar una línea de código

Encerrar la linea de código entre la tilde al revés ` Código en ASCII: alt96

Ejemplo:

<pre><code>`tu linea de codigo`</code></pre>

#### Insertar un bloque de código

Encerrar el bloque de código entre tres tildes al revés ``` Código en ASCII: alt96

Ejemplo:

<pre>
		```
		
		//bloque de codigo...
		
		```
</pre>


#### Resaltar el código

Encerramos el bloque de código con las tres tildes al revés ``` y le ponemos al lado el lenguaje que se está usando, ejemplo:

<pre>
		```java
		
		//bloque de codigo...
		
		```
</pre>

#### Insertar tablas

```plain

| TITULO1| TITULO2|

| ----- | ---- |

| CONTENIDO COLUMNA 1 | CONTENIDO COLUMNA 2 |


```

#### Otras referencias sobre Markdown:

http://www.genbeta.com/guia-de-inicio/que-es-markdown-para-que-sirve-y-como-usarlo

https://help.github.com/articles/markdown-basics

https://guides.github.com/features/mastering-markdown/
