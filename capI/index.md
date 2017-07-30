---
title       : Probabilidad Elemental    
subtitle    : Elementos de probabilidad 
author      : Kevin Pérez C, Profesor Asistente
job         : Ciencias Básicas - Universidad Pontificia Bolivariana
logo        : logou.png
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
widescreen  : true
smaller     : true
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, bootstrap, quiz, shiny, interactive]            
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
    
## Experimentos aleatorios 

La _teoría de la probabilidad_ es la parte de las matemáticas que se encarga del
estudio de los fenómenos o experimentos aleatorios. Existen dos tipos de fenómenos o experimentos en la naturaleza: los deterministas y los aleatorios. 

Un experimento determinista es aquel que produce el mismo resultado cuando se le repite bajo las mismas condiciones, por ejemplo, medir el volumen de un gas cuando la presión y la temperatura son constantes produce, teóricamente, siempre el mismo resultado.

> Por _**experimento aleatorio**_ entenderemos todo aquel experimento que cuando se le repite bajo las mismas condiciones iniciales, el resultado que se obtiene no siempre es el mismo.

---

## Espacio muestral 

> _**Definición**_ El espacio muestral, también llamado espacio muestra,
de un experimento aleatorio es el conjunto de todos los posibles resultados del experimento y se le denota, generalmente, por la letra griega $\Omega$ (omega mayúscula). A un resultado particular del experimento se le denota por la letra $\omega$ (omega minúscula).

_**Ejemplo:**_ Si un experimento aleatorio consiste en lanzar un dado y observar el número que aparece en la cara superior, entonces claramente el espacio muestral es el conjunto $\Omega = \{1, 2, 3, 4, 5, 6\}$. Como ejemplo de
un _evento_ para este experimento podemos definir el conjunto $A=\{2, 4, 6\}$, que corresponde al suceso de obtener como resultado un número par.

---

## Espacio muestral 

- _**Ejemplo:**_ Considere el experimento aleatorio de participar en un juego de lotería. Suponga que hay un millón de números en esta lotería y un jugador participa con un boleto. ¿Cuál es un posible espacio muestral para este experimento si únicamente uno de los posibles números es el ganador?

> - Naturalmente, al jugador le interesa conocer su suerte en este juego y puede proponer como espacio muestral el conjunto $\Omega = \{“ganar”, “perder”\}$. Sin
embargo puede también tomarse como espacio muestral el conjunto que contiene a todos los números participantes, es decir, $\Omega = \{1, 2, . . . , 10^6\}$.  

---

## Operaciones con conjuntos 

Nos interesa poder identificar a todos los posibles eventos en un experimento aleatorio, pues deseamos calcular la probabilidad de ocurrencia de cada uno de ellos. Recordemos que pueden obtenerse nuevos conjuntos a partir de una colección inicial de eventos y de llevar a cabo algunas operaciones sobre ellos, como las que definiremos más adelante.

Consideraremos que estos nuevos conjuntos resultantes son también _eventos_ y deseamos poder calcular su probabilidad. Es por esto que nos será útil revisar brevemente algunas operaciones usuales entre conjuntos. Estableceremos primero varios conceptos elementales y la notación a utilizar.

---

## Operaciones con conjuntos 

Supondremos que el espacio muestral $\Omega$ de un experimento aleatorio es una
especie de conjunto universal y, como hemos mencionado antes, cualquier
elemento de $\Omega$ lo denotaremos por la letra $\omega$. Al conjunto vacío lo denotaremos, como es usual, por el símbolo $\emptyset$.

Otros símbolos usuales son los de pertenencia ($\in$) o no pertenencia ($\notin$) de un elemento en un conjunto, y los de contención ($\subset$, $\subseteq$) o no contención ($\not\subset$) de un conjunto en otro. Se dice
que A es un subconjunto propio de B si $A\subseteq B$, es decir, si A está contenido en B pero no es todo B. La igualdad de dos conjuntos A y B significa que se cumplen las dos contenciones: $A\subset B$ y $B\subset A$. Por último, si A es un conjunto, denotamos la cardinalidad o número de elementos de ese conjunto por el símbolo $\#A$. Ahora procederemos a definir algunas operaciones entre conjuntos.

---

## Operaciones con conjuntos 

Sean A y B dos subconjuntos cualesquiera de $\Omega$. Recordamos a continuación
las operaciones básicas de unión, intersección, diferencia y complemento.

$$A \cup B = \{\omega \in \Omega: \omega \in A \,\, \mbox{o} \,\, \omega \in B  \},$$

$$A \cap B = \{\omega \in \Omega: \omega \in A \,\, \mbox{y} \,\, \omega \in B  \},$$

$$A - B = \{\omega \in \Omega: \omega \in A \,\, \mbox{y} \,\, \omega \notin B  \},$$

$$A^c = \{\omega \in \Omega: \omega \notin A  \},$$

Cuando los conjuntos se expresan en palabras, la operación unión, $A \cup B$,
se lee “A o B” y la intersección, $A \cap B$, se lee “A y B”.

---

## Operaciones con conjuntos 

<img class=center src= assets/img/img1.png height=450 />
<img class=center src= assets/img/img2.png height=450  />

---

## Operaciones con conjuntos 

_**Ejemplo:**_ Sea A el conjunto de aquellas personas que tienen hijos y B
la colección de aquellas personas que están casadas. Entonces el conjunto $A\cap B$ consta de aquellas personas que están casadas y tienen hijos, mientras que el conjunto $A \cap B^c$ está constituido por aquellas personas que tienen
hijos pero no están casadas. ¿Quién es $A^c \cap B$?.

Además, las operaciones unión e intersección son asociativas, esto es, satisfacen las siguientes igualdades:

$$A \cup (B \cup C) = (A \cup B) \cup C,$$
$$A \cap (B \cap C) = (A \cap B) \cap C,$$

---

## Operaciones con conjuntos 

y también son distributivas, es decir,

$$A \cap (B \cup C) = (A \cap B) \cup (A \cap C),$$
$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C),$$

Recordemos también la operación diferencia simétrica entre dos conjuntos
A y B, denotada por $A\Delta B$ y definida como sigue:  

$$A\Delta B= (A \cup B) - (B \cap A)$$

<img class=center src= assets/img/img3.png height=450 />

---

## Operaciones con conjuntos 

Recordemos además las muy útiles leyes de _De Morgan_:

$$(A \cup B)^c = A^c \cap B^c,$$
$$(A \cap B)^c = A^c \cup B^c,$$

La validez de estas dos igualdades puede extenderse a colecciones finitas e incluso arbitrarias de conjuntos.

### Conjuntos ajenos
Cuando dos conjuntos no tienen ningún elemento en común se dice que son ajenos, es decir, los conjuntos A y B son ajenos o disjuntos si se cumple la igualdad

$$(A \cap B) = \emptyset$$

---

## Opereaciones con conjuntos 

_**Ejemplo:**_ Los conjuntos $A = \{1, 2\}$,  $B =\{2, 3\}$ y $C=\{3, 4\}$ son ajenos pues $A\cap B \cap C = \emptyset$, pero no son ajenos dos a dos pues, por ejemplo, el conjunto $A \cap B$ no es vacío. Así, los conjuntos A, B y C son ajenos en el sentido de que la intersección de todos ellos es vacía, pero no son ajenos dos a dos 

### Conjunto potencia

El conjunto potencia de $\Omega$, denotado por $2^{\Omega}$, es aquel conjunto constituido por todos los subconjuntos posibles de $\Omega$. En términos estrictos, esta nueva colección deja de ser un conjunto y se le llama clase de subconjuntos de $\Omega$, aunque seguiremos usando el primer término en nuestro tratamiento elemental de conjuntos. Por ejemplo, si $\Omega = \{a, b, c\}$ entonces el conjunto $2^{\Omega}$ consta de 8 elementos, a saber,

$$2^{\Omega} = \big\{ \emptyset, \{a\}, \{b\}, \{c\}, \{a,b\}, \{a,c\}, \{b,c\}, \Omega \big\}$$

---

## Opereaciones con conjuntos 

### Producto cartesiano

El producto cartesiano de dos conjuntos A y B, denotado por $A\times B$, se
define como la colección de todas las parejas ordenadas $(a,b)$, en donde $a$
es cualquier elemento de A y $b$ es cualquier elemento de B. En símbolos,

$$A\times B = \big\{(a,b): a\in A \,\, \mbox{y} \,\, b\in B \big\}.$$

_**Ejemplo:**_ Si $A = \{a_1, a_2\}$ y $B = \{b_1, b_2, b_3\}$, entonces

$$A\times B = \big\{(a_1,b_1), (a_1,b_2), (a_1,b_3), (a_2,b_1), (a_2,b_2), (a_2,b_3) \big\}.$$

Si la cardinalidad de A es el número _n_ y la cardinalidad de B es _m_, entonces la cardinalidad del conjunto $A\times B$ es el producto $n\cdot m$. Este resultado es llamado principio de multiplicación y se aplica con mucha frecuencia en los procesos de conteo. 

---

## Definiciones de probabilidad 

La _**probabilidad**_ de un evento A es un número real en el intervalo $[0,1]$ que se denota por $P(A)$ y representa una medida de la frecuencia con la que se observa la ocurrencia de este evento cuando se efectúa el experimento aleatorio en cuestión.

### Probabilidad clásica 

> _**Definición**_ Sea A un subconjunto de un espacio muestral $\Omega$ de
cardinalidad finita. Se define la probabilidad clásica del evento A como el cociente
$$P(A)=\frac{\#A}{\#\Omega}$$
en donde el símbolo $\#A$ denota la cardinalidad o número de elementos del conjunto A.

Claramente esta definición es sólo válida para espacios muestrales finitos,
pues forzosamente necesitamos suponer que el número de elementos en $\Omega$ es finito.

---

## Definiciones de probabilidad 

_**Ejemplo:**_ Considere el experimento aleatorio de lanzar un dado equilibrado. El espacio muestral es el conjunto $\Omega = \{1, 2, 3, 4, 5, 6\}$ Si deseamos calcular la probabilidad (clásica) del evento A, correspondiente a obtener un número par, es decir, la probabilidad de 

$$P(A)=\frac{\#\{2, 4, 6\}}{\#\{1,2,3,4,5,6\}}=\frac{3}{6}=\frac{1}{2}=0.5$$

Es inmediato verificar que esta forma de calcular probabilidades satisface,
entre otras, las propiedades que se mencionan a continuación, las cuales aparecerán más adelante en la conceptualización axiomática de la probabilidad.

- $P(\Omega)=1$
- $P(A)\geq 0$
- $P(A\cup B)=P(A)+P(B)$, cuando A y B son ajenos 

---

## Definiciones de probabilidad 

### Probabilidad geométrica

Esta es una extensión de la definición de probabilidad clásica, en donde ahora la probabilidad de un evento se calcula ya no a través de su cardinalidad, sino mediante la determinación de su área, volumen o alguna característica geométrica equivalente, según el problema que se trate. Para el caso de áreas
la definición es la siguiente.

> _**Definición:**_  Si un experimento aleatorio tiene como espacio muestral $\Omega \subset R^2$ cuya área está bien definida y es finita, entonces se define la probabilidad geométrica de un evento $A \subseteq \Omega$ como
$$P(A)=\frac{\mbox{Área de A}}{\mbox{Área de }\Omega}$$ cuando el concepto de área del subconjunto A está bien definido.

---

## Definiciones de probabilidad 

_**Ejemplo (El problema del juego de una feria):**_ El juego de una feria consiste en lanzar monedas de radio $r$ sobre un tablero cuadriculado como el que se muestra en la Figura, en donde el lado de cada cuadrado mide $a$ unidades. Un jugador se hace acreedor a un premio si la moneda lanzada no toca ninguna de las líneas. ¿De qué tamaño deben ser $a$ y $r$ para que la probabilidad de ganar en este juego sea menor a $\frac{1}{4}$?  

<img class=center src= assets/img/img4.png height=450 />


---

## Definiciones de probabilidad 

_**Solución.**_ Primero debemos observar que es suficiente considerar lo que sucede únicamente en el cuadrado donde cae el centro de la moneda. No es difícil darse cuenta que la moneda no toca ninguna línea si su centro cae dentro del cuadrado interior que se muestra en la Figura. 

<img class=center src= assets/img/img5.png height=450 />

---

## Definiciones de probabilidad 

Por lo tanto, si A denota el evento de ganar con un lanzamiento en este juego, entonces la probabilidad de A es el cociente entre el área favorable y el área total, es decir,

$$P(A)=\frac{(a-2r)^2}{a^2}=1-\frac{2r}{a}$$
Si deseamos que esta probabilidad sea menor a 1/4, entonces de aquí puede uno encontrar que $a$ y $r$ deben cumplir la relación $a<4r$. Cuando $a=4r$,
la probabilidad de ganar es exactamente 1/4.

---

## Definiciones de probabilidad 

### Probabilidad frecuentista

Suponga que se realizan $n$ repeticiones de un cierto experimento aleatorio
y que se registra el número de veces que ocurre un determinado evento A. Esta información puede ser usada de la siguiente forma para definir la probabilidad de A.

> _**Definición:**_ Sea $n_A$ el número de ocurrencias de un evento A en $n$ realizaciones de un experimento aleatorio. La probabilidad frecuentista del evento A se define como el límite 
$$P(A)=\lim_{n \to \infty}\frac{n_A}{n}$$
En este caso, debemos hacer notar que no es humanamente posible llevar a cabo una infinidad de veces el experimento aleatorio y tampoco podemos garantizar, por ahora, la existencia de tal límite. Por lo tanto, mediante la definición anterior, no es posible encontrar de manera exacta la probabilidad de un evento cualquiera, aunque permite tener una aproximación empírica del valor de $P(A)$, es decir,
$$P(A)\approx \frac{n_A}{n}$$

---

## Definiciones de probabilidad 

### Probabilidad subjetiva 

En este caso, la probabilidad de un evento depende del observador, es decir,
depende de lo que el observador conoce del fenómeno en estudio. Puede parecer un tanto informal y poco seria esta definición de la probabilidad de un evento, sin embargo, en muchas situaciones es necesario recurrir a un experto para tener por lo menos una idea vaga de cómo se comporta el fenómeno de nuestro interés y saber si la probabilidad de un evento es alta o baja. Por ejemplo, ¿cuál es la probabilidad de que un cierto equipo de fútbol gane en su próximo partido? Ciertas circunstancias internas del equipo, las condiciones del equipo rival o cualquier otra condición externa, son elementos que sólo algunas personas conocen y que podrían darnos una idea más exacta de esta probabilidad.

---

## Definiciones de probabilidad 

### Probabilidad axiomática

En la definición axiomática de la probabilidad no se establece la forma explícita de calcular las probabilidades, sino únicamente se proponen las
reglas que el cálculo de probabilidades debe satisfacer. Los siguientes tres
postulados o axiomas fueron establecidos en 1933 por el matemático ruso
_Andrey Nikolaevich Kolmogorov_.

_**Axiomas de probabilidad**_

1. $P(A)\geq 0$
2. $P(\Omega) = 1$
3. $P\left(\bigcup_{k=1}^{\infty}A_k\right)=\sum_{k=1}^{\infty}P(A_k)$, cuando $A_1,A_2, ...$ son ajenos dos a dos.  

Recordemos que un axioma o postulado es una proposición que se acepta como válida y sobre la cual se funda una teoría, en este caso la teoría de la probabilidad

---

## Propiedades de la probabilidad 

Tomando como base los axiomas de _Kolmogorov_ y usando la teoría elemental de conjuntos, demostraremos que toda medida de probabilidad cumple con una serie de propiedades generales e interesantes.

> ### **Algunas propiedades de la probabilidad**  
- $P(A^c) = 1- P(A)$
- $P(\emptyset) = 0$
- Si $A\subseteq B$, entonces $P(A)\leq P(B)$.
- Si $A\subseteq B$, entonces $P(B-A)=P(B)-P(A)$.
- $0 \leq P(A) \leq 1$
- $P(A\cup B)=P(A)+P(B)-P(A\cap B)$


---

## Calculo de probabilidad de eventos 

### Ejemplos 

- Si un trabajo enviado a una impresora aparece primero en línea con probabilidad 60%, y segundo en línea con probabilidad 30%, entonces con probabilidad 90% aparece primero o segundo en línea.

- Durante una cierta construcción, un apagón de la red ocurre el lunes con probabilidad 0.7 y el martes con la probabilidad 0.5. Entonces, ¿aparece el lunes o el martes con probabilidad 0.7 + 0.5 = 1.2? Obviamente no, porque la probabilidad debe estar siempre entre 0 y 1! Las probabilidades no son aditivas aquí porque los apagones del lunes y del martes no son mutuamente excluyentes. En otras palabras, nos es imposible ver apagones en ambos días.

- En el ejemplo anterior, suponga que hay una probabilidad de 0.35 de experimentar apagones en ambos días, lunes y martes. Entonces la probabilidad de tener un apagón el lunes o el martes es igual

$$P(A\cup B) =  0.7+0.5-0.35 = 0.85$$

---

## Calculo de probabilidad de eventos 

- Si un sistema parece protegido contra un nuevo virus informático con probabilidad 0,7, entonces se expone con probabilidad
$$P(A^c)=1-P(A) = 1-0.7=0.3$$

- Un experimento aleatorio puede resultar en uno de los resultados $\{a,b,c,d\}$, con probabilidades 0.1, 0.3, 0.5, y 0.1 respectivamente. Sea $A$ que denota el evento $\{a,b\}$, $B$ el evento $\{b,c,d\}$ y $C$ el evento $\{d\}$, entonces 
$$P(A)=0.1+0.3=0.4$$

Como serían, $P(B)$ y $P(C)$.

---

## Calculo de probabilidad de eventos 

