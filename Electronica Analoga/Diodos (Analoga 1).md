2024-09-30 17:06

Tags: #Analoga #Diodos

Elemento de 2 terminales semiconductor con el siguiente símbolo:

![Esquema Del Diodo|300](Imagenes/EsquemaDiodo.png)

La ecuación del Diodo para el diodo cuando esta en **polarización directa**.

$$\LARGE I_{D}= I_{S}(e^{\frac{V_{D}}{nV_{T}}}-1)$$

Donde cada parámetro corresponde a:
* _ID (Corriente del diodo)_ : Cuando esta **polarizado en directa**.
* _IS (Corriente de Fuga)_: Corriente extremadamente pequeña cuando esta **polarizado en inversa**. Depende de la temperatura y características del diodo (Constante).
* _VD (Voltaje a través del diodo)_ : Este voltaje en **polarización directa** es fijo (0.1 v - 0.8 v). En **polarización inversa** depende del circuito y es negativo (Desde Ánodo hasta Cátodo).
* _VT (Voltaje térmico) :_ Parámetro establecido por la temperatura, dado por la siguiente ecuación:

$$\LARGE V_{T} = \frac {kT}{q} $$

Con k = constante de Boltzmann (1.38 x 10^-23 J/K)  ||  T = temperatura en Kelvin || q = Carga del electrón (1.6 x10^-19 C). 

* _n (Factor de Idealidad)_ : Idealmente seria de 1, no obstante, el valor suele rondar entre 1 -2 . Define la capacidad de emisión del diodo.

Si Id >> Is entonces la ecuación resultante es:
$$\LARGE I_{D}= I_{S}(e^{\frac{V_{D}}{nV_{T}}})$$
La curva característica de un Diodo, que incluye el comportamiento Zener para un tipo especifico de diodo:

![Curva Diodo|400](Imagenes/CurvaDiodo.png)


# Zener

En _polarización directa_ funciona como un diodo usual, no obstante, en _inversa_ presenta un comportamiento tal que, si se supera un valor de voltaje _vz_ entonces el diodo empieza a conducir corriente. En dado caso que siga aumentando _Vz_ el voltaje del diodo seguiría siendo un valor estable. Por ejemplo, si el diodo Zener esta diseñado para una tensión de **5.6 V** y se aplican **12 V** , el voltaje del diodo se mantendrá haciendo así un regulador de voltaje.

* Se debe tener en cuenta _Izmin_ y _Izmax_ al diseñar y permitir una buena regulación.
# Rizado en fuentes reguladas lineales de voltaje


# PDF_referencia 

![[E.Analoga.pdf]]