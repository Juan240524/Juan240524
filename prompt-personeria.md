# Página de campaña: Firmes por el Mauxi 2027

Vas a diseñar y construir desde cero la página web de mi campaña a personero estudiantil del Colegio de María Auxiliadora (Barranquilla, Colombia). Quiero que sea lo más bella y cuidada que puedas hacer, al nivel de la página de una universidad europea, un hotel histórico o una casa de moda.

Responde siempre en español y explícame brevemente por qué tomas cada decisión de diseño. Estoy aprendiendo.

## 1. Antes de escribir código

1. Lee `CLAUDE.md`, todo `referencias/` y todo `assets/`. Mira cada imagen de `referencias/capturas/` junto con lo que escribí sobre ella en `referencias/notas.md`, y resúmeme en pocas líneas qué entendiste de mi gusto antes de seguir. Las capturas que empiezan por `no-` muestran lo que NO quiero. Si `capturas/` está vacía, avísame.
2. Revisa qué skills tienes disponibles. Debes usar: `impeccable`, `design-taste-frontend` (taste), `emil-design-eng`, `apple-design`, `animate`, `mobile-native`, `review-animations` y `frontend-design` si está instalada. Si falta alguna, dímelo antes de seguir.
3. Ejecuta el `init` de impeccable para crear `PRODUCT.md`. Usa este documento para responder todo lo que puedas y pregúntame solo lo que falte.
4. Si el MCP de Figma está conectado y te paso un enlace de Figma, úsalo como referencia. Si no está conectado, ignóralo y sigue sin él.

## 2. Contenido

- El contenido está en `referencias/Firmes_por_el_Maux_2027_v2.html`. Usa su texto, no su diseño.
- La estructura es: presentación de la campaña, cuatro ejes (I. Académico, II. Convivencial, III. Ambiental, IV. Cultural), cada uno con propuestas principales y "propuestas express" (acciones rápidas, sin presupuesto, ejecutables en menos de 2 semanas), y un cierre.
- No inventes propuestas, cifras, citas, nombres ni logros. Si falta algo (fotos del equipo, lema, redes), pregúntame o deja un espacio claramente marcado.
- El nombre correcto es "Firmes por el Mauxi". Corrige cualquier "Maux".
- Antes de reescribir textos, pregúntame:
  - Si me refiero al estudiantado como "las estudiantes", "los estudiantes" o con lenguaje neutro. El original mezcla formas.
  - Si la numeración de las propuestas principales (hoy salta 1, 2, 9, 3, 4, 10…) significa algo o se debe reordenar.
- Reemplaza todos los emojis del original por iconografía coherente con el estilo.
- Puedes acortar y pulir textos para que se lean bien en celular, pero sin cambiar su significado. Muéstrame los cambios.

## 3. Dirección estética

**Estilo:** victoriano tradicional con estética italiana y francesa. Piensa en:

- La portada de un libro antiguo o un diploma grabado.
- La tipografía de Giambattista Bodoni (Parma) y la familia Didot (París).
- Bibliotecas florentinas, la Ópera Garnier, salones Beaux-Arts y Belle Époque.
- Grabados en metal, papel moneda antiguo, guilloché, sellos de lacre, cartuchos, filigranas, marcos dorados y tarjetas de visita del siglo XIX.

**Colores:** gama dorada, azul y blanca.

- El blanco es blanco porcelana o mármol, frío y limpio. No uses crema ni beige: es el cliché más común de las páginas hechas por IA.
- El azul es profundo (lapislázuli, azul de Prusia o azul real) y puede ser el color dominante.
- El dorado es para líneas, ornamentos, filetes y detalles. Que se sienta como pan de oro, no como amarillo plano. Usa degradados metálicos solo donde aporten y con mucha moderación.
- El dorado sobre blanco casi nunca pasa el contraste AA para texto. Úsalo en texto solo sobre azul o en tamaños grandes, y verifícalo.

**El equilibrio clave:** clásico en la apariencia, moderno en el uso. Debe verse como una pieza de herencia elegante, nunca como una invitación de boda barata, una plantilla "vintage" o un disfraz. La navegación, la legibilidad y la velocidad deben ser de página actual.

**Un solo elemento memorable.** Propón cuál. Una idea posible: un sello de lacre o un monograma "FM" que se estampa al cargar la página, jugando con la palabra "Firmes". Todo lo demás debe ser sobrio y disciplinado.

## 4. Reglas que mandan sobre las skills

Las skills tienen reglas por defecto que chocan con este estilo. Cuando choquen, gana este documento:

- **Tipografía serif:** está justificada porque el estilo es de herencia. Prefiero tipografías con raíz histórica real italiana, francesa o británica (por ejemplo Bodoni Moda, GFS Didot, Libre Caslon, EB Garamond, Cormorant), pero elige tú y justifícalo. Aloja las fuentes en el proyecto con `@font-face`.
- **Composiciones centradas y simétricas:** están permitidas donde sirvan al estilo clásico, pero varía las secciones para que no se repita el mismo esquema.
- **Ornamentos SVG hechos a mano:** están permitidos y son parte central del estilo. Crea un set coherente (esquinas, filetes divisorios, marcos, monograma, íconos de grabado) con el mismo grosor de trazo y la misma lógica. Pocos y bien hechos.
- **Versalitas (small caps)** en lugar de etiquetas en mayúsculas espaciadas.
- **Stack:** HTML, CSS y JavaScript sin frameworks, sin React, sin Next.js y sin Tailwind. Animaciones con CSS y la Web Animations API, sin librerías pesadas.

## 5. Calidad mínima

- Diseño primero para celular (360–390 px) y después para escritorio. La mayoría la abrirá desde WhatsApp o Instagram.
- Contraste AA mínimo, foco visible con teclado, HTML semántico y `alt` en todas las imágenes.
- Respeta `prefers-reduced-motion`.
- Imágenes en WebP con carga diferida. Lighthouse de 90 o más en rendimiento y accesibilidad.
- Etiquetas Open Graph para que el enlace se vea bien al compartirlo en WhatsApp.
- Debe funcionar en GitHub Pages sin pasos de compilación.

## 6. Flujo de trabajo

1. **Dirección:** propón 3 direcciones distintas dentro de este estilo. Para cada una incluye nombre, paleta en hex, tipografías, el elemento memorable, un wireframe ASCII del hero en celular y en escritorio, y una frase sobre su personalidad. Revisa cada dirección contra las listas de clichés de tus skills y corrige lo que suene genérico. Espera a que yo elija.
2. **Sistema:** con la dirección elegida, define tokens (colores, escala tipográfica, espaciado, ornamentos) en `DESIGN.md`.
3. **Construcción por secciones**, en este orden: hero, eje I, ejes II–IV, propuestas express, cierre. Después de cada sección toma capturas a 390 px y a 1440 px, critícalas tú mismo y corrige antes de mostrármelas.
4. **Revisión final:**
   - `critique` y `audit` de impeccable.
   - `review-animations` de Emil para todo el movimiento.
   - Las pautas de `mobile-native` en celular.
   - `polish` de impeccable como último paso.
5. **Entrega:** un `README.md` corto que explique cómo publicarla en GitHub Pages.

Haz commit con un mensaje claro cada vez que yo apruebe un avance. Pídeme confirmación antes de borrar archivos, hacer `git push` o instalar algo nuevo.

Empieza con el paso 1 de la sección 1.
