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

