## 1. Funciones en Java  

Las **funciones** son bloques de código reutilizables diseñados para realizar tareas específicas. En Java, las funciones se implementan como métodos dentro de una clase. A continuación, se explican en detalle sus componentes y características.

### 1.1 Declaración de Funciones  
Una función se declara especificando su tipo de retorno, nombre y parámetros. Su sintaxis general es:  

```java
public static <tipoRetorno> <nombreFuncion>(<tipoParametro> <nombreParametro>) {
    // cuerpo de la función
}
```  
- **Tipo de retorno**: Define el tipo de dato que devuelve la función (por ejemplo, `int`, `String`, `void`).  
- **Nombre de la función**: Debe ser descriptivo y seguir la convención camelCase.  
- **Parámetros**: Son los valores que la función recibe para operar. Se definen entre paréntesis.

### 1.2 Parámetros de Función  
Los parámetros permiten la entrada de datos a una función:  
- **Parámetros por valor**: Java pasa los argumentos por valor, es decir, copia el valor del argumento a la función.  
- **Parámetros de referencia**: Aunque Java no permite pasar objetos por referencia directa, el uso de referencias permite modificar el estado de los objetos.  

### 1.3 Retorno de Valores  
El tipo de retorno especificado determina qué tipo de dato puede devolver la función. Ejemplo:  

```java
public static int sumar(int a, int b) {
    return a + b;
}
```  

### 1.4 Funciones sin Retorno  
Las funciones declaradas con el tipo `void` no devuelven ningún valor. Son útiles para ejecutar tareas como mostrar información.  

```java
public static void mostrarMensaje(String mensaje) {
    System.out.println(mensaje);
}
```  

### 1.5 Llamada de Funciones  
Para ejecutar una función, se realiza una **llamada** mediante su nombre, seguido de los argumentos requeridos:  

```java
sumar(5, 3);
mostrarMensaje("Hola, Java!");
```

### 1.6 Ámbito de las Variables  
El ámbito (o alcance) de una variable define dónde puede ser utilizada. Existen tres niveles principales:  
1. **Variables locales**: Declaradas dentro de una función, su alcance se limita al bloque donde fueron creadas.  
2. **Variables de instancia**: Propias de una instancia de la clase, accesibles desde cualquier método no estático.  
3. **Variables estáticas**: Compartidas por todas las instancias de la clase.  

---

## 2. Arrays en Java  

Un **array** es una estructura de datos que permite almacenar múltiples elementos del mismo tipo en una colección fija y ordenada.

### 2.1 Declaración y Creación de Arrays  
Un array se declara especificando el tipo de datos y el tamaño:  

```java
int[] numeros = new int[5];
```  
- **Tipo de dato**: Define el tipo de los elementos almacenados.  
- **Tamaño**: Especifica la cantidad fija de elementos.  

### 2.2 Acceso a Elementos en un Array  
Se accede a los elementos mediante su índice, que inicia en `0`:  

```java
numeros[0] = 10; // Asignar valor
int valor = numeros[0]; // Leer valor
```  

### 2.3 Longitud de un Array  
El atributo `length` permite conocer el número de elementos en un array:  

```java
System.out.println(numeros.length);
```  

### 2.4 Inicialización de Arrays  
Los arrays pueden inicializarse directamente con valores:  

```java
int[] numeros = {1, 2, 3, 4, 5};
```  

### 2.5 Ejemplos de Arrays  
Ejemplo de uso:  

```java
String[] nombres = {"Ana", "Luis", "Carlos"};
for (String nombre : nombres) {
    System.out.println(nombre);
}
```  

### 2.6 ArrayList en Java  
Un **ArrayList** es una colección dinámica que puede cambiar su tamaño. Es parte de `java.util`.

#### Declaración y Creación  
```java
ArrayList<String> lista = new ArrayList<>();
```  

#### Agregar y Acceder a Elementos  
```java
lista.add("Elemento 1");
String elemento = lista.get(0);
```  

#### Tamaño y Comprobaciones  
```java
System.out.println(lista.size());
System.out.println(lista.contains("Elemento 1"));
```  

#### Eliminar y Buscar Elementos  
```java
lista.remove("Elemento 1");
int indice = lista.indexOf("Elemento 2");
```  

#### Ejemplo de Uso  
```java
ArrayList<Integer> numeros = new ArrayList<>();
numeros.add(10);
numeros.add(20);
numeros.forEach(System.out::println);
```  

---

## 3. API Swing  

La **API Swing** es una biblioteca gráfica para Java que facilita la creación de interfaces de usuario. Es conocida por su flexibilidad y capacidad multiplataforma.

### 3.1 Características Principales  
1. **Componentes Swing**: Proporciona componentes avanzados como botones, cuadros de texto y tablas.  
2. **Diseño basado en componentes**: Los elementos visuales se organizan en jerarquías.  
3. **Multiplataforma**: Las aplicaciones tienen un aspecto consistente en diferentes sistemas operativos.  
4. **Personalización y Apariencia**: Soporta temas y estilos visuales.  
5. **Manejo de eventos**: Utiliza el modelo de eventos para gestionar interacciones del usuario.  

### 3.2 JFrame  
`JFrame` es la ventana principal de una aplicación Swing:  

```java
JFrame frame = new JFrame("Mi Ventana");
frame.setSize(400, 300);
frame.setVisible(true);
```  

### 3.3 JPanel  
`JPanel` es un contenedor utilizado para organizar otros componentes:  

```java
JPanel panel = new JPanel();
frame.add(panel);
```  

### 3.4 Migración a JavaFX  
Aunque Swing sigue siendo popular, JavaFX es la tecnología más reciente para interfaces gráficas, ofreciendo características modernas como soporte para CSS y multimedia.
