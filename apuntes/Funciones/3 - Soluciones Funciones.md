# Funciones — Soluciones paso a paso

## Ejercicio 1 — Concentración de un medicamento

$$C(t)=\frac{a\,t}{t^2+9},\qquad t\geq 0,\ a>0$$

### a) Máximo a las 3 h y valor de $a$

Teoría: [[1 - Teoría Funciones#7. Monotonía y extremos|Monotonía y extremos]] · [[1 - Teoría Funciones#2. Derivadas|Derivadas]] · [[1 - Teoría Funciones#11. Optimización|Optimización]]

*Concentración máxima = máximo de la función: derivo e igualo a $0$, tratando $a$ como un número.*

$$C'(t)=\frac{a\,(t^2+9)-a\,t\cdot 2t}{(t^2+9)^2}=\frac{a\,(9-t^2)}{(t^2+9)^2}$$

$$C'(t)=0 \quad\text{cuando}\quad a(9-t^2)=0. \quad\text{Como } a\neq0:\quad t^2=9,\ \text{luego } t=\pm3$$

*$t=-3$ no tiene sentido. El signo de $C'$ lo decide $9-t^2$ ($a$ y el denominador son positivos).*

| $t$ | $(0,\,3)$ | $3$ | $(3,\,+\infty)$ |
|---|---|---|---|
| Signo de $C'(t)$ | $+$ | $0$ | $-$ |
| $C(t)$ | ↗ | máx. | ↘ |

*Uso el dato $C(3)=6$.*

$$C(3)=\frac{3a}{9+9}=\frac{a}{6}=6,\quad\text{luego}\quad a=36$$

> **Respuesta:** Para cualquier $a>0$, $C'(t)>0$ en $(0,3)$ y $C'(t)<0$ en $(3,+\infty)$, luego la concentración es máxima a las 3 horas. Como $C(3)=6$, $a=36$ y $C(t)=\dfrac{36t}{t^2+9}$.

### b) Dominio, continuidad y derivabilidad

Teoría: [[1 - Teoría Funciones#3. Dominio y puntos de corte|Dominio y puntos de corte]] · [[1 - Teoría Funciones#4. Continuidad|Continuidad]] · [[1 - Teoría Funciones#6. Derivabilidad|Derivabilidad]]

$$t^2+9=0 \quad\text{da}\quad t^2=-9 \quad \text{(sin solución real)}$$

*El denominador nunca se anula. En contexto, $t\geq0$.*

> **Respuesta:** Como función matemática, $\text{Dom}(C)=\mathbb{R}$, ya que $t^2+9\neq0$. En el contexto, $\text{Dom}(C)=[0,+\infty)$, porque el tiempo no puede ser negativo. $C$ es racional con denominador que no se anula, luego es continua y derivable en todo su dominio.

### c) Concentración inicial y cuándo es nula

Teoría: [[1 - Teoría Funciones#3. Dominio y puntos de corte|Dominio y puntos de corte]]

*Al tomarlo: $t=0$. Nula: $C(t)=0$.*

$$C(0)=\frac{0}{9}=0 \qquad\quad C(t)=0 \quad\text{solo si}\quad 36t=0,\ \text{es decir, } t=0$$

> **Respuesta:** Al tomar el medicamento la concentración es $0$ mg/l. No vuelve a ser nula, porque la única solución de $C(t)=0$ es $t=0$.

### d) Cuándo aumenta y cuándo disminuye

Teoría: [[1 - Teoría Funciones#7. Monotonía y extremos|Monotonía y extremos]]

*Es monotonía: uso la tabla de a) con $a=36$.*

$$C'(t)=\frac{36\,(9-t^2)}{(t^2+9)^2}$$

> **Respuesta:** La concentración aumenta en $(0,3)$ y disminuye en $(3,+\infty)$. Alcanza un máximo de $6$ mg/l a las 3 horas: punto $(3,\,6)$.

### e) Periodo de eficacia

*Es una inecuación. Multiplico por $t^2+9>0$ sin cambiar el sentido de la desigualdad.*

$$\frac{36t}{t^2+9}\geq 3{,}6 \quad\text{equivale a}\quad 36t\geq 3{,}6\,t^2+32{,}4$$

$$3{,}6\,t^2-36t+32{,}4\leq 0 \quad\text{y, dividiendo entre } 3{,}6,\quad t^2-10t+9\leq0$$

$$t^2-10t+9=0:\quad t=\frac{10\pm\sqrt{100-36}}{2}=\frac{10\pm8}{2},\ \text{luego } t=1 \text{ o } t=9$$

*Parábola hacia arriba: es $\leq0$ entre las raíces.*

| $t$ | $(0,1)$ | $(1,9)$ | $(9,+\infty)$ |
|---|---|---|---|
| $t^2-10t+9$ | $+$ | $-$ | $+$ |

> **Respuesta:** El medicamento es eficaz para $t\in[1,\,9]$, es decir, entre la primera y la novena hora: durante **8 horas**.

### f) Comportamiento a largo plazo

Teoría: [[1 - Teoría Funciones#1. Límites|Límites]] · [[1 - Teoría Funciones#5. Asíntotas|Asíntotas]]

*Largo plazo: $t\to+\infty$. Grado mayor abajo, así que el límite es $0$ y hay AH.*

$$\lim_{t\to+\infty}\frac{36t}{t^2+9}=0$$

*No hay AV (el denominador no se anula) ni AO (ya hay AH).*

> **Respuesta:** $\lim\limits_{t\to+\infty}C(t)=0$, luego $y=0$ es asíntota horizontal: el medicamento se va eliminando y la concentración tiende a $0$ mg/l, aunque nunca llega a cero. No hay asíntotas verticales ni oblicuas.

### g) Velocidad inicial y recta tangente en $t=0$

Teoría: [[1 - Teoría Funciones#10. Recta tangente|Recta tangente]] · [[1 - Teoría Funciones#2. Derivadas|Derivadas]]

*Velocidad = derivada; al tomarlo, $t=0$. Necesito $C(0)$ y $C'(0)$.*

$$C(0)=0 \qquad C'(0)=\frac{36\cdot 9}{9^2}=4$$

$$y-C(0)=C'(0)\,(t-0),\quad\text{luego}\quad y=4t$$

> **Respuesta:** Al tomarlo, la concentración aumenta a $4$ mg/l por hora. La tangente en $t=0$ es $y=4t$: indica cómo crecería la concentración si mantuviera esa velocidad inicial, y solo es una buena aproximación para $t$ cercano a $0$.

### h) Curvatura e instante de máxima disminución

Teoría: [[1 - Teoría Funciones#8. Curvatura y puntos de inflexión|Curvatura y puntos de inflexión]] · [[1 - Teoría Funciones#2. Derivadas|Derivadas]] · [[Tabla f, f' y f''#Qué significa cada signo|Tabla f, f' y f'']]

*Disminuye más rápido = $C'$ mínima (lo más negativa posible). Los extremos de $C'$ están donde $C''=0$: en los puntos de inflexión.*

*Derivo $C'(t)=\dfrac{36\,(9-t^2)}{(t^2+9)^2}$ como un cociente, $\left(\dfrac{u}{v}\right)'=\dfrac{u'v-uv'}{v^2}$. Primero cada parte por separado (el denominador lleva regla de la cadena):*

$$\begin{aligned} u&=36\,(9-t^2) & u'&=-72t \\ v&=(t^2+9)^2 & v'&=2\,(t^2+9)\cdot 2t=4t\,(t^2+9) \end{aligned}$$

*Sustituyo en la fórmula:*

$$C''(t)=\frac{-72t\,(t^2+9)^2-36\,(9-t^2)\cdot 4t\,(t^2+9)}{(t^2+9)^4}$$

*Todos los términos llevan $(t^2+9)$: lo simplifico una vez arriba y abajo.*

$$C''(t)=\frac{-72t\,(t^2+9)-144t\,(9-t^2)}{(t^2+9)^3}=\frac{-72t^3-648t-1296t+144t^3}{(t^2+9)^3}=\frac{72t^3-1944t}{(t^2+9)^3}$$

*Saco factor común $72t$ para estudiar el signo:*

$$C''(t)=\frac{72\,t\,(t^2-27)}{(t^2+9)^3}$$

$$C''(t)=0 \quad\text{cuando}\quad t=0 \text{ o } t^2=27,\ \text{es decir, } t=0 \text{ o } t=\pm 3\sqrt3$$

*En contexto solo vale $t=3\sqrt3\approx5{,}2$ ($t=0$ es el borde del dominio). El signo lo dan $t$ y $t^2-27$.*

| $t$ | $(0,\,3\sqrt3)$ | $3\sqrt3$ | $(3\sqrt3,\,+\infty)$ |
|---|---|---|---|
| $t$ | $+$ | | $+$ |
| $t^2-27$ | $-$ | $0$ | $+$ |
| $C''(t)$ | $-$ | $0$ | $+$ |
| $C(t)$ | convexa ◠ | P. I. | cóncava ◡ |

*Concentración y velocidad en ese instante:*

$$C(3\sqrt3)=\frac{36\cdot3\sqrt3}{27+9}=3\sqrt3\approx5{,}20 \qquad C'(3\sqrt3)=\frac{36\,(9-27)}{(27+9)^2}=\frac{-648}{1296}=-0{,}5$$

*$C''$ pasa de $-$ a $+$, así que $C'$ es mínima en $t=3\sqrt3$. En minutos: $0{,}196\cdot60\approx12$.*

> **Respuesta:** $C$ es convexa ◠ en $(0,\,3\sqrt3)$ y cóncava ◡ en $(3\sqrt3,\,+\infty)$, con punto de inflexión en $(3\sqrt3,\,3\sqrt3)\approx(5{,}20;\ 5{,}20)$. La concentración disminuye más rápido a las $3\sqrt3\approx5{,}2$ horas (unas 5 h 12 min), a $0{,}5$ mg/l por hora, cuando la concentración es de unos $5{,}20$ mg/l.

### i) Representación

Teoría: [[1 - Teoría Funciones#9. Representación gráfica|Representación gráfica]]

*Pasa por $(0,0)$, sube con pendiente 4 hasta el máximo $(3,6)$, baja, cambia de curvatura en $(5{,}2;\ 5{,}2)$ y se acerca a $y=0$ sin llegar a tocarla. Puntos de apoyo: $(1;\ 3{,}6)$, $(9;\ 3{,}6)$, $C(12)\approx2{,}82$ y $C(60)\approx0{,}6$.*

![[ej1_concentracion.svg|760]]

---

## Ejercicio 2 — Función con parámetros

$$f(x)=\frac{x^2+a\,x+b}{x-1}$$

### a) Continuidad según $a$ y $b$

Teoría: [[1 - Teoría Funciones#4. Continuidad|Continuidad]] · [[1 - Teoría Funciones#1. Límites|Límites]] · [[1 - Teoría Funciones#6. Derivabilidad|Derivabilidad]]

*Racional: continua en su dominio. En $x=1$, $f(1)$ no existe, así que siempre hay discontinuidad; el tipo depende de si el numerador también se anula ahí.*

$$\text{Numerador en } x=1:\quad 1+a+b$$

**Caso 1: $1+a+b\neq0$.** *Queda $\frac{k}{0}$: límite infinito.*

$$\lim_{x\to1}f(x)=\frac{1+a+b}{0}=\pm\infty,\quad \text{luego hay discontinuidad inevitable de salto infinito (AV)}$$

**Caso 2: $1+a+b=0$, es decir, $b=-1-a$.** *Queda $\frac00$: factorizo sabiendo que $x=1$ es raíz.*

$$x^2+ax-1-a=(x-1)(x+1+a),\quad\text{luego}\quad \lim_{x\to1}\frac{(x-1)(x+1+a)}{x-1}=\lim_{x\to1}(x+1+a)=2+a$$

*Límite finito pero $f(1)$ no existe: agujero. Al no ser continua en $x=1$, tampoco es derivable.*

> **Respuesta:** $f$ es continua en $\mathbb{R}-\{1\}$ para cualesquiera $a$ y $b$. En $x=1$:
> - Si $a+b\neq-1$: discontinuidad inevitable de salto infinito ($x=1$ es asíntota vertical).
> - Si $a+b=-1$: discontinuidad evitable, ya que $\lim\limits_{x\to1}f(x)=2+a$ pero $f(1)$ no existe.
>
> En ningún caso es derivable en $x=1$, porque no es continua.

### b) Cálculo de $a$ y $b$

Teoría: [[1 - Teoría Funciones#12. Ejercicios con parámetros|Ejercicios con parámetros]] · [[1 - Teoría Funciones#2. Derivadas|Derivadas]]

*"Pasa por $(2,8)$" se traduce en $f(2)=8$. "Tangente paralela al eje de abscisas en $x=3$" se traduce en $f'(3)=0$.*

$$f(2)=\frac{4+2a+b}{2-1}=8,\quad\text{luego}\quad 2a+b=4$$

$$f'(x)=\frac{(2x+a)(x-1)-(x^2+ax+b)\cdot1}{(x-1)^2}=\frac{x^2-2x-a-b}{(x-1)^2}$$

$$f'(3)=\frac{9-6-a-b}{4}=0,\quad\text{luego}\quad a+b=3$$

$$\begin{cases}2a+b=4\\ a+b=3\end{cases}\quad\text{Restando las dos ecuaciones:}\quad a=1,\quad b=2$$

> **Respuesta:** $a=1$, $b=2$, y $f(x)=\dfrac{x^2+x+2}{x-1}$.

### c) Dominio, cortes y asíntotas

Teoría: [[1 - Teoría Funciones#3. Dominio y puntos de corte|Dominio y puntos de corte]] · [[1 - Teoría Funciones#5. Asíntotas|Asíntotas]]

**Dominio.** $x-1=0$ cuando $x=1$.

**Cortes.**

$$\text{Eje X: } x^2+x+2=0,\quad \Delta=1-8=-7<0,\quad\text{luego no hay solución}$$
$$\text{Eje Y: } f(0)=\frac{2}{-1}=-2,\quad\text{punto } (0,-2)$$

**AV.** *Numerador en $x=1$: $4$. Miro el signo del denominador a cada lado.*

$$\lim_{x\to1^-}\frac{x^2+x+2}{x-1}=\frac{4}{0^-}=-\infty \qquad \lim_{x\to1^+}\frac{x^2+x+2}{x-1}=\frac{4}{0^+}=+\infty$$

**AH.** *Grado mayor arriba: no hay AH.*

$$\lim_{x\to\pm\infty}f(x)=\pm\infty$$

**AO.** *Grado de arriba = grado de abajo + 1: hay AO.*

$$m=\lim_{x\to\pm\infty}\frac{f(x)}{x}=\lim_{x\to\pm\infty}\frac{x^2+x+2}{x^2-x}=1$$
$$n=\lim_{x\to\pm\infty}\left(\frac{x^2+x+2}{x-1}-x\right)=\lim_{x\to\pm\infty}\frac{x^2+x+2-x^2+x}{x-1}=\lim_{x\to\pm\infty}\frac{2x+2}{x-1}=2$$

*Atajo: dividiendo, $f(x)=x+2+\dfrac{4}{x-1}$; el cociente $x+2$ es la AO.*

**Posición.** *Signo de $f(x)-(x+2)=\dfrac{4}{x-1}$.*

$$x\to+\infty:\ \frac{4}{x-1}>0 \ (\text{encima}) \qquad x\to-\infty:\ \frac{4}{x-1}<0\ (\text{debajo})$$

> **Respuesta:** $\text{Dom}(f)=\mathbb{R}-\{1\}$. No corta al eje X; corta al eje Y en $(0,-2)$.
> - Asíntota vertical $x=1$, con $\lim\limits_{x\to1^-}f(x)=-\infty$ y $\lim\limits_{x\to1^+}f(x)=+\infty$.
> - No tiene asíntotas horizontales.
> - Asíntota oblicua $y=x+2$: la gráfica queda por encima cuando $x\to+\infty$ y por debajo cuando $x\to-\infty$.

### d) Monotonía y extremos

Teoría: [[1 - Teoría Funciones#7. Monotonía y extremos|Monotonía y extremos]]

$$f'(x)=\frac{x^2-2x-3}{(x-1)^2}=\frac{(x-3)(x+1)}{(x-1)^2}$$

$$f'(x)=0 \quad\text{cuando}\quad x=3 \text{ o } x=-1$$

*Incluyo los críticos $-1$ y $3$ y el $1$ (fuera del dominio). El denominador es siempre positivo.*

| $x$ | $(-\infty,-1)$ | $-1$ | $(-1,1)$ | $1$ | $(1,3)$ | $3$ | $(3,+\infty)$ |
|---|---|---|---|---|---|---|---|
| $x-3$ | $-$ | | $-$ | | $-$ | $0$ | $+$ |
| $x+1$ | $-$ | $0$ | $+$ | | $+$ | | $+$ |
| $f'(x)$ | $+$ | $0$ | $-$ | ∄ | $-$ | $0$ | $+$ |
| $f(x)$ | ↗ | máx. | ↘ | ∄ | ↘ | mín. | ↗ |

$$f(-1)=\frac{1-1+2}{-2}=-1 \qquad f(3)=\frac{9+3+2}{2}=7$$

*Son extremos relativos de ramas distintas, separadas por la AV. No hay absolutos: la función toma valores tan grandes o pequeños como queramos.*

> **Respuesta:** $f$ es creciente en $(-\infty,-1)\cup(3,+\infty)$ y decreciente en $(-1,1)\cup(1,3)$. Tiene un máximo relativo en $(-1,-1)$ y un mínimo relativo en $(3,7)$. Que el máximo esté más bajo que el mínimo no es contradictorio: son relativos y están en ramas distintas, separadas por la asíntota $x=1$. No hay extremos absolutos, ya que $\lim\limits_{x\to1^+}f(x)=+\infty$ y $\lim\limits_{x\to1^-}f(x)=-\infty$.

### e) Curvatura

Teoría: [[1 - Teoría Funciones#8. Curvatura y puntos de inflexión|Curvatura y puntos de inflexión]]

*Más rápido que derivar el cociente: $f(x)=x+2+4(x-1)^{-1}$.*

$$f'(x)=1-4(x-1)^{-2} \qquad f''(x)=8(x-1)^{-3}=\frac{8}{(x-1)^3}$$

*$f''$ nunca vale $0$; su signo es el de $x-1$.*

| $x$ | $(-\infty,1)$ | $1$ | $(1,+\infty)$ |
|---|---|---|---|
| $f''(x)$ | $-$ | ∄ | $+$ |
| $f(x)$ | convexa ◠ | ∄ | cóncava ◡ |

> **Respuesta:** $f$ es convexa ◠ en $(-\infty,1)$ y cóncava ◡ en $(1,+\infty)$. No tiene puntos de inflexión: la curvatura cambia en $x=1$, que no pertenece al dominio.

### f) Tangentes paralelas a $3x+y=5$

Teoría: [[1 - Teoría Funciones#10. Recta tangente|Recta tangente]]

*Paralela = misma pendiente: $y=-3x+5$, $m=-3$. Resuelvo $f'(x)=-3$.*

$$\frac{x^2-2x-3}{(x-1)^2}=-3 \quad\text{equivale a}\quad x^2-2x-3=-3(x^2-2x+1)$$

$$4x^2-8x=0,\quad\text{es decir,}\quad 4x(x-2)=0$$

$$x=0 \quad\text{o}\quad x=2$$

$$x=0:\ f(0)=-2,\quad y+2=-3x,\quad\text{luego}\quad y=-3x-2$$
$$x=2:\ f(2)=8,\quad y-8=-3(x-2),\quad\text{luego}\quad y=-3x+14$$

> **Respuesta:** Las tangentes paralelas a $3x+y=5$ son $y=-3x-2$, en $(0,-2)$, e $y=-3x+14$, en $(2,8)$.

### g) Representación

Teoría: [[1 - Teoría Funciones#9. Representación gráfica|Representación gráfica]]

*AV $x=1$, AO $y=x+2$. Rama izquierda (convexa ◠): viene de $-\infty$ por debajo de la AO, sube al máximo $(-1,-1)$, pasa por $(0,-2)$ y cae a $-\infty$ junto a $x=1$. Rama derecha (cóncava ◡): baja desde $+\infty$ al mínimo $(3,7)$ y sube pegada a la AO por encima.*

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

Teoría: [[1 - Teoría Funciones#3. Dominio y puntos de corte|Dominio y puntos de corte]]

*Cada problema solo cuenta si cae en el intervalo de su trozo.*

$$\text{Trozo 1 } (x\leq0):\quad x+2=0 \text{ cuando } x=-2,\ \text{y como } -2\leq 0,\ \text{se excluye.}$$
$$\text{Trozo 2 } (x>0):\quad x+1>0 \text{ cuando } x>-1,\ \text{que se cumple para todo } x>0.$$

> **Respuesta:** $\text{Dom}(f)=\mathbb{R}-\{-2\}$. El denominador del primer trozo se anula en $x=-2$, que pertenece a su intervalo, así que se excluye. El logaritmo exige $x>-1$, que siempre se cumple en el segundo trozo ($x>0$).

### b) Continuidad y derivabilidad en $x=0$

Teoría: [[1 - Teoría Funciones#4. Continuidad|Continuidad]] · [[1 - Teoría Funciones#6. Derivabilidad|Derivabilidad]] · [[1 - Teoría Funciones#12. Ejercicios con parámetros|Ejercicios con parámetros]]

*Sin levantar el lápiz = continua; sin picos = derivable. $f(0)$ se calcula con el primer trozo ($x\leq0$).*

**Continuidad:**

$$f(0)=\frac{b}{2}\qquad \lim_{x\to0^-}\frac{ax+b}{x+2}=\frac b2 \qquad \lim_{x\to0^+}\big(1+\ln(x+1)\big)=1+\ln1=1$$

$$\frac b2=1,\quad\text{luego}\quad b=2$$

**Derivabilidad:** *derivo cada trozo en su intervalo abierto y sustituyo $x=0$.*

$$f'(x)=\begin{cases}\dfrac{a(x+2)-(ax+b)}{(x+2)^2}=\dfrac{2a-b}{(x+2)^2} & \text{si } x<0,\ x\neq-2\\[3mm] \dfrac{1}{x+1} & \text{si } x>0\end{cases}$$

$$f'(0^-)=\frac{2a-b}{4}\qquad f'(0^+)=\frac{1}{1}=1$$

$$\frac{2a-2}{4}=1,\quad\text{luego}\quad 2a-2=4\quad\text{y}\quad a=3$$

*Si $b=2$ y $a\neq3$: continua pero con pico. Si $b\neq2$: laterales finitos y distintos, salto.*

> **Respuesta:** $f$ es continua y derivable en $x=0$ si $b=2$ y $a=3$.
> - Si $b=2$ y $a\neq3$: continua pero no derivable (punto anguloso).
> - Si $b\neq2$: discontinuidad inevitable de salto finito (y por tanto no derivable).

### c) Puntos de corte

Teoría: [[1 - Teoría Funciones#3. Dominio y puntos de corte|Dominio y puntos de corte]]

*Con $a=3$, $b=2$. Resuelvo $f(x)=0$ en cada trozo y compruebo el intervalo.*

$$\text{Trozo 1: } \frac{3x+2}{x+2}=0 \text{ cuando } x=-\frac23 \quad (\leq 0,\ \text{vale})$$
$$\text{Trozo 2: } 1+\ln(x+1)=0 \text{ cuando } \ln(x+1)=-1, \text{ es decir, } x=e^{-1}-1\approx-0{,}63 \quad (\text{no es}>0,\ \text{se descarta})$$
$$\text{Eje Y: } f(0)=\frac{2}{2}=1$$

> **Respuesta:** Corta al eje X en $\left(-\tfrac23,\,0\right)$ y al eje Y en $(0,\,1)$. La solución $x=e^{-1}-1$ del segundo trozo se descarta porque no cumple $x>0$.

### d) Asíntotas

Teoría: [[1 - Teoría Funciones#5. Asíntotas|Asíntotas]] · [[1 - Teoría Funciones#1. Límites|Límites]]

**AV.** *Candidatos: $x=-2$ y $x=0$ (unión, pero ahí es continua). Numerador en $-2$: $-4$.*

$$\lim_{x\to-2^-}\frac{3x+2}{x+2}=\frac{-4}{0^-}=+\infty \qquad \lim_{x\to-2^+}\frac{3x+2}{x+2}=\frac{-4}{0^+}=-\infty$$

**En $-\infty$** (trozo 1): *mismo grado, cociente de coeficientes principales.*

$$\lim_{x\to-\infty}\frac{3x+2}{x+2}=3,\quad\text{luego hay AH } y=3$$

*Posición:* $f(x)-3=\dfrac{-4}{x+2}$, *positivo para $x\to-\infty$: encima.*

**En $+\infty$** (trozo 2):

$$\lim_{x\to+\infty}\big(1+\ln(x+1)\big)=+\infty,\quad\text{luego no hay AH}$$
$$m=\lim_{x\to+\infty}\frac{1+\ln(x+1)}{x}=0,\quad\text{luego no hay AO}$$

*El logaritmo crece más despacio que $x$.*

> **Respuesta:** Asíntota vertical $x=-2$, con $\lim\limits_{x\to-2^-}f(x)=+\infty$ y $\lim\limits_{x\to-2^+}f(x)=-\infty$. Asíntota horizontal $y=3$ cuando $x\to-\infty$, con la gráfica por encima. Cuando $x\to+\infty$, $f(x)\to+\infty$ sin asíntota horizontal ni oblicua.

### e) Monotonía

Teoría: [[1 - Teoría Funciones#7. Monotonía y extremos|Monotonía y extremos]]

*Derivadas de b) con $a=3$, $b=2$; $f'(0)=1$.*

$$f'(x)=\begin{cases}\dfrac{4}{(x+2)^2} & \text{si } x\leq 0,\ x\neq-2\\[3mm] \dfrac{1}{x+1} & \text{si } x>0\end{cases}$$

*Los dos trozos son siempre positivos y nunca valen $0$: no hay extremos ni tangentes horizontales.*

| $x$ | $(-\infty,-2)$ | $-2$ | $(-2,0)$ | $0$ | $(0,+\infty)$ |
|---|---|---|---|---|---|
| $f'(x)$ | $+$ | ∄ | $+$ | $1$ | $+$ |
| $f(x)$ | ↗ | ∄ | ↗ | | ↗ |

*Si $x_1<x_2$, ¿es siempre $f(x_1)<f(x_2)$? No: la AV corta la gráfica. Ej.: $f(-3)=7>f(0)=1$.*

> **Respuesta:** $f'(x)>0$ en todo el dominio, luego $f$ es creciente en $(-\infty,-2)\cup(-2,+\infty)$, sin extremos ni tangentes horizontales. Aun así, $x_1<x_2$ no implica siempre $f(x_1)<f(x_2)$: $-3<0$ pero $f(-3)=7>f(0)=1$, porque el dominio está cortado en $x=-2$.

### f) Curvatura

Teoría: [[1 - Teoría Funciones#8. Curvatura y puntos de inflexión|Curvatura y puntos de inflexión]]

$$f''(x)=\begin{cases}\dfrac{-8}{(x+2)^3} & \text{si } x<0,\ x\neq-2\\[3mm] \dfrac{-1}{(x+1)^2} & \text{si } x>0\end{cases}$$

*Si $x<-2$, $(x+2)^3<0$ y $f''>0$; si $-2<x<0$, $f''<0$. El segundo trozo es siempre negativo. En $x=0$ no cambia la curvatura.*

| $x$ | $(-\infty,-2)$ | $-2$ | $(-2,0)$ | $0$ | $(0,+\infty)$ |
|---|---|---|---|---|---|
| $f''(x)$ | $+$ | ∄ | $-$ | $-1$ | $-$ |
| $f(x)$ | cóncava ◡ | ∄ | convexa ◠ | | convexa ◠ |

> **Respuesta:** $f$ es cóncava ◡ en $(-\infty,-2)$ y convexa ◠ en $(-2,+\infty)$. No tiene puntos de inflexión: la curvatura solo cambia en $x=-2$, que no pertenece al dominio.

### g) Rectas tangentes

Teoría: [[1 - Teoría Funciones#10. Recta tangente|Recta tangente]]

*Corte con el eje X en $x=-\frac23$ (apartado c). Pendiente con el trozo 1:*

$$f'\!\left(-\tfrac23\right)=\frac{4}{\left(\frac43\right)^2}=\frac{4}{\frac{16}{9}}=\frac94$$
$$y-0=\frac94\left(x+\frac23\right),\quad\text{luego}\quad y=\frac94x+\frac32$$

*Unión de los trozos: $x=0$, con $f(0)=1$ y $f'(0)=1$.*

$$y-1=1\cdot(x-0),\quad\text{luego}\quad y=x+1$$

> **Respuesta:** La tangente en el corte con el eje de abscisas, $\left(-\tfrac23,0\right)$, es $y=\tfrac94x+\tfrac32$. La tangente en el punto de unión, $(0,1)$, es $y=x+1$, común a los dos trozos porque $f$ es derivable en $x=0$.

### h) Representación

Teoría: [[1 - Teoría Funciones#9. Representación gráfica|Representación gráfica]]

*Rama izquierda ($x<-2$, cóncava ◡): sale de la AH $y=3$ por encima y sube a $+\infty$ junto a $x=-2$. Rama central (convexa ◠): sube desde $-\infty$ junto a $x=-2$, pasa por $\left(-\tfrac23,0\right)$ y $(0,1)$ y sigue con el logaritmo, cada vez más despacio. Apoyo: $f(-4)=5$, $f(-3)=7$, $f(-1)=-1$, $f(1)\approx1{,}69$, $f(3)\approx2{,}39$.*

![[ej3_trozos.svg|560]]
