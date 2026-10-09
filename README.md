# 🤖 Basurero Inteligente con Arduino

**Proyecto de Robótica — ExpoLogros 2026**

## 📌 Descripción del proyecto

Nuestro proyecto consiste en la creación de un **basurero inteligente controlado mediante Arduino**, capaz de abrir y cerrar sus tapas automáticamente cuando detecta un objeto o una persona a una distancia determinada.

El sistema utiliza un sensor ultrasónico para medir la distancia y cuatro servomotores para controlar el movimiento de las tapas. De esta manera, buscamos automatizar una tarea cotidiana mediante la programación y la electrónica.

## 🎯 Objetivo

Diseñar y construir un basurero automatizado que permita abrir y cerrar sus tapas sin necesidad de levantarlas manualmente, aplicando conocimientos de robótica, programación y circuitos electrónicos.

## ⚙️ Materiales y componentes

Arduino UNO R3: 1 unidad.

Sensor ultrasónico HC-SR04: 1 unidad.
Servomotores tipo SG90 o similares: 4 unidades.
Protoboard: 1 unidad.
Portapilas para baterías AA: 2 unidades.
Baterías AA de 1.5 V: 4 unidades.
Cables jumper: varios.
Condensador electrolítico: 1 unidad.
Cable USB para Arduino: 1 unidad.

## 🔌 Conexiones del circuito

| Componente       | Pin del Arduino |
| ---------------- | --------------- |
| TRIG del HC-SR04 | D10             |
| ECHO del HC-SR04 | D11             |
| Servomotor 1     | D9              |
| Servomotor 2     | D6              |
| Servomotor 3     | D5              |
| Servomotor 4     | D3              |

**Nota:** La alimentación externa de los servomotores y el Arduino deben compartir GND (tierra común).

## 💻 Funcionamiento

El proyecto funciona mediante los siguientes pasos:

1. El sensor ultrasónico HC-SR04 emite una señal para detectar objetos cercanos.
2. El sensor mide el tiempo que tarda la señal en regresar.
3. El Arduino calcula la distancia en centímetros.
4. Si el objeto se encuentra a **20 cm o menos**, los cuatro servomotores reciben la orden de abrir las tapas.
5. Las tapas permanecen abiertas durante aproximadamente 3 segundos.
6. Si no se cumple la condición de apertura, el programa ordena cerrar las tapas.

### 🔄 Lógica del sistema

`Detectar → Medir → Procesar → Abrir → Cerrar`

## 🧠 Programación

El sistema está programado en C++ utilizando el entorno Arduino IDE y la librería `Servo.h` para controlar los servomotores.

Entre las principales funciones utilizadas se encuentran:

* `setup()`: configura los componentes al iniciar.
* `loop()`: repite continuamente el proceso.
* `pinMode()`: configura los pines del sensor.
* `digitalWrite()`: controla las señales del sensor ultrasónico.
* `pulseIn()`: mide la duración de la señal recibida.
* `servo.write()`: establece la posición de los servomotores.
* `if`: evalúa la condición para abrir las tapas.
* `delay()`: establece pausas durante el funcionamiento.

## 🌱 Beneficios del proyecto

* Reduce la necesidad de tocar directamente las tapas del basurero.
* Demuestra una aplicación práctica de la robótica.
* Permite aprender sobre sensores, motores y programación.
* Promueve la creatividad y la búsqueda de soluciones tecnológicas.
* Fomenta el aprendizaje mediante la construcción de prototipos.

## 🚀 Instalación y uso

1. Descarga o clona este repositorio.
2. Abre el archivo `.ino` en Arduino IDE.
3. Instala la librería `Servo.h`, si es necesario.
4. Conecta los componentes siguiendo el esquema del circuito.
5. Selecciona la placa Arduino UNO y el puerto correspondiente.
6. Sube el programa al Arduino.
7. Acerca la mano al sensor para comprobar el funcionamiento.

**Importante:** Verifica las conexiones y la alimentación antes de encender el circuito. Los cuatro servomotores deben contar con una fuente adecuada para su consumo de corriente.

## 👥 Integrantes del equipo

Tatiana Margarita Ramiréz — 4268927                                                                        
Alisson Ariana Avilés Renderos — 6078903                                                                    
Tony Joshua Cruz Portillo— 19732922                                                                        
Melanie Camila Hernández Galdámez — 6652086 

## 🏫 Institución educativa

**Complejo Educativo Catolico San Francisco**

**Evento:** ExpoLogros 2026

## 🏁 Conclusión

Con este proyecto demostramos que la combinación de programación, electrónica y robótica permite automatizar tareas cotidianas. Además, adquirimos experiencia en el uso de sensores ultrasónicos, el control de servomotores y la construcción de sistemas electrónicos.

**¡La robótica transforma ideas en soluciones!** 🤖♻️

