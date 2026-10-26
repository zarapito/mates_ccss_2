# Funciones — Teoría (2º Bach. CC. SS., Madrid)

**Índice**

**I. Herramientas**
- [[#1. Límites]]
- [[#2. Derivadas]]

**II. Estudio completo de una función**
- [[#3. Dominio y puntos de corte]]
- [[#4. Continuidad]]
- [[#5. Asíntotas]]
- [[#6. Derivabilidad]]
- [[#7. Monotonía y extremos]]
- [[#8. Curvatura y puntos de inflexión]]
- [[#9. Representación gráfica]]

**III. Problemas típicos**
- [[#10. Recta tangente]]
- [[#11. Optimización]]
- [[#12. Ejercicios con parámetros]]

---

# I. Herramientas

Cálculos que se usan en todo el bloque: los límites sirven para continuidad y asíntotas; las derivadas, para derivabilidad, monotonía, curvatura, tangentes y optimización.

## 1. Límites

🧮 $\lim\limits_{x\to a} f(x)=L$

🗣️ "cuando $x$ se acerca a $a$, $f(x)$ se acerca a $L$".

El **límite** cuando $x$ tiende a $a$ **existe** si los dos **límites laterales** existen y son iguales: $\lim\limits_{x\to a^-}$ (por la izquierda, valores $<a$) $=$ $\lim\limits_{x\to a^+}$ (por la derecha, $>a$).

> [!tip] Método
> **Paso 1:** sustituye $x$ por el valor (o por $\infty$).
> **Paso 2:** mira qué te ha salido:
> - **Un número** → ese es el límite. Fin.
> - **Uno de los casos de la tabla A** → el resultado es directo.
> - **Una indeterminación de la tabla B** → hay que operar antes de volver a sustituir.

**A. Resultados directos** (no son indeterminaciones)

| Al sustituir sale… | El límite es… | Ejemplo |
|---|---|---|
| $\dfrac{k}{0}$ (número entre $0$, con $k\neq0$) | $+\infty$ o $-\infty$. Para saber cuál, calcula los dos laterales mirando el signo de arriba y el de abajo | $\lim\limits_{x\to1^-}\dfrac{2}{x-1}=\dfrac{2}{0^-}=-\infty$ <br> $\lim\limits_{x\to1^+}\dfrac{2}{x-1}=\dfrac{2}{0^+}=+\infty$ |
| $\dfrac{k}{\infty}$ (número entre infinito) | $0$ | $\lim\limits_{x\to+\infty}\dfrac{3}{x^2}=0$ |
| $e^{+\infty}$ | $+\infty$ | $\lim\limits_{x\to+\infty}e^{x}=+\infty$ |
| $e^{-\infty}$ | $0$ | $\lim\limits_{x\to+\infty}e^{-x}=0$ |
| $\ln(+\infty)$ | $+\infty$ | $\lim\limits_{x\to+\infty}\ln x=+\infty$ |
| $\ln(0^+)$ | $-\infty$ | $\lim\limits_{x\to0^+}\ln x=-\infty$ |

**B. Indeterminaciones** (no se sabe el resultado: hay que operar)

| Al sustituir sale… | Qué hago | Ejemplo |
|---|---|---|
| $\dfrac{0}{0}$ | Factorizar arriba y abajo (Ruffini, identidades notables), simplificar y volver a sustituir. Si hay raíces, multiplicar por el conjugado | $\lim\limits_{x\to2}\dfrac{x^2-4}{x-2}=\lim\limits_{x\to2}\dfrac{(x-2)(x+2)}{x-2}=\lim\limits_{x\to2}(x+2)=4$ |
| $\dfrac{\infty}{\infty}$ | Comparar los grados de arriba y abajo (tabla C) | $\lim\limits_{x\to+\infty}\dfrac{6x^2-1}{2x^2+x}=\dfrac{6}{2}=3$ |
| $\infty-\infty$ con fracciones | Restar las fracciones (común denominador) y queda un $\frac{\infty}{\infty}$ | $\lim\limits_{x\to+\infty}\left(\dfrac{x^2}{x+1}-x\right)=\lim\limits_{x\to+\infty}\dfrac{-x}{x+1}=-1$ |
| $\infty-\infty$ con raíces | Multiplicar y dividir por el conjugado | $\lim\limits_{x\to+\infty}\left(\sqrt{x^2+1}-x\right)=\lim\limits_{x\to+\infty}\dfrac{1}{\sqrt{x^2+1}+x}=0$ |

**C. Cocientes de polinomios cuando $x\to\pm\infty$** (resuelve el $\frac{\infty}{\infty}$)

| Si el grado es… | El límite es… | Ejemplo |
|---|---|---|
| mayor abajo | $0$ | $\lim\limits_{x\to+\infty}\dfrac{3x+1}{x^2+5}=0$ |
| igual arriba y abajo | el cociente de los coeficientes principales (los de mayor grado) | $\lim\limits_{x\to+\infty}\dfrac{6x^2-1}{2x^2+x}=\dfrac{6}{2}=3$ |
| mayor arriba | $+\infty$ o $-\infty$. El signo sale de los coeficientes principales y de si $x\to+\infty$ o $x\to-\infty$ | $\lim\limits_{x\to+\infty}\dfrac{x^3}{x+1}=+\infty$ |

> [!note] Órdenes de infinito (cuando se mezclan tipos de funciones)
> De más lento a más rápido: $\ln x \;\ll\; x^n \;\ll\; e^x$. En un cociente, **manda el más rápido**:
> - Si el más rápido está abajo, el límite es $0$: $\lim\limits_{x\to+\infty}\dfrac{\ln x}{x}=0$.
> - Si el más rápido está arriba, el límite es $\infty$: $\lim\limits_{x\to+\infty}\dfrac{e^x}{x^2}=+\infty$.

---

## 2. Derivadas

🗣️ La **derivada** nos habla de **cómo varía el valor ($y$)** de nuestra función.

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

# II. Estudio completo de una función

Para analizar una función se siguen estos pasos en orden. Cada uno usa las herramientas de la parte I, y al final se juntan todos en la [[#9. Representación gráfica|representación gráfica]].

## 3. Dominio y puntos de corte

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
> En problemas reales el dominio se recorta siguiendo el enunciado o el sentido común: distancias $x\ge 0$, unidades producidas $x\geq0$, etc.

**Puntos de corte**

| 🗣️ Pregunta | 🧮 Qué hago | Resultado |
|---|---|---|
| ¿Dónde corta al eje X (abscisas)? | resuelvo $f(x)=0$ | puntos $(x_0,\,0)$ |
| ¿Dónde corta al eje Y (ordenadas)? | calculo $f(0)$ (si $0\in\text{Dom}$) | punto $(0,\,f(0))$ |

En funciones a trozos: **comprobar que la solución pertenece al intervalo del trozo**; si no, se descarta.

---

## 4. Continuidad

🗣️ Una función es **continua** si **se dibuja sin levantar el lápiz**: no hay agujeros, escalones ni asíntotas verticales.

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

**Pasos para estudiar la continuidad**: 1) dominio → 2) estudiar puntos sospechosos → 3) concluir: "$f$ es continua en … y tiene una discontinuidad (tipo) en $x=$ …".

---

## 5. Asíntotas

🗣️ Una asíntota es una **recta a la que la gráfica se acerca cada vez más** sin llegar a tocarla.

| Tipo | 🗣️ | 🧮 | Dónde buscar |
|---|---|---|---|
| **Vertical (AV)** $x=a$ | la gráfica se va hacia $\pm\infty$ cerca de $a$ | $\lim\limits_{x\to a^\pm} f(x)=\pm\infty$ | puntos fuera del dominio, bordes del dominio, uniones de trozos |
| **Horizontal (AH)** $y=k$ | la gráfica se acerca a $k$ hacia el infinito | $\lim\limits_{x\to\pm\infty} f(x)=k$ (número) | en $+\infty$ y en $-\infty$ **por separado** |
| **Oblicua (AO)** $y=mx+n$ | la gráfica se acerca a una recta inclinada hacia el infinito | $m=\lim\limits_{x\to\pm\infty}\dfrac{f(x)}{x}$ ($m\neq0$, finito) · $n=\lim\limits_{x\to\pm\infty}\big(f(x)-mx\big)$ | solo donde **no** hay AH |

**Qué significa cada resultado del límite**

| Límite | Si da un número | Si da $+\infty$ | Si da $-\infty$ |
|---|---|---|---|
| **AV**: $x\to a$ | no hay AV, la función se acerca a ese valor | **hay AV** | **hay AV** |
| **AH**: $x\to\pm\infty$ | **hay AH** | no hay AH, la función sube | no hay AH, la función baja |

> [!tip] Trucos
> - Una función puede tener **AH distinta** en $+\infty$ y en $-\infty$.

---

## 6. Derivabilidad

🗣️ Una función es **derivable** si **la gráfica es "suave"**: sin saltos y **sin picos** (sin puntos angulosos).

🧮 $f$ derivable en $a \iff f$ continua en $a$ **y** $f'(a^-)=f'(a^+)$ (derivadas laterales iguales).

**Si una función**...
   - es continua, a veces no es derivable.
   - es derivable, siempre es continua.
   - no es continua, tampoco será derivable.

**Pasos en una función a trozos** (punto de unión $x=a$):
1. Estudiar la **continuidad** en $a$. Si no es continua → no es derivable (fin).
2. Derivar **cada trozo** (con intervalos abiertos) y calcular $f'(a^-)$ y $f'(a^+)$ sustituyendo $a$ en cada derivada.
3. Si coinciden → derivable en $a$; si no → punto anguloso.

---

## 7. Monotonía y extremos

| $f'(x)$ | 🗣️ La función… |  |
|---|---|---|
| $>0$ | **crece** | ↗ |
| $<0$ | **decrece** | ↘ |
| $=0$ | tangente horizontal: **posible** máximo/mínimo | — |

**Pasos**
1. Calcular $f'(x)$ (simplificada y factorizada).
2. Resolver $f'(x)=0$ → **puntos críticos**.
3. Tabla de signos con: puntos críticos + puntos fuera del dominio (+ uniones de trozos).
4. Concluir:
   - Intervalos de crecimiento y decrecimiento (**abiertos**, unidos con $\cup$).
   - **Máximo relativo**: pasa de ↗ a ↘. 
   - **Mínimo relativo**: de ↘ a ↗.
   - Dar las **dos coordenadas** en máximos y mínimos: $(x_0,\ f(x_0))$ → sustituir en $f$, **no** en $f'$.

> [!warning] Relativo vs absoluto
> - **Relativo**: es el más alto/bajo "de los alrededores". Un máximo relativo puede ser **menor** que un mínimo relativo.
> - **Absoluto**: el más alto/bajo de **toda** la función.

---

## 8. Curvatura y puntos de inflexión

| $f''(x)$ | 🗣️ La función es… | Dibujo | 🗣️ Qué le pasa a $f'$ |
|---|---|---|---|
| $>0$ | **cóncava** | ◡ | la pendiente aumenta |
| $<0$ | **convexa** | ◠ | la pendiente disminuye |
| $=0$ | **posible** punto de inflexión | — | posible máximo/mínimo de $f'$ |

🗣️ Un **punto de inflexión** es donde la gráfica **cambia de curvatura** (◡ ↔ ◠). También es donde la función **crece (o decrece) más rápido** y $f'$ alcanza su máximo o mínimo.

**Pasos**: igual que monotonía pero con $f''$: calcular $f''$ → resolver $f''=0$ → tabla de signos (incluir puntos fuera del dominio) → intervalos ◡ / ◠ y puntos de inflexión con sus dos coordenadas $(x_0, f(x_0))$.

> [!warning] Si la curvatura cambia en un punto que **no está en el dominio**, **no** hay punto de inflexión.

> [!info] **Convenio de curvatura** (el de tus apuntes): $f''>0 \Rightarrow$ **cóncava ◡** · $f''<0 \Rightarrow$ **convexa ◠**.
> ⚠️ Algunos libros lo llaman al revés. Si dudas en el examen, **dibuja el símbolo ◡ / ◠** al lado de la palabra.

> Si el enunciado te da $f'(x)$ en vez de $f(x)$
> - Para **monotonía y extremos** no necesitas $f$: estudia directamente el signo de la $f'$ que te dan. Para la $y$ del extremo sí necesitas $f$.
> - Para **curvatura**, deriva la $f'$ que te dan y obtienes $f''$.
> - Para **obtener $f$** hay que buscar una primitiva, $f(x)=\int f'(x)\,dx + C$, y calcular $C$ con un punto por el que pase. Esto es del bloque de integrales.

---

## 9. Representación gráfica

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

---

# III. Problemas típicos

Problemas que no piden el estudio completo, sino usar una parte concreta de él.

## 10. Recta tangente

🗣️ La **recta tangente** es la recta que "roza" la gráfica en un punto y tiene su misma inclinación.

$$y-f(a)=f'(a)\,(x-a)$$

| Necesito | Cómo lo obtengo |
|---|---|
| $x$ del punto: $a$ | dato o se averigua |
| $y$ del punto: $f(a)$ | sustituyo $a$ en $f$ |
| Pendiente $m=f'(a)$ | sustituyo $a$ en $f'$ |

**Problemas típicos**

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

## 11. Optimización

🗣️ Encontrar **el valor de $x$ que hace máxima o mínima** una magnitud (beneficio, coste, área…).

**Pasos**
1. Identificar la **función a optimizar** y su variable (con unidades).
2. Si hay dos variables, usar la información del enunciado para dejar una sola.
3. Fijar el **dominio en contexto** (p. ej. $x\geq0$, $x\in[0,10]$). Por ejemplo, no podemos tener distancias negativas.
4. Derivar, resolver $f'(x)=0$.
5. Comprobar si es máximo o mínimo (signo de $f'$ o de $f''$: $f''<0$ máx., $f''>0$ mín.).
6. Si el dominio es cerrado, **comparar con los extremos** del intervalo.
7. **Responder a la pregunta con una frase** y unidades.

>[!tip] Recuerda leer bien **qué te preguntan**.
> Ejemplo: Función que representa los beneficios anuales
> - Valor de $x$ que maximiza los beneficios: $x$ del máximo
> - Beneficios anuales máximos: $f(x)$ (valor de la función en el máximo)

---

## 12. Ejercicios con parámetros

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
