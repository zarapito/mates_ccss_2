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

Los límites se usan en continuidad y asíntotas; las derivadas, en todo lo demás.

## 1. Límites

$\lim\limits_{x\to a} f(x)=L$: cuando $x$ se acerca a $a$, $f(x)$ se acerca a $L$.

El límite **existe** si los dos **límites laterales** existen y son iguales: $\lim\limits_{x\to a^-}$ (por la izquierda, valores $<a$) $=$ $\lim\limits_{x\to a^+}$ (por la derecha, $>a$).

> [!tip] Método
> 1. Sustituye $x$ por el valor (o por $\infty$).
> 2. Si sale un número, ese es el límite. Si sale un caso de la tabla A, el resultado es directo. Si sale una indeterminación (tabla B), opera y vuelve a sustituir.

**A. Resultados directos**

| Al sustituir sale… | El límite es… | Ejemplo |
|---|---|---|
| $\dfrac{k}{0}$ ($k\neq0$) | $+\infty$ o $-\infty$: calcula los dos laterales mirando el signo de arriba y el de abajo | $\lim\limits_{x\to1^-}\dfrac{2}{x-1}=\dfrac{2}{0^-}=-\infty$ <br> $\lim\limits_{x\to1^+}\dfrac{2}{x-1}=\dfrac{2}{0^+}=+\infty$ |
| $\dfrac{k}{\infty}$ | $0$ | $\lim\limits_{x\to+\infty}\dfrac{3}{x^2}=0$ |
| $e^{+\infty}$ | $+\infty$ | $\lim\limits_{x\to+\infty}e^{x}=+\infty$ |
| $e^{-\infty}$ | $0$ | $\lim\limits_{x\to+\infty}e^{-x}=0$ |
| $\ln(+\infty)$ | $+\infty$ | $\lim\limits_{x\to+\infty}\ln x=+\infty$ |
| $\ln(0^+)$ | $-\infty$ | $\lim\limits_{x\to0^+}\ln x=-\infty$ |

**B. Indeterminaciones**

| Al sustituir sale… | Qué hago | Ejemplo |
|---|---|---|
| $\dfrac{0}{0}$ | Factorizar (Ruffini, identidades notables), simplificar y volver a sustituir. Con raíces, multiplicar por el conjugado | $\lim\limits_{x\to2}\dfrac{x^2-4}{x-2}=\lim\limits_{x\to2}\dfrac{(x-2)(x+2)}{x-2}=\lim\limits_{x\to2}(x+2)=4$ |
| $\dfrac{\infty}{\infty}$ | Comparar grados (tabla C) | $\lim\limits_{x\to+\infty}\dfrac{6x^2-1}{2x^2+x}=\dfrac{6}{2}=3$ |
| $\infty-\infty$ con fracciones | Restar las fracciones: queda $\frac{\infty}{\infty}$ | $\lim\limits_{x\to+\infty}\left(\dfrac{x^2}{x+1}-x\right)=\lim\limits_{x\to+\infty}\dfrac{-x}{x+1}=-1$ |
| $\infty-\infty$ con raíces | Multiplicar y dividir por el conjugado | $\lim\limits_{x\to+\infty}\left(\sqrt{x^2+1}-x\right)=\lim\limits_{x\to+\infty}\dfrac{1}{\sqrt{x^2+1}+x}=0$ |

**C. Cocientes de polinomios cuando $x\to\pm\infty$**

| Si el grado es… | El límite es… | Ejemplo |
|---|---|---|
| mayor abajo | $0$ | $\lim\limits_{x\to+\infty}\dfrac{3x+1}{x^2+5}=0$ |
| igual arriba y abajo | el cociente de los coeficientes principales | $\lim\limits_{x\to+\infty}\dfrac{6x^2-1}{2x^2+x}=\dfrac{6}{2}=3$ |
| mayor arriba | $\pm\infty$ (signo según coeficientes principales y si $x\to+\infty$ o $-\infty$) | $\lim\limits_{x\to+\infty}\dfrac{x^3}{x+1}=+\infty$ |

> [!note] Órdenes de infinito
> De más lento a más rápido: $\ln x \;\ll\; x^n \;\ll\; e^x$. En un cociente manda el más rápido: si está abajo, el límite es $0$ ($\lim\limits_{x\to+\infty}\frac{\ln x}{x}=0$); si está arriba, es $\infty$ ($\lim\limits_{x\to+\infty}\frac{e^x}{x^2}=+\infty$).

---

## 2. Derivadas

La **derivada** indica **cómo varía el valor ($y$)** de la función: $f'(a)$ es la **pendiente de la gráfica en $a$**, es decir, la velocidad a la que cambia $f$ en ese punto (**tasa de variación instantánea**).

**Tabla de derivadas** (con regla de la cadena, $u=u(x)$)

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

> [!tip] Atajos
> - Cociente con constante arriba: $\left(\dfrac{k}{g}\right)'=\dfrac{-k\,g'}{g^2}$.
> - Si el numerador de la derivada se puede factorizar, factorízalo: facilita el estudio del signo.

---

# II. Estudio completo de una función

Los pasos se hacen en este orden y al final se juntan en la [[#9. Representación gráfica|representación gráfica]].

## 3. Dominio y puntos de corte

**Dominio**: los valores de $x$ que se pueden meter en la función. $\text{Dom}(f)=\{x\in\mathbb{R} : f(x) \text{ existe}\}$

| Tipo de función | Problema | Condición | Dominio |
|---|---|---|---|
| Polinómica, exponencial $a^{g(x)}$, raíz impar | ninguno | — | $\mathbb{R}$ (o el de $g$) |
| Racional $\dfrac{P(x)}{Q(x)}$ | denominador $=0$ | $Q(x)\neq 0$ | $\mathbb{R}-\{\text{raíces de } Q\}$ |
| Raíz par $\sqrt{g(x)}$ | dentro negativo | $g(x)\geq 0$ | resolver inecuación |
| Logaritmo $\ln g(x)$ | dentro $\leq 0$ | $g(x)> 0$ | resolver inecuación |
| A trozos | cada trozo **solo vale en su intervalo** | condición del trozo $\cap$ su intervalo | unión de lo que vale en cada trozo |

> [!tip] Funciones a trozos
> Un punto problemático solo importa si está **dentro del intervalo de su trozo**. Ej.: en $\frac{1}{x+2}$ definida solo para $x>0$, el $x=-2$ no molesta.

> [!note] Contexto
> El enunciado o el sentido común recortan el dominio: distancias $x\ge 0$, unidades producidas $x\geq0$, etc.

**Puntos de corte**

| Pregunta | Qué hago | Resultado |
|---|---|---|
| ¿Dónde corta al eje X (abscisas)? | resuelvo $f(x)=0$ | puntos $(x_0,\,0)$ |
| ¿Dónde corta al eje Y (ordenadas)? | calculo $f(0)$ (si $0\in\text{Dom}$) | punto $(0,\,f(0))$ |

En funciones a trozos, se descarta la solución que no pertenezca al intervalo de su trozo.

---

## 4. Continuidad

Una función es **continua** si **se dibuja sin levantar el lápiz**: sin agujeros, escalones ni asíntotas verticales.

$f$ es continua en $x=a$ si se cumplen las tres condiciones:

| | Condición | Significado |
|---|---|---|
| 1 | $f(a)$ existe | el punto existe |
| 2 | $\lim\limits_{x\to a^-}f(x)=\lim\limits_{x\to a^+}f(x)$ (finito) | la gráfica llega a la misma altura por los dos lados |
| 3 | $\lim\limits_{x\to a}f(x)=f(a)$ | y esa altura es la del punto |

Las funciones elementales son **continuas en su dominio**, así que solo hay que estudiar los **puntos fuera del dominio** y las **uniones entre trozos**.

**Tipos de discontinuidad**

| Tipo | Qué pasa | Dibujo |
|---|---|---|
| **Evitable** | límites laterales iguales y finitos, pero $\neq f(a)$ o $f(a)$ no existe | "agujero" |
| **Inevitable de salto finito** | límites laterales finitos pero distintos | "escalón" |
| **Inevitable de salto infinito** | algún lateral es $\pm\infty$ | asíntota vertical |

**Pasos**: 1) dominio → 2) estudiar los puntos sospechosos → 3) concluir: "$f$ es continua en … y tiene una discontinuidad (tipo) en $x=$ …".

---

## 5. Asíntotas

Una asíntota es una **recta a la que la gráfica se acerca cada vez más** sin llegar a tocarla.

| Tipo | Idea | Condición | Dónde buscar |
|---|---|---|---|
| **Vertical (AV)** $x=a$ | la gráfica se va a $\pm\infty$ cerca de $a$ | $\lim\limits_{x\to a^\pm} f(x)=\pm\infty$ | puntos fuera del dominio, bordes del dominio, uniones de trozos |
| **Horizontal (AH)** $y=k$ | la gráfica se acerca a la altura $k$ hacia el infinito | $\lim\limits_{x\to\pm\infty} f(x)=k$ (número) | en $+\infty$ y en $-\infty$ **por separado** |
| **Oblicua (AO)** $y=mx+n$ | la gráfica se acerca a una recta inclinada hacia el infinito | $m=\lim\limits_{x\to\pm\infty}\dfrac{f(x)}{x}$ ($m\neq0$, finito) · $n=\lim\limits_{x\to\pm\infty}\big(f(x)-mx\big)$ | solo donde **no** hay AH |

**Qué significa cada resultado del límite**

| Límite | Si da un número | Si da $+\infty$ | Si da $-\infty$ |
|---|---|---|---|
| **AV**: $x\to a$ | no hay AV, la función se acerca a ese valor | **hay AV** | **hay AV** |
| **AH**: $x\to\pm\infty$ | **hay AH** | no hay AH, la función sube | no hay AH, la función baja |

Una función puede tener **AH distinta** en $+\infty$ y en $-\infty$.

---

## 6. Derivabilidad

Una función es **derivable** si la gráfica es "suave": sin saltos y **sin picos** (puntos angulosos).

$f$ es derivable en $a$ si es continua en $a$ **y** $f'(a^-)=f'(a^+)$ (derivadas laterales iguales).

- Si es derivable, siempre es continua.
- Si es continua, no siempre es derivable: puede tener un pico.
- Si no es continua, tampoco es derivable.

**Pasos en una función a trozos** (punto de unión $x=a$):
1. Estudiar la **continuidad** en $a$. Si no es continua, no es derivable.
2. Derivar **cada trozo** (en intervalos abiertos) y sustituir $a$: $f'(a^-)$ y $f'(a^+)$.
3. Si coinciden, es derivable en $a$; si no, hay un punto anguloso.

---

## 7. Monotonía y extremos

| $f'(x)$ | La función… | |
|---|---|---|
| $>0$ | **crece** | ↗ |
| $<0$ | **decrece** | ↘ |
| $=0$ | tangente horizontal: **posible** máximo o mínimo | — |

**Pasos**
1. Calcular $f'(x)$ (simplificada y factorizada).
2. Resolver $f'(x)=0$: **puntos críticos**.
3. Tabla de signos con los puntos críticos, los puntos fuera del dominio y las uniones de trozos.
4. Concluir:
   - Intervalos de crecimiento y decrecimiento (**abiertos**, unidos con $\cup$).
   - **Máximo relativo**: pasa de ↗ a ↘. **Mínimo relativo**: de ↘ a ↗.
   - Dar las **dos coordenadas** $(x_0,\ f(x_0))$, sustituyendo en $f$, **no** en $f'$.

> [!warning] Relativo vs absoluto
> - **Relativo**: el más alto/bajo "de los alrededores". Un máximo relativo puede ser **menor** que un mínimo relativo.
> - **Absoluto**: el más alto/bajo de **toda** la función.

---

## 8. Curvatura y puntos de inflexión

| $f''(x)$ | La función es… | Dibujo | Qué le pasa a $f'$ |
|---|---|---|---|
| $>0$ | **cóncava** | ◡ | la pendiente aumenta |
| $<0$ | **convexa** | ◠ | la pendiente disminuye |
| $=0$ | **posible** punto de inflexión | — | posible máximo/mínimo de $f'$ |

Un **punto de inflexión** es donde la gráfica **cambia de curvatura** (◡ ↔ ◠). Es también donde la función crece (o decrece) **más rápido**, porque ahí $f'$ alcanza su máximo o mínimo.

**Pasos**: igual que en monotonía, pero con $f''$. Si la curvatura cambia en un punto que **no está en el dominio**, ahí **no** hay punto de inflexión.

> [!info] Convenio de curvatura
> Si $f''>0$, la función es **cóncava ◡**; si $f''<0$, es **convexa ◠**. Algunos libros lo llaman al revés: en el examen, **dibuja el símbolo** al lado de la palabra.

> [!note] Si el enunciado da $f'(x)$ en vez de $f(x)$
> - **Monotonía y extremos**: estudia directamente el signo de esa $f'$. Para la $y$ del extremo sí necesitas $f$.
> - **Curvatura**: deriva esa $f'$ para obtener $f''$.
> - **Obtener $f$**: $f(x)=\int f'(x)\,dx + C$, con $C$ calculada a partir de un punto de la gráfica (bloque de integrales).

---

## 9. Representación gráfica

**Pasos** (en este orden)

- [ ] **Dominio** (y continuidad)
- [ ] **Cortes** con los ejes
- [ ] **Asíntotas** (AV con límites laterales, AH/AO en $+\infty$ y $-\infty$)
- [ ] **Monotonía** y **extremos**
- [ ] **Curvatura** y **puntos de inflexión**
- [ ] Algunos **valores extra** si hace falta
- [ ] Dibujar: primero las asíntotas (discontinuas), luego los puntos, y unir respetando crecimiento y curvatura.

Si algo no encaja (p. ej. crece hacia una AH desde arriba), revisa los signos: casi siempre es un error de cálculo.

---

# III. Problemas típicos

Usan solo una parte del estudio completo.

## 10. Recta tangente

La **recta tangente** "roza" la gráfica en un punto y tiene su misma inclinación.

$$y-f(a)=f'(a)\,(x-a)$$

| Necesito | Cómo lo obtengo |
|---|---|
| $x$ del punto: $a$ | dato o se averigua |
| $y$ del punto: $f(a)$ | sustituyo $a$ en $f$ |
| Pendiente $m=f'(a)$ | sustituyo $a$ en $f'$ |

| Me piden la tangente… | Planteo |
|---|---|
| en el punto de abscisa $a$ | $a$ dado |
| con pendiente $m$ | $f'(x)=m$ |
| paralela a la recta $y=mx+n$ | $f'(x)=m$ (misma pendiente) |
| paralela a $Ax+By=C$ | pendiente $m=-\frac{A}{B}$ (despejando $y$); luego $f'(x)=m$ |
| paralela al eje X / horizontal | $f'(x)=0$ |
| en los cortes con el eje X | $f(x)=0$ |
| en el punto de inflexión | $f''(x)=0$ |

---

## 11. Optimización

Encontrar **el valor de $x$ que hace máxima o mínima** una magnitud (beneficio, coste, área…).

**Pasos**
1. Identificar la **función a optimizar** y su variable (con unidades).
2. Si hay dos variables, usar el enunciado para dejar una sola.
3. Fijar el **dominio en contexto** (p. ej. $x\geq0$, $x\in[0,10]$): no hay distancias negativas.
4. Derivar y resolver $f'(x)=0$.
5. Comprobar si es máximo o mínimo (signo de $f'$, o $f''<0$ máx. / $f''>0$ mín.).
6. Si el dominio es cerrado, **comparar con los extremos** del intervalo.
7. **Responder con una frase** y unidades.

> [!tip] Lee bien qué te preguntan
> Con una función de beneficios anuales:
> - "¿Qué valor de $x$ maximiza los beneficios?" → la $x$ del máximo.
> - "¿Cuáles son los beneficios máximos?" → $f(x)$ en el máximo.

---

## 12. Ejercicios con parámetros

**Diccionario: enunciado → ecuación**

| El enunciado dice… | Escribo… |
|---|---|
| La gráfica pasa por $(a,b)$ | $f(a)=b$ |
| Corta al eje X en $x=a$ | $f(a)=0$ |
| Corta al eje Y en $y=b$ | $f(0)=b$ |
| Tiene máximo/mínimo (extremo) en $x=a$ | $f'(a)=0$ |
| Tiene máximo/mínimo en el punto $(a,b)$ | $f'(a)=0$ **y** $f(a)=b$ (2 ecuaciones) |
| Tangente horizontal / paralela al eje X en $x=a$ | $f'(a)=0$ |
| La tangente en $x=a$ tiene pendiente $m$ | $f'(a)=m$ |
| La tangente en $x=a$ tiene la misma pendiente que la recta (o función) $g$ | $f'(a)=g'(a)$ |
| La tasa de variación instantánea (velocidad) en $t=a$ vale $v$ | $f'(a)=v$ |
| Las gráficas de $f$ y $g$ se cortan | $f(x)=g(x)$ (sistema) |
| Punto de inflexión en $x=a$ | $f''(a)=0$ |
| AV en $x=a$ | el denominador se anula en $a$ (y el numerador no) |
| AH $y=k$ | $\lim\limits_{x\to\pm\infty}f(x)=k$ |
| Continua en $x=a$ ("sin levantar el lápiz") | $\lim\limits_{x\to a^-}f=\lim\limits_{x\to a^+}f=f(a)$ |
| Derivable en $x=a$ ("sin saltos ni picos") | continua **y** $f'(a^-)=f'(a^+)$ |

**Método**: 1) Traducir cada dato a una ecuación. 2) Tantas ecuaciones como parámetros. 3) Resolver el sistema. 4) **Comprobar** (p. ej. que es máximo y no mínimo).
