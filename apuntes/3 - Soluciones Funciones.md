# Funciones — Soluciones paso a paso

> [!info] Cómo leer las soluciones
> - *En cursiva*: lo que piensa el alumno. Por qué se hace cada paso (**no se escribe en el examen**).
> - Bloques matemáticos: el desarrollo que **sí** se escribe.
> - **✍️ Respuesta:** el texto final que hay que escribir en el examen.
>
> Enunciados en [[2 - Ejercicios Funciones]] · Teoría en [[1 - Teoría Funciones]].

---

## Ejercicio 1 — Concentración de un medicamento

$$C(t)=\frac{a\,t}{t^2+9},\qquad t\geq 0,\ a>0$$

### a) Máximo a las 3 h y valor de $a$

*"Concentración máxima" significa **máximo de la función**. Para encontrarlo derivo e igualo a $0$. Como me piden demostrarlo "para cualquier $a$", trabajo con $a$ como si fuera un número.*

*Derivada de un cociente: $\left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}$, con $f=at$ y $g=t^2+9$.*

$$C'(t)=\frac{a\,(t^2+9)-a\,t\cdot 2t}{(t^2+9)^2}=\frac{a\,(9-t^2)}{(t^2+9)^2}$$

$$C'(t)=0 \iff a(9-t^2)=0 \overset{a\neq0}{\iff} t^2=9 \iff t=\pm3$$

*$t=-3$ no tiene sentido (tiempo negativo). Compruebo que $t=3$ es un **máximo** con el signo de $C'$. El denominador y $a$ son siempre positivos, así que el signo lo decide $9-t^2$.*

| $t$ | $(0,\,3)$ | $3$ | $(3,\,+\infty)$ |
|---|---|---|---|
| Signo de $C'(t)$ | $+$ | $0$ | $-$ |
| $C(t)$ | ↗ | máx. | ↘ |

*Ahora uso el dato: el valor máximo, $C(3)$, es $6$.*

$$C(3)=\frac{3a}{9+9}=\frac{a}{6}=6 \;\Longrightarrow\; a=36$$

> **✍️ Respuesta:** Para cualquier $a>0$, $C'(t)>0$ en $(0,3)$ y $C'(t)<0$ en $(3,+\infty)$, luego la concentración es máxima a las 3 horas. Como $C(3)=6$, se obtiene $a=36$. Por tanto $C(t)=\dfrac{36t}{t^2+9}$.

### b) Dominio, continuidad y derivabilidad

*Función racional: el problema sería que el denominador valga $0$.*

$$t^2+9=0 \iff t^2=-9 \quad \text{(sin solución real)}$$

*El denominador nunca se anula, así que como función matemática vale para todo $\mathbb{R}$. Pero $t$ es un tiempo **desde que se toma** el medicamento, así que $t\geq0$. Las racionales son continuas y derivables en su dominio.*

> **✍️ Respuesta:** Como función matemática, $\text{Dom}(C)=\mathbb{R}$, ya que $t^2+9\neq0$ para todo $t$. En el contexto, $\text{Dom}(C)=[0,+\infty)$, porque el tiempo no puede ser negativo. $C$ es una función racional cuyo denominador no se anula nunca, por lo que es continua y derivable en todo su dominio.

### c) Concentración inicial y cuándo es nula

*"En el momento de tomarlo" es $t=0$. "Es nula" significa $C(t)=0$ (corte con el eje horizontal).*

$$C(0)=\frac{0}{9}=0 \qquad\quad C(t)=0\iff 36t=0\iff t=0$$

> **✍️ Respuesta:** Al tomar el medicamento la concentración es $0$ mg/l (la gráfica pasa por $(0,0)$). No vuelve a ser nula en ningún otro instante, porque la única solución de $C(t)=0$ es $t=0$.

### d) Cuándo aumenta y cuándo disminuye

*"Aumenta / disminuye" es **monotonía**. Ya tengo la tabla del apartado a), ahora con $a=36$.*

$$C'(t)=\frac{36\,(9-t^2)}{(t^2+9)^2}$$

> **✍️ Respuesta:** La concentración aumenta durante las 3 primeras horas, en $(0,3)$, y disminuye a partir de entonces, en $(3,+\infty)$. Alcanza un máximo de $6$ mg/l a las 3 horas: punto $(3,\,6)$.

### e) Periodo de eficacia

*"Al menos 3,6" significa $\geq 3{,}6$: es una **inecuación**. Puedo multiplicar por $t^2+9$ sin cambiar el sentido de la desigualdad, porque siempre es positivo.*

$$\frac{36t}{t^2+9}\geq 3{,}6 \iff 36t\geq 3{,}6\,t^2+32{,}4 \iff 3{,}6\,t^2-36t+32{,}4\leq 0 \overset{:3{,}6}{\iff} t^2-10t+9\leq0$$

$$t^2-10t+9=0 \iff t=\frac{10\pm\sqrt{100-36}}{2}=\frac{10\pm8}{2}\iff t=1,\ t=9$$

*Es una parábola que se abre hacia arriba, así que es $\leq0$ **entre** las raíces.*

| $t$ | $(0,1)$ | $(1,9)$ | $(9,+\infty)$ |
|---|---|---|---|
| $t^2-10t+9$ | $+$ | $-$ | $+$ |

> **✍️ Respuesta:** El medicamento es eficaz para $t\in[1,\,9]$, es decir, desde la primera hora hasta la novena después de tomarlo: durante **8 horas**.

### f) Comportamiento a largo plazo

*"A largo plazo" significa $t\to+\infty$. Es un $\frac{\infty}{\infty}$ de polinomios y el grado del denominador es mayor, así que el límite es $0$. Si el límite en $\infty$ es un número, hay **AH**.*

$$\lim_{t\to+\infty}\frac{36t}{t^2+9}=0$$

*AV no hay, porque el dominio no tiene "huecos". AO tampoco, porque ya hay AH.*

> **✍️ Respuesta:** $\lim\limits_{t\to+\infty}C(t)=0$, luego $y=0$ es una asíntota horizontal. A largo plazo el medicamento se va eliminando y la concentración tiende a $0$ mg/l, aunque nunca llega a ser exactamente cero. No hay asíntotas verticales ni oblicuas.

### g) Velocidad inicial y recta tangente en $t=0$

*"Velocidad a la que aumenta" es la **derivada**. "Justo al tomarlo" es $t=0$. Para la tangente necesito el punto $(0, C(0))$ y la pendiente $C'(0)$.*

$$C(0)=0 \qquad C'(0)=\frac{36\cdot 9}{9^2}=4$$

$$y-C(0)=C'(0)\,(t-0)\;\Longrightarrow\; y=4t$$

> **✍️ Respuesta:** En el momento de tomarlo, la concentración aumenta a una velocidad de $4$ mg/l por hora. La recta tangente en $t=0$ es $y=4t$: indica cómo crecería la concentración si mantuviera esa velocidad inicial. Es una buena aproximación solo para valores de $t$ cercanos a $0$.

### h) Curvatura e instante de máxima disminución

*"Disminuye más rápidamente" significa que la derivada $C'$ (la velocidad) es **mínima** (lo más negativa posible). Los máximos y mínimos de $C'$ se buscan con $C''=0$, es decir, en los **puntos de inflexión**.*

*Derivo $C'(t)=36\,(9-t^2)\,(t^2+9)^{-2}$ con la regla del producto y la regla de la cadena:*

$$C''(t)=36\left[-2t\,(t^2+9)^{-2}+(9-t^2)\cdot(-2)(t^2+9)^{-3}\cdot 2t\right]$$

*Saco factor común $(t^2+9)^{-3}$:*

$$C''(t)=\frac{36\left[-2t(t^2+9)-4t(9-t^2)\right]}{(t^2+9)^3}=\frac{36\,(2t^3-54t)}{(t^2+9)^3}=\frac{72\,t\,(t^2-27)}{(t^2+9)^3}$$

$$C''(t)=0\iff t=0 \ \text{ o } \ t^2=27\iff t=0,\ t=\pm 3\sqrt3$$

*En contexto solo vale $t=3\sqrt3\approx5{,}2$. $t=0$ es el borde del dominio, así que no puede ser punto de inflexión. El denominador es positivo: el signo lo dan $t$ y $t^2-27$.*

| $t$ | $(0,\,3\sqrt3)$ | $3\sqrt3$ | $(3\sqrt3,\,+\infty)$ |
|---|---|---|---|
| $t$ | $+$ | | $+$ |
| $t^2-27$ | $-$ | $0$ | $+$ |
| $C''(t)$ | $-$ | $0$ | $+$ |
| $C(t)$ | convexa ◠ | P. I. | cóncava ◡ |

*Calculo la concentración y la velocidad en ese instante:*

$$C(3\sqrt3)=\frac{36\cdot3\sqrt3}{27+9}=3\sqrt3\approx5{,}20 \qquad C'(3\sqrt3)=\frac{36\,(9-27)}{(27+9)^2}=\frac{-648}{1296}=-0{,}5$$

*Mientras $C''<0$, $C'$ decrece, y después crece. Por tanto $C'$ es mínima en $t=3\sqrt3$. Paso a horas y minutos: $0{,}196\cdot60\approx12$ min.*

> **✍️ Respuesta:** $C$ es convexa ◠ en $(0,\,3\sqrt3)$ y cóncava ◡ en $(3\sqrt3,\,+\infty)$, con un punto de inflexión en $(3\sqrt3,\,3\sqrt3)\approx(5{,}20;\ 5{,}20)$. La concentración disminuye más rápidamente a las $3\sqrt3\approx5{,}2$ horas (unas 5 h 12 min). En ese instante disminuye a $0{,}5$ mg/l por hora y la concentración es de unos $5{,}20$ mg/l.

### i) Representación

*Resumen: pasa por $(0,0)$, sube con pendiente 4 hasta el máximo $(3,6)$, baja, cambia de curvatura en $(5{,}2;\ 5{,}2)$ y se acerca a $y=0$ sin tocarla. Puntos de apoyo: $(1;\ 3{,}6)$ y $(9;\ 3{,}6)$, del apartado e), y $C(12)=\frac{432}{153}\approx2{,}82$.*

![[ej1_concentracion.svg|560]]

---

## Ejercicio 2 — Función con parámetros

$$f(x)=\frac{x^2+a\,x+b}{x-1}$$

### a) Continuidad según $a$ y $b$

*Racional: es continua en su dominio. El único punto problemático es donde se anula el denominador, $x=1$. Allí $f(1)$ no existe, así que **siempre** hay discontinuidad. Lo que cambia es el **tipo**, y depende de si el numerador también se anula en $x=1$.*

$$\text{Numerador en } x=1:\quad 1+a+b$$

**Caso 1: $1+a+b\neq0$.** *Queda $\frac{k}{0}$ con $k\neq0$, así que el límite es $\pm\infty$.*

$$\lim_{x\to1}f(x)=\frac{1+a+b}{0}=\pm\infty \;\Rightarrow\; \text{discontinuidad inevitable de salto infinito (AV)}$$

**Caso 2: $1+a+b=0$, es decir, $b=-1-a$.** *Queda $\frac00$. Factorizo el numerador sabiendo que $x=1$ es raíz.*

$$x^2+ax-1-a=(x-1)(x+1+a) \;\Rightarrow\; \lim_{x\to1}\frac{(x-1)(x+1+a)}{x-1}=\lim_{x\to1}(x+1+a)=2+a$$

*El límite existe y es finito, pero $f(1)$ no existe: es un "agujero".*

*Derivable en $x=1$: imposible, porque para ser derivable hay que ser continua.*

> **✍️ Respuesta:** $f$ es continua en $\mathbb{R}-\{1\}$ para cualesquiera $a$ y $b$. En $x=1$:
> - Si $a+b\neq-1$: discontinuidad inevitable de salto infinito ($x=1$ es asíntota vertical).
> - Si $a+b=-1$: discontinuidad evitable, ya que $\lim\limits_{x\to1}f(x)=2+a$ pero $f(1)$ no existe.
>
> En ningún caso es derivable en $x=1$, porque no es continua en ese punto.

### b) Cálculo de $a$ y $b$

*Traduzco cada dato a una ecuación (diccionario de la teoría):*
- *"Pasa por $(2,8)$" se traduce en $f(2)=8$.*
- *"Tangente paralela al eje de abscisas en $x=3$" significa tangente horizontal, pendiente $0$, es decir, $f'(3)=0$.*

$$f(2)=\frac{4+2a+b}{2-1}=8\;\Longrightarrow\; 2a+b=4$$

$$f'(x)=\frac{(2x+a)(x-1)-(x^2+ax+b)\cdot1}{(x-1)^2}=\frac{x^2-2x-a-b}{(x-1)^2}$$

$$f'(3)=\frac{9-6-a-b}{4}=0\;\Longrightarrow\; a+b=3$$

$$\begin{cases}2a+b=4\\ a+b=3\end{cases}\;\overset{(1)-(2)}{\Longrightarrow}\; a=1,\quad b=2$$

> **✍️ Respuesta:** $a=1$, $b=2$, y la función es $f(x)=\dfrac{x^2+x+2}{x-1}$.

### c) Dominio, cortes y asíntotas

**Dominio.** $x-1=0\iff x=1$.

**Cortes.**

$$\text{Eje X: } x^2+x+2=0,\quad \Delta=1-8=-7<0 \;\Rightarrow\; \text{no hay solución}$$
$$\text{Eje Y: } f(0)=\frac{2}{-1}=-2 \;\Rightarrow\; (0,-2)$$

**AV.** *Candidato: $x=1$. Numerador en 1: $1+1+2=4$. Miro el signo del denominador a cada lado.*

$$\lim_{x\to1^-}\frac{x^2+x+2}{x-1}=\frac{4}{0^-}=-\infty \qquad \lim_{x\to1^+}\frac{x^2+x+2}{x-1}=\frac{4}{0^+}=+\infty$$

**AH.** *Grado del numerador (2) mayor que el del denominador (1): el límite es infinito y no hay AH.*

$$\lim_{x\to\pm\infty}f(x)=\pm\infty$$

**AO.** *Grado del numerador = grado del denominador + 1: hay AO.*

$$m=\lim_{x\to\pm\infty}\frac{f(x)}{x}=\lim_{x\to\pm\infty}\frac{x^2+x+2}{x^2-x}=1$$
$$n=\lim_{x\to\pm\infty}\left(\frac{x^2+x+2}{x-1}-x\right)=\lim_{x\to\pm\infty}\frac{x^2+x+2-x^2+x}{x-1}=\lim_{x\to\pm\infty}\frac{2x+2}{x-1}=2$$

*Atajo: al dividir, $x^2+x+2=(x-1)(x+2)+4$, de donde $f(x)=x+2+\dfrac{4}{x-1}$. El cociente $x+2$ es la AO.*

**Posición.** *Signo de $f(x)-(x+2)=\dfrac{4}{x-1}$.*

$$x\to+\infty:\ \frac{4}{x-1}>0 \ (\text{encima}) \qquad x\to-\infty:\ \frac{4}{x-1}<0\ (\text{debajo})$$

> **✍️ Respuesta:** $\text{Dom}(f)=\mathbb{R}-\{1\}$. No corta al eje X; corta al eje Y en $(0,-2)$.
> - Asíntota vertical $x=1$, con $\lim\limits_{x\to1^-}f(x)=-\infty$ y $\lim\limits_{x\to1^+}f(x)=+\infty$.
> - No tiene asíntotas horizontales.
> - Asíntota oblicua $y=x+2$ (en $+\infty$ y en $-\infty$). La gráfica queda por encima de ella cuando $x\to+\infty$ y por debajo cuando $x\to-\infty$.

### d) Monotonía y extremos

$$f'(x)=\frac{x^2-2x-3}{(x-1)^2}=\frac{(x-3)(x+1)}{(x-1)^2}$$

$$f'(x)=0\iff x=3,\ x=-1$$

*En la tabla incluyo los puntos críticos $-1$ y $3$ **y** el $1$ (fuera del dominio). El denominador es un cuadrado, siempre positivo.*

| $x$ | $(-\infty,-1)$ | $-1$ | $(-1,1)$ | $1$ | $(1,3)$ | $3$ | $(3,+\infty)$ |
|---|---|---|---|---|---|---|---|
| $x-3$ | $-$ | | $-$ | | $-$ | $0$ | $+$ |
| $x+1$ | $-$ | $0$ | $+$ | | $+$ | | $+$ |
| $f'(x)$ | $+$ | $0$ | $-$ | ∄ | $-$ | $0$ | $+$ |
| $f(x)$ | ↗ | máx. | ↘ | ∄ | ↘ | mín. | ↗ |

$$f(-1)=\frac{1-1+2}{-2}=-1 \qquad f(3)=\frac{9+3+2}{2}=7$$

*¿Máximo $-1$ menor que mínimo $7$? Son **relativos**: cada uno es extremo "en su zona", y las dos zonas están separadas por la AV. Absolutos no hay, porque la función alcanza valores tan grandes o tan pequeños como queramos (límites $\pm\infty$).*

> **✍️ Respuesta:** $f$ es creciente en $(-\infty,-1)\cup(3,+\infty)$ y decreciente en $(-1,1)\cup(1,3)$. Tiene un máximo relativo en $(-1,-1)$ y un mínimo relativo en $(3,7)$. Que el máximo esté más bajo que el mínimo no es contradictorio: los extremos son relativos y están en ramas distintas de la gráfica, separadas por la asíntota $x=1$. $f$ no tiene extremos absolutos, ya que $\lim\limits_{x\to1^+}f(x)=+\infty$ y $\lim\limits_{x\to1^-}f(x)=-\infty$.

### e) Curvatura

*Derivar otra vez el cociente es largo. Es más rápido usar $f(x)=x+2+4(x-1)^{-1}$:*

$$f'(x)=1-4(x-1)^{-2} \qquad f''(x)=8(x-1)^{-3}=\frac{8}{(x-1)^3}$$

*$f''$ nunca vale $0$ (numerador $8$). Su signo es el de $(x-1)^3$, es decir, el de $x-1$.*

| $x$ | $(-\infty,1)$ | $1$ | $(1,+\infty)$ |
|---|---|---|---|
| $f''(x)$ | $-$ | ∄ | $+$ |
| $f(x)$ | convexa ◠ | ∄ | cóncava ◡ |

> **✍️ Respuesta:** $f$ es convexa ◠ en $(-\infty,1)$ y cóncava ◡ en $(1,+\infty)$. No tiene puntos de inflexión: la curvatura cambia en $x=1$, pero ese punto no pertenece al dominio.

### f) Tangentes paralelas a $3x+y=5$

*"Paralela" significa misma pendiente. Despejo $y$ para verla: $y=-3x+5$, luego $m=-3$. Busco dónde $f'(x)=-3$.*

$$\frac{x^2-2x-3}{(x-1)^2}=-3 \iff x^2-2x-3=-3(x^2-2x+1) \iff 4x^2-8x=0\iff 4x(x-2)=0$$

$$x=0 \quad\text{o}\quad x=2$$

*Para cada punto calculo $f$ y aplico $y-f(a)=f'(a)(x-a)$ con $f'(a)=-3$.*

$$x=0:\ f(0)=-2 \;\Rightarrow\; y+2=-3x \;\Rightarrow\; y=-3x-2$$
$$x=2:\ f(2)=8 \;\Rightarrow\; y-8=-3(x-2) \;\Rightarrow\; y=-3x+14$$

> **✍️ Respuesta:** Hay dos rectas tangentes paralelas a $3x+y=5$: $y=-3x-2$, en el punto $(0,-2)$, e $y=-3x+14$, en el punto $(2,8)$.

### g) Representación

*Resumen: AV $x=1$, AO $y=x+2$. Rama izquierda: viene de $-\infty$ por debajo de la AO, sube hasta el máximo $(-1,-1)$, baja pasando por $(0,-2)$ y cae a $-\infty$ junto a $x=1$; es convexa ◠. Rama derecha: baja desde $+\infty$ junto a $x=1$ hasta el mínimo $(3,7)$, pasa por $(2,8)$ y sube pegándose a la AO por encima; es cóncava ◡.*

![[ej2_parametros.svg|560]]

---

## Ejercicio 3 — Función a trozos

$$
f(x)=\begin{cases}
\dfrac{a\,x+b}{x+2} & \text{si } x\leq 0\\[3mm]
1+\ln(x+1) & \text{si } x>0
\end{cases}
$$

### a) Dominio

*Cada trozo solo importa **en su intervalo**. Miro el problema de cada expresión y si cae dentro de su trozo.*

$$\text{Trozo 1 } (x\leq0):\quad x+2=0\iff x=-2,\ \text{y como } -2\leq 0,\ \text{se excluye.}$$
$$\text{Trozo 2 } (x>0):\quad x+1>0\iff x>-1,\ \text{que se cumple para todo } x>0.$$

> **✍️ Respuesta:** $\text{Dom}(f)=\mathbb{R}-\{-2\}$. El denominador del primer trozo se anula en $x=-2$, que pertenece a su intervalo ($x\leq0$), así que se excluye. El logaritmo exige $x>-1$, pero el segundo trozo solo se usa para $x>0$, donde siempre se cumple; por eso no excluye ningún punto.

### b) Continuidad y derivabilidad en $x=0$

*"Sin levantar el lápiz" significa **continua**; "sin picos" significa **derivable**. Planteo las dos condiciones en $x=0$. Como $0$ entra en el primer trozo ($x\leq0$), $f(0)$ se calcula con ese trozo.*

**Continuidad:**

$$f(0)=\frac{b}{2}\qquad \lim_{x\to0^-}\frac{ax+b}{x+2}=\frac b2 \qquad \lim_{x\to0^+}\big(1+\ln(x+1)\big)=1+\ln1=1$$

$$\frac b2=1\;\Longrightarrow\; b=2$$

**Derivabilidad:** *derivo cada trozo en su intervalo **abierto** y sustituyo $x=0$.*

$$f'(x)=\begin{cases}\dfrac{a(x+2)-(ax+b)}{(x+2)^2}=\dfrac{2a-b}{(x+2)^2} & \text{si } x<0,\ x\neq-2\\[3mm] \dfrac{1}{x+1} & \text{si } x>0\end{cases}$$

$$f'(0^-)=\frac{2a-b}{4}\qquad f'(0^+)=\frac{1}{1}=1$$

$$\frac{2a-2}{4}=1\;\Longrightarrow\; 2a-2=4\;\Longrightarrow\; a=3$$

*Casos "malos": si $b=2$ pero $a\neq3$, la función es continua pero las derivadas laterales no coinciden y hay un pico. Si $b\neq2$, los límites laterales son finitos ($\frac b2$ y $1$) pero distintos, y hay un salto.*

> **✍️ Respuesta:** Para que $f$ sea continua y derivable en $x=0$ hace falta $b=2$ y $a=3$.
> - Si $b=2$ y $a\neq3$, $f$ es continua en $x=0$ pero no derivable: hay un punto anguloso.
> - Si $b\neq2$, $f$ tiene en $x=0$ una discontinuidad inevitable de salto finito (y por tanto no es derivable).

### c) Puntos de corte

*Con $a=3$, $b=2$. Corte con el eje X: resuelvo $f(x)=0$ **en cada trozo** y compruebo que la solución pertenece a ese trozo.*

$$\text{Trozo 1: } \frac{3x+2}{x+2}=0\iff x=-\frac23 \quad (\leq 0\ ✅)$$
$$\text{Trozo 2: } 1+\ln(x+1)=0\iff \ln(x+1)=-1\iff x=e^{-1}-1\approx-0{,}63 \quad (\text{no es}>0\ ❌)$$
$$\text{Eje Y: } f(0)=\frac{2}{2}=1$$

> **✍️ Respuesta:** Corta al eje X en $\left(-\tfrac23,\,0\right)$ y al eje Y en $(0,\,1)$. La solución $x=e^{-1}-1$ del segundo trozo se descarta porque no cumple $x>0$.

### d) Asíntotas

**AV.** *Candidatos: $x=-2$ (fuera del dominio) y $x=0$ (unión). En $x=0$ es continua, así que no hay AV. En $x=-2$, el numerador vale $3(-2)+2=-4$.*

$$\lim_{x\to-2^-}\frac{3x+2}{x+2}=\frac{-4}{0^-}=+\infty \qquad \lim_{x\to-2^+}\frac{3x+2}{x+2}=\frac{-4}{0^+}=-\infty$$

**En $-\infty$** (trozo 1): *mismo grado arriba y abajo; el límite es el cociente de los coeficientes principales.*

$$\lim_{x\to-\infty}\frac{3x+2}{x+2}=3 \;\Rightarrow\; \text{AH } y=3$$

*Posición:* $f(x)-3=\dfrac{3x+2-3x-6}{x+2}=\dfrac{-4}{x+2}$. *Para $x\to-\infty$, $x+2<0$, así que es positivo y la gráfica queda encima.*

**En $+\infty$** (trozo 2):

$$\lim_{x\to+\infty}\big(1+\ln(x+1)\big)=+\infty \;\Rightarrow\; \text{no hay AH}$$
$$m=\lim_{x\to+\infty}\frac{1+\ln(x+1)}{x}=0 \;\Rightarrow\; \text{no hay AO}$$

*El logaritmo crece más despacio que $x$ (órdenes de infinito). Como $m=0$, no hay recta oblicua.*

> **✍️ Respuesta:** $f$ tiene una asíntota vertical $x=-2$, con $\lim\limits_{x\to-2^-}f(x)=+\infty$ y $\lim\limits_{x\to-2^+}f(x)=-\infty$. Tiene una asíntota horizontal $y=3$ cuando $x\to-\infty$, y la gráfica queda por encima de ella. Cuando $x\to+\infty$, $f(x)\to+\infty$ sin asíntota horizontal ni oblicua: crece cada vez más despacio.

### e) Monotonía

*Uso las derivadas del apartado b) con $a=3$, $b=2$. En $x=0$ es derivable y $f'(0)=1$.*

$$f'(x)=\begin{cases}\dfrac{4}{(x+2)^2} & \text{si } x\leq 0,\ x\neq-2\\[3mm] \dfrac{1}{x+1} & \text{si } x>0\end{cases}$$

*Primer trozo: $4$ entre un cuadrado, siempre positivo. Segundo trozo: con $x>0$, $x+1>0$, también positivo. Nunca vale $0$, así que no hay tangentes horizontales ni extremos.*

| $x$ | $(-\infty,-2)$ | $-2$ | $(-2,0)$ | $0$ | $(0,+\infty)$ |
|---|---|---|---|---|---|
| $f'(x)$ | $+$ | ∄ | $+$ | $1$ | $+$ |
| $f(x)$ | ↗ | ∄ | ↗ | | ↗ |

*¿$x_1<x_2 \Rightarrow f(x_1)<f(x_2)$ siempre? No: la AV "rompe" la gráfica. Contraejemplo: $f(-3)=\frac{-7}{-1}=7$ y $f(0)=1$.*

> **✍️ Respuesta:** $f'(x)>0$ en todo su dominio, luego $f$ es creciente en $(-\infty,-2)\cup(-2,+\infty)$. No tiene extremos relativos ni puntos con tangente horizontal, porque $f'(x)\neq0$ siempre. Sin embargo, no es cierto que $x_1<x_2$ implique siempre $f(x_1)<f(x_2)$: por ejemplo, $-3<0$ pero $f(-3)=7>f(0)=1$. Esto ocurre porque el dominio está "cortado" en $x=-2$.

### f) Curvatura

$$f''(x)=\begin{cases}\dfrac{-8}{(x+2)^3} & \text{si } x<0,\ x\neq-2\\[3mm] \dfrac{-1}{(x+1)^2} & \text{si } x>0\end{cases}$$

*Primer trozo: el signo depende de $(x+2)^3$. Si $x<-2$, $(x+2)^3<0$ y $f''>0$; si $-2<x<0$, $f''<0$. Segundo trozo: siempre negativo. En $x=0$ los dos dan $-1$: no hay cambio de curvatura.*

| $x$ | $(-\infty,-2)$ | $-2$ | $(-2,0)$ | $0$ | $(0,+\infty)$ |
|---|---|---|---|---|---|
| $f''(x)$ | $+$ | ∄ | $-$ | $-1$ | $-$ |
| $f(x)$ | cóncava ◡ | ∄ | convexa ◠ | | convexa ◠ |

> **✍️ Respuesta:** $f$ es cóncava ◡ en $(-\infty,-2)$ y convexa ◠ en $(-2,+\infty)$. No tiene puntos de inflexión: el único cambio de curvatura es en $x=-2$, que no pertenece al dominio.

### g) Rectas tangentes

*Corte con el eje X: $x=-\frac23$, del apartado c), con $f\!\left(-\frac23\right)=0$. Pendiente con el trozo 1:*

$$f'\!\left(-\tfrac23\right)=\frac{4}{\left(\frac43\right)^2}=\frac{4}{\frac{16}{9}}=\frac94$$
$$y-0=\frac94\left(x+\frac23\right)\;\Longrightarrow\; y=\frac94x+\frac32$$

*Unión de los trozos: $x=0$, con $f(0)=1$ y $f'(0)=1$.*

$$y-1=1\cdot(x-0)\;\Longrightarrow\; y=x+1$$

> **✍️ Respuesta:** La recta tangente en el punto de corte con el eje de abscisas, $\left(-\tfrac23,0\right)$, es $y=\tfrac94x+\tfrac32$. La recta tangente en el punto de unión, $(0,1)$, es $y=x+1$, y es la misma para los dos trozos, porque $f$ es derivable en $x=0$.

### h) Representación

*Resumen: rama izquierda ($x<-2$): sale de la AH $y=3$ por encima y sube a $+\infty$ junto a $x=-2$; es cóncava ◡. Rama central: sube desde $-\infty$ junto a $x=-2$, pasa por $\left(-\tfrac23,0\right)$ y $(0,1)$ y continúa sin pico con el logaritmo, que sigue subiendo cada vez más despacio; es convexa ◠. Puntos de apoyo: $f(-4)=5$, $f(-3)=7$, $f(-1)=-1$, $f(1)=1+\ln2\approx1{,}69$, $f(3)=1+\ln4\approx2{,}39$.*

![[ej3_trozos.svg|560]]
