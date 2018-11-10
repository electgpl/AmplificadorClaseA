# Amplificador de Audio en Clase A

![N|Solid](https://raw.githubusercontent.com/electgpl/AmplificadorClaseA/master/Imagenes/Circuito_Montado_Disipador.jpg)

Este proyecto se trata de un amplificador de audio de potencia en clase A.
Existen muchas Clases de amplificación, que responden a distintas topologias y tecnologías de diseño.
Las mas comunes en Audio hoy en día son la Clase AB y la Clase D, siendo la mas antigua la clase AB, aunque la Clase A también es antigua pero tiene algunos pros y contra respecto a las demás clases de amplificador.

## Pros:

  - No posee distorsión por cruce, esta existe en todos los Clase AB.
  - No posee fuentes de ruido, esta existe en todos los Clase D.
  - Distorsión Harmónica Total reducida, aquí depende del diseño, pero es muy baja.
  - Ancho de banda mayor de respuesta en frecuencia
  
## Contras:

  - Un bajo rendimiento de energía, al rededor del 30%, (ejemplo: 10W de consumo, 3W de salida).
  - Exceso de Temperatura, de la mano del rendimiento, mucha energía disipada en calor.
  - Fuentes de alimentación costosas, Se requiere de fuentes bien filtradas y de potencia.

## Circuito

![N|Solid](https://raw.githubusercontent.com/electgpl/AmplificadorClaseA/master/Imagenes/Circuito%20Amplificador.png)

Como podemos ver, el circuito posee muy pocos componentes, tenemos remarcado en Amarillo el transistor que se encarga de generar una fuente de corriente constante, y en Azul los transistores que se encargan de amplificar el Audio.
Ambos transistores de potencia son TIP3055, son algo grandes, pero por la relación precio producto, vamos a trabajar holgados en cuanto a potencia de disipación y nuestro amplificador tendrá mejor performance.
Tenemos una etapa principal que es un preamplificador en base al 2N3906, luego este excita el driver de potencia en base al BD135 y por ultimo este alimenta la base de potencia del TIP3055, con esto conformamos las veces de amplificación del circuito.
Como fuente de corriente CCR, tenemos otro TIP3055 junto a la polarizacion directa, podremos lograr al rededor de 1A de corriente constante.
Es necesario dotar estos transistores de buenos disipadores de calor.

## Analisis

Analizamos este circuito en LTSpice y podremos ver la respuesta en frecuencia que arranca desde los 4Hz y termina casi en 100kHz, esto nos proporciona un ancho de banda bastante grande y nos asegura una buena respuesta en frecuencia de nuestro amplificador para trabajar en todo el rango de audio 20Hz a 20kHz.

![N|Solid](https://raw.githubusercontent.com/electgpl/AmplificadorClaseA/master/Analisis/LTSpice_Bode.png)

## Diseño

> Diseñado con EAGLE, en solo dos capas con componentes THT para facilitar
> la integración al alumno, el desarrollo del PCB en el hogar y mantener
> el menor costo posible.

![N|Solid](https://raw.githubusercontent.com/electgpl/AmplificadorClaseA/master/Imagenes/20181019_105856.jpg)

Patrocinado
----
¿Dónde fabricamos nuestros PCBs?
Nuestros PCBs los fabricamos con la empresa PCBWay, esta empresa nos permite realizar pequeñas cantidades como prototipos rápidos para nuestros desarrollos a medida.
También nos permite realizar grandes producciones para realizar proyectos comerciales.
Servicio de prototipo de PCB por tan solo $5 las 10 unidades.
Cada nuevo miembro recibirá un bono de $5, más servicio express de 24Hs o 48Hs.
Servicio de ensamblado de PCB por $88 más envió gratis en todo el mundo, más esténcil, más componentes.
Un servicio de calidad!
https://www.pcbway.es/

[![N|Solid](https://github.com/electgpl/Banners/blob/master/PCBWay_600x160.gif)](https://www.pcbway.es/)


License
----

MIT
