<pre>

	<p align=center>

Tecnológico Nacional de México
Instituto Tecnológico de Tijuana

Departamento de Sistemas y Computación
Ingeniería en Sistemas Computacionales

Semestre:
Agosto - Diciembre 2023

Materia:
Lenguajes de interfaz

Docente:
M.C. Rene Solis Reyes 

Unidad:
3

Título del trabajo:
Trabajos U3

Estudiante:
Eduardo Alberto Garcia Pineda 20212407

</p>

# 1.1 Los componentes básicos de una computadora personal

Componentes esenciales de una computadora y cómo interactúan entre sí:

La placa madre actúa como el sistema nervioso central y circulatorio, conectando todos los demás componentes para permitir el flujo de datos. La CPU procesa las entradas de dispositivos como teclado y ratón, con su velocidad medida por un reloj interno. Los núcleos dentro de la CPU ejecutan instrucciones, y la memoria (RAM) almacena datos temporalmente. Para almacenamiento a largo plazo, se utilizan discos duros o unidades de estado sólido. El ROM contiene instrucciones básicas y no se puede cambiar fácilmente, pero retiene su contenido sin energía.

# 1.2 La función y el propósito de una CPU y algunos de sus componentes

Las primeras computadoras eran dispositivos de gran tamaño, como el que ocupaba 1800 pies cuadrados o 167 metros cuadrados. El concepto de una unidad central de procesamiento (CPU) surgió en la década de 1960 con la miniaturización gracias a transistores e circuitos integrados. La CPU realizaba funciones de interpretación de instrucciones y procesamiento de datos, aunque es importante destacar que no pueden pensar, solo ejecutan instrucciones.

En la década de 1970, surgieron las CPUs comerciales, llamadas microprocesadores, como circuitos integrados únicos. La CPU consta de una unidad de control (CU) que envía señales de control a otras partes del sistema, y una unidad aritmética y lógica (ALU) que realiza la mayoría de las instrucciones matemáticas y lógicas. También contiene registros, como el contador de programa (PC), el registro de instrucciones actual (CIR), el registro de dirección de memoria (MAR) y el registro de datos de memoria (MDR).

El acumulador (ACC) se utiliza como registro principal para operaciones. Existen varios tipos de CPU, siendo las de propósito general las más comunes en PC y laptops. Sin embargo, hay CPUs específicas para tareas particulares, como en electrodomésticos, automóviles, dispositivos IoT y procesadores de señales digitales, cada una con sus propios diseños y requisitos. Estas diferencias pueden incluir variaciones en el diseño, cantidad y tipo de registros, e incluso la presencia o ausencia de ciertas partes del procesador según las necesidades específicas de cada aplicación.

# 1.3 El propósito de RAM, ROM, buses y registros

El concepto de "bus" en computadoras se refiere a la forma en que se mueve la información a través de grupos de cables en la placa base. Los buses conectan los distintos componentes de la computadora, similar al sistema nervioso en el cuerpo. En la CPU, existen tres buses principales: el bus de control, el bus de direcciones y el bus de datos. Estos transmiten instrucciones de control, direcciones de memoria y datos entre la CPU, la memoria y los controladores de entrada/salida.

La memoria puede ser volátil o no volátil. La memoria volátil, como la RAM, pierde datos cuando se pierde la alimentación, mientras que la no volátil, como la ROM, retiene su contenido. Se describen registros y se destacan los diferentes tipos de memoria utilizados en computadoras, como la RAM para almacenar programas en ejecución y la ROM para almacenar instrucciones básicas del firmware.

# 1.4 Códigos de operación, operandos y modos de direccionamiento de memoria

Una instrucción en bruto para la CPU, a menudo llamada instrucción de código máquina, consiste en una serie de dígitos binarios. En la informática, todo, desde instrucciones y datos hasta variables de programa, partes de una imagen o indicadores de estado, se representa como señales eléctricas en binario. La lógica de la computadora se basa en el álgebra booleana, que se centra en los principios de verdadero y falso, fácilmente expresados en binario con solo dos valores posibles para cada bit.

Aunque para los humanos es más fácil entender los resultados en decimal, la programación y el diseño de máquinas se volvieron más difíciles con la computación decimal, y rápidamente se eliminaron las computadoras en decimal. Las instrucciones binarias constan de varias partes, siendo la primera parte el código de operación u opcode, que varía según la familia de procesadores y define la operación a realizar. El resto de la instrucción son operandos, que son datos operados por la operación.

Se ejemplifica una instrucción simplificada en binario, donde el primer nibble (4 bits) es el opcode (0110) que podría significar "SUMA", y los siguientes dos nibbles son operandos binarios (1001 y 0010) que representan "Sumar 9 y 2". Se mencionan los modos de direccionamiento, que indican cómo interpretar los operandos. Algunas CPU tienen instrucciones completamente diferentes para cada modo de direccionamiento, mientras que otras utilizan parte del opcode para indicar el modo.

Se mencionan algunos modos de direccionamiento comunes, como el direccionamiento inmediato, que proporciona los datos como operandos, y el direccionamiento directo e indirecto, que proporcionan una ubicación de memoria en el operando. El direccionamiento directo especifica direcciones en los operandos, indicando a la CPU dónde obtener los datos, ya sea de otra ubicación de memoria, un registro de la CPU o un dispositivo externo. El direccionamiento indirecto utiliza operandos que contienen una dirección, que a su vez contiene la dirección de los datos a ser recuperados y utilizados en el programa.

# 2.1 Introducción a la ALU y la unidad de decodificación

La ALU es una parte fundamental de la CPU y realiza una variedad de operaciones, algunas aritméticas como sumar, restar, multiplicar, etc., y otras lógicas como AND, NOT o operaciones de desplazamiento que a menudo operan a nivel de bit. Aunque la ALU es un sistema complejo, se puede representar en un modelo bastante simple. Necesita elementos para llevar a cabo sus operaciones, como el código de operación (opcode) que le informa qué operación realizar y, por lo tanto, qué circuito usar.

Otro elemento que la ALU puede necesitar para completar su tarea es el contenido del registro de estado, algo que no se ha discutido antes. Este registro simple almacena el estado de tareas anteriores, por ejemplo, si la tarea anterior fue una adición y el resultado fue demasiado grande para almacenar, se establecería la bandera de desbordamiento. Si se hizo una comparación entre dos valores, el registro de estado puede establecer una bandera que indique si eran iguales o no.

Para realizar sus tareas, la ALU necesita uno o dos operandos, los datos o direcciones que necesita para llevar a cabo las instrucciones. Dos resultados saldrán de la ALU: el resultado, que generalmente se enviará directamente al acumulador, y una actualización del registro de estado para la siguiente operación. La ALU solo opera con números enteros; los números reales generalmente se envían a la Unidad de Punto Flotante (FPU), que a su vez tiene múltiples ALUs dentro.

Antes de que la ALU pueda ejecutar sus instrucciones, estas deben ser decodificadas, tarea que realiza la unidad de decodificación. La unidad decodificadora divide la instrucción en partes componentes (opcode y operandos) de manera que la ALU pueda realizar las operaciones correctas utilizando la circuitería adecuada. Un decodificador simple tomará un valor binario, los opcodes, y lo separará de manera que el resultado tenga solo un bit "alto", indicando qué circuito usar.

Esta implementación del conjunto de instrucciones del procesador facilita que la ALU utilice la circuitería correspondiente con un solo bit alto.

# 2.2 Operaciones aritméticas y lógicas

Las operaciones aritméticas son quizás las más simples de considerar y generalmente las asociamos con operaciones "matemáticas", como el semisumador que suma dos bits. Estas operaciones son bloques de construcción de circuitos simples que se pueden combinar para formar circuitos más complejos. En este caso, dos circuitos para sumar dos bits cada uno se han combinado para sumar dos bits más un bit de acarreo. Estos, a su vez, pueden combinarse para producir un circuito que sume un byte completo.

Existen dos tipos principales de operaciones lógicas a nivel de bits. El primero está directamente relacionado con las operaciones booleanas que quizás hayas encontrado antes, como AND, OR, NOT, y similares. Estas operaciones tienen diversas funciones, como invertir un binario positivo mediante una operación NOT en cada bit (conocido como complemento a uno). Esto forma parte del proceso de creación de un entero negativo en binario de complemento a dos.

Un procesador almacena el estado de operaciones anteriores en un registro de estado. Por ejemplo, si una suma es demasiado grande para almacenarse, se almacena un indicador de desbordamiento como 1. Un AND se puede utilizar para identificar el valor de un solo bit en el registro de estado, como el indicador de desbordamiento.

El otro tipo de operación lógica es un desplazamiento (shift). Hay varios tipos de desplazamientos; un desplazamiento aritmético conserva el bit más significativo (el de mayor valor de posición). Cada desplazamiento a la derecha es equivalente a dividir (o desplazar a la derecha) por dos. Un desplazamiento aritmético a la izquierda es lo opuesto, equivalente a multiplicar por dos. Un desplazamiento lógico funciona de la misma manera pero no conserva el bit de signo, por lo que es ideal para enteros sin signo.

Aunque realizar cálculos mediante desplazamientos es una manera rápida y simple para la CPU, se debe tener cuidado para no perder precisión ya que los contenidos binarios pueden salirse del registro.

# 2.3 Entrada, proceso y salida

Todos los ordenadores se rigen por un modelo conocido como IPO, o entrada, procesamiento y salida. Toman entrada, a menudo del usuario haciendo clic con el ratón o escribiendo en el teclado. La computadora, ya sea en la unidad de escritorio o dentro de la computadora portátil, procesa estos clics y toques para llevar a cabo las instrucciones del usuario, y luego la salida aparece en la pantalla, en los auriculares, o si eres realmente anticuado, en la impresora. Incluso los microprocesadores en los dispositivos más pequeños siguen el mismo modelo. La entrada puede provenir de un sensor, puede ser el microprocesador más pequeño, y la salida puede ser luces LED, zumbadores o incluso solo algunos datos enviados a un servidor en algún lugar.

El modelo IPO también es fundamental para el desarrollo de software y es un enfoque común en el análisis de sistemas: si un software tiene definidas sus entradas y salidas, y el desarrollador produce los procesos que hacen que las entradas generen las salidas correctas, entonces el sistema está haciendo lo que debe hacer.

Esto sigue siendo cierto a la escala más pequeña. Considera este fragmento de código ensamblador de un procesador conceptual. El código ensamblador es simplemente código máquina: las instrucciones se representan mediante mnemotécnicos en lugar de números binarios para que sea más fácil de leer para los humanos.

Esta instrucción se puede leer como "sumar el contenido del registro AH y el registro BH y almacenar el resultado en el registro BH". Las entradas son los operandos, los registros AH y BH. El proceso es sumar los dos, por lo que se instruye a la ALU a llevar a cabo ese proceso mediante el opcode ADD. Y la salida es, por supuesto, la suma de los contenidos de AH y BH, que en este caso se almacena nuevamente en el registro BH.

Es importante saber que algunas operaciones pueden llevar a cabo una tarea completa, pero algunas tareas pueden requerir múltiples operaciones. La atención a instrucciones simples de ciclo único o instrucciones más complejas, a menudo de varios ciclos, es la principal diferencia entre las arquitecturas de CPU RISC y CISC.

# 3.1 El ciclo de recuperación, decodificación y ejecución y el impacto de las interrupciones

Desde el momento en que se enciende hasta el momento en que se apaga, una computadora sigue el ciclo fetch-decode-execute, o FDE. Lo que sucede dentro de este ciclo depende de la arquitectura de la computadora.

La arquitectura Von Neumann, una de las más conocidas, tiene una única unidad de memoria y una única unidad de control. La computadora sigue un ciclo FDE de tres pasos: fetch (obtención), decode (decodificación) y execute (ejecución). En este modelo, el programa se inicia con el contador de programa (PC) establecido en la dirección de la primera instrucción. Luego, la dirección se envía a través del bus de direcciones, los datos se obtienen del bus de datos y se colocan en el registro de datos de memoria (MDR) y, finalmente, se copian en el registro de instrucciones actual (CIR). Luego sigue la etapa de decodificación, donde el módulo de decodificación dentro de la unidad de control (CU) decodifica la instrucción. En la etapa de ejecución, el opcode y los operandos se envían a las partes relevantes del procesador para su procesamiento.

Contrastando con esto está la arquitectura Harvard, que tiene dos unidades de control comunicándose con dos espacios de memoria separados, uno para instrucciones y otro para datos. Cada unidad de memoria tiene su propio bus de direcciones y bus de datos. Aunque la arquitectura Harvard tiene ventajas de velocidad, la arquitectura Von Neumann, con su memoria compartida, es más flexible y está asociada con las computadoras de propósito general.

En ambos casos, puede haber interrupciones en el ciclo. Los dispositivos hardware o el software pueden requerir atención, lo que lleva a una interrupción. Cuando esto sucede, el procesador almacena los códigos de estado actuales, el contenido de los registros y el valor del contador de programa en una pila y maneja el nuevo proceso que necesita llevarse a cabo. Luego, los valores se copian nuevamente desde la pila y el procesamiento continúa.

Algunos procesadores, como los procesadores RISC (conjunto de instrucciones reducido), tienen un ciclo de cinco etapas, donde la obtención, decodificación y ejecución son similares al ciclo Von Neumann, pero la lectura y escritura de datos desde y hacia la memoria se realizan en fases separadas.

# 3.2 Una variedad de factores que afectan el rendimiento de una CPU

Es un error común pensar que el rendimiento se trata únicamente de velocidad. Se compara el rendimiento de una computadora con el movimiento de autos en una carretera: la velocidad está dictada por la carretera, de la misma manera en que las instrucciones están dictadas por la circuitería por la que pasan. El "clock speed" en computadoras se refiere al número de pulsos que produce un reloj cada segundo (medido en hertzios), lo cual representa la cantidad de ciclos de instrucción que se activan en ese período de tiempo, no la velocidad a la que van las señales en sí mismas.

Muchos procesadores son ahora multicore, lo que significa que tienen múltiples unidades de procesamiento dentro de la CPU. Aunque algunas partes, como la memoria y la mayoría de los buses, son compartidas, la parte "núcleo" de la CPU que hemos discutido anteriormente se duplica, permitiendo el paralelismo, es decir, la ejecución de múltiples procesos al mismo tiempo. La eficacia del paralelismo depende del tipo de aplicación: algunas se benefician mucho de tener múltiples núcleos, mientras que otras no.

El concepto de "cache" es como una ubicación temporal de fácil acceso que agiliza la recuperación de información. La cache en una CPU es una memoria muy rápida que se utiliza para almacenar instrucciones y datos que se utilizan con frecuencia, siendo más rápida que la RAM. La cache se organiza en niveles, siendo el nivel 1 el más rápido y cercano al núcleo de la CPU, y el nivel 3 el más lento pero más grande.

La medición del rendimiento de una CPU implica factores como el número de instrucciones a ejecutar, los ciclos por instrucción, la duración del ciclo de reloj y la frecuencia del reloj. También se puede mejorar la ejecución mediante la descarga de parte del procesamiento a coprocesadores especializados, como la unidad de punto flotante que puede manejar números reales de manera más rápida que la ALU principal.

# 3.3 Algoritmos de programación y canalización

La primera computadora multitarea (o multi-programación) fue la Leo III, construida en 1961. En el caso de Leo III, el primer programa se ejecutaría hasta que necesitara usar un periférico, momento en el cual el siguiente programa se ejecutaría mientras el periférico realizaba su tarea. Esto se considera una forma de programación no preemptiva: no importaba cuán importante fuera una tarea, seguiría ejecutándose hasta que se completara, incluso si surgía una tarea más importante.

En la programación preemptiva, una tarea de menor importancia podría ejecutarse, pero si surgiera una tarea más importante, la ejecución se transferiría a esta última. En los sistemas modernos, la programación preemptiva cambia entre procesos tan rápidamente que parece que muchas cosas están sucediendo simultáneamente, como reproducir música, navegar por la web, escribir notas y escanear virus.

La mayoría de los procesos tienen un tiempo específico después del cual deben devolver la ejecución al sistema operativo, que luego programa la próxima tarea, ya sea según la prioridad (programación basada en prioridad) o simplemente en el orden en que se encuentra (programación round-robin).

Otro aspecto clave de la eficiencia de un CPU es el "pipelining". Un sistema de tuberías intenta comenzar la etapa de búsqueda de la siguiente instrucción cuando la instrucción anterior está pasando a la etapa de decodificación, de modo que todas las partes de la CPU estén en uso constante. Sin embargo, esto puede volverse complicado si las instrucciones toman tiempos diferentes para completarse o si una instrucción posterior intenta actuar sobre los resultados de una instrucción anterior que aún no ha terminado. Hay diversas soluciones para estos problemas, incluida la idea de "vaciar" el procesador de instrucciones antes de comenzar la siguiente, cuando sea apropiado. También se pueden agrupar componentes y utilizar los retrasos dentro de los componentes como memoria para evitar que la instrucción avance demasiado rápido.

# 4.1 La necesidad y el diseño de las instrucciones en código ensamblador

Se explica la dificultad de encontrar errores en datos binarios y cómo Kathleen Booth y David Wheeler intentaron abordar este problema al implementar mnemotécnicos en código ensamblador. Se destaca la importancia de la sintaxis en el código ensamblador, similar a los lenguajes de alto nivel. Se mencionan instrucciones de código ensamblador, explicando el vínculo entre las mnemotécnicas y las operaciones que representan. Se introduce el concepto de direccionamiento en las instrucciones. Se señala que agregar etiquetas facilita el salto a ubicaciones específicas en el código.

# 4.2 Creación de código de máquina utilizable a partir del lenguaje ensamblador

Comúnmente se utiliza la frase "relación 1 a 1" entre el código ensamblador y el código máquina, aunque esto no es completamente preciso. La relación entre el código ensamblador y el código máquina es más estrecha que la de, por ejemplo, Python y el código máquina. El proceso de conversión del código ensamblador al código ejecutable implica el uso de un ensamblador que produce código objeto, el cual aún no es completamente ejecutable. Luego, un enlazador combina todos los archivos objeto en un único archivo ejecutable: el código máquina (.exe en Windows). Para microcontroladores, el código se almacena en ROM o EEPROM, y se utiliza un dispositivo especial para cargar el código en los chips.

En el caso del emulador ASim, no parece pasar por este proceso. ASim es un emulador y no produce código máquina. Puede ejecutarse en cualquier plataforma debido a que funciona a través de JavaScript y Python en un servidor remoto.

Se presenta un programa que utiliza la operación XOR para cambiar el caso de un carácter ASCII. El código lee un carácter desde la consola, lo compara con el número 0 y, si se ha ingresado algo, realiza la operación XOR y muestra el resultado en la consola. La conversión a hexadecimal se explica y se muestra cómo se ejecuta la operación XOR en registros específicos.

# 4.3 Los procesos básicos involucrados en la compilación

Aunque puede haber uno, o a veces más de uno, lenguaje ensamblador para cada familia de procesadores, hay literalmente cientos de lenguajes de nivel superior. Ninguno de estos se ejecutará directamente en una computadora. Algunos, como Prolog o SQL, son declarativos: el programador indica lo que quiere y el software obtiene los datos relevantes. Otros son imperativos: el programador le dice a la computadora qué hacer. Pero incluso estos varían enormemente: muchos, como Python, son interpretados, cada línea de código se interpreta como una o más instrucciones y se ejecuta sobre la marcha. Esta interpretación debe realizarse cada vez que se ejecuta el código. Otros, como C, son compilados, el código fuente completo se convierte en código ejecutable una vez, antes de ejecutarse.

El proceso de convertir el código fuente en código ejecutable varía según el lenguaje y la elección del compilador. En el enfoque más simple, como el utilizado en C, hay cuatro procedimientos principales. El código fuente, junto con los archivos de encabezado, pasa por un preprocesador. Esto produce un archivo intermedio, que se compila en código ensamblador. Un ensamblador convierte esto en código objeto que, junto con archivos de biblioteca, se envía a través de un enlazador para producir código ejecutable. Todo este proceso se conoce comúnmente como compilación. Aunque no todos los compiladores siguen los mismos pasos en el mismo orden, en general, se deben completar tareas como el análisis léxico, la creación de una tabla de símbolos, el análisis sintáctico, la creación de un árbol sintáctico y el análisis semántico antes de generar el código. A lo largo de todo el proceso, los sistemas trabajan arduamente para optimizar el código y hacerlo eficiente para el procesador en lugar de ser eficiente para estilos de codificación de alto nivel.
