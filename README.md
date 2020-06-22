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

**1. Jack de Potencia**
Algunos modelos de Arduino cuentan con un Jack de alimentación que nos permite conectar una fuente de alimentación de forma directa, comúnmente este Jack viene en los modelos grandes o más completos.

**2. Conector de comunicación tipo USB**
Este componente nos permitirá la conexión con el ordenador y también la alimentación del Arduino. Cabe aclarar que existen diferentes tipos de conectores USB por lo que cada modelo de Arduino contará con su propio conector, inclusive algunos modelos de Arduino no lo incluyen, en su mayoría los modelos que no incluyen un conector serial son los modelos pequeños.

**3.Pin Vin**
Con este pin podemos alimentar nuestro Arduino sin la necesidad de alimentarlo mediante el Jack de potencia o el Conector USB. Este pin viene en todos los modelos de Arduino ya que en modelos pequeños no dispondremos de Jack de potencia o conector USB.

**4.Pin de 5V**
Este pin nos permite alimentar otros componentes electrónicos que no necesiten de una gran potencia como lo serían algunos sensores. Este pin tiene la finalidad de evitarnos el cableado de alimentación de componentes que estén cerca del Arduino y que trabajan con potencias bajas.

**5.Pin de 3.3V**
Al igual que el pin de 5V, este pin nos permite alimentar componentes que trabajan con voltajes de referencia bajos evitándose usar fuentes alternas de alimentación.

**6.Pin de GND**
El pin de GND (Tierra) es común en todos los circuitos electrónicos de corriente continua y nos permite conectar el mismo a otros componentes externos o en caso de usar el pin de alimentación Vin debemos conectar este pin directo al GND de nuestra fuente de alimentación.

**7.Pines Analógicos**
La placa Arduino puede leer valores de voltaje analógicos siempre y cuando estos no superen los 5V ya que valores superiores de voltaje podrían dañar nuestra placa. Con voltajes analógicos nos referimos a valores de voltaje que no son constantes con respecto al tiempo, es decir valores variables de voltaje. Cabe aclarar que Arduino es capaz únicamente de leer valores de voltaje analógicos, pero no es capaz de enviar señales analógicas. Estos pines están representados en la placa por la letra A.

**8.Pines Digitales**
Al trabajar con electrónica digital estamos hablando de enviar valores de voltaje de 0V o 5V (0 y 1 lógico). Estos pines pueden ser de entrada y salida es decir pueden enviar y recibir señales digitales. Estos pines van numerados del 0 hasta n, donde n dependerá del modelo de Arduino usado. Los pines de entrada analógica también pueden ser usados como pines digitales.

**9.Pines PWM**
Primero debemos aclarar que es una señal PWM. Esta es una señal de tipo digital sus siglas traducidas del inglés significan Modulación por Ancho de Pulso (Pulse Width Modulation) una señal digital posee 2 estados lógicos (0 o 1) si en un intervalo de tiempo dado nosotros hacemos que nuestro circuito envié ambas señales de manera repetitiva y constante ya estamos generando una onda cuadrada la cual será una señal PWM. Las aplicaciones de una señal PWM son el envió de información y modificar la cantidad de energía que se envía a una carga.
Con respecto al modificar la cantidad de energía que se envía a una carga esta aplicación de una señal PWM es muy útil cuando trabajamos con leds o motores ya que podemos modificar su intensidad sin necesidad de trabajar con señales analógicas. Esto lo podemos realizar mediante la modificación de sus ciclos de trabajo.

**10.**
**11.**
**12.**
**13.**
**14.**
**15.**


