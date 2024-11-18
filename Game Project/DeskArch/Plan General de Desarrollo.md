### **"Wander the Echoes of Forgotten Roads"**
Este documento contiene el plan general para el desarrollo de tu juego, estructurado en tres fases clave: prototipo, desarrollo de mecánicas centrales, y la expansión final del contenido narrativo y del juego. Cada una de estas fases está diseñada para guiar paso a paso en el proceso de creación, con instrucciones claras y detalladas, permitiéndote avanzar sin depender de asistencia adicional.

Para obtener los detalles específicos de cada fase, revisa los archivos correspondientes:

- [**Fase 1 - Prototipo y Fundamentos Iniciales**](Fase1.md)
- [**Fase 2 - Desarrollo de Mecánicas Centrales y Profundización de la Narrativa**](Fase2.md)
- [**Fase 3 - Expansión y Perfeccionamiento del Contenido del Juego**](Fase3.md)

---

### **Introducción al Proyecto**

**"Wander the Echoes of Forgotten Roads"** es un juego de género realista steampunk que se jugará en **desktop Arch Linux**. El juego se desarrollará en **C++ sin makefile**, con una estructura sólida y modular que facilitará la expansión a lo largo de sus diferentes fases.

El juego incluirá un **mapa ASCII** interactivo, donde el jugador podrá **moverse**, **luchar contra mobs hostiles y no-hostiles**, y **conseguir objetos**. Estos objetos podrán ser gestionados a través de un sistema de **inventario completo** y un **mercado** que permitirá el intercambio de ítems con NPCs. Además, contará con una **narrativa estilo MUD**, totalmente offline, escalonada y distribuida en diferentes capas, tanto en los diálogos, como en los ítems y las descripciones de las áreas del juego.

---

### **Narrativa Escalonada y Expansión del Lore**

La narrativa del juego está diseñada para desarrollarse en diferentes capas, añadiendo profundidad y riqueza a medida que el jugador interactúa con el mundo. Este estilo de narrativa escalonada es clave para crear una inmersión profunda en el universo steampunk del juego.

#### **Capas Narrativas**

- **Capa 1**: Describe de forma sencilla los elementos básicos del entorno y los personajes que el jugador encuentra. Esta capa está presente desde el comienzo y proporciona la base del juego.
- **Capa 2**: Se desbloquea a medida que el jugador progresa en el juego, revelando más detalles del mundo y profundizando en las historias que se esconden tras cada objeto, personaje o área.
- **Capa 3**: Explora el trasfondo del lore y la historia, vinculando los eventos actuales del juego con la mitología del mundo, las relaciones entre personajes, y la historia oculta en los objetos. No afecta directamente al gameplay, pero añade una rica capa de significado a todo lo que el jugador encuentra.

Este enfoque narrativo es similar al utilizado en el proyecto **CyberCodeOnline**, del cual se toma como referencia su integración de historias en los objetos y su capacidad para profundizar en el lore sin interferir directamente con la jugabilidad.

---

### **Mapa ASCII y Exploración**

El mapa ASCII es uno de los elementos más característicos del juego, no solo por su estética minimalista, sino por su capacidad de representar un mundo amplio y lleno de posibilidades sin necesidad de gráficos complejos. El jugador podrá explorar libremente, descubriendo nuevas áreas, enemigos, y objetos que desbloquean fragmentos adicionales de la narrativa escalonada.

A medida que el jugador avanza y regresa a lugares previamente visitados, las descripciones del mapa también evolucionan, añadiendo detalles sobre los cambios en el entorno, la presencia de nuevos personajes, o las repercusiones de las acciones pasadas del jugador.

---

### **Sistema de Inventario y Comercio**

El inventario es un elemento clave en la progresión del jugador, permitiendo la gestión de los objetos que se encuentran en el mundo. Los ítems tendrán descripciones narrativas que añaden contexto e historia a cada objeto, enriqueciendo la experiencia del jugador. Algunos de estos ítems también tendrán un valor práctico, mejorando las capacidades de combate o proporcionando efectos especiales.

El **sistema de comercio con NPCs** permitirá al jugador intercambiar objetos, crear nuevas relaciones con personajes, y obtener equipo o recursos adicionales para continuar su aventura.

El diseño modular del inventario y del sistema de comercio te permitirá expandir fácilmente el catálogo de ítems y la interacción con los NPCs en fases posteriores del desarrollo.

---

### **Filosofía del Desarrollo Modular**

El proyecto está diseñado de forma modular, lo que permitirá añadir nuevas funcionalidades sin complicaciones a medida que avances en el desarrollo. La estructura clara y organizada del código facilita la expansión del juego, permitiendo añadir nuevas mecánicas, objetos, y capas narrativas en el futuro sin afectar el núcleo del juego.

Esta filosofía permitirá trabajar de manera autónoma y estructurada, teniendo siempre una base sólida y bien fundamentada para cada nueva fase del desarrollo.
