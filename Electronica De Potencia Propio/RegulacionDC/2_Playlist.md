2024-10-20 00:33

Tags: #Topologia #Potencia 

# Playlist Power supplies

![](https://youtube.com/playlist?list=PLUTV_UMnJSciYeKoJLuQ6jxYsMEeWET3f&si=DVA62JLb710QZ_0s)

Antes del capacitor de filtrado en AC/DC se debe proponer una medida para la _inrush current_ siendo un pico de corriente generado por el primer instante donde el capacitor actua como un corto.

Para solucionar esto se usa , por ejemplo, un NTC (Negative Temperature Coefficient), siendo un termistor que:

* Cuando esta frio, se tiene una alta resistencia, que actua como limitador de la corriente 
* Cuando se caliente, se tiene una baja resistencia, lo que ya no limita la corriente.

Generando un limitador de corriente simple, aun asi tiene desventajas como:
 
 * Se debe dejar enfriar totalmente cuando se apaga el circuito.
 * Perdidas de potencia.

 Se puede disponer de un _Power Factor Correction circuit_ antes del capacitor de filtrado, para mejorar la eficiencia energetica del circuito, reducir armonicos en la corriente y reducir la corriente de entrada alineando las fases de voltaje y corriente.


