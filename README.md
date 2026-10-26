# Apuntes de Matemáticas CCSS II

Web de apuntes para 2º de Bachillerato (Ciencias Sociales, PAU Madrid), publicada con GitHub Pages.

## Estructura

```
index.html          ← la web (menú, fórmulas, gráficas). No hace falta tocarla salvo para añadir documentos
.nojekyll           ← indica a GitHub Pages que publique los archivos tal cual
apuntes/            ← los apuntes en Markdown (los mismos que se abren en Obsidian)
  Inicio.md
  1 - Teoría Funciones.md
  2 - Ejercicios Funciones.md
  3 - Soluciones Funciones.md
  img/              ← gráficas (SVG)
```

Los `.md` usan la sintaxis de Obsidian: `$...$` y `$$...$$` para fórmulas, `[[enlaces]]`, `![[imagen.svg|560]]` y callouts `> [!tip]`. La web los interpreta igual que Obsidian, así que **puedes editar los mismos archivos en Obsidian y subirlos sin cambiar nada**.

## Añadir un tema nuevo

1. Sube el nuevo `.md` a `apuntes/` (y sus imágenes a `apuntes/img/`).
2. En `index.html`, busca `const SECTIONS` y añade el nombre del archivo (sin `.md`):

```js
const SECTIONS = [
  { group: 'Inicio', docs: ['Inicio'] },
  { group: 'Funciones', docs: ['1 - Teoría Funciones', '2 - Ejercicios Funciones', '3 - Soluciones Funciones'] },
  { group: 'Integrales', docs: ['4 - Teoría Integrales'] },   // ← ejemplo
];
```
