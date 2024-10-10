2024-10-09 16:35

Tags: #Potencia #Transistores 

 A priori, se divide en 2 grandes categorías de operación (Recomendaciones de diseño en _Motorola Series in solid state electronics_):
## Linear Mode Regulator
Posee las siguientes **ventajas**:
* Modelo simple.
* Operación silenciosa ( Ruido generalmente despreciable a la salida).
* Respuesta dinámica rápida a cambios de carga. 
* Para salidas _< 10 W_ mucho mas barato.

Posee las siguientes _desventajas_:
* Solo puede ser usado como _Buck_ o _Step Down_.
* Solo es capaz de regular una entrada a la vez.
* Poca eficiencia en potencia (_30% - 60% de eficiencia_).
## Switching Mode Regulator
Posee las siguientes **ventajas**:
* Alta eficiencia en potencia (_68% - 90% de eficiencia_) (Los transistores de potencia trabajan en sus puntos óptimos, _Saturación_ y _Corte_).
* Mayor independencia entre _Vin_ y _Vo_, lo que significa que sirve como _Buck_ o _Boost_.
* Mas barato en altas potencias.

Posee las siguientes _desventajas_:
* Modelo mucho mas complicado.
* Operación ruidosa (Aplica considerable ruido a la señal de salida) que involucra _EMC_ .
* Respuesta dinámica lenta a cambios de carga (trasient response time).






