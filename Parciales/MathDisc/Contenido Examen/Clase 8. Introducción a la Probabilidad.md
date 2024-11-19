z ## 1. **Introducción**
La probabilidad es una rama fundamental de las matemáticas que se ocupa del estudio de la incertidumbre y los eventos aleatorios. Su importancia radica en su amplia aplicación en campos como las ciencias, la economía, la ingeniería, y más. El estudio de la probabilidad permite predecir resultados a largo plazo basados en patrones observados, siendo una herramienta esencial en la toma de decisiones informadas.

## 2. **Experimentos Deterministas y Experimentos Aleatorios**
   ### 2.1. **Experimentos Deterministas**
   Un experimento determinista es aquel en el que, bajo las mismas condiciones, siempre se obtiene el mismo resultado. El resultado es predecible con certeza.  
   **Ejemplos**:  
   - La caída de un objeto bajo la influencia de la gravedad.  
   - La suma de dos números.

   ### 2.2. **Experimentos Aleatorios**
   Un experimento aleatorio es aquel cuyo resultado no se puede predecir con certeza, incluso si se repiten las mismas condiciones.  
   **Ejemplos**:  
   - Lanzar una moneda.  
   - Lanzar un dado.

   ### 2.3. **Clasificación de Experimentos Aleatorios**
   - **Experimentos de Tipo A**: Tienen un número finito de resultados posibles.  
     **Ejemplo**: Lanzamiento de un dado (seis posibles resultados).  
   - **Experimentos de Tipo B**: Tienen un número infinito de resultados posibles.  
     **Ejemplo**: Medir el tiempo exacto que tarda una bombilla en apagarse.

## 3. **Teorías Probabilísticas**
   ### 3.1. **Conceptos y Definiciones Básicas**
   La probabilidad mide la posibilidad de que ocurra un evento. En términos simples, es una manera de cuantificar la incertidumbre.  
   
   ### 3.2. **Orden Aleatorio**
   Un orden aleatorio se refiere a situaciones en las que no se puede predecir un resultado individual, pero sí es posible describir el comportamiento de múltiples experimentos en conjunto.  
   **Ejemplo**: Lanzar repetidamente una moneda. Aunque no se puede predecir el resultado de un solo lanzamiento, se espera que a largo plazo el número de caras sea aproximadamente igual al número de cruces.

   ### 3.3. **Espacio Muestral (S)**
   El espacio muestral es el conjunto de todos los posibles resultados de un experimento aleatorio.  
   **Ejemplo**: Para el lanzamiento de un dado, $S = \{1, 2, 3, 4, 5, 6\}$

   ### 3.4. **Suceso o Evento Aleatorio**
   Un suceso es cualquier subconjunto del espacio muestral. Puede ser un evento simple o compuesto.  
   **Ejemplo**: En el lanzamiento de un dado, obtener un número par $A = \{2, 4, 6\}$ es un evento compuesto.

   ### 3.5. **Experimento Aleatorio**
   Un experimento aleatorio es un proceso cuyo resultado no se puede predecir con certeza, pero sigue reglas bien definidas.  
   **Ejemplo**: Lanzar una moneda, con posibles resultados de cara o cruz.

## 4. **Definición Clásica de Probabilidad**
   ### 4.1. **Definición Formal**
   La probabilidad clásica se define como el cociente entre el número de resultados favorables y el número total de posibles resultados en un espacio muestral finito.  
   **Fórmula**:  
$P(A) = \frac{\text{Número de resultados favorables a } A}{\text{Número total de resultados en el espacio muestral}}$

   ### 4.2. **Ejemplo de Aplicación**
   En el lanzamiento de un dado, la probabilidad de obtener un número par es:  
$P(\text{número par}) = \frac{3}{6} = \frac{1}{2}$

## 5. **Diagrama de Árbol**
   ### 5.1. **Concepto del Diagrama de Árbol**
   Un diagrama de árbol es una representación gráfica que muestra todos los posibles resultados de un experimento secuencial.  
   
   ### 5.2. **Construcción de un Diagrama de Árbol**
   Los pasos para construir un diagrama de árbol son:
   1. Dibuja un nodo inicial que representa el punto de partida del experimento.
   2. Extiende ramas desde el nodo inicial para cada uno de los posibles resultados del primer paso del experimento.
   3. Añade más ramas para los posibles resultados de los pasos posteriores.

   ### 5.3. **Ejemplo de Diagrama de Árbol: Lanzamiento de Dos Monedas**
   Al lanzar dos monedas, los posibles resultados son:
 $(C, C), (C, X), (X, C), (X, X)$
   Diagrama de árbol:
```text
Primer lanzamiento:
	   C
	 /    
   O
	 \    
	   X
```

   ### 5.4. **Uso del Diagrama de Árbol para Calcular Probabilidades**
   Para calcular la probabilidad de obtener exactamente una cara en dos lanzamientos de una moneda:  
- Resultados favorables: $(C, X)$, $(X, C)$ 
- Probabilidad: $P(\text{exactamente una cara}) = \frac{2}{4} = \frac{1}{2}$