# Diseño de Interfaz de Arduino  -  Proyecto Final

## Introduccion
En el marco del curso 'Diseño de Interfaz mediante Arduino' de la Universidad de Chile, realicé un proyecto que fusiona la programación y el hardware sumado al Diseño Industrial para crear un producto que integre estos dos campos de aprendizaje. Este trabajo final fue una excelente ocasión para poner en práctica los conocimientos adquiridos y poner en práctica el potencial de combinar disciplinas que en muchos casos parecen distantes. El resultado es un producto que no solo cumple una función específica, sino que también abre las puertas a futuras aplicaciones.
Nuestro proyecto surge del gran interés por los recientemente descubiertos sensores, algo totalmente novedoso para mí, y la posibilidad de integrarlos a mecanismos que permitan ampliar la gama de posibilidades que ofrece un objeto.


### Metas de la asignatura

Poder realizar un circuito eléctrico funcional, donde no se genere ningún cortocircuito.
Realizar un código de programación con el lenguaje de Arduino 
Que el proyecto sea lo más cercano a lo que teníamos en mente inicialmente

## Investigación
Se realizó una investigación referida a qué modelo de arduino convenía, que componentes eran necesarios, sus cantidades y sobre todo nos centramos en que variedad de sensores existía en el mercado. 
Dentro de estos últimos, podemos encontrar desde sensores de alcohol, térmicos, ultrasónicos, de presión, fotosensibles, etc. los cuales ofrecían un abanico de oportunidades para incluir dentro del proyecto.

Luego asesoramiento en el tema con los profesores, ayudantes y vendedores, además de debates con el equipo de trabajo, terminamos eligiendo los Sensores Ultrasónicos, que captan aquellos objetos que se encuentran en su entorno, activandose. El trabajo con este tipo de sensores permite regular la distancia específica con la que se quiere trabajar, teniendo rangos de corta, mediana y larga distancia.

Realizamos una variedad de estudios de que podía llegar a ser nuestro producto ideal y dentro de las diferentes variables tiradas sobre la mesa elegimos dotar a un robot de la capacidad de movilizarse de forma autónoma, esquivando obstáculos y redirigiendo su rumbo. Para lograr esto nos vimos condicionados a investigar cuales eran los alcances de la Arduino para analizar la viabilidad del proyecto.
Finalmente, corroborado esto último, iniciamos la etapa propositiva/creativa.

## Desarrollo de propuesta

Luego de definir el tipo de sensor, comenzamos a dibujar propuestas de diseño teniendo en cuenta la morfología que subjetivamente nos interesaba y un tamaño estimado de lo que podía llegar a ser el proyecto. 

### Materiales
- Castor Wheel (1) = Realizar movimientos sin impedimentos de ejes o direcciones
- Caja de pilas (1) = Portapilas
- Pilas AA (4)
- Método de alimentación del robot
- Sensor Ultrasonico HC.SR04 (1) = Detección de Obstáculos
- Servo SG90 (1) = Ampliar el espectro de análisis del sensor.
- Soporte para Servo Motor (1)
- Placa Shield Sensor V5 (1) = Ampliación de pines para conectar servomotores y sensores con mayor facilidad
- Mecanismo de engranajes (1) = Habilitan el movimiento
- Arduino Uno R3 (1)
- Driver de Motor L298N (1) = Puente H para regulación de los motores DC
- Placa de acrílico transparente (1) = Soporte / "chasis" del prototipo
- Motor DC (2) = Habilita el movimiento de las ruedas hacia adelante / atrás
- Piezas para fijación de Motor (2) = Soportes laterales para fijación de los motores DC
- LED (2) = Rojo y Verde
- Buzzer (1) = Emisión de sonidos
- ProtoBoard (1) = Conexión de LEDs y pines
- Resistencias (3) = 220v
- Interruptor (1) = ON/OFF
- Neumáticos con llanta (2) = Ruedas conectadas a los laterales del motores DC permitiendo dirección
- Cables Hembra - Hembra (11)
- Cables Macho - Hembra (5)
- Tornillos y tuercas = Fijación de componentes
- Banda elástica (1) = Fijación de sensor
- Cinta bifaz (1) = Pegado de placas y Servo


### Rápidamente nos dimos cuenta de tres factores a tener en cuenta:

Los componentes tenían un cierto tamaño que respetar, es decir no podíamos jugar tanto con las plataformas donde apoyan los componentes debido a que estábamos trabajando con alrededor de 50 componentes estándar con medidas preestablecidas.
Debía y convenía que fuese lo más pequeño posible: con nuestras primeras aproximaciones, entendimos que por cuestiones de distancias entre componentes no podemos posicionar uno en una punta y otro en otra debido a que iban conectados por cables que no daban mucho juego.
Era de vital importancia encontrar una coherencia entre componentes donde se establezca un orden, como un cuerpo humano, donde los componentes centrales, como la fuente de poder -el corazón por ejemplo-, se ubique en el centro y los componentes de menor funcionalidad hacia los laterales. 

El objetivo al que teníamos que arribar era el poder permitir que el código permita que el robot avance hasta detectar algún obstáculo a una distancia media (20cm), haciéndolo retroceder hasta que no detecte ningún objeto en su sensor, girando ( haciendo que una rueda se mantenga quieta con un delay y la otra se active, rotando). Pasado ese delay, deberían girar las dos ruedas al mismo tiempo, avanzando nuevamente. De esta manera, se evitaría cualquier colisión potencial. 

Como advertencias/ señales para el usuario para el usuario, propusimos que un LED se mantenga encendido en verde hasta que se encuentre una interrupción, cambiando a rojo y sonando un buzzer al retrocede.

El circuito eléctrico  se compone del Arduino UNO como “cerebro” del sistema, transmitiendo / recibiendo información o energía a / de:
 Puente H (rectángulo rojo del gráfico), encargado de direccionar y dar potencia a los motores DC (encargados de mover las ruedas que van incrustadas en la punta del motor).
Sensor Ultrasónico HC.SR04, que recibe información del medio y la envía de nuevo al Arduino UNO.
Pilas que envían 12v al sistema.
ProtoBoard donde se instalan LEDs, Buzzer y resistencias.
Todos estos componentes están conectados por cables que transmiten señales, voltaje e información. 

El código para programar estas funciones fue una situación de prueba y error, quizás el objetivo que buscábamos representaba un desafío más grande del esperado debido a la minuciosidad del código, la variedad de funciones y nuestro conocimiento básico en el tema. Encontramos muchas situaciones donde nos faltaban algunos detalles como cierre de comillas, paréntesis o corchetes al abrir o terminar funciones.

Como guía teníamos para tomar como referencia la comunidad de Arduino, la cual es abierta y envían códigos que quizá coinciden parcialmente con los que se necesitan desarrollar, debiendo hacer modificaciones. Uno que nos facilitó la comunidad, fue el código que permite adelantar, retroceder y girar.




