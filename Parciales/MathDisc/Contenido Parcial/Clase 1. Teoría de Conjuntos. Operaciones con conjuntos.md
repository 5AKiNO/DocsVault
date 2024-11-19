#### 1. Conjuntos
Los conjuntos son colecciones bien definidas de objetos o elementos. El estudio de los conjuntos proporciona una base para la matemática discreta y es esencial para la comprensión de otros conceptos matemáticos.

##### 1.1. Conceptos básicos
Un conjunto es una colección de elementos que pueden identificarse como miembros de ese conjunto. Los elementos pueden ser objetos concretos o abstractos, y deben cumplir con la característica de pertenecer o no pertenecer al conjunto de forma clara.

**Ejemplo:**
$A = \{ 1, 2, 3, 4, 5 \}$
El número 3 pertenece al conjunto $( A )$, lo que se denota como:
$[ 3 \in A ]$

##### 1.2. Representación de un conjunto
Los conjuntos pueden representarse de diversas formas, cada una adecuada según el contexto o el tipo de conjunto.

###### 1.2.1. Por extensión
Se enumeran todos los elementos del conjunto.

**Ejemplo:**
$[ B = \{ a, b, c, d \} ]$

###### 1.2.2. Por comprensión
Se describe una propiedad común a todos los elementos del conjunto.

**Ejemplo:**
$[ C = \{ x \mid x \text{ es un número par menor que 10} \} ]$
$[ C = \{ 2, 4, 6, 8 \} ]$

###### 1.2.3. Representación gráfica - Diagrama de Venn-Euler
Los diagramas de Venn y Euler son representaciones gráficas de conjuntos y sus relaciones. 

**Ejemplo:**
Considera los conjuntos:
$[ A = \{ 1, 2, 3 \}, B = \{ 2, 3, 4 \} ]$
Su intersección y unión pueden representarse gráficamente.

##### 1.3. Relaciones entre conjuntos
Existen diversas formas en las que los conjuntos pueden relacionarse entre sí.

###### 1.3.1. Pertenencia o no pertenencia a un conjunto
La pertenencia a un conjunto se expresa mediante el símbolo $( \in )$, mientras que la no pertenencia se denota como $( \notin )$.

**Ejemplo:**
Si $( A = \{ 1, 2, 3 \} )$, entonces:
$[ 2 \in A ]$
$[ 5 \notin A ]$

###### 1.3.2. Relación de contención
Un conjunto $( A )$ está contenido en un conjunto $( B )$ si todos los elementos de $( A )$ también pertenecen a $( B )$, denotado como $( A \subseteq B )$.

**Ejemplo:**
Si $( A = \{ 1, 2 \} )$ y $( B = \{ 1, 2, 3 \} )$, entonces:
$[ A \subseteq B ]$

##### 1.4. Cardinalidad de un conjunto
La cardinalidad de un conjunto es el número de elementos que contiene.

**Ejemplo:**
Si $( A = \{ 1, 2, 3 \} )$, la cardinalidad de $( A )$ es:
$[ |A| = 3 ]$

##### 1.5. Clases de conjuntos
Los conjuntos pueden clasificarse según diferentes criterios.

###### 1.5.1. Conjunto unitario
Es un conjunto que contiene un solo elemento.

**Ejemplo:**
$[ A = \{ a \} ]$

###### 1.5.2. Conjunto vacío
El conjunto vacío es aquel que no contiene ningún elemento, denotado como $( \emptyset )$ o $( \{\} )$.

**Ejemplo:**
$[ A = \emptyset ]$

###### 1.5.3. Conjunto universal
El conjunto universal es el conjunto que contiene todos los elementos bajo consideración en un contexto particular, denotado como $( U )$.

**Ejemplo:**
Si el conjunto universal $( U )$ es el conjunto de todos los números naturales menores que 10, entonces:
$[ U = \{ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 \} ]$

###### 1.5.4. Conjuntos disjuntos
Dos conjuntos son disjuntos si no tienen ningún elemento en común.

**Ejemplo:**
Si $( A = \{ 1, 2 \} )$ y $( B = \{ 3, 4 \} )$, entonces:
$[ A \cap B = \emptyset ]$

###### 1.5.5. Conjunto finito
Un conjunto finito tiene un número limitado de elementos.

**Ejemplo:**
$[ A = \{ a, b, c \} ]$

###### 1.5.6. Conjuntos infinitos
Un conjunto es infinito si tiene un número ilimitado de elementos.

**Ejemplo:**
El conjunto de los números naturales es infinito:
$[ \mathbb{N} = \{ 1, 2, 3, 4, \dots \} ]$

##### 1.6. Igualdad de conjuntos
Dos conjuntos son iguales si contienen los mismos elementos.

**Ejemplo:**
Si $( A = \{ 1, 2, 3 \} )$ y $( B = \{ 3, 2, 1 \} )$, entonces:
$[ A = B ]$

##### 1.7. Equivalencia de conjuntos
Dos conjuntos son equivalentes si tienen la misma cardinalidad.

**Ejemplo:**
Si $( A = \{ a, b, c \} )$ y $( B = \{ 1, 2, 3 \} )$, entonces:
$[ |A| = |B| = 3 ]$

##### 1.8. Conjuntos numéricos
Los conjuntos numéricos incluyen diversas categorías de números que cumplen con diferentes propiedades.

###### 1.8.1. Números naturales
El conjunto de los números naturales incluye los enteros positivos y, a veces, el cero.

**Ejemplo:**
$[ \mathbb{N} = \{ 0, 1, 2, 3, 4, \dots \} ]$

###### 1.8.2. Números enteros
El conjunto de los números enteros incluye los números naturales y sus negativos.

**Ejemplo:**
$[ \mathbb{Z} = \{ \dots, -3, -2, -1, 0, 1, 2, 3, \dots \} ]$

###### 1.8.3. Números racionales
Los números racionales son aquellos que pueden expresarse como una fracción de dos enteros.

**Ejemplo:**
$[ \mathbb{Q} = \left\{ \frac{a}{b} \mid a, b \in \mathbb{Z}, b \neq 0 \right\} ]$

###### 1.8.4. Números irracionales
Los números irracionales no pueden expresarse como una fracción de enteros.

**Ejemplo:**
$[ \pi, \sqrt{2} ]$

###### 1.8.5. Números reales
El conjunto de los números reales incluye tanto los racionales como los irracionales.

**Ejemplo:**
$[ \mathbb{R} = \{ x \mid x \text{ es racional o irracional} \} ]$

#### 2. Operaciones con conjuntos
Las operaciones entre conjuntos permiten la manipulación y combinación de estos para crear nuevos conjuntos.

##### 2.1. Complemento
El complemento de un conjunto $( A )$, denotado como $( A' )$, es el conjunto de todos los elementos que no pertenecen a $( A )$, pero que están en el conjunto universal $( U )$.

**Ejemplo:**
Si $( U = \{ 1, 2, 3, 4, 5 \} )$ y $( A = \{ 1, 2 \} )$, entonces el complemento de $( A )$ es:
$[ A' = \{ 3, 4, 5 \} ]$

##### 2.2. Unión de conjuntos
La unión de dos conjuntos $( A )$ y $( B )$, denotada como $( A \cup B )$, es el conjunto de todos los elementos que pertenecen a $( A )$, a $( B )$, o a ambos.

**Ejemplo:**
Si $( A = \{ 1, 2 \} )$ y $( B = \{ 2, 3 \} )$, entonces:
$[ A \cup B = \{ 1, 2, 3 \} ]$

##### 2.3. Intersección de conjuntos
La intersección de dos conjuntos $( A )$ y $( B )$, denotada como $( A \cap B )$, es el conjunto de elementos que pertenecen tanto a $( A )$ como a $( B )$.

**Ejemplo:**
Si $( A = \{ 1, 2 \} )$ y $( B = \{ 2, 3 \} )$, entonces:
$[ A \cap B = \{ 2 \} ]$

##### 2.4. Diferencia de conjuntos
La diferencia entre dos conjuntos $( A )$ y $( B )$, denotada como $( A - B )$, es el conjunto de elementos que pertenecen a $( A )$ pero no a $( B )$.

**Ejemplo:

**
Si $( A = \{ 1, 2, 3 \} )$ y $( B = \{ 2, 3 \} )$, entonces:
$[ A - B = \{ 1 \} ]$

##### 2.5. Producto cartesiano
El producto cartesiano de dos conjuntos $( A )$ y $( B )$, denotado como $( A \times B )$, es el conjunto de todos los pares ordenados $($(a, b)$)$, donde $( a \in A )$ y $( b \in B )$.

**Ejemplo:**

Si $( A = \{ 1, 2 \} )$ y $( B = \{ 3, 4 \} )$, entonces: $A \times B = \{ (1, 3), (1, 4), (2, 3), (2, 4) \}$