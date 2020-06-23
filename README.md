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
![](img/1..png)
![](img/2..png)
![](img/3..png)

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

TinkerCad tiene un emulador de circuitos electrónicos que viene incluido con un Arduino UNO para emular, incluido un editor de código de Arduino con algunas librerías y un depurador.
Todas estas características hacen que no se no haga tan complicado crear programas y circuitos dentro de este entorno ya que el software es sumamente intuitivo y sencillo de usar. 
Entorno

![](img/7.png)

En la parte derecha contamos con un menú desplegable con distintos componentes electrónicos que nos facilita el software. En la parte izquierda se muestra un recuadro con distintos tutoriales en caso de no tener conocimientos básicos en simuladores de circuitos electrónicos.
En el menú superior contamos con distintos botones funcionales como lo son: el inicio de simulación, depurador, editor de códigos e inclusive contamos con la opción de compartir.
El principio de simulación es sencillo ya que únicamente debemos establecer puntos de conexión mediante las líneas que creamos.

#### Editor de código TinkerCAD
El funcionamiento de este editor de código es similar al software propio de Arduino en caso de que decidamos trabajar con texto ya que su sintaxis de programación es la misma. TinkerCAD cuenta con un generador de códigos mediante bloques el funcionamiento de este es más intuitivo ya que nos evitamos el escribir muchas líneas de código ya que al ser una herramienta visual es más sencillo. El software también nos permite crear un código mezclando bloques y texto.

![](img/8.png)

Ejemplos realizados (revisar el resto de documento para conocer programación y diagramas):
 - Simulación de semáforo
 - Simulación de barrido de diodos
### MicroBit
En el caso específico del microbit necesitamos saber, que es, cuáles son sus características, que tipo de proyectos podemos realizar con él, cuál es su manera de operar. Debemos indagar todos esos aspectos debido a que no se conoce nada sobre la placa en la que se va a trabajar.
**¿Qué es MicroBit?**

MicroBit es una tarjeta de circuitos del tamaño de la palma de una mano con una serie de 25 ledes y un chip Bluetooth para conexión inalámbrica. Puede ser programada para mostrar letras, números y otros símbolos y caracteres.
Micro Bit fue diseñada para alentar a los niños a participar activamente en la creación de software para computadoras y la creación de nuevas cosas, en lugar de ser consumidores de medios. Creada para funcionar junto con otros sistemas, como Raspberry Pi

**¿Cuáles son las características de MicroBit?**
 - Incluye dos botones, un acelerómetro y una brújula, y unos anillos a los cuales pueden ser conectados otros sensores.
 - En lugar de introducir el código directamente en la computadora, los usuarios deben escribirlo en una elección de cuatro lenguajes de programación basados en una PC, o en una tableta o teléfono inteligente, a través de una aplicación.
 - Después deben transferir los códigos a Micro Bit, que funciona como un dispositivo independiente que puede ser usado para proyectar mensajes y registrar movimientos, entre otras tareas.
 - También puede agregarse a otros dispositivos para formar el “cerebro” de un robot o desarrollar un instrumento musical.
 - Una nueva función posibilita las comunicaciones entre esas máquinas, lo cual significa que una Micro Bit pueda transmitir información a otra, abriendo un nuevo espectro de posibilidades.

**Componentes de MicroBit**
 - **Leds:**
 Microbit dispone de 25 LEDs programables individualmente que te permiten mostrar texto, números e imágenes.
 
 ![](img/9.png)
 
 - **Botones:**
 Hay dos botones en la cara frontal de micro:bit (etiquetados como A y B). Puedes detectar cuándo son pulsados de forma independiente o a la vez y ejecutar una acción en cada caso.
 
 ![](img/10.png)
 
 - **Pines de entrada y salida:**
 Microbit es ampliable hasta donde imagines. Dispone de 25 conectores situados en el borde inferior . A través de ellos podrás programar motores, LEDs o cualquier otro componente o sensor externo que conectes de Arduino o similares.
 
 ![](img/11.png)
 
 - **Sensor de luz:**
 Los LEDs de la placa micro:bit también pueden actuar como entrada haciendo que detecten la luz ambiente.
 
 ![](img/12.png)
 
 - **Sensor de temperatura:**
 El sensor de temperatura integrado en la placa detecta la temperatura ambiente en grados Celsius.
 
  ![](img/13.png)
 
 - **Acelerómetro:**
El acelerómetro mide la aceleración de tu micro:bit. Se activa cuando tu placa se mueve y también puede detectar otras acciones como agitar, girar y hasta soltar tu micro:bit en caída libre!

![](img/14.png)

- **Brujula:**
La brújula detecta el campo magnético terrestre por lo que puedes saber en qué dirección está orientada tu micro:bit. (Necesita ser calibrada para asegurar un resultado preciso.)

![](img/15.png)

- **Radio:**
La radio te permite comunicar tu micro:bit con otras micro:bit. Por ejemplo, puedes conectar todas las tarjetas dentro de un aula a una misma emisora, usarla para enviar mensajes entre ellas y mucho más!.

![](img/16.png)

- **Bluetooth:**
El BLE (Bluetooth Low Energy) permite a micro:bit enviar y recibir datos vía bluetooth para comunicarse de forma inalámbrica con PCs, Teléfonos y Tablets.

![](img/17.png)

- **USB y conector para batería externa:**
La placa micro:bit puede alimentarse a través del puerto USB. También dispone de un conector específico para 2 pilas AAA o una batería.
Al igual que en Arduino, esta placa almacena en su memoria un único programa que se ejecuta en cuanto recibe alimentación (ya que carece de un conmutador de encendido y apagado).


![](img/18.png)

#### Plataforma de trabajo de MicroBit
Esta pequeña tarjeta va de la mano con la pagina creada por sus desarrolladores, ya que están podemos encontrar herramientas de programación debido a que esta tarjeta tiene un entorno de programación gráfico propio la pagina posee el apartado MakeCode de Microsoft, un sencillo editor gráfico online muy potente y gratuito que posibilita introducirnos en el mundo de la programación de forma intuitiva a través del lenguaje de programación visual o de bloques. Con él aprendemos a pensar como un programador sin caer en los molestos errores de sintaxis. MakeCode es, sin duda, una herramienta a tener muy en cuenta por nuestros profesores.
BBC MicroBit también se puede programar con JavaScript, Pyton y Scratch (añadiendo una extensión).

![](img/19.png)

### Raspberry Pi
#### ¿Que es un Raspberry y para qué sirve?
Raspberry Pi, es un «es un ordenador de tamaño de tarjeta de crédito que se conecta a su televisor y un teclado». Es una placa que soporta varios componentes necesarios en un ordenador común.«Es un pequeño ordenador capaz, que puede ser utilizado por muchas de las cosas que su PC de escritorio hace, como hojas de cálculo, procesadores de texto y juegos. También reproduce vídeo de alta definición», apuntan en la página web del producto.
Este proyecto fue ideado en 2006 pero no fue lanzado al mercado febrero de 2012. Ha sido desarrollado por un grupo de la Universidad de Cambridge y su misión es fomentar la enseñanza de las ciencias de la computación los niños. De hecho, en enero de este año Google donó más de 15.000 Raspberry Pi para colegios en Reino Unido.
Es un ordenador muy funcional y debido a su tamaño puede funcionar para muchos otros propósito, claro, hay que tener algunas ideas sobre programación o de computación. Por ejemplo, el primer proyecto de un joven con Raspberry Pi fue convertir su consola NES dañada en una operativa y pudo jugar algunos viejos títulos.
#### Componentes del Raspberry Pi 4
 - Características de la Raspberry Pi 4 Broadcom BCM2711, Cortex núcleo cuádruple-A72 (ARM v8) 64-bit SoC @ 1.5GHz
 - SDRAM LPDDR4-2400 de 1 GB, 2 GB, 4 GB y 8 GB (según el modelo)
 - 2,4 GHz y 5,0 GHz IEEE 802.11ac inalámbrico, Bluetooth 5.0, BLE
 - Gigabit Ethernet 2 puertos USB 3.0; 2 puertos USB 2.0.
 - Cabezal GPIO estándar de 40 pines de Raspberry Pi (totalmente compatible con las placas anteriores)
 - 2 × puertos micro-HDMI (soportados hasta 4kp60)
 - Puerto de pantalla MIPI DSI de 2 vías
 - Puerto de cámara MIPI CSI de 2 carriles
 - Puerto de audio estéreo de 4 polos y de vídeo compuesto H.265 (decodificación 4kp60)
 - H264 (decodificación 1080p60, decodificación 1080p30)
 - Gráficos OpenGL ES 3.0
 - Ranura para tarjetas Micro-SD para cargar el sistema operativo y el almacenamiento de datos
 - 5V DC a través de conector USB-C (mínimo 3A*)
 - 5V DC vía cabezal GPIO (mínimo 3A*)
 - Alimentación a través de Ethernet (PoE) habilitada (requiere PoE HAT separado)
 - Temperatura de funcionamiento: 0 – 50 grados C ambiente
 #### El procesador
 El procesador encapsulado, que utiliza el mismo dispersor de calor para un mejor control térmico que el modelo anterior, puede tener el mismo aspecto desde el exterior. Pero mientras que el modelo de la Raspberry Pi 3 se construyó en torno al procesador Broadcom BCM2837, un ARM Cortex-A53 de cuatro núcleos a 1,4 GHz, la nueva placa se ha construido en torno al Broadcom BCM2711, un ARM Cortex-A72 de cuatro núcleos a 64 bits a 1,5 GHz. Aunque esto no parezca significativo, hay algunas grandes diferencias entre las arquitecturas centrales de estos dos procesadores. 
Mientras que el A53 fue diseñado como un núcleo de rango medio, y para la eficiencia, el A72 es un núcleo de rendimiento, así que a pesar de la aparentemente pequeña diferencia en la velocidad del reloj, la diferencia de rendimiento real entre los núcleos es realmente significativa.
#### USB y Ethernet
La diferencia más notable con respecto a los modelos anteriores es que el Microchip LAN7515, que actuaba como hub USB y como controlador Ethernet para la Pi, no aparece en la nueva placa. En su lugar se encuentra el VLI VL805, que proporciona un concentrador USB 3.0 a través de un bus PCI Express. 
El uso del bus PCI Express proporcionado por el nuevo BCM2711 significa que no sólo ahora tenemos capacidad USB 3.0, sino que el Gigabit Ethernet que se proporcionaba anteriormente a través del bus USB y el chip LAN7515 -que tenía un rendimiento máximo limitado a unos 300Mbps- ahora se proporciona utilizando el Broadcom BCM54213PE en un bus separado para el tráfico USB. 
Esto significa que, en lugar de ser estrangulado como vimos con el modelo B+ de Raspberry Pi 3, la nueva Raspberry Pi 4 tiene una Gigabit Ethernet “real”. 
La nueva placa Raspberry Pi tiene tanto Gigabit Ethernet “real” como dos puertos USB 3.0, así como un par de puertos USB 2 más.
#### Soporte Inalámbrico
El mismo chip Cypress CYW43455 que vimos en Raspberry Pi 3, modelo B+, proporciona soporte inalámbrico en un módulo apantallado por RF. Ofrece redes inalámbricas IEEE 802.11.b/g/n/ac de banda dual de 2.4GHz y 5GHz, así como Bluetooth 5.0 y Bluetooth LE.
#### La Memoria
Para completar todo está la LPDDR4 SDRAM para la placa, que viene en forma de un chip empaquetado en Micron FBGA, y aquí es donde aparece otra gran diferencia con respecto a los modelos anteriores de Raspberry Pi. A diferencia de cualquier placa anterior, la nueva Raspberry Pi 4 está disponible en tres modelos diferentes, cada uno de los cuales ofrece diferentes opciones de memoria. La nueva placa puede venir con 1 GB, 2 GB o 4 GB de RAM.
#### Alimentación de la placa
Otra gran diferencia es la toma de corriente, que se ha ido es la toma micro-USB de los modelos anteriores, y en su lugar hay una toma USB-C. Es un cambio comprensible. Las tolerancias en la fuente de alimentación para el modelo B+ de Raspberry Pi 3 ya eran bastante finas, y la nueva placa puede requerir hasta 3 amperios, eso no es algo que la anterior fuente micro-USB pudiera proporcionar. La placa también puede alimentarse a través de una fuente de alimentación de 5V DC utilizando los cabezales GPIO, y al igual que la Raspberry Pi 3, modelo B+, antes de que lo haga la nueva Raspberry Pi 4 también puede alimentarse a través de Power over Ethernet (PoE) utilizando el PoE HAT oficial que se lanzó junto con el modelo anterior el año pasado.

![](img/20.png)

#### ¿Que es GPIO?
General Purpose Input Output (GPIO) es un sistema de entrada y salida de propósito general, es decir, consta de una serie de pines o conexiones que se pueden usar como entradas o salidas para múltiples usos. Estos pines están incluidos en todos los modelos de Raspberry Pi aunque con diferencias.

![](img/21.png)

 - Amarillo (2): Alimentación a 3.3V.
 - Rojo (2): Alimentación a 5V.
 - Naranja (26): Entradas / salidas de proposito general. Pueden configurarse como entradas o salidas. Ten presente que el nivel alto es de 3.3V y no son tolerantes a tensiones de 5V.
 - Gris (2): Reservados.
 - Negro (8): Conexión a GND o masa.
 - Azul (2): Comunicación mediante el protocolo I2C para comunicarse con periféricos que siguen este protocolo.
 - Verde (2): Destinados a conexión para UART para puerto serie convencional.
 - Morado (5): Comunicación mediante el protocolo SPI para comunicarse con periféricos que siguen este protocolo.

Ejemplos realizados (revisar el resto de documento para conocer programación y diagramas) :
 - Reloj Binario
 - Luz Ambiental
 ## 5.Diagramas
 ### Arduino
 #### Simulación de semáforo usando TinkerCAD
 
 ![](img/22.png)
 
 El siguiente circuito pretende emular los ciclos de tiempo que tendría cada luz en un semáforo y el cambio que el mismo presenta en la vida real es decir si la luz de un semáforo es roja la otra es verde y para cambiar al color contrario primero el semáforo debe cambiar a amarillo. 
 
 #### Simulación de barrido de diodos usando TinkerCAD
 
 ![](img/23.png)
 
 En este circuito generamos un encendido de manera secuencial de 5 diodos LED, la secuencia de encendido dependerá de los casos que envíe nuestro dip switch a manera de tablas de verdad donde tenemos 3 casos:
  - El caso 0 mantiene apagados todos los diodos LED del circuito.
  - El caso 1 enciende los LEDs de adentro hacia afuera.
  - El caso 2 enciende los LEDs de afuera hacia adentro.
  
### Microbit
Los diferentes programas realizados en la plataforma de microbit.org se pueden representar mediante diagrama de bloques dentro del lenguaje de JavaScript.
#### Simulación de solicitud de pare en semaforo

 ![](img/24.png)
 
#### Contador de números dentro de los dispositivos

 ![](img/25.png)
 
 ### Raspberry
 Para los ejemplos propuestos se uso utilizo python
 Entonces la conexion entre el unicorn y la raspberry puesta en un difusor que se puede hacer con una impresora 3d o comprarla en linea 
 queda asi:
 
 ![](img/26.png)
 ![](img/27.png)
 
El Reloj Binario emulado se ve asi:

![](img/28.png)
![](img/29.png)

## 6. Lista de Componentes
### Arduino
#### Simulación de semáforo
 - Arduino Uno.
 - Resistencias de 1k.
 - Diodos LED: 2 Rojos, 2 Verdes y 2 Amarillos.
 - TinkerCAD
#### Simulación Barrido de Diodos
 - Arduino Uno
 - Resistencias de 1k
 - Diodos LED : Distintos Colores
 - 1 Dip Switch
 - Protoboard
 - TinkerCAD
### MicroBit
#### Simulación solicitud de pare en un semáforo
 - MicroBit
 - Cable de conexión USB
 - Programación en JavaScript
#### Contador de números dentro de los positivos
 - MicroBit
 - Cable de conexión USB
 - Programación en JavaScript
### Raspberry
#### Luz Ambiental
 - Pi Zero W
 - Unicorn pHAT con 32 LED de neopixel RGB programables
 - Encabezados de 2x20 pines macho y hembra
 - Colgante y difusor de luz blanca y amarilla
 - Cable USB A a micro-B de 50 cm
 - Adaptador mini HDMI a HDMI
#### Reloj Binario
 - Sense Hat o Emulador de Sense Hat
 - Raspberry pi 3 o 4
 - Periféricos
 - Cargador Usb Tipo C
 - Conexión Ethernet o Wi-Fi
## 7. Mapa de Variables
### Arduino
#### Simulación de semáforo:

![](img/30.png)

 #### Simulación Barrido de Diodos
 
 ![](img/31.png)
 
 ### MicroBit
 #### Contador de números dentro de los positivos 
 
 ![](img/32.png)
 
 
 
 
 
 
