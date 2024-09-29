2024-09-29 16:02

Tags: #C

Inicializar se refiere a darle un espacio de memoria a la variable, mas no darle un valor a la misma. 
	- Initialized = The object is given a known value at the point of definition.
	- Assignment = The object is given a known value beyond the point of definition.
	- Uninitialized = The object has not been given a known value yet.

El comportamiento indefinidio puede generarse por la generacion de un codigo que el lenguaje no sabe interpretar correctamente, los sintomas de esto son:
- Your program produces different results every time it is run.
- Your program consistently produces the same incorrect result.
- Your program behaves inconsistently (sometimes produces the correct result, sometimes not).
- Your program seems like it’s working but produces incorrect results later in the program.
- Your program crashes, either immediately or later.
- Your program works on some compilers but not others.
- Your program works until you change some other seemingly unrelated code.
- 
Adicionalmente: ya no quiero