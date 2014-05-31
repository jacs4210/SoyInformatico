# Matemáticas Discretas
Las matemáticas discretas son un área de las matemáticas encargadas del estudio de los conjuntos discretos: finitos o infinitos numerables. En oposición a las matemáticas continuas, que se encargan del estudio de conceptos como la continuidad y el cambio continuo, la matemáticas discretas estudian estructuras cuyos elementos pueden contarse uno por uno separadamente. Sirven para resolver problemas analíticos, incluyendo teoría básica de conjuntos, combinatoria, relaciones y funciones, propiedades básicas de grafos y sus aplicaciones en la ciencia de la computación.

## Tabla de contenido

- [Progresión aritmética](#progresi%C3%B3n-aritmetica)
- [Progresión geométrica](#progresi%C3%B3n-geom%C3%A9trica)
- Principio de inducción matemática (PIM)
- Relaciones recursivas de una semilla
- Relaciones recursivas de dos semillas
- Conjuntos
    - Conjuntos contables o enumerables
    - Conjunto finito
    - Conjunto infinito
    - Conjunto universo
  - Operaciones entre conjuntos
    - Unión
    - Intercepción
    - Diferencia o resta
    - Diferencia simétrica
    - Complemento
    - Producto cartesiano
  - Partes de un conjunto o conjunto potencia
  - Partición de conjuntos
- Conteo
  - Principio de la multiplicación
  - Principio de adición
  - Combinación
  - Combinación con repetición
  - Permutación
  - Permutación con repetición (objetos indistinguibles)
  - Permutación sin repetición
  - Principio de inclusión y exclusión
- Relaciones
  - Propiedades
    - Reflexiva
    - Simetrica
    - Transitiva
  - Clasificación
    - Uno a uno
    - Uno a muchos
    - Muchos a uno
    - Muchos a muchos
  - Relaciones de equivalencia
  - Cerradura
- Funciones
  - Dominio, codominio y rango
  - Función inyectiva
  - Función sobreyectiva
  - Función biyectiva
  - Función compuesta
  - Función inversa
- Grafos
  - Grafo no dirigido
  - Grafo dirigido
  - Terminología de grafos
  - Representación de un grafo en una matriz de adyacencia
  - Representación de un grafo en una lista de adyacencia
  - Arboles
- FAQs
- [Referencias](#referencias)

## Progresión aritmetica

Es una sucesión de números tales que la diferencia de dos términos sucesivos cualesquiera de la secuencia es una constante, cantidad llamada diferencia de la progresión o razón de cambio. Por ejemplo, la sucesión matemática: 3, 5, 7, 9, 11,... es una progresión aritmética de constante o razón de cambio de 2. Así como: 5, 2, -1, -4 es una progresión aritmética de constante "-3".

**Hallar el término n-esimo de una progresión aritmética**

Formula:

![formula enesimo aritmetica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/formula-enesimo-artimetica.png)

>La formula solo es válida para los n>=1 donde "a" es el primer término de la sucesión, "r" la razón de cambio y "n" es una variable cualquiera que se reemplaza por el número de término que se desea encontrar en la sucesión. 

**Hallar la suma de los n-terminos de la sucesión**

Fórmula:

![formula sucesion aritmetica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/formula-suma-sucesion-artimetica.png)

>Donde "n" es una constante que sirve para reemplazarla por la cantidad de términos que se desea sumar. La letra "a" hace referencia al primer término de la sucesión y "Tn" es el término general o n-ésimo de la sucesión.

Ejemplo:

![Ejemplo 1 sobre progresión aritmetica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/ejemplo-1-progresion-aritmetica.png)

Nota: Puede editar este ejemplo con la aplicación [Daum Equation Editor](https://chrome.google.com/webstore/detail/daum-equation-editor/dinfmiceliiomokeofbocegmacmagjhe?hl=en) y debe copiar y pegar el texto plano a continuación:

```plain
Hallar\quad el\quad n-esimo\quad termino\quad y\quad la\quad suma\quad de\quad la\quad siguente\quad secuencia:\\ \\ 1\quad +\quad 3\quad +\quad 5\quad +\quad 7\quad +\quad 9...\quad +\quad (\quad \quad \quad \quad \quad )\quad =\quad (\quad \quad \quad \quad \quad \quad )\\ \\ r\quad =\quad 2\quad \qquad hace\quad referencia\quad a\quad la\quad razón\quad de\quad cambio.\\ a\quad =\quad 1\qquad hace\quad referencia\quad al\quad primer\quad término.\\ \\ { t }_{ n\quad  }\quad =\quad a\quad +\quad (n-1)r\\ \qquad =\quad 1\quad +\quad (n-1)2\\ \qquad =\quad 1\quad +\quad 2n-2\\ { t }_{ n }\quad =\quad 2n-1\\ \\ Ya\quad tenemos\quad el\quad n-esimo\quad termino:\quad 1\quad +\quad 3\quad +\quad 5\quad +\quad 7\quad +\quad 9...\quad +\quad 2n-1\quad =\quad (\quad \quad \quad \quad )\\ \\ Ahora\quad hallamos\quad la\quad suma\quad de\quad los\quad n-terminos:\\ \\ { S }_{ n }\quad \quad =\quad \frac { n\quad ({ a }_{ 1 }\quad +\quad { t }_{ n }) }{ 2 } \\ \qquad \quad =\quad \frac { n\quad (1\quad +\quad 2n-1) }{ 2 } \\ \qquad \quad =\quad \frac { n\quad (2n) }{ 2 } \\ { S }_{ n }\quad \quad =\quad { n }^{ 2 }\\ \\ Por\quad lo\quad tanto\quad la\quad secuencia\quad queda\quad así:\\ \\ 1\quad +\quad 3\quad +\quad 5\quad +\quad 7\quad +\quad 9\quad +\quad ...\quad +\quad (2n-1)\quad =\quad { n }^{ 2 }\\  
```

Computacionalmente y de forma recursiva sería así:

```plain
entero sum;
sum = potencia(n,2);
fin programa;
```

Computacionalmente y de una forma **no tan eficiente** sería un ciclo:

```plain
entero sum = 0;
para (entero i=1; i<=n; i++){
  sum += (2*i-1);
}
fin programa;
```

## Progresión geométrica

Una progresión geométrica es una secuencia en la que el elemento se obtiene multiplicando el elemento anterior por una constante denominada razón o factor de la progresión, ejemplo: 5, 25, 125... la razón de cambio es 5, porque multiplicado por el anterior me da el siguiente término.

**Hallar el término n-esimo**

Formula:

![Formula progresión geométrica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/formula-progresion-geometrica.png)

>Donde "a" es el primer término y "r" la razón de cambio.

Nota: Código fuente de la formula en Daum Equation Editor:

```plain
{ T }_{ n }\quad =\quad a{ r }^{ n-1 }\\ \\ ó\\ \\ \left\{ { T }_{ 1 }\quad =\quad { a }_{ 1 }\\ { T }_{ n }\quad =\quad { T }_{ (n-1) }r \right \quad para\quad los\quad n>=2
```

**Hallar la suma de los n-terminos**

Formula:

![Formula suma progresión geométrica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/formula-suma-termino-progresion-geometrica.png)

Código de la formula en Daum Equation Editor:

```plain
{ S }_{ n }\quad =\quad \frac { a\quad (1\quad -{ \quad r }^{ n }) }{ 1-r } \quad para\quad 0\quad <=\quad r\quad <\quad 1\\ \\ ó\\ \\ { S }_{ n }\quad =\quad \frac { a\quad ({ r }^{ n }\quad -\quad 1) }{ r-1 } \quad para\quad r\quad >\quad 1
```

Ejemplo:

![Ejemplo progresión geométrica](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/ejemplo-1-progresion-geometrica.png)

Código fuente de la formula en Daum Equation Editor:

```plain
Hallar\quad el\quad término\quad n-esimo\quad y\quad la\quad suma\quad de\quad los\quad n-terminos\quad de\quad la\quad siguiente\quad sucesión:\\ \\ 5\quad +\quad 15\quad +\quad 45\quad +\quad ...\quad +\quad (\quad \quad \quad \quad \quad \quad )\quad =\quad (\quad \quad \quad \quad \quad \quad )\\ \\ Solución:\\ \\ Sabemos\quad que\quad r\quad =\quad 3\quad y\quad a\quad =\quad 5\\ \\ Hallemos\quad el\quad término\quad n-esimo:\\ \\ { T }_{ n }\quad \quad =\quad a{ r }^{ n-1 }\\ { T }_{ n }\quad \quad =\quad 5\quad *\quad { 3 }^{ n-1 }\\ \\ Por\quad lo\quad tanto\quad quedaría\quad así:\\ \\ 5\quad +\quad 15\quad +\quad 45\quad +\quad ...\quad +\quad { (3 }^{ n-1 }\quad *\quad 5)\quad =\quad (\quad \quad \quad \quad \quad \quad )\\ \\ Ahora,\quad hallemos\quad la\quad suma\quad de\quad los\quad n-terminos:\\ \\ Como\quad r\quad >\quad 1,\quad entonces:\\ \\ { S }_{ n }\quad =\quad \frac { a\quad ({ r }^{ n }\quad -\quad 1) }{ r-1 } \\ \\ { S }_{ n\quad =\quad  }\frac { 5\quad (\quad { 3 }^{ n }\quad -\quad 1) }{ 3-1 } \\ \\ { S }_{ n\quad =\quad  }\frac { 5\quad *\quad { 3 }^{ n }\quad -\quad 5 }{ 2 } \\ \\ Por\quad lo\quad tanto,\quad la\quad secuencia\quad queda\quad así:\\ \\ 5\quad +\quad 15\quad +\quad 45\quad +\quad ...\quad +\quad { (3 }^{ n-1 }\quad *\quad 5)\quad =\quad \frac { 5\quad *\quad { 3 }^{ n }\quad -\quad 5 }{ 2 } 
```

## Principio de inducción matemática (PIM)

El PIM  se utiliza para validar teoremas o formulas con el objetivo de asegurar que funcionará para cualquier valor en n.

El PIM tiene dos pasos:

** Paso básico **

Es demostrar que para n = 1 es verdad.

** Paso Inductivo **

Vamos a suponer que la formula es valida para k, entonces es verdadera también para k+1

Ejemplo:

![ejemplo del pim](https://raw.githubusercontent.com/victorhtorres/SoyInformatico/master/MatematicasDiscretas/Images/ejemplo-pim.png)

>El PIM es importante utilizarlo en las formulas de nuestro código, asegurando que siempre funcionarán para cualquier valor en n.

## Referencias

http://es.wikipedia.org/wiki/Matem%C3%A1ticas_discretas







