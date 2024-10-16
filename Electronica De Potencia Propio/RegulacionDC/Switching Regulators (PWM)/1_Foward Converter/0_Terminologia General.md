2024-10-15 20:05

Tags:  

### Shunt Capacitor

- **Función**: Se conecta en paralelo (shunt) para:
  - Mejorar el **factor de potencia** compensando cargas inductivas.
  - **Reducir pérdidas** de energía.
  - Mantener el **voltaje estable**.
  - **Filtrar armónicos** en algunos casos.

- **Aplicaciones**:
  - Líneas de transmisión y sistemas industriales.
  - Estabilización de voltaje en sistemas de distribución.
### Series Inductor

- **Función**: Se conecta en serie para:
  - **Almacenar energía** en forma de campo magnético.
  - Actuar como **filtro de corriente**, bloqueando señales de alta frecuencia.
  - **Limitar corrientes** de arranque.
  - Compensar **reactancia capacitiva** en líneas de transmisión.

- **Aplicaciones**:
  - Filtrado de señales en fuentes de alimentación.
  - Suavizado de corriente en fuentes conmutadas.
  - Corrección del factor de potencia capacitivo.

Todo esto usado para los filtros LC.

### Elementos Current Sense

Desarrollar voltaje proporcional a la corriente de salida de la carga. En caso de que se genere una _sobrecorriente_ por un voltaje muy alto, el sistema fuerza la reduccion del voltaje.

* _Voltage mode regulatos_ : Se activa al detectar una sobre corriente. (Current foldback limiting)
* _Current mode regulators_ : Se mide la corriente del primerio del transformador y se usa para la limitacion de la corriente. 
---

	Current Foldback limiting : Tecnica de proteccion usado en fuentes que limita la corriente de salida.

---
### Elementos Voltage Feedback

Usualmente un divisor de tension que reduce el _voltaje de salida_ a un voltaje de referencia.
Se compara la salida del divisor de tension despues de su ajuste con el voltaje de referencia, si _Vout > Vref o Vout < Vref_ se genera una señal de error para ajustar la salida siendo que _Error  = Diferencia entre la salida y la referencia_. 

### Etapa de Control general

Se busca cumplir los siguientes criterios:

* Voltaje -> PWM conversion
* Voltaje de referencia estable
* Oscilador
* Deteccion de sobre-corrientes
* Control de la conversion de la fuente en general

Tambien se busca incluir un _circuito de inico suave_ , circuito _dead time limiting_ y circuito _apagado remoto_. 
 
---
### Dead Time Timing

**Dead time** es un breve periodo en el que **ambos transistores en un circuito conmutado están apagados** para evitar que conduzcan simultáneamente, lo que podría causar un **cortocircuito**.

#### Función principal:
- **Evitar cortocircuitos** (shoot-through) al garantizar que un transistor esté completamente apagado antes de encender el otro.
- **Protección** de los componentes contra sobrecorrientes.
- **Mejora de eficiencia** al prevenir cortocircuitos que generarían pérdidas de energía.

#### Ajuste del Dead Time:
- **Demasiado corto**: Puede provocar cortocircuitos si ambos transistores conducen al mismo tiempo.
- **Demasiado largo**: Introduce ineficiencia y pérdida de potencia al aumentar el tiempo en que ambos transistores están apagados.

#### Aplicaciones:
- Convertidores DC-DC e inversores que utilizan transistores para controlar el flujo de corriente.

---
### Single-Ended Supply

Un **single-ended supply** es un tipo de fuente de alimentación que proporciona solo un voltaje positivo o negativo respecto a tierra (**ground**), en lugar de ambos (como en una fuente de alimentación simétrica).
#### Características:
- **Un solo voltaje**: Solo se suministra un voltaje (positivo o negativo) respecto a tierra.
- **Conexión a tierra**: Uno de los terminales está conectado directamente a tierra, y el otro lleva el voltaje de salida.
- **Común en circuitos sencillos**: Usado en amplificadores y circuitos de bajo consumo que no requieren fuentes simétricas.

#### Ejemplos:
- **Fuentes de alimentación de 5V, 12V o 24V**.
- **Uso en amplificadores operacionales** que funcionan con voltaje positivo respecto a tierra.

---
### Double-Ended Switch

Un **double-ended switch** es un dispositivo de conmutación que utiliza dos transistores o interruptores electrónicos, generalmente en configuraciones de puente completo o media puente, donde ambos extremos de la carga están conectados a interruptores. Esto permite el control del flujo de corriente en ambas direcciones a través de la carga.

#### Características:
- **Control bidireccional**: Permite que la corriente fluya en ambas direcciones a través de la carga.
- **Uso de dos interruptores**: Conformado por dos transistores o MOSFETs en la configuración de conmutación.
- **Alta eficiencia**: Optimiza el uso de energía en circuitos de potencia.

#### Aplicaciones:
- **Convertidores de potencia** como inversores y convertidores DC-DC.
- **Motor drivers**: Control de motores en aplicaciones que requieren inversión de la dirección del flujo de corriente.

#### Ventajas:
- **Mejor control** sobre la dirección de la corriente.
- **Mayor flexibilidad** en aplicaciones de potencia.

#### Desventajas:
- **Mayor complejidad**: Requiere más componentes y un diseño más sofisticado en comparación con un solo interruptor.

---
### Flip-Flop

Un **flip-flop** es un tipo de circuito secuencial que tiene dos estados estables y puede almacenar un bit de información (0 o 1). Se utiliza en sistemas digitales para el **almacenamiento de datos** y el **control de secuencias**.

#### Características:
- **Biestable**: Tiene dos estados posibles (alto o bajo, 1 o 0).
- **Almacena un bit**: Puede recordar su estado hasta que se actualice con una señal externa.
- **Controlado por señales de reloj**: Normalmente sincronizado con un pulso de reloj que controla cuándo cambia de estado.

#### Tipos de Flip-Flop:
- **SR Flip-Flop**: Controlado por entradas "Set" (S) y "Reset" (R).
- **D Flip-Flop**: Almacena el valor presente en la entrada de datos (D) en el flanco del reloj.
- **JK Flip-Flop**: Similar al SR, pero sin el estado inválido.
- **T Flip-Flop**: Cambia de estado (toggle) con cada pulso de reloj.

#### Aplicaciones:
- **Memoria digital**: Almacenamiento temporal en registros y contadores.
- **Sistemas de control**: Sincronización y control de secuencias en circuitos digitales.
- **Divisores de frecuencia**: Usado para reducir la frecuencia de una señal.

--- 
### Bipolar Flux Mode of Operation

El **bipolar flux mode of operation** es un modo de funcionamiento común en transformadores y convertidores de potencia que involucran el flujo magnético en dos direcciones opuestas durante el ciclo de operación. En este modo, el núcleo magnético del transformador o inductor alterna entre dos niveles de saturación, generando flujo en ambas polaridades (positiva y negativa).

#### Características:
- **Flujo magnético bidireccional**: El flujo magnético cambia de dirección dentro del núcleo, alternando entre polaridades positiva y negativa.
- **Uso eficiente del núcleo**: Este modo aprovecha al máximo el núcleo magnético al permitir que funcione en ambas direcciones.
- **Aplicación en conmutación**: Se utiliza en convertidores de potencia conmutada y en transformadores que operan en circuitos AC.

#### Ventajas:
- **Mayor utilización del núcleo magnético**: Se utiliza todo el ciclo de histéresis del núcleo, aumentando la eficiencia.
- **Reducción de tamaño**: Se puede usar un núcleo más pequeño al aprovechar ambos extremos de la curva de saturación.
  
#### Aplicaciones:
- **Convertidores DC-DC**: En configuraciones como push-pull o puente completo.
- **Transformadores**: Para transformar energía en sistemas de corriente alterna.

#### Desventajas:
- **Requiere conmutación precisa** para evitar la saturación excesiva del núcleo.
- **Mayor complejidad** en el control comparado con modos unipolares.


