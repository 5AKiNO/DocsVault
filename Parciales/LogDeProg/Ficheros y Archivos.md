
INTRODUCCION

Toda persona que haya interactuado con los ordenadores tiene alguna noción de lo que es un fichero o archivo.

Se crean para almacenar, por ejemplo, el texto escrito mediante un editor de textos ( Bloc de Notas, Code::Blocks)

En general, la mayor parte de las aplicaciones necesitan leer datos de ficheros o escribir datos en ficheros para un uso posterior por el mismo u otro programa.

Concepto de fichero
La jerarquía de datos
Podemos establecer una jerarquía para los distintos tipos de datos, organizándolos en diferentes niveles:

Bit: Su valor es 0 o 1. Es la unidad mínima de información.

Byte: 8 bits: Pueden usarse para almacenar caracteres o números pequeños

Campo: Grupo de bytes con un significado, por ejemplo, un nombre de persona, un entero, un real

Registro: Un grupo de campos relacionados. Por ejemplo, los campos nombre, apellidos, edad y DNI pueden ser un registro para describir a una persona en un contexto determinado. En C++, un registro se programa con una clase, class. No programaremos clases en este curso, pero vector<T> es un buen ejemplo de clase que venimos utilizando.

Fichero: Un grupo de campos o registros relacionados.

Base de datos: Un grupo de ficheros relacionados. Hablaremos sobre ellas en la parte de Fundamentos de Informática.

Ficheros
Un fichero o archivo es una colección ordenada de datos que tienen entre sí una relación y que se almacenan de forma permanente en un dispositivo de memoria no volátil.

En este contexto, permanente quiere decir que, salvo fallos catastróficos o hasta que sean borrados a propósito, estos datos permanecen en el medio en que se almacenan (medios magnéticos o de otro tipo) y continúan existiendo después de que el programa que los creó deja de ejecutarse, incluso después de apagar el ordenador.

Esto marca la diferencia con los datos que son provisionalmente almacenados en la memoria RAM, la memoria volátil del ordenador, que no sobreviven al programa que los crea y mucho menos a la desconexión del computador.

Utilidad de los ficheros
El concepto de fichero es una abstracción del Sistema Operativo (S.O.) que, de forma transparente al programador, utiliza los recursos del hardware creando sobre ellos una estructura lógica para representarlos, facilitando a los lenguajes de programación el uso de interfaces de usuario simples y versátiles.

El Sistema Operativo crea todo el sistema de ficheros del ordenador: los directorios para organizarlos, las tablas para localizarlos en el disco, etc.

Los ficheros son enormemente importantes en programación. No sólo debido al hecho evidente de que brindan el soporte que permite la mera existencia de las aplicaciones en el disco duro. Si no existieran los ficheros, por ejemplo, toda la interacción del usuario con una aplicación concreta, como la introducción y la obtención de resultados parciales, tendría que ser laboriosamente recreada cada vez que se ejecutara el programa. La existencia del fichero hace posible que, al terminar una sesión de trabajo, se almacenen los datos y resultados en el disco, para poder retomar la tarea en una sesión posterior.

Por otra parte, los ficheros son útiles como vehículos para el intercambio de información entre diferentes aplicaciones: los datos resultantes escritos en un fichero por el programa A podrán servir como entrada de un programa B. Huelga comentar el masivo sistema de distribución de documentos a través de Internet.

El formato
Un fichero tiene un formato predefinido, conocido de antemano, lo que permite su lectura y/o escritura siguiendo unas pautas preestablecidas.

Ejemplo Para almacenar matrices de números se ha decidido utilizar ficheros que siguen el siguiente formato:

Los dos primeros valores son el tamaño en filas (fil) y columnas (col) de la matriz

A continuación, aparecen en el fichero los fil*col valores de la matriz separados por espacios en blanco (incluidos tabuladores, retornos de línea, etc.)

Por ejemplo, si deseamos almacenar con ese formato la matriz:

⎡⎣⎢135246⎤⎦⎥
[
1
2
3
4
5
6
]
cualquier variante similar a las tres mostradas en la siguiente figura sería válida:

../../_images/ficheros1.jpg
Tres ficheros (Bloc de notas) con el mismo formato de la misma matriz

Otro formato podría utilizar el carácter retorno de línea para diferenciar las filas:

../../_images/ficheros2.jpg
Dos ficheros (Bloc de notas) con el mismo formato de la misma matriz

Lo relevante de estos dos ejemplos es que, para una correcta lectura o escritura de la matriz, el formato del fichero debe ser conocido de antemano.

Un inconveniente del segundo formato es que, cuando se lee el archivo, el tamaño de la matriz no se conoce hasta que se ha completado la lectura.

Los sistemas operativos utilizan la extensión de los ficheros (pdf, docx, ppt, cbp, cpp, etc.) para asociar al proceso de lectura del archivo la aplicación informática adecuada. Y, por supuesto, la aplicación abrirá correctamente el archivo si el formato es el idóneo.



Tipos de ficheros
Como hemos comentado, el contenido y la estructura de un fichero responde a un criterio de diseño libre, elegido por el desarrollador de una aplicación.

En cualquier caso, en relación a la forma en que los datos son almacenados, los ficheros podríamos clasificarlos como:

Ficheros binarios: Contienen una representación exacta del contenido binario de los datos, ceros y unos. Por tanto, no son directamente editables.

Ejemplo: Representación de 3 números enteros int, 255, 3, y 10 en complemento a 2.

¡Cada entero ocupa el mismo número de bytes: 4!

../../_images/fichero_binario.jpg
Fichero binario

Ficheros de texto: Los datos están representados con los caracteres alfanuméricos que los representan. Pueden ser leídos y modificados a través de un editor de texto.

Ejemplo: Representación de 3 números enteros 255, 3 y 10 cuyas cifras están codificadas en ASCII. Los números se separan por un espacio en blanco (20H en ASCII) para poder diferenciarlos.

¡Cada entero ocupa un número de bytes distinto!

../../_images/fichero_texto.jpg
Fichero texto

En este curso trabajaremos con ficheros de texto. Vamos a ver que el trabajo con los ficheros de texto es esencialmente análogo al trabajo con entrada/salida convencional a través del teclado y la pantalla.

Los ficheros binarios son también extremadamente útiles. Una vez comprendido el funcionamiento de los ficheros tipo texto, el alumno que desee ampliar conocimientos no tendrá ninguna dificultad en utilizarlos.


Programación con ficheros
Los S.O. actuales hacen un tratamiento unificado de estos recursos y tratan, por ejemplo, a la pantalla y al teclado como ficheros de salida y de entrada respectivamente, ficheros que están siempre listos para ser utilizados. Es una muestra más del mecanismo de abstracción mencionado anteriormente.

Recalquemos que cuando en C++ usamos cout, estamos escribiendo datos en el fichero por defecto o estándar, la pantalla, y que cuando empleamos cin, estamos leyendo datos del fichero por defecto o estándar, el teclado.

Cuando no usamos los ficheros estándar, tanto en C++ como en cualquier otro lenguaje de programación, debemos realizar algunas tareas adicionales:

Abrir el fichero: hay que asociar el fichero (definido a nivel del S.O.) con un objeto que provea la fuente de datos y definir si se va utilizar para entrada o para salida de datos, es decir, para leer o para escribir.

Cerrar el fichero: una vez finalizada la interacción con el objeto que representa el fichero, este hecho debe ser informado al S.O. mediante los métodos apropiados. Así, el S.O. podrá realizar las acciones requeridas para garantizar que el fichero queda en un estado consistente y seguro.

Nótese que el programador no tiene que preocuparse de la naturaleza física del medio de almacenamiento.

El concepto de flujo de datos (stream)
Las operaciones de lectura/escritura hacen uso del concepto de flujo o corriente de datos (stream). El símil se basa en el hecho de interpretar la entrada/salida como una corriente o río de datos, donde estos son representados por la aparición en serie, uno tras otro, de los bytes que representan cada uno de los valores transferidos.

El concepto de transferencia de datos en serie es clave. Si desde el teclado queremos introducir el número 543, es evidente que antes de escribir el 3, debemos escribir el 4 y antes el 5. En el caso de los ficheros se utiliza el mismo paradigma, se escribe un dato siempre a continuación del anterior.

../../_images/ficheros3.jpg
La naturaleza en serie de los flujos de datos es muy relevante: no se puede acceder de forma directa (random access) a los datos del fichero, como ocurre cuando leemos o escribimos en un elemento de un vector usando el operador de indexación [].

Memoria intermedia (buffers)
La entrada/salida desde/hacia ficheros está mediada, de forma transparente al programador, por el uso de áreas de la memoria RAM, conocidas como búferes (buffers).

Los búferes cumplen distintos cometidos, pero el fundamental es el de servir como pulmón de la CPU. Dado que los procesos de lectura/escritura en los dispositivos son mucho más lentos que los realizados en la RAM, los datos son temporalmente leídos/escritos en búferes. De esta forma, los accesos a un dispositivo lento no ralentizan las aplicaciones.

Además, este método de trabajo reduce los accesos al disco, con el único inconveniente de que una terminación anormal del programa puede provocar la pérdida de los datos.

Finalmente, aunque nosotros no lo vamos a estudiar en la asignatura, una vez que el fichero o parte de él está en un búfer en memoria, podemos utilizar acceso directo a datos intermedios.

Necesidad de cerrar el fichero
Cuando nuestro programa ha terminado de utilizar un fichero debe cerrarlo.

¿Por qué es necesario cerrar el fichero?

La escritura/lectura se realiza sobre los búferes y estos son eventualmente transferidos al medio físico. Cuando se cierra el fichero, se fuerza a realizar esa transferencia. De otro modo, se podría incurrir en pérdida de información.

La utilización de un fichero puede comportar un consumo importante de memoria del ordenador (búferes y otros elementos). Si no se cierra el fichero, esa memoria permanece bloqueada, sin uso, y, por tanto, inutilizada.

El Sistema Operativo establece un número máximo de ficheros que pueden estar abiertos simultáneamente a cargo de una aplicación. Si no cerramos los ficheros que, de momento, no estamos utilizando, puede que nuestro programa no pueda abrir otros que sí son necesarios.


Ficheros en C++ 
Para trabajar con ficheros en C++ debe incluirse la cabecera fstream.

Dependiendo de lo que deseemos hacer con el fichero, usaremos objetos de las clases:

ifstream ( input file stream), clase orientada para la lectura

ofstream (output file stream). clase orientada para la escritura

fstream (file stream), cuando deseemos alternativamente leer o escribir del mismo fichero en el mismo programa.

A diferencia de cin y cout, que son objetos predefinidos de acceso global, listos para su uso, los objetos que representan flujos de datos a/desde ficheros deben ser definidos por el programador.

La apertura del fichero consiste en definir un objeto de la clase deseada (ifstream, ofstream ó fstream).

Para escribir o leer, se usan los operadores de inserción << y extracción >> como si del teclado o consola se tratase.

El fichero se cierra implícitamente cuando el objeto sale del ámbito en el que se ha definido o explícitamente llamando a la función miembro close().

En lo que sigue vamos a ver un pequeño subconjunto de las posibilidades que ofrece C++, y solo para trabajar con ficheros tipo texto.

Para muchos problemas, con las herramientas que aquí se estudian, es más que suficiente.

Escritura de un fichero tipo texto
Ejemplo: escritura en un fichero de los 10 primeros enteros

#include <fstream>  // Para ofstream
#include <iostream> // Para cout
using namespace std;

int main()
{
  ofstream fich("ejemplo.dat");
  if (!fich)
  {
    cout << "Error al abrir ejemplo.dat\n";
    exit(EXIT_FAILURE);
  }

  for (int i = 0; i < 10; ++i)
    fich << i << endl;
}
Analicemos las líneas más significativas:

ofstream fich("ejemplo.dat");

ofstream es una clase que permite crear la instancia fich para escribir en un fichero. En este caso, se crea un fichero para escritura llamado "ejemplo.dat".

Es conveniente saber dónde el IDE va a crear o leer por defecto el archivo. En el caso de Code::Blocks, el directorio por defecto es el del proyecto.

if (!fich){...}

Verificar si se ha creado el objeto fich. Si hay error, el operador ! devuelve true.

exit(EXIT_FAILURE);

En general, y en el marco de la asignatura, en presencia de un error al intentar abrir el fichero, se optará por dar por finalizado el programa. Otra opción podría ser volver a solicitar el nombre del fichero al usuario del programa.

fich << i << endl;

A la hora de trabajar con el fichero, la operativa es idéntica a la que se usa con cout. En este caso, el papel del objeto estándar para la salida cout se sustituye por fich, y los datos, en lugar de dirigirse hacia la consola, se almacenan en el fichero "ejemplo.dat". Nótese que basta sustituir fich por cout para visualizar el aspecto que tendrán en el archivo los datos.

Nótese que no se ha procedido a cerrar el fichero mediante una sentencia del tipo fich.close(). En este ejemplo no es necesario, aunque cerrarlo explícitamente es totalmente legítimo. Lo que ocurre es que cuando cualquier objeto en C++ sale del ámbito en el que se encuentra declarado, una función interna llamada destructor se encarga automáticamente de liberar los recursos que ese objeto haya podido acaparar. En este caso, el destructor de la clase ofstream se encarga de cerrar el fichero, aunque nosotros no lo hayamos hecho.

Lectura de un fichero tipo texto
Ejemplo 2: lectura de un fichero con enteros: Variante 1

En esta variante, se sabe que el fichero tiene números enteros, separados por espacios en blanco, ¡pero no sabemos cuántos!

../../_images/ficheros4.jpg
Fichero utilizado en el ejemplo

#include <fstream>  // Para ifstream
#include <iostream> // Para cout
#include <vector>
using namespace std;

void muestra_vector(const vector<int>&);
int main()
{
  ifstream fich("ejemplo.dat");
  if (!fich.is_open())
  {
    cout << "Error al abrir ejemplo.dat\n";
    exit(EXIT_FAILURE);
  }

  int valor;
  vector<int> datos;
  while (fich >> valor)
    datos.push_back(valor);
  muestra_vector(datos);
}

void muestra_vector(const vector<int>& v)
{
  for (auto x : v)
    cout << x << " ";
  cout << endl;
}
Analicemos las líneas más significativas:

ifstream fich("ejemplo.dat");

ifstream es una clase que permite crear la instancia fich para leer de un fichero. En este caso, se abre un fichero para lectura llamado "ejemplo.dat".

if (!fich.is_open())

Es otra forma similar a !fich para verificar que se ha podido abrir el archivo.

while (fich >> valor){...}

Dado que no sabemos el número de elementos, incluso el archivo puede estar vacío, utilizamos un bucle while.

Cuando el operador de extracción >> llega al final del fichero fich, la operación se evalúa como false, lo que permite salir del bucle.

De nuevo, destacar que el papel que tenía cin en la lectura desde el teclado ahora es asumido por la lectura desde el fichero fich.

Ejemplo 3: lectura de un fichero con enteros: Variante 2

A diferencia del ejemplo anterior, ahora el formato del archivo informa en primer lugar del número de elementos que componen la secuencia de enteros. Esto suele ser una ventaja, dado que nos permite reservar de antemano espacio para nuestro vector.

../../_images/ficheros5.jpg
Fichero utilizado en el ejemplo

#include <fstream>  // Para ifstream
#include <iostream> // Para cout
#include <vector>
using namespace std;
void muestra_vector(const vector<int>&);
int main()
{
  ifstream fich("ejemplo.dat");
  if (!fich.is_open())
  {
    cout <<"Error al abrir ejemplo.dat\n";
    exit(EXIT_FAILURE);
  }
  int num_elementos;
  fich >> num_elementos;
  vector<int> datos;
  datos.reserve(num_elementos);
  for (int i = 0; i < num_elementos; ++i)
  {
    int valor;
    fich >> valor;
    datos.push_back(valor);
  }
  muestra_vector(datos);
}
void muestra_vector(const vector<int>& v)
{
  for (auto x : v)
    cout << x << " ";
  cout << endl;
}
Analicemos las líneas más significativas:

int num_elementos;

fich >> num_elementos;

Leemos el primer dato del archivo que, para este formato, es el número de elementos.

datos.reserve(num_elementos);

Es opcional su uso, pero evitamos tras las bambalinas que vector tenga que ir solicitando al S.O. nuevo espacio en memoria conforme la capacidad del vector se sobrepasa.

for (int i = 0; i < num_elementos; ++i)

Ahora sabemos el número de elementos a leer y, por lo tanto, un bucle for es el más adecuado para esta tarea.

En los dos ejemplos anteriores se ha utilizado un fichero con los datos deliberadamente dispersos, con múltiples e innecesarios espacios en blanco y caracteres nueva línea. El único objetivo es resaltar que, al igual que ocurre con cin, el proceso de extracción ignora este tipo de caracteres. En condiciones normales, lo habitual es utilizar un fichero con alguna de las distribuciones mostradas en la figura.

Ficheros con número de elementos como primer dato
Opción 1

Opción 2

../../_images/ficheros6.jpg
../../_images/ficheros7.jpg
Leyendo ficheros con un formato complejo
Los ejemplos anteriores basados en enteros trabajan con ficheros que poseen una única secuencia de valores.

Las aplicaciones prácticas requieren ser capaces de crear y leer ficheros que tengan una estructura compleja conocida de tamaño arbitrario, con independencia del número de datos que estos ficheros almacenen. En estos ficheros pueden mezclarse comentarios y datos, tanto numéricos como cadenas de caracteres.

Algunos ejemplos entre los innumerables que podrían citarse, pueden ser:

los datos del censo de una ciudad o un país: nombre y apellidos, DNI, dirección y edad de los votantes.

la sucesión de temperaturas recogidas por diferentes sensores en diferentes lugares.

las filas y columnas de una matriz de dimensiones arbitrarias.

Todos los problemas tienen en común que el significado de los datos y la estructura básica de la organización de los mismos tienen que ser conocidos por el programador.

El volumen total de los datos (cantidad de personas, número de lecturas del sensor, dimensiones de la matriz) es, en general, desconocido. Sin embargo, como ya hemos apuntado en un apartado anterior, añadir al formato metadatos suele ser de gran ayuda. El ejemplo sobre el almacenamiento de una matriz visto en un apartado anterior es relevante: el formato incluye inicialmente el número de filas y columnas.

Nos limitaremos en esta asignatura a trabajar con ficheros tipo texto donde los datos de interés están separados por espacios en blanco.

Para ilustrar las dificultades que surgen para ficheros con formatos demasiado complejos, vamos a analizar el aparentemente simple ejemplo siguiente.

Ejemplo 4: lectura de un fichero con cadenas de caracteres

El fichero mostrado en la figura almacena el nombre y apellidos de una serie de personas. En la primera línea, tiene el número de personas almacenadas.

../../_images/ficheros8.jpg
Para la lectura vamos a ensayar el uso de string con la intención de almacenar los nombres y apellidos. Este programa, del que mostramos un extracto, es una variante del ejemplo anterior, cambiando int por string.

Veamos lo que ocurre:

...
int main()
{
  ifstream fich("nombre_apellidos.txt");
  ...

  int num_elementos;
  fich >> num_elementos;
  vector<string> datos;
  datos.reserve(num_elementos);
  for (int i = 0; i < num_elementos; ++i)
  {
    string valor;
    fich >> valor;
    datos.push_back(valor);
  }
  muestra_vector(datos);
}
Como era de esperar, no se produce el resultado deseado. El programa sólo ha sido capaz de almacenar en el vector los valores {Enrique, López, Beneito}. No debemos olvidar que el operador de extracción >> procesa el flujo de datos entre dos caracteres distintos que espacios en blanco. Los espacios en blanco, incluido el carácter nueva línea, son ignorados. Desde la óptica del operador de extracción >> el fichero en realidad tiene 13 datos, 13 cadenas de caracteres.

Una solución para este problema es usar la función getline() de la biblioteca string, que permite extraer de un fichero bloques de texto, por ejemplo, correspondientes a líneas.

En general, cuando de un fichero se necesitan extraer cadenas de caracteres que incluyen espacios en blanco, como apellidos compuestos, tipo de la Torre, o valores separados por comas, etc. el análisis (parsing) del texto da lugar a código relativamente complejo y que no merece la pena estudiar en un curso básico.

Veamos algún ejemplo de formato de archivo complejo más simple y no por ello menos útil.

Ejemplo 5: Clasificación de pilotos

Se dispone de un fichero con nombre «pilotos_y_clasificaciones.txt» que almacena las clasificaciones de los pilotos de una competición automovilística.

El formato es siguiente:

en la 1ª línea se almacena el número de carreras disputadas

en la 2ª línea el número total de pilotos

a partir de las dos primeras líneas, aparecen grupos de 2 líneas:

una con el nombre del piloto

otra con los puestos conseguidos, separados por un espacio, en las carreras disputadas hasta el momento. Un 0 en la línea de puestos significa que el piloto no finalizó la carrera.

En un fichero inicial, con 0 carreras disputadas, las líneas con los puestos no aparecen.

El orden de los pilotos en el fichero no es relevante.

El objetivo es obtener la puntuación actual de cada uno de los pilotos. El sistema de puntuación en cada carrera es {10,8,6,5,4,3,2,1}, siendo 10 la puntuación conseguida por el piloto que acaba en la 1ª posición, 8 puntos la del que acaba en 2ª posición y así hasta 1 punto para el piloto que finaliza en 8ª posición. Por tanto, el resto de pilotos no consiguen puntos.

En la tabla se representan dos ejemplos del fichero en dos situaciones: la inicial y otra con 4 carreras disputadas.

Pilotos y clasificaciones
Sin carreras disputadas

4 carreras disputadas

../../_images/ficheros9.jpg
../../_images/ficheros10.jpg
Aunque C++ permite formas más compactas y eficientes de resolver este problema, nos contentaremos con obtener dos vectores:

uno con las cadenas de caracteres correspondientes a los pilotos

otro con sus puntuaciones acumuladas, en posiciones correlativas a la de los pilotos

Para ello utilizaremos una función con prototipo:

void puntuacion(vector<string>& pilotos, vector<int>& puntos, string nombre_fichero);

Dado que el fichero contiene los puestos conseguidos y no las puntuaciones, utilizaremos una función con prototipo:

int calcula_puntuacion(const vector<int>& puestos);

que nos permita obtener la puntuación a partir de los puestos.

Una posible implementación es la que sigue:

#include <fstream>  // Para ifstream
#include <iostream> // Para cout
#include <vector>
using namespace std;

void puntuacion(vector<string>& pilotos, vector<int>& puntos, string nombre_fichero);
int calcula_puntuacion(const vector<int>& puestos);
void muestra_puntuacion(const vector<string>&, const vector<int>&);

int main()
{
  vector<string> pilotos;
  vector<int> puntos;
  puntuacion(pilotos, puntos, "pilotos_clasificaciones.txt");
  muestra_puntuacion(pilotos, puntos);
}

void puntuacion(vector<string>& pilotos, vector<int>& puntos, string nombre_fichero)
{
  ifstream fich(nombre_fichero);
  if (!fich.is_open())
  {
    cout <<"Error al abrir " << nombre_fichero << "\n";
    exit(EXIT_FAILURE);
  }

  int num_carreras;
  fich >> num_carreras;
  int num_pilotos;
  fich >> num_pilotos;

  pilotos.clear();  // Por si vienen con datos a la función
  puntos.clear();

  for (int i = 0; i < num_pilotos; ++i)
  {
    string piloto;
    fich >> piloto;
    pilotos.push_back(piloto);
    vector<int> puestos;
    for (int j = 0; j < num_carreras; ++j)
    {
      int puesto;
      fich >> puesto;
      puestos.push_back(puesto);
    }
    puntos.push_back(calcula_puntuacion(puestos));
  }
}


int calcula_puntuacion(const vector<int>& puestos)
{
  const vector<int> puntos{10,8,6,5,4,3,2,1};

  int suma = 0;
  for (auto puesto : puestos)
    if (puesto > 0 && puesto < puntos.size() + 1)
      suma += puntos[puesto - 1];
  return suma;
}

void muestra_puntuacion(const vector<string>& pilotos, const vector<int>& puntos)
{
  cout << "\nLa puntuación actual es:\n\n";
  for (int i = 0; i < pilotos.size(); ++i)
    cout << pilotos[i] << " " << puntos[i] << endl;
  cout << endl << endl;
}
Es importante tener claro que la lectura de un fichero es secuencial. Si los datos del fichero hubiesen sido introducidos por teclado, bastaría sustituir fich >> ... por cin >> .... La única diferencia es que cuando se introducen los datos por teclado, previamente se muestra un mensaje con cout al usuario indicando qué valor debe introducir. En el caso de un fichero, donde se presupone que el programador conoce el formato del fichero, esta información que aporta el cout es implícita.

Modos de apertura
En todos los ejemplos previos hemos utilizado los modos de apertura de un fichero por defecto.

La clase ofstream por defecto crea ficheros tipo texto para escritura. Si el fichero existe, equivale a su borrado previo.

La clase ifstream por defecto abre ficheros tipo texto para lectura. Si el fichero no existe, se generará un error.

C++ permite especificar explícitamente otros modos (flags) de apertura. Están definidos en el espacio de nombres ios. Algunos de ellos son:

ios:: binary: El fichero será binario

ios:: in: Fichero modo lectura

ios:: out: Fichero modo escritura

ios:: app: Fichero en modo añadir (append)

De entre estos modos, nos interesa el modo ios:: app. Este modo permite añadir datos al final de un fichero ya existente y, por tanto, no se pierden los datos anteriores.

Este modo es muy interesante porque permite trabajar en modo escritura con un fichero en diferentes sesiones. Un posible uso del modo añadir sería ofstream fich(nombre_fichero, ios::app);.

Veamos un ejemplo.

Ejemplo 6: Añadir a un fichero números enteros

#include <fstream>  // Para ofstream
#include <iostream> // Para cout
using namespace std;

void guarda_entero(int valor, string nombre_fichero);
int main()
{
  for (int i = 0; i < 10; ++i)
    guarda_entero(i, "ejemplo.txt");
}

void guarda_entero(int valor, string nombre_fichero)
{
  ofstream fich{nombre_fichero, ios::app};
  if (!fich)
  {
    cout << "Error al abrir " << nombre_fichero << endl;
    exit(EXIT_FAILURE);
  }
  fich << valor << endl;
}
Nótese que en cada llamada a guarda_valor() se abre y cierra el fichero: la bandera ios::app permite que el contenido anterior del fichero no se pierda.

Ejemplo 
Listado de notas
Descripción del programa
Con el programa se desea realizar una sencilla aplicación que permita a un profesor almacenar en un fichero el DNI de los alumnos y sus notas en un examen.

El formato del fichero es:

DNI1 Nota1

DNI2 Nota2

…

El campo DNI será un string, como por ejemplo 13132654A y el campo Nota un double, como por ejemplo 6.7.

En definitiva, el formato consiste en una sucesión alternada de campos string y double separados por espacios en blanco.

Como es lógico, la aplicación permitirá ser utilizada en diferentes instantes de tiempo. Por ello, cada vez que el profesor introduzca una nueva nota:

se abrirá el fichero con las notas ya introducidas

añadirá la nueva nota a las ya existentes

salvará a disco cerrando el fichero

Además de almacenar las notas, el programa permitirá calcular alguna propiedad estadística simple de las notas introducidas hasta ese momento. En el ejemplo, la peor nota, la mejor y la media.

El programa no verificará la validez del DNI. Una aplicación comercial lo haría. Tampoco comprueba si el DNI de un alumno ya se encuentra almacenado y, por tanto, o el profesor ha cometido un error o quizás desea alterar la nota.

La aplicación exigirá que la nota esté en el intervalo [0,10].

Diseño del programa
El programa comienza solicitando el nombre del fichero donde se almacenan alumnos y notas.

Un menú permitirá elegir entre 2 opciones:

Introducir nueva nota

Se abrirá el fichero para escritura usando el modo ios::app. Así podremos añadir la nueva nota al final del mismo.

Calcular estadísticas

Se abrirá el fichero para lectura

Los prototipos de las funciones son los siguientes:

Introducción del nombre del fichero:

string introduce_nombre_fichero();
Menú con las opciones:

Salir del programa

Introducir nota

Listado y estadísticas

int menu();
Introducción de una nota

void introduce_nota(const string& nom_fich);
Listado y estadísticas

void calcula_estadisticas(const string& nom_fich);
Esta función invocará a otra que lee el fichero y carga en dos vectores los DNI y las notas. Para ello se usará una función con prototipo:

void lee_notas(const string& nom_fich, vector<string>& dnis,
               vector<double>& notas);
Para mostrar por pantalla los resultados, se utilizará una función con signatura:

void listado(const vector<string>& dnis, const vector<double>& notas,
             size_t indice_minima, size_t indice_maxima, double media);
La función introduce_nombre_fichero()
Se limita a devolver un string con el nombre del fichero.

string introduce_nombre_fichero()
{
   cout << "Nombre con extension del fichero de notas: ";
   string nombre_fichero;
   cin >> nombre_fichero;
   return nombre_fichero;
}
La función menu()
A estas alturas del curso, esta función no tiene mayor misterio. Una posible implementación es:

int menu()
{
   int opcion;
   do
   {
      cout << "Pulse 0 para salir del programa\n"
           << "Pulse 1 para introducir nota\n"
           << "Pulse 2 para listado y estadísticas\n";
      cin >> opcion;
   }
   while (opcion < 0 || opcion > 2);
   return opcion;
}
La función introduce_nota()
La función abre el fichero en modo escritura y para añadir datos. Tras solicitar el DNI y la nota, estos añaden al final del fichero.

void introduce_nota(const string& nombre_fichero)
{
   cout << "DNI con letra de control del alumno: ";
   string dni;
   cin >> dni;
   double nota;
   do
   {
      cout << "Nota(0 al 10): ";
      cin >> nota;
      if (nota < 0 || nota > 10)
         cout << "\n\nERROR: La nota no es válida.\n\n";
   }while (nota < 0 || nota > 10);

   ofstream fichero(nombre_fichero, ios::app);
   if (!fichero)
   {
      cout << "Error, "<< nombre_fichero
           << " no pudo abrirse para escritura.\n";
      exit(EXIT_FAILURE);
   }
   fichero << dni << " " << nota << endl;
}
Nótese el uso del modo ios::app. Para respetar el formato, en la línea:

fichero << dni << " " << nota << endl;

se separan el DNI y la nota por un espacio en blanco, " " y se introduce una nueva línea, endl.

La función lee_notas()
La función pasa por referencia los vectores donde se almacenarán los DNI y las notas. Dado que el formato no informa del número de alumnos, se usa un bucle while para la lectura.

void lee_notas(const string& nombre_fichero, vector<string>& dnis, vector<double>& notas)
{
   ifstream fichero(nombre_fichero);
   if (!fichero)
   {
      cout << "Error, "<< nombre_fichero
           << " no pudo abrirse para lectura.\n";
      exit(EXIT_FAILURE);
   }

   string dni;
   while (fichero >> dni)
   {
      dnis.push_back(dni);
      double nota;
      fichero >> nota;
      notas.push_back(nota);
   }
}
La condición de salida del bucle while es fichero >> dni, dado que cuando se llegue al final del fichero es el primer dato que al intentar ser leído dará error.

La función listado()
Es la función encargada de mostrar los resultados. Se ha usado el tipo size_t pero hubiese sido perfectamente válido utilizar int.

void listado(const vector<string>& dnis, const vector<double>& notas,
             size_t indice_minima, size_t indice_maxima, double media)
{
   cout << "******************************************\n";
   for (size_t i = 0; i < dnis.size(); ++i)
      cout << dnis[i] << " " << notas[i] << endl;

   cout << "******************************************\n";
   cout << "Nota minima: " << dnis[indice_minima]
      << " con nota " << notas[indice_minima] << endl;
   cout << "Nota maxima: " << dnis[indice_maxima]
      << " con nota " << notas[indice_maxima] << endl;
   cout << "Nota media: " << media << endl;
   cout << "******************************************\n";
}
La función calcula_estadisticas()
Tras leer el fichero y crear los vectores de DNI y notas, se verifica que el fichero no estaba vacío. Posteriormente se calculan las estadísticas y, finalmente, se listan por pantalla.

void calcula_estadisticas(const string& nombre_fichero)
{
   vector<string> dnis;
   vector<double> notas;
   lee_notas(nombre_fichero, dnis, notas);

   if (dnis.empty())
   {
      cout << "\n\nEl fichero esta vacío.\n\n";
      return;
   }

   size_t indice_minima = 0, indice_maxima = 0;
   double nota_minima = notas[0];
   double nota_maxima = notas[0];
   double media = 0.;

   for (size_t i = 0; i < dnis.size(); ++i)
   {
      if (notas[i] < nota_minima)
      {
         nota_minima = notas[i];
         indice_minima = i;
      }
      else if (notas[i] > nota_maxima)
      {
         nota_maxima = notas[i];
         indice_maxima = i;
      }
      media += notas[i];
   }
   media /= dnis.size();

   listado(dnis, notas, indice_minima, indice_maxima, media);
}
La función main()
Nótese como el uso de funciones hace que, con un simple vistazo, la función main() nos apunte claramente el objeto y la estructura del programa.

int main()
{
   string nombre_fichero = introduce_nombre_fichero();
   while (int opcion = menu())
      if(opcion == 1)
         introduce_nota(nombre_fichero);
      else
         calcula_estadisticas(nombre_fichero);
}

extraído de  UVA-Escuela de ingenierías industriales- fundamentos de la programación en c++
© Copyright 2020, Fundamentos de Programación
fuente: https://www2.eii.uva.es/fund_inf/cpp/temas/10_ficheros/ejemplos.html
fin
