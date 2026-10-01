# DESIGN · Firmes por el Mauxi 2027

Dirección elegida: **Acta**. La página es un documento oficial grabado, a medio camino entre diploma y papel de valor: campo azul con guilloché, cartucho, filetes dorados y un sello de lacre azul con el monograma FM. Juega con la palabra *Firmes*: un compromiso que se firma y se sella.

Clásico en la apariencia, moderno en el uso. Si una decisión hace la página más lenta, menos legible o más difícil de usar en un celular, pierde.

---

## 1. Color

Estrategia: **azul dominante** (portada, franjas de los ejes y cierre) sobre páginas de **porcelana fría**. El dorado solo dibuja: filetes, marcos, esquinas, sello y números. Nunca hay crema ni beige.

| Token | Hex | Rol |
|---|---|---|
| `--azul` | `#182C66` | Azul real. Campo dominante, títulos sobre porcelana. |
| `--azul-hondo` | `#0F1D47` | Fondo del cierre, sombra del lacre. |
| `--guilloche` | `#2B4590` | Líneas de guilloché sobre `--azul`. Solo decorativo (1,5:1). |
| `--azul-niebla` | `#B9C6E4` | Texto secundario sobre azul. |
| `--porcelana` | `#F3F6FA` | Fondo de página. Blanco frío. |
| `--porcelana-2` | `#E4EAF3` | Paneles y bandas suaves sobre porcelana. |
| `--tinta` | `#111C38` | Texto principal sobre porcelana. |
| `--tinta-2` | `#46536E` | Texto secundario sobre porcelana. |
| `--oro` | `#D9B865` | Pan de oro: texto y ornamentos **sobre azul**. |
| `--oro-claro` | `#F0DDA0` | Brillo del degradado metálico (solo sello y monograma). |
| `--oro-filete` | `#9C7A2E` | Filetes y ornamentos **sobre porcelana**. Texto solo ≥ 24 px. |

### Contraste verificado (WCAG 2.x)

| Par | Ratio | Uso permitido |
|---|---|---|
| tinta / porcelana | 15,5 | Todo texto |
| tinta-2 / porcelana | 7,1 | Todo texto |
| tinta-2 / porcelana-2 | 6,4 | Todo texto |
| azul / porcelana | 12,2 | Todo texto |
| porcelana / azul | 12,2 | Todo texto |
| porcelana / azul-hondo | 15,1 | Todo texto |
| oro / azul | 6,9 | Todo texto |
| oro / azul-hondo | 8,5 | Todo texto |
| azul-niebla / azul | 7,7 | Todo texto |
| oro-filete / porcelana | 3,7 | Solo texto grande (≥ 24 px) y gráficos |
| oro / porcelana | 1,8 | **Prohibido** para texto |
| guilloché / azul | 1,5 | Solo decoración |

### Metal

El dorado es plano por defecto (`--oro`, `--oro-filete`). El degradado metálico solo aparece en dos lugares: el monograma del sello y el filete central del cartucho de portada.

```css
--oro-metal: linear-gradient(135deg, #9C7A2E 0%, #D9B865 38%, #F0DDA0 50%, #D9B865 62%, #9C7A2E 100%);
```

---

## 2. Tipografía

| Familia | Archivo | Rol |
|---|---|---|
| **Libre Caslon Display** | `assets/fonts/libre-caslon-display.woff2` (25 KB) | Títulos, números de propuesta, cartucho. Voz de documento firmado: Caslon es la letra de los grandes documentos de los siglos XVIII y XIX. |
| **EB Garamond** (variable 400–700) | `assets/fonts/eb-garamond-wght.woff2` (74 KB) | Texto, botones y **versalitas reales** (`smcp`, `c2sc`). Garamond francés, cómodo en párrafos largos. |

Las dos están recortadas al español (incluye `¿¡ñáéíóú «» ° ₂ №`) y alojadas con `@font-face` y `font-display: swap`. Licencias en `assets/fonts/OFL-*.txt`.

### Reglas

- **Versalitas, nunca mayúsculas espaciadas.** Las etiquetas usan `font-variant-caps: all-small-caps` (EB Garamond), con `letter-spacing: 0.04em`.
- **Números de estilo antiguo** en el texto corrido (`font-variant-numeric: oldstyle-nums`); **números alineados** en la rejilla de datos (`lining-nums tabular-nums`).
- **Sin cursiva de caligrafía** y sin acentuar una palabra suelta del titular con otro color o estilo.
- El texto no lleva mayúsculas sostenidas.
- Medida de línea: 34 a 62 caracteres (`max-width: 62ch` en el texto corrido).

### Escala (base en celular 19 px, fluida hasta escritorio)

| Token | Valor | Uso |
|---|---|---|
| `--t-etiqueta` | `clamp(1rem, 0.96rem + 0.2vw, 1.0625rem)` | Versalitas de etiqueta, rejilla de datos |
| `--t-cuerpo` | `clamp(1.1875rem, 1.12rem + 0.3vw, 1.3125rem)` | Texto corrido (19 → 21 px) |
| `--t-entrada` | `clamp(1.3125rem, 1.2rem + 0.6vw, 1.625rem)` | Entradillas de eje |
| `--t-h3` | `clamp(1.5rem, 1.3rem + 1vw, 2.125rem)` | Nombre de cada propuesta |
| `--t-h2` | `clamp(2.25rem, 1.6rem + 3vw, 4rem)` | Título de eje |
| `--t-numeral` | `clamp(3.5rem, 2.6rem + 4vw, 6rem)` | Número de propuesta (1–11) |
| `--t-display` | `clamp(3rem, 1.9rem + 5.6vw, 7rem)` | «Firmes por el Mauxi» en la portada |

Interlineado: cuerpo 1.55; títulos 1.05 a 1.15; etiquetas 1.3.

---

## 3. Espacio y retícula

Base de 4 px. Una sola escala para toda la página. Hay más espacio encima de un título que debajo.

| Token | Valor |
|---|---|
| `--s-1` | 0.25rem (4 px) |
| `--s-2` | 0.5rem (8 px) |
| `--s-3` | 0.75rem (12 px) |
| `--s-4` | 1rem (16 px) |
| `--s-5` | 1.5rem (24 px) |
| `--s-6` | 2rem (32 px) |
| `--s-7` | 3rem (48 px) |
| `--s-8` | 4rem (64 px) |
| `--s-9` | 6rem (96 px) |
| `--s-10` | 8rem (128 px) |
| `--seccion` | `clamp(4rem, 2.5rem + 6vw, 8rem)` (espacio vertical entre secciones) |
| `--margen` | `clamp(1rem, 0.5rem + 2.5vw, 2.5rem)` (margen lateral: 16 px en celular) |
| `--ancho` | `76rem` (contenido máximo en escritorio) |

- Celular primero: una columna, 360 a 390 px.
- Escritorio: retícula de 12 columnas con `--ancho`; nunca hay desplazamiento horizontal de la página.
- La portada usa `min-height: 100svh`, no `100vh` (por la barra de direcciones móvil).

---

## 4. Ornamentos (set SVG propio)

Todos se dibujan a mano en SVG, con la **misma lógica**: trazo de **1 px** a tamaño real (`vector-effect: non-scaling-stroke`), extremos rectos, ángulos de 45° y la misma rejilla de 24 unidades. Ninguno usa relleno salvo los puntos y el sello. Son pocos y siempre se repiten igual.

| Pieza | Descripción | Dónde |
|---|---|---|
| **Guilloché** | Patrón de rosetas de líneas finas (`--guilloche` sobre `--azul`), en un `<pattern>` SVG que se repite. Pesa menos de 3 KB. | Portada, franjas de eje, cierre |
| **Marco de acta** | Doble filete: exterior de 1 px y, separado por 4 px, uno interior de 1 px. | Cartucho de portada, propuestas principales |
| **Esquina** | Cuarto de roseta grabada con un punto central. Es la misma pieza girada en las cuatro esquinas. | Marcos de acta |
| **Filete central** | Línea con un rombo en el centro (◆) y remates cortos. | Separadores entre bloques |
| **Monograma FM** | Las letras F y M en Libre Caslon Display, entrelazadas dentro de un doble anillo con texto circular «Firmes por el Mauxi · 2027». | Sello de lacre, favicon, imagen Open Graph |
| **Íconos de grabado** | 24 × 24, trazo 1,25. Uno por cada propuesta express y herramienta; reemplazan todos los emojis del original. | Propuestas express, herramientas |

Prohibido: pergamino, manchas de envejecido, bordes quemados, texturas de papel, cintas, querubines, caligrafía.

---

## 5. Componentes

- **Cartucho de portada:** marco de acta sobre el campo de guilloché, con el nombre de la campaña, el candidato y el llamado a la acción. El sello se asienta en su borde.
- **Propuesta principal (acta):** fondo porcelana, marco de acta con esquinas, número grande en Caslon (1–11), versalita de categoría, título, texto y una línea final en `--oro-filete` con la idea fuerza.
- **Propuesta express (talón):** piezas idénticas que se leen de un barrido, como estampillas o talones de un talonario. Llevan ícono, título, texto y una **rejilla fija de datos**: *Frecuencia · Herramienta · Arranque*, en celdas y nunca separadas por puntos medios.
- **Botón:** rectángulo con doble filete, texto en versalitas. Primario: `--oro` sobre `--azul` (en portada y cierre) o `--azul` sobre `--porcelana`. El objetivo táctil mide al menos 44 × 44 px. Sin flechas «→».
- **Índice:** navegación fija y compacta con los ejes I–IV en números romanos. Se usa completa con teclado.
- **Foco:** contorno de 2 px con separación de 3 px; `--azul` sobre porcelana y `--oro` sobre azul.

---

## 6. Movimiento

Un solo momento orquestado: **el sello**. Todo lo demás es sobrio.

| Token | Valor | Uso |
|---|---|---|
| `--dur-micro` | 160ms | Estados de botones y enlaces |
| `--dur-ui` | 240ms | Abrir y cerrar el índice |
| `--dur-sello` | 900ms | Estampado del sello |
| `--ease-salida` | `cubic-bezier(0.22, 1, 0.36, 1)` | Entradas |
| `--ease-sello` | `cubic-bezier(0.3, 1.35, 0.5, 1)` | Presión y asentamiento del lacre |

- **Sello (portada):** baja desde una escala de 1.4 y opacidad 0, presiona a 0.96 y se asienta en 1. Un anillo de cera se expande una vez. Solo se animan `transform` y `opacity`, con la Web Animations API.
- **Cierre:** el mismo sello reaparece y «firma» el compromiso.
- Las secciones no aparecen con fundidos al hacer scroll; el contenido está visible desde el principio.
- `prefers-reduced-motion: reduce`: el sello aparece ya asentado, sin animación.

---

## 7. Calidad mínima

- Contraste AA verificado (tabla de la sección 1), foco visible y HTML semántico con `header`, `nav`, `main`, `section` y `footer`.
- Imágenes en WebP con `loading="lazy"` (excepto la de la portada), `alt` descriptivo y `width`/`height` declarados.
- Lighthouse ≥ 90 en rendimiento y accesibilidad.
- Open Graph y una imagen de vista previa de 1200 × 630 con el sello y el nombre.
- Funciona en GitHub Pages sin compilación: `index.html`, `styles.css`, `main.js`.
