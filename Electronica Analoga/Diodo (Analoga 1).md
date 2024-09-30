2024-09-30 17:06

Tags: #Analoga #Diodos

Elemento de 2 terminales semiconductor con el siguiente símbolo:

![Esquema Del Diodo|300](Imagenes/EsquemaDiodo.png)

La ecuación del Diodo es:

$$ I_{D}= I_{S}(e^{\frac{V_{D}}{nV_{T}}}-1)$$

```tikz
\usepackage{circuitikz}
\begin{document}

\begin{circuitikz}[american, voltage shift=0.5]
\draw (0,0)
to[isource, l=$I_0$, v=$V_0$] (0,3)
to[short, -*, i=$I_0$] (2,3)
to[R=$R_1$, i>_=$i_1$] (2,0) -- (0,0);
\draw (2,3) -- (4,3)
to[R=$R_2$, i>_=$i_2$]
(4,0) to[short, -*] (2,0);
\end{circuitikz}

\end{document}
```
