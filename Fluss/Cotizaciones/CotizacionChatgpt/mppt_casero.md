
# Construcción de un MPPT Casero (Maximum Power Point Tracker)

## Introducción
Un controlador MPPT (Maximum Power Point Tracker) es un dispositivo que optimiza la energía que se extrae de paneles solares. Ajusta la carga para mantener la eficiencia máxima, buscando el punto de potencia máxima del panel en función de las condiciones de luz solar.

### Componentes principales para un MPPT casero

### 1. **Controlador PWM**
- **Modelos recomendados**:
  - **Texas Instruments TL494**: Controlador PWM de doble salida, adecuado para la regulación de energía en convertidores MPPT caseros.
  - **Texas Instruments UC3843**: Controlador PWM de modo de corriente, utilizado en aplicaciones de regulación y conversión de energía.

### 2. **MOSFET de potencia**
- **Modelos recomendados**:
  - **IRLB8721**: MOSFET de canal N de baja resistencia Rds(on), ideal para conmutación rápida y alta eficiencia en un MPPT casero.
  - **STMicroelectronics STP75NF75**: MOSFET de potencia con características de baja resistencia y alta capacidad de conmutación.

### 3. **Inductor**
- **Modelos recomendados**:
  - **Coilcraft XAL7070 Series**: Inductor de alta corriente con baja resistencia en DC, ideal para aplicaciones de convertidores MPPT.
  - **Würth Elektronik WE-HC Series**: Inductor de almacenamiento de energía, adecuado para la etapa de conversión en un MPPT casero.

### 4. **Capacitores de filtro**
- **Modelos recomendados**:
  - **Nichicon UPM Series**: Capacitores electrolíticos de baja ESR, perfectos para suavizar las oscilaciones de corriente en la salida.
  - **Panasonic EEH-ZA Series**: Capacitores de polímero sólido, con larga vida útil y baja resistencia en serie.

### 5. **Diodo Schottky**
- **Modelos recomendados**:
  - **Vishay SS36**: Diodo Schottky de conmutación rápida con baja caída de tensión directa.
  - **ON Semiconductor MBRS340T3G**: Diodo Schottky de baja caída para reducir las pérdidas y mejorar la eficiencia en el MPPT.

### 6. **Microcontrolador**
- **Modelos recomendados**:
  - **Arduino Uno**: Placa de microcontrolador ideal para proyectos caseros con capacidad de control y ajuste del punto de máxima potencia.
  - **ESP32**: Microcontrolador con conectividad WiFi y Bluetooth, permite la implementación de un MPPT con seguimiento remoto y monitoreo de datos.

### 7. **Sensor de corriente y voltaje**
- **Modelos recomendados**:
  - **INA219**: Sensor de corriente y voltaje con interfaz I2C, adecuado para medir el consumo y ajustar el punto de máxima potencia.
  - **ACS712**: Sensor de corriente basado en efecto Hall, ideal para monitorear la corriente en el MPPT.

### 8. **Pantalla LCD (opcional)**
- **Modelos recomendados**:
  - **LCD 16x2**: Pantalla estándar para mostrar el voltaje, corriente y potencia generada por el sistema.
  - **OLED 0.96"**: Pantalla más pequeña y eficiente para mostrar la información en tiempo real.

### 9. **Protección de sobrecorriente**
- **Modelos recomendados**:
  - **Littelfuse 0154005.MAT1**: Fusibles de alta velocidad para proteger el MPPT de sobrecorriente y cortocircuitos.
  - **Bourns MF-R090**: Resettable fuses para proteger contra sobrecalentamiento y sobrecorriente.

### 10. **Circuito de seguimiento del punto de máxima potencia (MPPT Algorithm)**
- **Algoritmos recomendados**:
  - **Perturb and Observe (P&O)**: Es uno de los algoritmos más simples y efectivos para implementar en un MPPT casero. Se basa en ajustar la carga y observar cómo cambia la potencia generada.
  - **Incremental Conductance**: Este algoritmo mide los cambios en la corriente y voltaje para ajustar el punto de máxima potencia con mayor precisión que el método P&O.

## Consideraciones de diseño

- **Frecuencia de conmutación**: Elige una frecuencia de conmutación adecuada, generalmente en el rango de 50 kHz a 100 kHz, para evitar pérdidas excesivas y reducir el tamaño de los componentes pasivos.
- **Eficiencia**: Selecciona componentes de alta eficiencia como MOSFETs de baja Rds(on) y diodos Schottky para minimizar las pérdidas de conmutación.
- **Protección térmica**: Es importante implementar disipadores de calor o ventilación adecuada para los MOSFETs y diodos, ya que los sistemas MPPT manejan grandes corrientes.

## Aplicaciones
- Sistemas de energía solar caseros para optimizar la energía captada por los paneles solares.
- Controladores de carga para baterías solares de 12V, 24V o 48V.
- Sistemas de energía renovable en entornos fuera de la red eléctrica (off-grid).

