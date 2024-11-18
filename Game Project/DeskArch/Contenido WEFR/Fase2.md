En la **Fase 2**, el enfoque es ampliar las funcionalidades del prototipo inicial, añadiendo elementos clave para hacer el juego más complejo y profundo. Esto incluye el **sistema de combate**, un **inventario interactivo**, y la ampliación de la **narrativa escalonada**.

---

### **Objetivo de la Fase 2**

- Desarrollar las **mecánicas centrales** del juego: combate, inventario, y comercio básico.
- **Profundizar** la narrativa escalonada introducida en la Fase 1, ampliando las descripciones y el trasfondo del mundo a medida que el jugador avanza.
- Mantener la estructura clara y organizada del proyecto, permitiendo fácil expansión en fases posteriores.

---

### **Componentes Fundamentales de la Fase 2**

#### **1. Sistema de Combate Básico**

**Fundamentación:**
- El combate es una parte crucial del progreso del jugador. Este sistema debe ser simple inicialmente, pero lo suficientemente flexible para que puedas añadir complejidad (habilidades, tipos de enemigos, etc.) en el futuro.
- El jugador debe enfrentarse a **mobs hostiles** y tener la posibilidad de atacar, defenderse, o escapar.
  
**Funcionalidad Mínima:**
- **Encuentros Aleatorios**: En ciertas partes del mapa, el jugador se encontrará con enemigos. Estos encuentros pueden ser activados al azar o al ingresar a ciertas áreas.
- **Acciones Básicas de Combate**:
  - **Atacar**: El jugador puede atacar a los enemigos con armas básicas. Inicialmente, el combate se puede resolver con un intercambio simple de puntos de daño.
  - **Defenderse o Huir**: El jugador puede intentar evadir el combate o minimizar el daño recibido.
- **Estadísticas de Combate**:
  - Cada enemigo y el jugador tienen estadísticas como `salud` y `ataque`. Los encuentros deben actualizar estas estadísticas en función de las acciones realizadas.

**Narrativa Escalonada en el Combate**:
- **Capa 1 (Básica)**: Cuando el jugador entra en combate, la narrativa describe de forma simple al enemigo y el entorno del enfrentamiento.
  - Ejemplo: *"Un enemigo emerge de entre las sombras. Su mirada es fría y mortal."*
  
- **Capa 2 (Avanzada)**: Si el jugador derrota al enemigo o si interactúa con el entorno tras el combate, nuevas capas de la narrativa se desbloquean. Ejemplo:
  - *"Tras la batalla, encuentras una nota arrugada en el suelo. Las palabras son crípticas, pero mencionan un lugar lejano y olvidado."*

---

#### **2. Sistema de Inventario**

**Fundamentación:**
- El inventario permite al jugador gestionar los objetos que encuentra o compra, mejorando así su capacidad de supervivencia y progresión en el juego.
- En esta fase, el inventario debe permitir al jugador recoger, usar y equipar ítems. Los objetos pueden incluir armas, consumibles, y artefactos con historias propias.

**Funcionalidad Mínima:**
- **Recolección de Ítems**: El jugador debe poder recoger ítems tras derrotar enemigos o al explorar el mapa. Estos ítems se almacenan en el inventario.
- **Gestión de Inventario**: El jugador puede visualizar, seleccionar, y usar o equipar los objetos.
- **Tipos de Ítems**:
  - **Armas**: Para mejorar las estadísticas de combate del jugador.
  - **Consumibles**: Ítems que restauran salud o proporcionan otros efectos temporales.
  - **Objetos Narrativos**: Algunos ítems tendrán historias integradas que añaden profundidad al mundo del juego.

**Narrativa en el Inventario**:
- Cada ítem del inventario puede tener una pequeña descripción narrativa que añada contexto, similar a **CyberCode Online**. Esto no necesariamente afectará la jugabilidad, pero enriquecerá la inmersión.
  - Ejemplo: *"Este amuleto de metal oxidado pertenecía a un cazador olvidado. Aunque parece inofensivo, su presencia te causa inquietud."*

---

#### **3. Comercio con NPCs**

**Fundamentación:**
- El comercio introduce una mecánica económica donde el jugador puede intercambiar ítems con NPCs en ciertas áreas del mapa, permitiendo obtener recursos adicionales o mejorar su equipo.
  
**Funcionalidad Mínima:**
- **NPCs Comerciales**: En el mapa, habrá NPCs dedicados al comercio. El jugador podrá interactuar con ellos para comprar y vender ítems.
- **Economía Básica**: Cada ítem tendrá un valor asociado, y el jugador necesitará administrar sus recursos para decidir qué comprar o vender.
- **Interfaz de Comercio**: El jugador debe poder seleccionar ítems de su inventario para vender, o elegir ítems del NPC para comprar.

**Narrativa Escalonada en el Comercio**:
- **Capa 1 (Funcional)**: Cuando el jugador interactúe con un comerciante, la narrativa describirá el NPC y su entorno.
  - Ejemplo: *"El comerciante parece nervioso, sus ojos siempre vigilando los alrededores. 'Tengo lo que necesitas, pero no será barato.'"*
  
- **Capa 2 (Opcional)**: Si el jugador realiza varias transacciones o regresa al mismo comerciante, la narrativa puede profundizar en la relación con el NPC o revelar detalles adicionales sobre el mundo.
  - Ejemplo: *"Después de algunos intercambios, el comerciante se relaja un poco. 'Hay más cosas en este mundo que dinero y espadas, forastero. ¿Has oído hablar de la reliquia de los Tres Reinos?'"*

---

#### **4. Expansión de la Narrativa Escalonada**

**Fundamentación:**
- En la Fase 2, se amplía la narrativa escalonada introducida en la Fase 1. A medida que el jugador avanza en el juego, las descripciones deben volverse más complejas y ricas en detalles.
  
**Narrativa Escalonada Avanzada**:
- **Capa 2 (Detalles Contextuales)**: Cada área del mapa debe tener una descripción más detallada cuando el jugador regrese por segunda o tercera vez, o después de ciertas interacciones. Ejemplo:
  - En un camino por segunda vez: *"El sendero que antes parecía inofensivo ahora está cubierto de huellas recientes. Alguien o algo ha pasado por aquí, y no está solo."*
  
- **Interacciones Narrativas Avanzadas**:
  - Las interacciones del jugador con NPCs, enemigos, o ítems pueden desbloquear fragmentos de la historia que antes no estaban disponibles. Esto puede incluir notas, cartas, o diálogos adicionales con NPCs.
  
**Ampliación del Lore en Objetos**:
- Los ítems del inventario no solo tienen descripciones funcionales, sino también detalles narrativos más profundos que aportan al lore del mundo.
  - Ejemplo: *"Esta espada parece normal, pero se dice que perteneció a un caballero que enfrentó a las fuerzas del caos en la Batalla de Haverstock. Ahora solo quedan leyendas, pero algunos creen que la hoja aún alberga magia oscura."*

---

### **5. Expansión de la Estructura del Proyecto**

A medida que introduces nuevas funcionalidades, es importante mantener la estructura del código clara y modular, lo que te permitirá continuar desarrollando sin problemas.

**Estructura del Proyecto Ampliada:**

```
Wander_the_Echoes_of_Forgotten_Roads/
├── src/
│   ├── main.cpp               // Punto de entrada del juego
│   ├── Map.cpp                // Mapa del mundo
│   ├── Player.cpp             // Lógica del jugador
│   ├── Combat.cpp             // Sistema de combate
│   ├── Inventory.cpp          // Manejo del inventario
│   ├── NPC.cpp                // Lógica de los NPCs y comercio
│   ├── Narrative.cpp          // Manejo de la narrativa escalonada
├── include/
│   ├── Map.h                  // Declaraciones de la clase Map
│   ├── Player.h               // Declaraciones de la clase Player
│   ├── Combat.h               // Declaraciones para el combate
│   ├── Inventory.h            // Declaraciones para el inventario
│   ├── NPC.h                  // Declaraciones de NPCs
│   ├── Narrative.h            // Declaraciones para la narrativa
├── assets/                    // Archivos de texto para descripciones narrativas y diálogos
└── README.md                  // Documentación actualizada sobre el proyecto
```

---

### **Conclusión de la Fase 2**

Al completar esta fase, habrás implementado:
- Un **sistema de combate** básico que te permitirá avanzar y expandirlo con nuevas mecánicas.
- Un **sistema de inventario** funcional y flexible, con la posibilidad de añadir más tipos de ítems y sus respectivas narrativas.
- Un **sistema de comercio** con NPCs que permite la interacción económica.
- La **expansión de la narrativa escalonada**