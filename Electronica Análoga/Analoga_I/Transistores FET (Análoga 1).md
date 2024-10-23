2024-09-30 17:13

Tags: #Transistores #Analoga 

## JFET

Transistor de efecto de campo, que funciona con junturas semiconductoras y un canal que se encuentra _Normalmente abierto_.

![|400](JFET1.png)

El símbolo usado actualmente se usa para _MOSFET_ también, debido al poco uso comercial del _JFET_.

![|400](JFET2.png)

La ecuacion de transferencia es:

$$ \LARGE I_{D}=I_{DSS}(1-\frac{V_{GS}}{V_{P}})^{2}$$ 
Donde los terminos constantes son :
* _Idss_ : Constante que representa la corriente _Id_ en saturacion con _Vgs = 0 V_. 
* _Vp_  = _Vgs(off)_ : Voltaje entre **gate** - **source** , donde la corriente _id  = 0A_.

	*JFET CANAL N* -> -V
	*JFET CANAL P* -> +V

La curva de transferencia entre _Vds - Id_ muestra el punto de valor de _Idss_ y _Vp_ para un _Vgs = 0v_.

![|500](Imagenes/Jfet3.png)

En _Vds = Vp_ se genera estrangulamiento del canal y se entra en saturación. La curva va a variar dependiendo de si es un _N-JFET_ O _P-JFET_:

![[JFET4.png]]

Y la otra curva correspondiente para _N-JFET_:

![[JFET5.png]]

El punto de operacion ***Q*** se halla con la interseccion lineal de otra ecuacion que representa la relacion entre ambos terminos de forma lineal.

![[JFET6.png]]


## MOSFET

### Empobrecimiento



### Enriquecimiento


