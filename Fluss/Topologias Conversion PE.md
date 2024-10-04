2024-10-04 01:09

Tags: #Fluss #Potencia 



Un convertir de potencia electronico son en general circuitos de conmutacion semiconductora con 4 formas generales:
### DC / DC Converter (Switching Regulator) : 
Convierte el nivel de _Vin_  a un nuevo nivel _ßVout_ con _ß>0_.

#### Non - isolated 
### DC / AC Converter (Inverter):
Convierte un nivel _Vin_ AC de entrada a una onda cualquiera AC.

### AC / DC Converter (Rectifier) :
Convierte una señal _Vins_ AC de entrada a un nivel _Vout_ DC de salida. 
(Causa armonicos y bajo FP)

### AC / AC converter (AC controllers and Cycloconverters):
Si convierte una señal _Vins_ AC cambiando unicamente la **amplitud** -> AC controller.

	(FVFF) -> Fixed Voltage Fixed Frecuency
	a (VVFF) -> Variable Voltage Fixed Frecuency

Si convierte una señal _Vins_ AC cambiando la **amplitud** y **frecuencia** -> Cycloconverter.

	(FVFF) a (VVVF) -> Variable Voltage Variable Frecuency

Si en la topología se usan _Controlled switches_  se le llama **Matrix Converter**.
