#### 1. Definición y Concepto de la Distribución Binomial

**1.1 Definición:**  
La distribución binomial describe el número de éxitos en una secuencia de *N* ensayos independientes, donde cada ensayo tiene dos posibles resultados: éxito (con probabilidad *p*) o fracaso (con probabilidad *q* = 1 - *p*)

**1.2 Concepto Clave:**  
Esta distribución es útil para modelar experimentos donde se pueden obtener solo dos resultados por ensayo (éxito o fracaso), y donde los ensayos son independientes entre sí.  
Ejemplo: Al lanzar una moneda, "éxito" puede ser obtener cara y "fracaso", cruz

#### 2. Fórmulas y Ejemplos

**2.1 Fórmula Principal:**  
La probabilidad de obtener exactamente *X* éxitos en *N* ensayos se calcula mediante la siguiente fórmula:
$P(X = x) = \binom{N}{x} p^x q^{N-x}$
Donde:
- $\binom{N}{x}$ es el coeficiente binomial:
  $\binom{N}{x} = \frac{N!}{x!(N-x)!}$
- *p* es la probabilidad de éxito en cada ensayo.
- *q* es la probabilidad de fracaso.

**2.2 Ejemplo 1: Lanzamiento de una moneda**  
Si lanzamos una moneda 5 veces, con una probabilidad de 0.5 para obtener cara, ¿cuál es la probabilidad de obtener exactamente 3 caras?  
**Solución:** Aplicamos la fórmula con *N* = 5, *X* = 3, *p* = 0.5, *q* = 0.5.

**2.3 Ejemplo 2: Encuesta con dos resultados**  
En una encuesta, el 70% de las personas eligen el producto A. Si seleccionamos 10 personas, ¿cuál es la probabilidad de que exactamente 7 elijan el producto A?  
**Solución:** Aplicamos la fórmula con *N* = 10, *X* = 7, *p* = 0.7, *q* = 0.3.

#### 3. Leyenda de los Parámetros

- **N:** Número de ensayos o pruebas realizados.
- **X:** Número de éxitos obtenidos en los *N* ensayos.
- **p:** Probabilidad de éxito en cada ensayo.
- **q:** Probabilidad de fracaso en cada ensayo (*q* = 1 - *p*).

#### 4. Propiedades de la Distribución Binomial

**4.1 Media (Esperanza Matemática):**  
La media o valor esperado es:
$\mu = N \cdot p$
Esto representa el número promedio de éxitos en *N* ensayos.

**4.2 Varianza:**  
La varianza mide la dispersión de los éxitos alrededor de la media:
$\sigma^2 = N \cdot p \cdot q$

**4.3 Desviación Estándar:**  
La desviación estándar es la raíz cuadrada de la varianza:
$\sigma = \sqrt{N \cdot p \cdot q}$

**4.4 Coeficiente de Sesgo:**  
El coeficiente de sesgo indica la inclinación de la distribución hacia los éxitos o fracasos:
$\text{Sesgo} = \frac{q - p}{\sqrt{N \cdot p \cdot q}}$

**4.5 Coeficiente de Curtosis:**  
La curtosis mide el grado de agudeza o achatamiento de la distribución:
$\text{Curtosis} = \frac{1 - 6pq}{Npq}$

#### 5. Ejemplos Prácticos

**5.1 Ejemplo 3: Defectos en una línea de producción**  
En una fábrica, la probabilidad de que un producto sea defectuoso es 0.02. Si se inspeccionan 100 productos, ¿cuál es la probabilidad de encontrar exactamente 3 defectuosos?  
**Solución:** Aplicamos la fórmula con *N* = 100, *X* = 3, *p* = 0.02, *q* = 0.98. Además, calculamos la media, varianza y desviación estándar para este caso.