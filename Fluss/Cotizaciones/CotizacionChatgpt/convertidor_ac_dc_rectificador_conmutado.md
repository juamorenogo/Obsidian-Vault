
# Convertidor AC/DC con rectificador conmutado

## Introducción
Un convertidor AC/DC con rectificador conmutado es un dispositivo que convierte corriente alterna (AC) en corriente continua (DC) utilizando un rectificador de estado sólido con interruptores controlados. Estos rectificadores son más eficientes que los rectificadores convencionales no controlados y permiten un control preciso sobre el voltaje de salida y la corriente.

## Componentes principales

### 1. **Rectificador conmutado (Switched Rectifier)**
- **Modelo recomendado**:
  - **STMicroelectronics STTH60L06**: Rectificador de conmutación rápida con baja caída de tensión directa, ideal para aplicaciones de convertidores de alta eficiencia.

### 2. **Filtros de entrada y salida**
- **Modelo recomendado**:
  - **Murata Power Solutions 810R Series**: Filtros EMI/EMC para minimizar el ruido de alta frecuencia generado por la conmutación de los rectificadores.
  - **TDK-Lambda RSEV Series**: Filtro de salida para la reducción de ondulación en la señal de corriente continua.

### 3. **Controladores de conmutación**
- **Modelo recomendado**:
  - **Texas Instruments UCC28700**: Controlador de conmutación flyback de alta eficiencia, utilizado para controlar el ciclo de trabajo de los interruptores y mejorar la regulación de voltaje.
  - **Infineon IR2153**: Controlador de PWM con protección integrada, adecuado para topologías de rectificación conmutada.

### 4. **Transistores de potencia**
- **Modelo recomendado**:
  - **Infineon Technologies IPP60R099P7**: MOSFET de canal N con baja resistencia Rds(on), ideal para rectificadores conmutados en aplicaciones de alta frecuencia.
  - **IXYS VISHAY FRED PT**: Diodos rápidos para conmutación en rectificadores controlados.

### 5. **Capacitores de filtro**
- **Modelos recomendados**:
  - **Nichicon UHW Series**: Capacitores electrolíticos de alta capacidad y bajo ESR, perfectos para suavizar la señal DC de salida.
  - **Panasonic EEH-ZA Series**: Capacitores de polímero sólido con larga vida útil y baja resistencia.

### 6. **Inductor de filtro**
- **Modelos recomendados**:
  - **Coilcraft SER2915H Series**: Inductores de alta corriente diseñados para filtrar señales de conmutación en circuitos rectificadores.
  - **Würth Elektronik WE-HC Series**: Inductores de almacenamiento de energía adecuados para convertidores AC/DC.

### 7. **Control de retroalimentación**
- **Modelos recomendados**:
  - **Texas Instruments TL431**: Referencia de voltaje ajustable para controlar la retroalimentación del voltaje de salida.
  - **ON Semiconductor NCP431**: Controlador de voltaje de referencia para regulación de la señal de salida.

### 8. **Protección de sobrecorriente**
- **Modelos recomendados**:
  - **Littelfuse 0154005.MAT1**: Fusibles de alta velocidad para proteger contra sobrecorriente en la salida DC.
  - **Bourns MF-R090**: Resettable fuses para proteger el circuito contra sobrecalentamiento y cortocircuitos.

## Consideraciones de diseño

- **Frecuencia de conmutación**: La frecuencia de conmutación alta, como en el rango de 50 kHz a 500 kHz, permite el uso de componentes más pequeños y mejora la eficiencia, pero requiere un diseño cuidadoso de los filtros EMI.
- **Eficiencia**: Utilizar MOSFETs de baja resistencia y diodos de conmutación rápida ayuda a reducir las pérdidas por conmutación y mejorar la eficiencia global del convertidor.
- **Protección**: Implementar protecciones como control de sobrecorriente, sobrevoltaje y térmicas para garantizar la seguridad y longevidad del dispositivo.

## Aplicaciones típicas
- Fuentes de alimentación conmutadas (SMPS)
- Convertidores para sistemas de energía renovable
- Fuentes de alimentación para equipos industriales y de telecomunicaciones

