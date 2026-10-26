# Tabla resumen: $f$, $f'$ y $f''$

$f$, $f'$ y $f''$ responden a tres preguntas distintas sobre la gráfica de $f$. Convenio de curvatura: $f''>0$ **cóncava ◡**, $f''<0$ **convexa ◠**.

## ¿De qué habla cada una?

| | $f(x)$ | $f'(x)$ | $f''(x)$ |
|---|---|---|---|
| Pregunta | ¿A qué **altura** está la gráfica? | ¿La gráfica **sube o baja**? | ¿Cómo se **curva**? |
| Qué mide | el valor de $y$ | la pendiente de la tangente (velocidad de cambio de $f$) | cómo cambia la pendiente (velocidad de cambio de $f'$) |
| Se estudia en | [[1 - Teoría Funciones#3. Dominio y puntos de corte\|dominio y cortes]] | [[1 - Teoría Funciones#7. Monotonía y extremos\|monotonía y extremos]] | [[1 - Teoría Funciones#8. Curvatura y puntos de inflexión\|curvatura e inflexión]] |

## Qué significa cada signo

| Signo | $f(x)$ | $f'(x)$ | $f''(x)$ |
|---|---|---|---|
| **Positivo** | gráfica **por encima** del eje X | $f$ **crece** ↗ | $f$ **cóncava** ◡ ($f'$ crece) |
| **Cero** | gráfica **corta** el eje X | tangente horizontal: **posible** máximo o mínimo | **posible** punto de inflexión |
| **Negativo** | gráfica **por debajo** del eje X | $f$ **decrece** ↘ | $f$ **convexa** ◠ ($f'$ decrece) |

$f''$ es para $f'$ lo mismo que $f'$ para $f$. Por eso un **punto de inflexión de $f$** es un **máximo o mínimo de $f'$**: el punto donde $f$ sube (o baja) más rápido.

## Ejemplo: $f(x)=x^3-3x$

Las tres gráficas comparten el eje $x$; las líneas discontinuas marcan los puntos clave.

![[derivadas_f_f1_f2.svg|680]]

| Intervalo | $(-\infty,-\sqrt3)$ | $(-\sqrt3,-1)$ | $(-1,0)$ | $(0,1)$ | $(1,\sqrt3)$ | $(\sqrt3,+\infty)$ |
|---|---|---|---|---|---|---|
| $f$ | $-$ debajo | $+$ encima | $+$ encima | $-$ debajo | $-$ debajo | $+$ encima |
| $f'=3x^2-3$ | $+$ ↗ | $+$ ↗ | $-$ ↘ | $-$ ↘ | $+$ ↗ | $+$ ↗ |
| $f''=6x$ | $-$ ◠ | $-$ ◠ | $-$ ◠ | $+$ ◡ | $+$ ◡ | $+$ ◡ |

Cada columna se lee de arriba abajo: en $(-\sqrt3,-1)$ la gráfica está **por encima** del eje, **sube** y es **convexa**.

> [!warning] Los tres signos son independientes
> En $(-\infty,-\sqrt3)$ la función es **negativa pero crece**. Hay que estudiar cada una por separado.

## Puntos especiales

| En $x=a$… | En la gráfica de $f$ | En el ejemplo |
|---|---|---|
| $f(a)=0$ | **corte** con el eje X | $x=-\sqrt3,\ 0,\ \sqrt3$ |
| $f'(a)=0$ y $f'$ pasa de $+$ a $-$ | **máximo relativo** | $(-1,\ 2)$ |
| $f'(a)=0$ y $f'$ pasa de $-$ a $+$ | **mínimo relativo** | $(1,\ -2)$ |
| $f''(a)=0$ y $f''$ cambia de signo | **punto de inflexión** | $(0,\ 0)$ |

Los puntos se dan con sus dos coordenadas $(a,\ f(a))$, sustituyendo en $f$.

## Que valga cero no basta

$f'(a)=0$ y $f''(a)=0$ solo dan **candidatos**: lo que decide es que **el signo cambie**.

| Función | En $x=0$ | Conclusión |
|---|---|---|
| $f(x)=x^3$ | $f'(0)=0$, pero $f'=3x^2\geq0$ a ambos lados | no hay extremo (es un punto de inflexión) |
| $f(x)=x^4$ | $f''(0)=0$, pero $f''=12x^2\geq0$ a ambos lados | no hay inflexión (es un mínimo) |

También puede haber extremos donde $f'$ **no existe** (un pico en la unión de dos trozos). Y en un punto **fuera del dominio** nunca hay extremo ni inflexión.

## Criterio de la segunda derivada

Si $f'(a)=0$:

| $f''(a)$ | Conclusión |
|---|---|
| $<0$ | **máximo** (cima de una zona ◠) |
| $>0$ | **mínimo** (fondo de una zona ◡) |
| $=0$ | no decide: tabla de signos de $f'$ |

En el ejemplo: $f''(-1)=-6<0$ (máximo) y $f''(1)=6>0$ (mínimo).

## En contexto

| | Medicamento $C(t)$ | Beneficio $B(x)$ |
|---|---|---|
| $f$ | concentración en el instante $t$ | beneficio al vender $x$ unidades |
| $f'$ | velocidad a la que sube o baja la concentración | cuánto aumenta el beneficio por cada unidad más |
| $f''$ | si esa velocidad aumenta o disminuye | si cada unidad extra aporta más o menos que la anterior |
| $f'=0$ | concentración **máxima** | beneficio **máximo** |
| Punto de inflexión | la concentración baja **más rápido** ([[3 - Soluciones Funciones#h) Curvatura e instante de máxima disminución\|Ejercicio 1 h]]) | a partir de ahí, cada unidad aporta menos |
