En esta fase inicial, el objetivo es construir el esqueleto del juego para que puedas comenzar a probar las funcionalidades básicas mientras desarrollas la narrativa y mecánicas esenciales.
#### **Objetivo de la Fase 1**

- Crear un **prototipo funcional** que cubra las bases del mapa ASCII, movimiento del jugador, descripciones narrativas escalonadas simples, y estructura del proyecto en C++ sin makefile.
- Preparar el terreno para añadir mecánicas más complejas en fases posteriores (combate, inventario, mercado, etc.).
- Introducir la narrativa escalonada inicial para que el jugador tenga una experiencia narrativa que evolucione con la exploración.

---

### **Estructura del Proyecto - Prototipo**

En esta fase, establecerás la estructura básica del código y comenzarás a desarrollar funcionalidades clave. Se recomienda seguir la organización de carpetas planteada previamente, donde cada funcionalidad esté bien separada en módulos para facilitar la expansión.

**Estructura del proyecto:**

```
Wander_the_Echoes_of_Forgotten_Roads/
├── src/
│   ├── main.cpp               // Punto de entrada del juego
│   ├── Map.cpp                // Mapa del mundo
│   ├── Player.cpp             // Lógica del jugador
│   ├── Narrative.cpp          // Manejo de la narrativa escalonada
├── include/
│   ├── Map.h                  // Declaraciones de la clase Map
│   ├── Player.h               // Declaraciones de la clase Player
│   ├── Narrative.h            // Declaraciones para la narrativa
├── assets/                    // Archivos de texto para descripciones narrativas
└── README.md                  // Documentación sobre el proyecto
```

---

### **Componentes Fundamentales del Prototipo**

#### **1. Mapa ASCII y Movimiento del Jugador**

**Fundamentación:**
- El mapa es la base sobre la cual se desarrollarán todas las interacciones del jugador. Utilizando un **array bidimensional**, cada celda del mapa representa una parte del entorno, como un sendero, una pared, un enemigo, etc.
- El jugador debe poder moverse en las cuatro direcciones cardinales (Norte, Sur, Este, Oeste), y el mapa se actualizará en la pantalla según el movimiento.
  
**Funcionalidad Mínima:**
- **Movimiento**: El jugador debe poder moverse en un mapa de tamaño fijo (ej. 10x10) usando teclas de dirección (WASD o flechas).
- **Visualización**: Cada movimiento del jugador actualizará el mapa en la terminal, mostrando su posición y el entorno inmediato.
- **Interacciones Iniciales**: Al moverse por el mapa, se activarán narrativas básicas que describen el lugar donde se encuentra el jugador.

---

#### **2. Narrativa Escalonada Básica (Primera Capa)**

**Fundamentación:**
- Esta es la primera capa de la narrativa escalonada. Al moverse el jugador por el mapa, se activan descripciones simples pero inmersivas. En esta fase inicial, estas descripciones son funcionales pero con un toque de misterio, lo que invita a seguir explorando.

**Funcionalidad Mínima:**
- **Descripciones Iniciales**: Cada posición del mapa tendrá una descripción básica asignada. Ejemplo:
  - En un camino: *"Te encuentras en un sendero de piedra. El aire es denso y sientes que algo te observa."*
  - Cerca de una puerta: *"Una puerta oxidada bloquea el paso. No parece haber manera de abrirla desde aquí."*
  
- **Narrativa Escalonada (Primer Nivel)**: Las descripciones evolucionarán a medida que el jugador regrese a las mismas áreas o interactúe con objetos específicos. Esta capa inicial se centrará en dar contexto al entorno sin sobrecargar al jugador.

- **Archivos de texto externos**: Puedes usar archivos de texto en la carpeta **`assets/`** para almacenar las descripciones narrativas. Esto facilita la edición y expansión del contenido sin modificar el código.

---

#### **3. Estructura del Jugador**

**Fundamentación:**
- El jugador es el núcleo de las interacciones con el mapa y la narrativa. En esta fase, la lógica del jugador debe centrarse en las estadísticas básicas y el control del movimiento.

**Funcionalidad Mínima:**
- **Atributos Iniciales**: El jugador debe tener atributos simples como `salud` y `posición` en el mapa.
- **Interacciones Básicas**: Al moverse a nuevas áreas, el jugador desencadena eventos narrativos, aunque no se introduce aún el combate ni el inventario.

---

#### **4. Proceso Narrativo en el Prototipo**

**Fundamentación:**
- La narrativa es uno de los pilares del juego, y en esta fase se enfocará en describir el entorno de manera escalonada. Las descripciones se dividen en niveles, y solo el primer nivel será implementado en esta fase.

**Narrativa Escalonada Inicial:**
- **Capa 1 (Funcional y Sencilla)**: La narrativa se activa cuando el jugador entra en una nueva celda del mapa, brindando una descripción básica. Ejemplo:
  - En la primera visita a un camino, el jugador recibe una descripción simple: *"Un camino de piedra se extiende frente a ti. Todo parece tranquilo."*
  
- **Progresión a Capa 2 (Posibilidad futura)**: En fases posteriores, si el jugador regresa al mismo lugar o activa ciertos eventos, las descripciones se ampliarán para añadir más detalles.

**Gestión Narrativa con Archivos Externos**:
- Utiliza archivos externos para manejar la narrativa. Cada archivo de texto puede contener las descripciones de un área específica. Esto no solo es modular, sino que también facilita la escalabilidad y modificación.

---

### **5. Estructura del Código sin Makefile**

**Fundamentación:**
- En esta fase inicial, no se necesita un **makefile**. La compilación se realizará manualmente, asegurando que entiendes el proceso y el código base.

**Compilación Manual**:
1. Navega al directorio del proyecto donde están los archivos `.cpp`.
2. Usa un compilador como `g++` para compilar el código de manera manual. Ejemplo:
   ```bash
   g++ src/main.cpp src/Map.cpp src/Player.cpp src/Narrative.cpp -o wander_game
   ```
3. Ejecuta el archivo compilado:
   ```bash
   ./wander_game
   ```

---

### **6. Plan de Expansión para Fases Posteriores**

Al terminar la Fase 1, tendrás un prototipo funcional que incluye las siguientes características:
- **Mapa y movimiento básico del jugador**: Una estructura visual inicial en ASCII.
- **Narrativa escalonada inicial**: Una capa básica de narrativa que se activará al moverse por el mapa.
- **Interacciones básicas**: Descripciones reactivas que establecen el tono del juego.
  
A partir de aquí, estarás listo para:
- Ampliar la narrativa con más capas.
- Introducir el sistema de combate y la interacción con NPCs.
- Añadir un sistema de inventario para gestionar objetos.
- Implementar comercio con NPCs y avanzar en las mecánicas económicas.