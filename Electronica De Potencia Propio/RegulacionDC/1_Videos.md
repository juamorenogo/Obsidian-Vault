2024-10-19 16:15

Tags: #Topologia #Potencia 

# Primer Video

![Video1](https://youtu.be/cX4q0e124C4?si=j6k2GIxVV4WIN-XA)

### Esquemático


![](Imagenes/Diagrama1.png)

---

# Segundo Video

![Limitador de Corriente](https://youtu.be/8uoo5pAeWZI?si=Sz2Bsc3s1KFEHKS4)

*  _IC para regulacion y conmutacion:_  LM2587S ->Simple switcher 5A flyback regulator
Para limitar la corriente se realiza un circuito que va hacia el terminal de feedback del IC. Para eso:

![Circuito de modificacion Feedback](Imagenes/Diagrama2.png)

---
# Tercer Video


![](https://youtu.be/FqT_Ofd54fo?si=tBv_ojucm705dLfL)

Pasos para diseño Buck simple-> Escoger _IC_: 
* Establecer rango de operacion voltaje entrada
* Determinar voltaje de salida
* Determinar maxima corriente de salida

[DC/DC Converters – Mouser](https://www.mouser.com/c/power/dc-dc-converters/?srsltid=AfmBOorSJ_temlc_aFRMOY-lKa8-2LfH7ot_4R8Su2WBiLWjtNTFclX-)

Pagina para mirar diferentes _IC_.

Despues se necesita hallar la corriente maxima de conmutacion:
* Calcular _Duty Cycle_ 
* Calcular el _rizado de corriente de inductor_
* Comparar con _IC_ seleccionado.
* Calcular picos de corriente.
* Seleccionar inductor de acuerdo a esto.

Revisar datos nominales de los demas elementos.

![](Imagenes/Feedback1.png)

---
# Cuarto video


![](https://youtu.be/HOXgOWoN0EY?si=bT1CMxrYeFGIKOGH)

Para el flyback se manera es un acomplamiento de inductancias, no como tal un transformador. La diferencia es que se posiciona un diodo de manera que la energia se almacene en el nucleo del transformador.

### Revisar con mas cuidado.

--- 

# Quinto Video

![](https://youtu.be/W6NOV6b8kxs?si=sYswvj2VCOn1Ukxo)

