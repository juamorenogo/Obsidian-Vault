2024-10-03 22:16

Tags: #Thyristor #Fluss #Potencia
 

## Switches PE

Un switch ideal PE se define como un elemento de 3 terminales; _in_ , _out_ y _control_ que tiene un consumo de 0 Watts.

## Tipos de switches

Se asume una tensión  _0 V_ , una corriente de fuga de _0 A_ y un cambio instantáneo de estado. Se clasifican como:
* Uncontrolled switch: Sin terminal de control. _(Diodo)_
* Semi-controlled switch: Con terminal de control pero limitacion en su accionar _(SCR / Thyristor)._
	En el caso de un _Thyristor_ por el terminal de control se puede "prender" permitiendo el paso de corriente (Funcionando como un diodo), no obstante, no se puede apagar sin un circuito adicional. 

		Dispositivo PNPN : Thyristor -> Caso especial SRC, TRIAC, DIAC
	
	_SRC:_  Simbolo usado para un SRC (silicon controller rectifier) siendo el caso mas básico de Thyristor que es unidireccional como un diodo. Se mantendra prendido mientras _iA > Holding current (iH)_ siendo  independiente de lo que ocurre en el _gate_ . 
	
	![Thyristor | 500](Imagenes/Thyristor.jpeg)
	
	_Triac:_ Simbolo usado para un Triac (Triode for AC) modelado como 2 _Thyristors_, haciendo que sea tenga un dispositivo bidireccional de corriente para aplicaciones de baja potencia y fase unica (Motores de unica fase).
	
	![Triac | 500](Imagenes/Triac.jpeg) 

	
* Controlled switch: Con terminal de control y control de apagado y cerrado _(BJT , MOSFET , IGBT , GTO THYRISTOR  MCT)_
