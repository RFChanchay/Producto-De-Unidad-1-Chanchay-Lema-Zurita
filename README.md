# Arduino, Micro Bit y Raspberry Pi

## 1. Planteamineto del problema

## 2. Objetivos
   - **General**
     - Analizar los componentes, características y plataformas de desarrollo básicas para los dispositivos Arduino, Micro:Bit y Raspberry Pi
   - **Específicos**
     - Identificar los componentes principales de cada dispositivo y determinar sus funciones.
     - Explorar los entornos de desarrollo básicos existentes para cada dispositivo.
     - Explorar los entornos de desarrollo básicos existentes para cada dispositivo.
## 3. Estado del Arte
![](img/1.png)
![](img/2.png)
![](img/3.png)

En lo que respecta a nuestro Producto de Unidad cada una de estas investigaciones tienen su aportación pero estas deberán ser analizadas desde 3 perspectivas distintas

 - Respecto al uso del Arduino en un alimentador canino, nosotros asociamos al producto de unidad él cómo podemos facilitar nuestras actividades diarias con el uso de una simple placa electrónica y la creación de un algoritmo. Esto nos abre más posibilidades en usos facilitandonos las actividades diarias.
 - El micro:bit dentro de nuestro producto de unidad está directamente relacionado en el aprendizaje sobretodo en lo que es programación ya que al ser una plataforma fácil de entender será fácil de usar tanto en niños como en jóvenes como nosotros que estamos empezando a desarrollar habilidades dentro del campo de la informática.
 - En relación del raspberry podemos considerar el uso que se le da con respecto a la computación y al internet de las cosas ya que podemos reducir costos en equipos y espacio con el uso de este pequeño dispositivo ampliando nuestra gama de posibilidades y beneficios.
## 4. Marco Teórico
### Arduino
#### ¿Que es Arduino?
Cuando hablamos de Arduino, hablamos de 3 apartados distintos:
- Una placa de hardware libre: Al hablar de Arduino físicamente hablamos de una placa electrónica multipropósito de libre modificación por parte de sus usuarios, la cual tendrá distintos componentes conectados entre sí. Algunos de sus componentes son cristales, resistencias, capacitores, pines de conexión, etc. Pero el más importante de sus componentes es el microcontrolador, el cual se encargará de realizar los distintos cálculos y de procesar la información recibida para enviar respuestas dependiendo de cómo lo hayamos programado.  Al hablar de hardware libre queremos decir que su modelo o diagramas están abiertas a modificaciones por parte de los usuarios. Arduino a su vez es una placa de Hardware ya que posee componentes electrónicos conectados entre sí. Todos sus componentes electrónicos son controlados mediante un microcontrolador, en Arduino encontraremos los microcontroladores de la familia AVR. (Torrente, 2013)
- Un Software o Entorno de desarrollo libre: Arduino es también el programa que instalamos en nuestra computadora (Windows, MacOS y Linux) donde podemos desarrollar, compilar y cargar nuestro código. (Torrente, 2013)
- Un lenguaje de programación libre: Por ‘’Lenguaje de programación ‘’ nos referimos a un lenguaje artificial diseñado para dar instrucciones a una máquina. Arduino tiene un lenguaje de programación similar a otros lenguajes respecto a sus bloques de control y flujo, pero su sintaxis es mucho más amigable para realizar proyectos de electrónica. (Torrente, 2013)
#### Componentes de un Arduino
Arduino tiene una inmensa gama de modelos lo que hace que definir todos los componentes sea complicado, por lo cual describiremos los componentes existentes en todos los modelos de manera general:
![](img/4.png)

**1. Jack de Potencia:**
Algunos modelos de Arduino cuentan con un Jack de alimentación que nos permite conectar una fuente de alimentación de forma directa, comúnmente este Jack viene en los modelos grandes o más completos.

**2. Conector de comunicación tipo USB:**
Este componente nos permitirá la conexión con el ordenador y también la alimentación del Arduino. Cabe aclarar que existen diferentes tipos de conectores USB por lo que cada modelo de Arduino contará con su propio conector, inclusive algunos modelos de Arduino no lo incluyen, en su mayoría los modelos que no incluyen un conector serial son los modelos pequeños.

**3. Pin Vin:**
Con este pin podemos alimentar nuestro Arduino sin la necesidad de alimentarlo mediante el Jack de potencia o el Conector USB. Este pin viene en todos los modelos de Arduino ya que en modelos pequeños no dispondremos de Jack de potencia o conector USB.

**4. Pin de 5V:**
Este pin nos permite alimentar otros componentes electrónicos que no necesiten de una gran potencia como lo serían algunos sensores. Este pin tiene la finalidad de evitarnos el cableado de alimentación de componentes que estén cerca del Arduino y que trabajan con potencias bajas.

**5. Pin de 3.3V:**
Al igual que el pin de 5V, este pin nos permite alimentar componentes que trabajan con voltajes de referencia bajos evitándose usar fuentes alternas de alimentación.

**6. Pin de GND:**
El pin de GND (Tierra) es común en todos los circuitos electrónicos de corriente continua y nos permite conectar el mismo a otros componentes externos o en caso de usar el pin de alimentación Vin debemos conectar este pin directo al GND de nuestra fuente de alimentación.

**7. Pines Analógicos:**
La placa Arduino puede leer valores de voltaje analógicos siempre y cuando estos no superen los 5V ya que valores superiores de voltaje podrían dañar nuestra placa. Con voltajes analógicos nos referimos a valores de voltaje que no son constantes con respecto al tiempo, es decir valores variables de voltaje. Cabe aclarar que Arduino es capaz únicamente de leer valores de voltaje analógicos, pero no es capaz de enviar señales analógicas. Estos pines están representados en la placa por la letra A.

**8. Pines Digitales:**
Al trabajar con electrónica digital estamos hablando de enviar valores de voltaje de 0V o 5V (0 y 1 lógico). Estos pines pueden ser de entrada y salida es decir pueden enviar y recibir señales digitales. Estos pines van numerados del 0 hasta n, donde n dependerá del modelo de Arduino usado. Los pines de entrada analógica también pueden ser usados como pines digitales.

**9. Pines PWM:**
Primero debemos aclarar que es una señal PWM. Esta es una señal de tipo digital sus siglas traducidas del inglés significan Modulación por Ancho de Pulso (Pulse Width Modulation) una señal digital posee 2 estados lógicos (0 o 1) si en un intervalo de tiempo dado nosotros hacemos que nuestro circuito envié ambas señales de manera repetitiva y constante ya estamos generando una onda cuadrada la cual será una señal PWM. Las aplicaciones de una señal PWM son el envió de información y modificar la cantidad de energía que se envía a una carga.
Con respecto al modificar la cantidad de energía que se envía a una carga esta aplicación de una señal PWM es muy útil cuando trabajamos con leds o motores ya que podemos modificar su intensidad sin necesidad de trabajar con señales analógicas. Esto lo podemos realizar mediante la modificación de sus ciclos de trabajo.

![](img/5.png)

El ciclo de trabajo en una señal PWM se determina en función de la siguiente fórmula:

![](img/6.png)

Donde Ta es el Tiempo en estado alto, T es el periodo de la señal y C es el ciclo de trabajo.
Si a un Led le enviamos una señal PWM con un ciclo de trabajo del %50 su intensidad será del %50 respecto a su máxima, mientras que si enviamos una señal con un ciclo de %0 el diodo estará apagado.
En Arduino tenemos pines que permiten enviar señales de este tipo y están identificados con el siguiente símbolo en su placa ~.

**10.Pin Aref:**
Este pin nos permite tomar valores de voltaje de referencia para sensores analógicos que envíen valores al Arduino mayor a su rango de bit siempre y cuando estén en el rango de 0v a 5v.

**11.Botón Reset, Pin Reset:**
Este botón y pin nos permiten reiniciar nuestro código desde el principio tanto en funciones como en valores es decir vuelve a iniciar el código sin información guardada y comenzando desde su primera línea de código.

**12. LED de alimentación:**
Son 2 leds que nos indican cuando se está transmitiendo información (TX) y recibiendo información (RX) por medio de su puerto de comunicación serial.

**13.Indicador RX y TX:**
Este componente nos permite regular la alimentación que reciba nuestro Arduino de la fuente par que el Arduino tenga 5V limpios de alimentación.

**14.Regulador de Voltaje:**
Este circuito integrado es el encargado de la comunicación en si ya que por medio de este componente pasan todos los datos que enviemos o recibamos del ordenador y los dirige al microcontrolador de nuestro Arduino.

**15.Circuito de comunicación:**
Este componente es el encargado de generar los pulsos de reloj de nuestro Arduino los cuales genera la velocidad de procesamiento.

**16.Cristal:**
Este conector nos permite recibir nuestro código sin necesidad de usar la comunicación USB pero para esto es necesario el uso de programadoras externas.

**17.Conector ICSP:**
Es un led indicador de que nuestro Arduino se encuentra alimentado y operando.

**18.Microcontrolador:**
Este es cerebro de nuestro Arduino el encargado de procesar datos e instrucciones. Este cuenta con:
  - Memoria: SRAM, Flash, EEPROM, ROM, etc.
  - Buses
  - UART
  - Otras comunicaciones.
  - CPU
En otras palabras el microcontrolador es el Arduino ya que los pines del Arduino son jacks que facilitan la conexión con los pines del microcontrolador.
Arduino usa la gama de microcontroladores AVR de Atmel pertenecientes a la familia de microcontroladores RISC. Cada microcontrolador posee diferentes características: tamaños, RAM, ROM, etc. El microcontrolador usado dependerá exclusivamente del modelo de Arduino.

#### Componentes Arduino Uno
Para el modelo Arduino UNO contaremos con los siguientes componentes
 - El microprocesador ATmega328
 - 32 kbytes de memoria Flash (Memoria donde se guardará nuestro programas y datos permanentes)
 - 1 kbyte de memoria RAM (Memoria Temporal o de Datos Volátiles)
 - 16 MHz (Velocidad de trabajo del microcontrolador)
 - 14 pins para entradas/salidas digitales (programables)
 - 5 pins para entradas analógicas (Pueden ser usadas como digitales)
 - 6 pins para salidas analógicas (salidas PWM)
 - Microcontrolador ATmega328
 - Voltaje de operación 5V
 - Voltaje de entrada (recomendado) 7-12 V
 - Voltaje de entrada (limite) 6-20 V
 - DC corriente I/O Pin 40 mA
 - DC corriente 3.3V Pin 50 mA
 - EEPROM 512 bytes (Memoria ROM borrable eléctricamente)
 
#### TinkerCAD
**¿Qué es CAD?**

Cuando hablamos de CAD nos referimos al diseño asistido por computadora traducido de sus siglas en inglés computer-aided design.
**¿Qué es TinkerCAD?**

TinkerCAD es un software desarrollado por AutoDesk para la creación de modelos 3D basado en geometría sólida constructiva (CSG), este software tiene la particularidad que no es necesario ser un gran experto en diseño 3D ya que inclusive niños pueden crear sus modelos a manera de aprendizaje.
**¿Cómo se relaciona TinkerCAD con Arduino?**

nkerCad tiene un emulador de circuitos electrónicos que viene incluido con un Arduino UNO para emular, incluido un editor de código de Arduino con algunas librerías y un depurador.
Todas estas características hacen que no se no haga tan complicado crear programas y circuitos dentro de este entorno ya que el software es sumamente intuitivo y sencillo de usar. 
Entorno



