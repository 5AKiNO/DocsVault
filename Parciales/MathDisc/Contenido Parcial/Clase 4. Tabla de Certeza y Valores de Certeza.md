#### 1. Valores de Certeza

##### 1.1. Definición de Valores de Certeza  
Los valores de certeza en lógica son los posibles valores de verdad (Verdadero o Falso) que pueden tomar las proposiciones lógicas.

##### 1.2. Interpretación de los Valores de Certeza  
- **Verdadero (T)** se representa como 1.  
- **Falso (F)** se representa como 0.

##### 1.3. Importancia de los Valores de Certeza en la Lógica Proposicional  
Los valores de certeza permiten evaluar la validez de proposiciones complejas y construir **tablas de verdad** que son fundamentales para analizar proposiciones y relaciones lógicas.

---

#### 2. Tablas de Certeza

Las tablas de certeza, también conocidas como **tablas de verdad**, muestran cómo se distribuyen los valores de verdad en las diferentes combinaciones de proposiciones atómicas.

##### 2.1. Conjunción (∧)  
- **Definición**: La conjunción es verdadera solo si ambas proposiciones son verdaderas.  
- **Tabla de certeza**:

| P   | Q   | P ∧ Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | F     |
| F   | T   | F     |
| F   | F   | F     |

- **Ejemplo**: "Llueve y el suelo está mojado".

##### 2.2. Disyunción Inclusiva (∨)  
- **Definición**: La disyunción inclusiva es verdadera si al menos una de las proposiciones es verdadera.  
- **Tabla de certeza**:

| P   | Q   | P ∨ Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | T     |
| F   | T   | T     |
| F   | F   | F     |

- **Ejemplo**: "Llueve o el suelo está mojado".

##### 2.3. Disyunción Exclusiva (⊕)  
- **Definición**: La disyunción exclusiva es verdadera si una y solo una de las proposiciones es verdadera.  
- **Tabla de certeza**:

| P   | Q   | P ⊕ Q |
| --- | --- | ----- |
| T   | T   | F     |
| T   | F   | T     |
| F   | T   | T     |
| F   | F   | F     |

- **Ejemplo**: "O llueve o el suelo está mojado, pero no ambos".

##### 2.4. Negación (¬)  
- **Definición**: La negación invierte el valor de verdad de una proposición.  
- **Tabla de certeza**:

| P   | ¬P  |
| --- | --- |
| T   | F   |
| F   | T   |

- **Ejemplo**: "No está lloviendo".

##### 2.5. Implicancia Condicional (→)  
- **Definición**: La implicación condicional es falsa solo si la primera proposición es verdadera y la segunda es falsa.  
- **Tabla de certeza**:

| P   | Q   | P → Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | F     |
| F   | T   | T     |
| F   | F   | T     |

- **Ejemplo**: "Si llueve, entonces el suelo está mojado".

##### 2.6. Bicondicional o Equivalencia (↔)  
- **Definición**: El bicondicional es verdadero cuando ambas proposiciones tienen el mismo valor de verdad.  
- **Tabla de certeza**:

| P   | Q   | P ↔ Q |
| --- | --- | ----- |
| T   | T   | T     |
| T   | F   | F     |
| F   | T   | F     |
| F   | F   | T     |

- **Ejemplo**: "Llueve si y solo si el suelo está mojado".

---

#### 3. Tautologías, Contingencias y Contradicciones

##### 3.1. Tautología  
Una **tautología** es una proposición que es siempre verdadera, independientemente de los valores de verdad de las proposiciones que la componen.  
- **Ejemplo**: "P ∨ ¬P" (Una proposición o su negación es siempre verdadera).

##### 3.2. Contingencia  
Una **contingencia** es una proposición que puede ser verdadera o falsa dependiendo de los valores de verdad de sus componentes.  
- **Ejemplo**: "P ∧ Q" (La conjunción de dos proposiciones puede tener distintos valores de verdad).

##### 3.3. Contradicción  
Una **contradicción** es una proposición que es siempre falsa, independientemente de los valores de verdad de las proposiciones que la componen.  
- **Ejemplo**: "P ∧ ¬P" (Una proposición y su negación no pueden ser verdaderas al mismo tiempo).