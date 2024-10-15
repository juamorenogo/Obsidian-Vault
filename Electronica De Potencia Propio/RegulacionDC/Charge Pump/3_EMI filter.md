2024-10-15 16:25

Tags: #Potencia #Topologia 

	Filtros _LC_ funcionan como filtros de _HFRFI (High Frecuency Radio Interference)_ . 

La **frecuencia de filtro** no debera ser 2 - 3 veces mas que la frecuencia de la fuente. A su vez, añade una impedancia inductiva entre la fuente y _Bulk filter Capacitor_, lo que reduce transientes peligrosos de corriente y voltaje.

---
### Diagrama general switcheo

![|400](Imagenes/Generalswitcheo.jpeg)

![|400](Imagenes/OndasGeneralSwitch.jpeg)


---
Por otro lado, el _Bulk filter Capacitor_ se refiere a un elemento con la funcion de almacenar energia de alta - baja frecuencia usada por la fuente en cada ciclo de los transistores. Se conforma usando:

* Capacitor electrolitico para componentes harmonicos de la corriente de _supply's switching frequency_.

* Capacitor ceramico para los harmónicos de la _frecuencia de conmutacion_.

En general:
* Brinda estabilidad al sistema.
* Filtra el rizado y componentes armonicos. 
* Mejor eficiencia.

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
