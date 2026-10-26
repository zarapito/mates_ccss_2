# Apuntes de Matemáticas CCSS II

Web de apuntes para 2º de Bachillerato (Ciencias Sociales, PAU Madrid), publicada con GitHub Pages.

## Estructura

```
index.html                 ← la web (menú, fórmulas, gráficas)
.nojekyll                  ← indica a GitHub Pages que publique los archivos tal cual
apuntes/
  Inicio.md
  Funciones/               ← un bloque = una carpeta
    1 - Teoría Funciones.md
    Tabla f, f' y f''.md
    2 - Ejercicios Funciones.md
    3 - Soluciones Funciones.md
    img/                   ← gráficas del bloque (SVG)
```

Los `.md` usan la sintaxis de Obsidian: `$...$` y `$$...$$` para fórmulas, `[[enlaces]]`, `![[imagen.svg|560]]` y callouts `> [!tip]`. La web los interpreta igual que Obsidian, así que se pueden editar en Obsidian y subir sin cambios. La carpeta `apuntes/` puede abrirse directamente como vault.

## Añadir un bloque nuevo

1. Crea una carpeta en `apuntes/` (p. ej. `apuntes/Integrales/`) con sus `.md` y, si hace falta, una subcarpeta `img/`.
2. En `index.html`, busca `const SECTIONS` y añade el bloque con el nombre de la carpeta y de los archivos (sin `.md`):

```js
const SECTIONS = [
  { group: 'Inicio', folder: '', docs: ['Inicio'] },
  { group: 'Funciones', folder: 'Funciones', docs: ['1 - Teoría Funciones', "Tabla f, f' y f''", '2 - Ejercicios Funciones', '3 - Soluciones Funciones'] },
  { group: 'Integrales', folder: 'Integrales', docs: ['1 - Teoría Integrales'] },   // ← ejemplo
];
```

Los nombres de los documentos deben ser distintos entre bloques (por eso llevan el nombre del bloque al final).
