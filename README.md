# DS1307 RTC
## De la o Quiñonez Fabian 19211625
![DS1307 RTC](https://user-images.githubusercontent.com/83306485/190031036-34d42335-557b-4ab2-9b7e-21f0ac4305cd.png)

El Reloj en Tiempo Real (RTC por sus siglas en inglés real-time clock) es un componente presenten en la mayoría de aparatos eléctronicos como Ordenadores, microondas, relojes digitales, etc.

Prácticamente lleva la cuenta de segundos, minutos y horas, ademas de día, mes y año automáticamente, válido hasta el año 2100.
Cuenta con 56 byte de memoria RAM respaldada por una batería exterior que mantienen fecha y hora cuando no hay corriente eléctrica que lo alimente
La batería por su parte puede durar hasta 10 años por su bajo consumo de energía

![Protoboard arduino a RTC](https://www.prometec.net/wp-content/uploads/2014/11/Sesion-55_bb.jpg)

Para conectar el DS1307 al protoboard solo hace falta conectar GND-GND, 5v-5v,SDA-A4 y SCL-A5. El PIN SQW es una salidda digital que genera frecuencias programables (de 1Hz, 4kHz, 8kHz, 32kHz) que podemos emplear como base de tiempos para el reloj de cualquier circuito sin neesidad de un cristal adicional de cuarzo y circuito oscilador.

Es importante mencionar que la comunicación física es a través de un protocolo llamado Bus I2C o TWI. Este bus cuenta con dos lineas: de datos y de reloj, ambas del tipo ccolector abierto. Por lo que se requieren resistencias Pull-UP para generar un estado lógico alto. Estas resistencias van en los pines SDA Y SCL.

