# Funciones — Teoría (2º Bach. CC. SS., Madrid)

**Índice**
- [[#1. Dominio y puntos de corte]]
- [[#2. Límites]]
- [[#3. Asíntotas]]
- [[#4. Continuidad]]
- [[#5. Derivadas]]
- [[#6. Derivabilidad]]
- [[#7. Monotonía y extremos]]
- [[#8. Curvatura y puntos de inflexión]]
- [[#9. Recta tangente]]
- [[#10. Optimización]]
- [[#11. Ejercicios con parámetros]]
- [[#12. Representación gráfica]]

---

## 1. Dominio y puntos de corte

🗣️ **Dominio** = los valores de $x$ que puedo meter en la función.
🧮 $\text{Dom}(f)=\{x\in\mathbb{R} : f(x) \text{ existe}\}$

| Tipo de función | Problema ❌ | Condición ✅ | Dominio |
|---|---|---|---|
| Polinómica, exponencial $a^{g(x)}$, raíz impar | ninguno | — | $\mathbb{R}$ (o el de $g$) |
| Racional $\dfrac{P(x)}{Q(x)}$ | denominador $=0$ | $Q(x)\neq 0$ | $\mathbb{R}-\{\text{raíces de } Q\}$ |
| Raíz par $\sqrt{g(x)}$ | dentro negativo | $g(x)\geq 0$ | resolver inecuación |
| Logaritmo $\ln g(x)$ | dentro $\leq 0$ | $g(x)> 0$ | resolver inecuación |
| A trozos | cada trozo **solo vale en su intervalo** | condición del trozo $\cap$ su intervalo | unión de lo que vale en cada trozo |

> [!tip] Funciones a trozos
> Un punto problemático de un trozo **solo importa si está dentro del intervalo de ese trozo**.
> Ej.: en $\frac{1}{x+2}$ definida solo para $x>0$, el $x=-2$ **no molesta**.

> [!note] Contexto
> En problemas reales el dominio se recorta siguiendo el enunciado o el sistema común: distancias $x\ge 0$, unidades producidas $x\geq0$, etc.

**Puntos de corte**

| 🗣️ Pregunta | 🧮 Qué hago | Resultado |
|---|---|---|
| ¿Dónde corta al eje X (abscisas)? | resuelvo $f(x)=0$ | puntos $(x_0\,0)$ |
| ¿Dónde corta al eje Y (ordenadas)? | calculo $f(0)$ (si $0\in\text{Dom}$) | punto $(0\,f(0))$ |

En funciones a trozos: **comprobar que la solución pertenece al intervalo del trozo**; si no, se descarta.

---

## 2. Límites
🧮 $\lim\limits_{x\to a} f(x)=L$
🗣️ "cuando $x$ se acerca a $a$, $f(x)$ se acerca a $L$".

**Límites laterales**: $\lim\limits_{x\to a^-}$ (por la izquierda, valores $<a$) y $\lim\limits_{x\to a^+}$ (por la derecha, $>a$).
El límite existe si los dos laterales existen y son iguales.

**Resultados**

| Expresión | Resultado | Cómo saber el signo |
|---|---|---|
| $\dfrac{k}{0}$ ($k\neq0$) | $\pm\infty$ | estudiar signo con límites laterales |
| $\dfrac{k}{\pm\infty}$ | $0$ | — |
| $e^{+\infty}$ / $e^{-\infty}$ | $+\infty$ / $0$ | — |
| $\ln(0^+)$ / $\ln(+\infty)$ | $-\infty$ / $+\infty$ | — |

**Indeterminaciones**

| Tipo | Cómo se resuelve |
|---|---|
| $\dfrac{\infty}{\infty}$ (cocientes de polinomios) | comparar grados: grado num < den $\to 0$; iguales $\to$ cociente de coeficientes principales; num > den $\to \pm\infty$ |
| $\dfrac{0}{0}$ | factorizar (Ruffini) y simplificar; con raíces, multiplicar por el conjugado |
| $\infty-\infty$ | con fracciones: restar (común denominador); con raíces: conjugado |
| Órdenes de infinito | $\ln x \ll x^n \ll e^x$ (el "más rápido" manda). Ej.: $\lim\limits_{x\to+\infty}\dfrac{\ln x}{x}=0$ |

---

## 3. Asíntotas

🗣️ Una asíntota es una **recta a la que la gráfica se acerca cada vez más** sin llegar a tocarla.

| Tipo | 🗣️ Idea | 🧮 Condición | Dónde buscar |
|---|---|---|---|
| **Vertical (AV)** $x=a$ | la gráfica se va hacia $\pm\infty$ cerca de $a$ | $\lim\limits_{x\to a^\pm} f(x)=\pm\infty$ | puntos fuera del dominio, bordes del dominio, uniones de trozos |
| **Horizontal (AH)** $y=k$ | la gráfica se acerca a $k$ hacia el infinito | $\lim\limits_{x\to\pm\infty} f(x)=k$ (número) | en $+\infty$ y en $-\infty$ **por separado** |
| **Oblicua (AO)** $y=mx+n$ | la gráfica se acerca a una recta inclinada hacia el infinito | $m=\lim\limits_{x\to\pm\infty}\dfrac{f(x)}{x}$ ($m\neq0$, finito) · $n=\lim\limits_{x\to\pm\infty}\big(f(x)-mx\big)$ | solo donde **no** hay AH |

**Qué significa cada resultado del límite**

| Límite | Si da un número | Si da $+\infty$ | Si da $-\infty$ |
|---|---|---|---|
| AV: $x\to a$ | no hay AV, la función se acerca a ese valor | **hay AV** | **hay AV** |
| AH: $x\to\pm\infty$ | **hay AH** | no hay AH, la función sube | no hay AH, la función baja |

> [!tip] Trucos
> - Una función puede tener **AH distinta** en $+\infty$ y en $-\infty$.

---

## 4. Continuidad

🗣️ Continua = **se dibuja sin levantar el lápiz**.

🧮 $f$ continua en $x=a \iff$ se cumplen las tres condiciones:

| | Condición | 🗣️ |
|---|---|---|
| 1 | $f(a)$ existe | el punto existe |
| 2 | $\lim\limits_{x\to a^-}f(x)=\lim\limits_{x\to a^+}f(x)$ (finito) | la gráfica llega a la misma altura por los dos lados |
| 3 | $\lim\limits_{x\to a}f(x)=f(a)$ | y esa altura es la del punto |

Las funciones elementales (polinómicas, racionales, raíces, exponenciales, logarítmicas) son **continuas en su dominio**.
➡️ Solo hay que estudiar: **puntos fuera del dominio** y **uniones entre trozos**.

**Tipos de discontinuidad**

| Tipo | 🧮 Qué pasa | 🗣️ Dibujo |
|---|---|---|
| **Evitable** | límites laterales iguales finitos (números), pero $\neq f(a)$ o $f(a)$ no existe | "agujero" en la gráfica |
| **Inevitable de salto finito** | límites laterales finitos (números) pero distintos | "escalón" |
| **Inevitable de salto infinito** | algún lateral es $\pm\infty$ | asíntota vertical |

**Pasos**: 1) dominio → 2) estudiar puntos sospechosos → 3) concluir: "$f$ es continua en … y tiene discontinuidad … en $x=$ …".

---

## 5. Derivadas

🗣️ La derivada nos habla de cómo varía el valor de nuestra función.
🧮 $f'(a)$ = **pendiente de la gráfica en $a$** = velocidad a la que cambia $f$ en ese instante (**tasa de variación instantánea**).

**Tabla de derivadas** (con regla de la cadena: $u=u(x)$)

| Función | Derivada | Ejemplo |
|---|---|---|
| $k$ | $0$ | $(5)'=0$ |
| $x^n$ / $u^n$ | $n\,x^{n-1}$ / $n\,u^{n-1}\cdot u'$ | $\big((x^2+1)^3\big)'=3(x^2+1)^2\cdot 2x$ |
| $\sqrt{u}$ | $\dfrac{u'}{2\sqrt{u}}$ | $(\sqrt{x^2+1})'=\dfrac{2x}{2\sqrt{x^2+1}}$ |
| $e^{u}$ | $e^{u}\cdot u'$ | $(e^{-x})'=-e^{-x}$ |
| $a^{u}$ | $a^{u}\cdot \ln a\cdot u'$ | $(2^x)'=2^x\ln 2$ |
| $\ln u$ | $\dfrac{u'}{u}$ | $(\ln(x+1))'=\dfrac{1}{x+1}$ |

**Reglas de operaciones**

| Operación | Regla |
|---|---|
| Suma | $(f\pm g)'=f'\pm g'$ |
| Constante | $(k\cdot f)'=k\cdot f'$ |
| Producto | $(f\cdot g)'=f'g+fg'$ |
| Cociente | $\left(\dfrac{f}{g}\right)'=\dfrac{f'g-fg'}{g^2}$ |
| Cadena | $\big(f(g(x))\big)'=f'(g(x))\cdot g'(x)$ |

> [!tip] Cociente con $k$ arriba: $\left(\dfrac{k}{g}\right)'=\dfrac{-k\,g'}{g^2}$ (más rápido).
> Si al derivar un cociente el numerador **factoriza**, ¡factoriza! Facilita el estudio del signo.

---

## 6. Derivabilidad

🗣️ Derivable = **la gráfica es "suave"**: sin saltos y **sin picos** (sin puntos angulosos).

🧮 $f$ derivable en $a \iff f$ continua en $a$ **y** $f'(a^-)=f'(a^+)$ (derivadas laterales iguales).

| | |
|---|---|
| Derivable $\Rightarrow$ Continua | ✅ siempre |
| Continua $\Rightarrow$ Derivable | ❌ no siempre (ej.: pico) |
| No continua $\Rightarrow$ No derivable | ✅ siempre |

**Pasos en una función a trozos** (punto de unión $x=a$):
1. Estudiar la **continuidad** en $a$. Si no es continua → no es derivable (fin).
2. Derivar **cada trozo** (con intervalos abiertos) y calcular $f'(a^-)$ y $f'(a^+)$ sustituyendo $a$ en cada derivada.
3. Si coinciden → derivable en $a$; si no → punto anguloso.

---

## 7. Monotonía y extremos

| $f'(x)$ | 🗣️ La función… | Símbolo |
|---|---|---|
| $>0$ | **crece** | ↗ |
| $<0$ | **decrece** | ↘ |
| $=0$ | tangente horizontal: **posible** máximo/mínimo | — |

**Pasos**
1. Calcular $f'(x)$ (simplificada y factorizada).
2. Resolver $f'(x)=0$ → **puntos críticos**.
3. Tabla de signos con: puntos críticos + puntos fuera del dominio (+ uniones de trozos).
4. Concluir:
   - Intervalos de crecimiento y decrecimiento (**abiertos**, unidos con $\cup$, nunca con "y").
   - **Máximo relativo**: pasa de ↗ a ↘. **Mínimo relativo**: de ↘ a ↗.
   - Dar las **dos coordenadas**: $(x_0,\ f(x_0))$ → sustituir en $f$, **no** en $f'$.

> [!warning] Relativo vs absoluto
> - **Relativo**: es el más alto/bajo "de su barrio". Un máximo relativo puede ser **menor** que un mínimo relativo.
> - **Absoluto**: el más alto/bajo de **toda** la función. En un intervalo cerrado $[a,b]$: comparar $f$ en los puntos críticos **y en los extremos** $a$ y $b$.

---

## 8. Curvatura y puntos de inflexión

| $f''(x)$ | 🗣️ La función es… | Dibujo | 🗣️ Qué le pasa a $f'$ |
|---|---|---|---|
| $>0$ | **cóncava** | ◡ | la pendiente aumenta |
| $<0$ | **convexa** | ◠ | la pendiente disminuye |
| $=0$ | **posible** punto de inflexión | — | posible máximo/mínimo de $f'$ |

**Punto de inflexión** 🗣️ donde la gráfica **cambia de curvatura** (◡ ↔ ◠).

**Pasos**: igual que monotonía pero con $f''$: calcular $f''$ → resolver $f''=0$ → tabla de signos (incluir puntos fuera del dominio) → intervalos ◡ / ◠ y puntos de inflexión con sus dos coordenadas $(x_0, f(x_0))$.

> [!tip] Interpretación
> Un punto de inflexión es donde la función **crece (o decrece) más rápido**: allí $f'$ alcanza su máximo o mínimo.
> Si la curvatura cambia en un punto que **no está en el dominio**, **no** hay punto de inflexión.

> [!info] **Convenio de curvatura** (el de tus apuntes): $f''>0 \Rightarrow$ **cóncava ◡** · $f''<0 \Rightarrow$ **convexa ◠**.
> ⚠️ Algunos libros lo llaman al revés. Si dudas en el examen, **dibuja el símbolo ◡ / ◠** al lado de la palabra.

---

## 9. Recta tangente

🗣️ La recta que "roza" la gráfica en un punto y tiene su misma inclinación.

$$y-f(a)=f'(a)\,(x-a)$$

| Necesito | Cómo lo obtengo |
|---|---|
| $x$ del punto: $a$ | dato o se averigua |
| $y$ del punto: $f(a)$ | sustituyo $a$ en $f$ |
| Pendiente $m=f'(a)$ | sustituyo $a$ en $f'$ |

**Problemas típicos: ¿cómo encuentro $a$?**

| 🗣️ Me piden la tangente… | 🧮 Planteo |
|---|---|
| en el punto de abscisa $a$ | $a$ dado |
| con pendiente $m$ | $f'(x)=m$ |
| paralela a la recta $y=mx+n$ | $f'(x)=m$ (misma pendiente) |
| paralela a $Ax+By=C$ | despejar $y$ para ver la pendiente $m=-\frac{A}{B}$; luego $f'(x)=m$ |
| paralela al eje X / horizontal | $f'(x)=0$ |
| en los cortes con el eje X | $f(x)=0$ |
| en el punto de inflexión | $f''(x)=0$ |

---

## 10. Optimización

🗣️ Encontrar **el valor de $x$ que hace máxima o mínima** una magnitud (beneficio, coste, área…).

**Pasos**
1. Identificar la **función a optimizar** y su variable (con unidades).
2. Si hay dos variables, usar la **condición/ligadura** del enunciado para dejar una sola.
3. Fijar el **dominio en contexto** (p. ej. $x\geq0$, $x\in[0,10]$).
4. Derivar, resolver $f'(x)=0$.
5. Comprobar si es máximo o mínimo (signo de $f'$ o de $f''$: $f''<0$ máx., $f''>0$ mín.).
6. Si el dominio es cerrado, **comparar con los extremos** del intervalo.
7. **Responder a la pregunta con una frase** y unidades.

---

> [!tip] Si el enunciado te da $f'(x)$ en vez de $f(x)$
> - Para **monotonía y extremos** no necesitas $f$: estudia directamente el signo de la $f'$ que te dan. Para la $y$ del extremo sí necesitas $f$.
> - Para **curvatura**, deriva la $f'$ que te dan y obtienes $f''$.
> - Para **obtener $f$** hay que buscar una primitiva, $f(x)=\int f'(x)\,dx + C$, y calcular $C$ con un punto por el que pase. Esto es del bloque de integrales.

## 11. Ejercicios con parámetros

**Diccionario: lenguaje natural → ecuación** 🗣️ → 🧮

| El enunciado dice… | Escribo… |
|---|---|
| La gráfica pasa por $(a,b)$ | $f(a)=b$ |
| Corta al eje X en $x=a$ | $f(a)=0$ |
| Corta al eje Y en $y=b$ | $f(0)=b$ |
| Tiene máximo/mínimo (extremo) en $x=a$ | $f'(a)=0$ |
| Tiene máximo/mínimo en el punto $(a,b)$ | $f'(a)=0$ **y** $f(a)=b$ (¡2 ecuaciones!) |
| Tangente horizontal / paralela al eje X en $x=a$ | $f'(a)=0$ |
| La tangente en $x=a$ tiene pendiente $m$ | $f'(a)=m$ |
| La tangente en $x=a$ tiene la misma pendiente que la recta (o función) $g$ | $f'(a)=g'(a)$ |
| La tasa de variación instantánea (velocidad) en $t=a$ vale $v$ | $f'(a)=v$ |
| Las gráficas de $f$ y $g$ se cortan | $f(x)=g(x)$ (sistema) |
| Punto de inflexión en $x=a$ | $f''(a)=0$ |
| AV en $x=a$ | denominador se anula en $a$ (y numerador no) |
| AH $y=k$ | $\lim\limits_{x\to\pm\infty}f(x)=k$ |
| Continua en $x=a$ ("sin levantar el lápiz") | $\lim\limits_{x\to a^-}f=\lim\limits_{x\to a^+}f=f(a)$ |
| Derivable en $x=a$ ("sin saltos ni picos") | continua **y** $f'(a^-)=f'(a^+)$ |

**Método**: 1) Traducir cada dato a una ecuación. 2) Tantas ecuaciones como parámetros. 3) Resolver el sistema. 4) **Comprobar** (p. ej. que es máximo y no mínimo).

---

## 12. Representación gráfica

**Checklist** (en este orden)

- [ ] **Dominio** (y continuidad)
- [ ] **Cortes** con los ejes
- [ ] **Asíntotas** (AV con límites laterales, AH/AO en $+\infty$ y $-\infty$)
- [ ] **Monotonía** y **extremos**
- [ ] **Curvatura** y **puntos de inflexión**
- [ ] Tabla con algunos **valores extra** si hace falta
- [ ] Dibujar: primero asíntotas (discontinuas - - -), luego puntos, luego unir respetando crecimiento y curvatura.

> [!tip] Coherencia
> Si algo "no encaja" (p. ej. crece hacia una AH desde arriba), revisa los signos: casi siempre es un error de cálculo.
