2024-10-08 21:22

Tags: #Potencia #Motor #DC  

Tiene 2 funcionamientos basicos de acuerdo a la direccion de giro.
### Foward Running : 
El voltaje de armadura y corriente son positivas dando giro en la direccion _"Normal"_ (Foward Motoring Operation en el cuadrante **1**). **+V , +A** 

### Foward Bracking:
El voltaje de armadura es positivo pero la corriente es negativa y se frena el motor en su dirección _"Normal"_ (Foward regenerating operation en el cuadrante **2**) **+V , -A**.

### Reverse Starting:
El voltaje de armadura y corriente son negativos dando giro contrario a la direccion _"Normal"_ (Reverse starting en el cuadrante _3_) **-V , -A**.

### Reverse Braking:
El voltaje de armadura es negativo y la corriente es positiva dando giro contrario a la direccion _"Normal"_ (Reverse regenerating Operation en el cuadrante _4_) **-V , +A**.

![Motor |500](Imagenes/MotorDc_1.jpeg )

## Choppers 

Como Interruptor electrónico (Mosfet o IGBT) que regula el flujo de una _fuente de corriente DC_ hacia una carga por medio de su conmutación variando el _Ducy Cycle DT_ y _frecuencia_ (varia la energía que pasa a la carga). 

El resultado en realidad es una onda cuadrada de _Vin_ a _0_ cuyo voltaje promedio es un nivel _DC_ menor a la entrada, no obstante, se usa un filtrado _LC_ que suaviza finalmente la onda (El inductor suaviza la corriente y el capacitor el voltaje). Si la carga es un _Motor DC_ entonces varia la velocidad del motor ***(Modulación por ancho de pulso PWM)***.

### Tipos de Choppers:
Dependiendo del cuadrante donde trabaje se le asigna un nombre. Para cada caso, el switch _S_ se refiere a cualquier elemento de interruptor electrónico.
#### First Quadrant 1 type A
Esquema del circuito con formas de ondas:

![Q1| 400](Imagenes/Q1.jpeg)

#### Second Quadrant 2 type B

Esquema del circuito con formas de onda:

#### Third Quadrant 3 type 