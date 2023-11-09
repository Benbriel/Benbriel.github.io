---
title: 'T5SCA'
date: 2023-03-03
excerpt: "This is T5SCA"
category: SCA
---
Se realizó una simulación de la evolución de un sistema de dos niveles conectado a un baño térmico. El Hamiltoniano del sistema es

\begin{equation}
  H = \frac{\Delta}{2} \sigma^z + \Omega \sigma^x
\end{equation}

El sistema se simuló de $t = 0$ a $t  = t_f = 150$, con distintos $\{ \Omega \} = \{ \gamma \} =\text{linspace}(\Delta/10, \Delta, 10)$. Cada $\Omega$ se simuló con 100 semillas distintas, y un array de 1000 tiempos equidistantes. A continuación se muestran algunos resultados para distintos $\Omega$ y semillas.

En primera instancia, se puede notar que tanto la amplitud como la frecuencia de oscilación entre estados $\ket{g}$ y $\ket{e}$ aumentan con $\Omega$. Esto es un comportamiento esperado de tal sistema en la frecuencia de Rabi, que es la frecuencia de resonancia $\gamma = \Omega$ del sistema.

Por otro lado, vemos que el sistema, mientras no haya saltos, muestra un comportamiento de oscilador armónico amortiguado sobre un centro que tiende a un valor entre $0$ y $1$, dependiendo de $\Omega$. Se simuló algunas veces para $\Omega > \Delta$, y se vio como este límite parece converger a $\alpha=0.5$ para $\Omega$ grandes.

En la figura \ref{fig:net} se puede ver tanto $n_+$ como $n_-$ y $n_{net} = n_+ - n_-$ con respecto a 100 simulaciones hasta $t_f$. Se observa cómo $n_+/t_f$ y $n_-/t_f$ aumentan con $\Omega$, mientras que $n_{net}/t_f$ disminuye. Lo primero ocurre porque la probabilidad de saltos aumenta con $\Omega$, debido a que $H_C$ aumenta y, por ende, la norma de $\ket{\psi}$ disminuye más rápido con respecto a $\tau$. Lo segundo ocurre porque (aparentemente) a partir de $\Omega = \Delta/2$ es más probable que $k=0$ sea escogido para realizar el salto. En este caso los $n$ representan interacciones con el baño, donde un aumento en $n_+$ se puede relacionar con la absorción de energía, y para $n_-$ la emisión de la misma. Por lo tanto, $n_{net}$ representa la energía total absorbida por el sistema. (Si el baño fuera un láser, por ejemplo, entonces $-n_{net}$ podría ser la cantidad de fotones emitidos por el sistema. Se puede notar que $n_{net}$ nunca será mayor a 1, ya que el sistema tiene solo dos niveles.)

La figura \ref{fig:excited} muestra los promedios de las trayectorias para distintos $\Omega$, y se puede ver que la probabilidad de que el sistema esté en el estado $\ket{e}$ se comporta de forma browniana, pero convergiendo hasta un valor $\alpha$ que disminuye con $\Omega$.
