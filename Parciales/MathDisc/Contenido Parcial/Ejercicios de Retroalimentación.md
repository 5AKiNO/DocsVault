#### I) Encierra en círculo la letra que antecede a la respuesta correcta
1) Dado los conjuntos $A = \{1,2,3,4\}$ y $B = \{3,4,5,6\}$, ¿cuál es el resultado de la intersección $A \cap B$?
- a) $\{1,2,3,4,5,6\}$
- **b) $\{3,4\}$ (Respuesta correcta)
- c) $\{1,2\}$
- d) $\{5,6\}$

2) Si $A = \{x \mid x \text{ es un número par menor que 10}\}$ y $B = \{x \mid x \text{ es un múltiplo de 3 menor que 10}\}$, ¿cuál es la unión $A \cup B$?
- **a) $\{2,4,6,8,3,9\}$ (Respuesta correcta)
- b) $\{3,6,9\}$
- c) $\{2,4,8\}$
- d) $\{1,2,3,4,5,6,7,8,9\}$

3) Dado $A = \{2,4,6\}$ y $B = \{4,6,8\}$, ¿cuál es el complemento de $A$ con respecto a $B$, es decir, $B - A$?
- a) $\{2,6\}$
- **b) $\{8\}$ (Respuesta correcta)
- c) $\{4,6\}$
- d) $\{2,4\}$

4) Si $A = \{1,2,3,4,5\}$ y $B = \{3,4,5,6,7\}$, ¿cuál es la diferencia simétrica $A \Delta B$?
- **a) $\{1,2,6,7\}$ (Respuesta correcta)
- b) $\{3,4,5\}$
- c) $\{1,2,3,6,7\}$
- d) $\{1,6\}$

5) ¿Cuál de los siguientes conjuntos está escrito por extensión?
- a) $A = \{x \mid x \text{ es un número impar menor que 10}\}$
- **b) $B = \{2,4,6,8,10\}$ (Respuesta correcta)
- c) $C = \{x \mid x \text{ es una vocal en el alfabeto español}\}$
- d) $\{x \mid x \text{ es un número par mayor que 5 y menor que 11}\}$

6) ¿Cuál de los siguientes conjuntos está correctamente representado por comprensión y por extensión?
- **a) Comprensión: $A = \{x \mid x \text{ es un número primo menor que 10}\}$, Extensión: $A = \{2,3,5,7\}$ (Respuesta correcta)
- b) Comprensión: $B = \{x \mid x \text{ es un múltiplo de 2 mayor que 10 y menor que 20}\}$, Extensión: $B = \{11,13,15,17\}$
- c) Comprensión: $C = \{x \mid x \text{ es un número impar mayor que 20 y menor que 30}\}$, Extensión: $C = \{22,24,26,28\}$
- d) Comprensión: $D = \{x \mid x \text{ es un número mayor que 5 y menor que 10}\}$, Extensión: $D = \{5,6,7,8,9\}$

7) Dada la función $f: \mathbb{R} \to \mathbb{R}$, definida como $f(x) = 2x + 3$, ¿cuál de las siguientes afirmaciones es correcta sobre esta función?
- a) La función es inyectiva pero no sobreyectiva.
- b) La función es sobreyectiva pero no inyectiva.
- **c) La función es biyectiva.** (Respuesta correcta)
- d) La función no es inyectiva ni sobreyectiva.

8) ¿Cuál de las siguientes funciones es sobreyectiva?
- a) $f: \mathbb{R} \to \mathbb{R}, \ f(x) = x^2$
- b) $f: \mathbb{R} \to \mathbb{R}, \ f(x) = \frac{1}{x}$
- c) $f: \mathbb{R} \to \mathbb{R}^+, \ f(x) = e^x$
- **d) $f: \mathbb{R} \to \mathbb{R}, \ f(x) = x^3$ (Respuesta correcta)

9) La expresión $\frac{x-2}{x^3+8}$ no está definida para $x$ igual a:
- a) $0$
- b) $2$
- c) $-8$
- **d) $-2$ (Respuesta correcta)
- e) $4$

#### II) Simboliza las siguientes proposiciones

1) No vi la película, pero leí la novela:
   - $\neg p \land q$

2) Ni vi la película ni leí la novela:
   - $\neg p \land \neg q$

3) No es cierto que viese la película y leyese la novela:
   - $\neg (p \land q)$

4) Si hay verdadera democracia, entonces no hay detenciones arbitrarias ni otras violaciones de los derechos civiles:
   - $p \to (\neg q \land \neg r)$

5) No es cierto que no me guste Matemática:
   - $\neg (\neg p)$, es decir, $p$

6) Si y sólo si viera un marciano con mis propios ojos, creería que hay vida extraterrestre:
   - $p \leftrightarrow q$

7) Si los elefantes volaran o supieran tocar el acordeón, pensaría que estoy como una regadera y dejaría que me internaran en un psiquiátrico:
   - $(p \lor q) \to (r \land s)$

#### III) Tabla de verdad y determinación de tautología, contradicción o contingencia

Dada la proposición $(p \land \neg r) \leftrightarrow [q \lor \neg (\neg r \to p)]$, construimos su tabla de verdad:

| $p$ | $q$ | $r$ | $\neg r$ | $p \land \neg r$ | $\neg r \to p$ | $\neg (\neg r \to p)$ | $q \lor \neg (\neg r \to p)$ | $(p \land \neg r) \leftrightarrow [q \lor \neg (\neg r \to p)]$ |
| --- | --- | --- | -------- | ---------------- | -------------- | --------------------- | ---------------------------- | --------------------------------------------------------------- |
| V   | V   | V   | F        | F                | V              | F                     | V                            | V                                                               |
| V   | V   | F   | V        | V                | V              | F                     | V                            | V                                                               |
| V   | F   | V   | F        | F                | V              | F                     | F                            | V                                                               |
| V   | F   | F   | V        | V                | V              | F                     | F                            | V                                                               |
| F   | V   | V   | F        | F                | F              | V                     | V                            | V                                                               |
| F   | V   | F   | V        | F                | V              | F                     | V                            | V                                                               |
| F   | F   | V   | F        | F                | F              | V                     | F                            | V                                                               |
| F   | F   | F   | V        | F                | V              | F                     | F                            | V                                                               |

**Conclusión**: La expresión es una **tautología**.

#### IV) Programa de radio favorito

### Datos:
- 16 personas escuchan deportes.
- 18 personas escuchan teatro.
- 15 personas escuchan noticias.
- 7 personas escuchan deportes y teatro.
- 5 personas escuchan teatro y noticias.
- 6 personas escuchan deportes y noticias.
- 3 personas escuchan los tres programas.

##### a) ¿Cuántas personas escuchan los deportes o el teatro y no las noticias?
$(Deportes \cup Teatro) \cap \neg Noticias = 22$

##### b) ¿Cuántas personas escuchan solamente el teatro?
$Solo \, Teatro = 9$

### c) ¿Cuántas personas escuchan sólo las noticias?

$Solo \, Noticias = 7$

### d) ¿Cuántas personas escuchan dos clases de programas y no tres?

$Dos \, Programas = 9$

### e) ¿Cuántas personas han sido interrogadas en total?

$Total = 34$