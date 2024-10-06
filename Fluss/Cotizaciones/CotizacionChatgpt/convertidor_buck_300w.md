
# Convertidor Buck DC/DC con potencia de entrada de 300W

## Introducción
Un convertidor Buck es un dispositivo que convierte corriente continua (DC) de un voltaje más alto a uno más bajo, manteniendo la eficiencia energética. En este diseño, se considerará un convertidor Buck con una potencia de entrada de **300 W**.

### Especificaciones de diseño

- **Potencia de entrada**: 300 W
- **Eficiencia estimada**: 90%
- **Tensión de entrada (\( V_{	ext{in}} \))**: 24V
- **Tensión de salida (\( V_{	ext{out}} \))**: 12V
- **Corriente de entrada (\( I_{	ext{in}} \))**: 12.5 A
- **Corriente de salida (\( I_{	ext{out}} \))**: 22.5 A
- **Potencia de salida**: 270 W (debido a la eficiencia)

### Componentes principales

### 1. **MOSFET de potencia**
- **Modelos recomendados**:
  - **IRLB8721**: MOSFET de canal N con baja resistencia Rds(on) y alta capacidad de conmutación, ideal para manejar 22.5 A de corriente de salida.
  - **STMicroelectronics STP75NF75**: MOSFET con características adecuadas para conmutación rápida y eficiencia elevada en convertidores de alta potencia.

### 2. **Inductor**
- **Modelos recomendados**:
  - **Coilcraft XAL7070 Series**: Inductor de alta corriente con baja resistencia DC, diseñado para manejar la corriente de salida de 22.5 A en un convertidor Buck.
  - **Würth Elektronik WE-HC Series**: Inductores diseñados para aplicaciones de alta potencia con bajas pérdidas por resistencia.

### 3. **Diodo Schottky**
- **Modelos recomendados**:
  - **Vishay SS36**: Diodo Schottky de baja caída de tensión directa, ideal para minimizar las pérdidas en la etapa de conmutación.
  - **ON Semiconductor MBRS340T3G**: Diodo Schottky para reducir pérdidas por conmutación en sistemas de conversión DC/DC.

### 4. **Capacitores de filtro**
- **Modelos recomendados**:
  - **Nichicon UPM Series**: Capacitores electrolíticos de baja ESR, diseñados para suavizar las oscilaciones de voltaje en la salida del convertidor.
  - **Panasonic EEH-ZA Series**: Capacitores de polímero sólido con alta capacidad de corriente y baja resistencia, perfectos para filtrado en convertidores Buck.

### 5. **Controlador PWM**
- **Modelos recomendados**:
  - **Texas Instruments LM2596**: Controlador de conmutación Buck con regulación precisa, eficiente para manejar potencias de entrada de hasta 300W.
  - **STMicroelectronics L7986A**: Controlador de modo síncrono Buck para aplicaciones de alta eficiencia y regulación precisa.

### 6. **Protección de sobrecorriente y sobrevoltaje**
- **Modelos recomendados**:
  - **Littelfuse 0154005.MAT1**: Fusibles de alta velocidad para proteger el circuito contra sobrecorriente.
  - **Bourns MF-R090**: Fusibles reseteables para proteger contra cortocircuitos y sobrecalentamiento en el convertidor Buck.

### Consideraciones de diseño

1. **Frecuencia de conmutación**: Se recomienda una frecuencia de conmutación entre **50 kHz y 100 kHz**. A frecuencias más altas, puedes reducir el tamaño del inductor y capacitores, pero las pérdidas por conmutación pueden aumentar.
   
2. **Disipación de calor**: Dado que se manejarán corrientes elevadas (hasta 22.5 A en la salida), es importante incluir **disipadores de calor** para los MOSFETs y posiblemente un ventilador para mantener el sistema en condiciones térmicas adecuadas.

3. **Control de la eficiencia**: Utilizar componentes como MOSFETs con baja resistencia Rds(on) y diodos Schottky de alta velocidad minimiza las pérdidas en la conversión, lo que es crucial para mantener la eficiencia en el 90%.

4. **Capacidad del inductor**: El inductor debe ser dimensionado correctamente para evitar la saturación a corrientes elevadas. Un inductor con baja resistencia DC reducirá las pérdidas por calor en el sistema.

## Aplicaciones
- Reguladores de voltaje para dispositivos electrónicos que requieren una entrada de potencia elevada.
- Sistemas de conversión de energía para baterías o fuentes de energía renovable.
- Fuentes de alimentación para sistemas embebidos y microcontroladores de alta demanda.
