# Cómo llenar esta carpeta

Aquí van las imágenes que le muestran a Claude Code el estilo que quieres. Es la parte que más influye en el resultado, porque las palabras "victoriano" o "elegante" significan cosas distintas para cada persona. Las capturas le enseñan tu gusto exacto.

## Qué hay en esta carpeta

- `Firmes_por_el_Maux_2027_v2.html`: tu página actual. Claude Code saca de aquí el texto de las propuestas, no el diseño. No la borres ni le cambies el nombre.
- `capturas/`: aquí van tus capturas de pantalla.
- `notas.md`: aquí escribes qué te gusta y qué no de cada captura.

## Paso 1: busca referencias

Abre los sitios de la lista de abajo y quédate solo con los que te gusten de verdad. No hace falta usarlos todos. Si encuentras otros que te gusten más, mejor.

**Casas francesas e italianas con estética del siglo XIX**

- Officine Universelle Buly (París, 1803): https://buly1803.com/en-us
- Santa Maria Novella (Florencia, 1221): https://eu.smnovella.com/
- Mariage Frères (París, 1854): https://www.mariagefreres.com/en/
- Ladurée (París): https://www.laduree.com/
- Cire Trudon (París): https://trudon.com/
- Fornasetti (Milán): https://www.fornasetti.com/

**Hoteles históricos**

- Grand Hotel Tremezzo (Lago de Como): https://www.grandhoteltremezzo.com/en/
- Ritz Paris: https://www.ritzparis.com/

**Instituciones**

- Ópera de París: https://www.operadeparis.fr/
- Universidad de Bolonia: https://www.unibo.it/

**Tipografías** (para ver letras con raíz italiana y francesa)

- Bodoni Moda: https://fonts.google.com/specimen/Bodoni+Moda
- GFS Didot: https://fonts.google.com/specimen/GFS+Didot

**Para buscar más ideas**

- Pinterest: busca "victorian ornament", "belle époque poster", "engraved certificate", "wax seal design", "art nouveau border".
- Awwwards (https://www.awwwards.com): busca "luxury" o "heritage".

**Objetos reales** (también sirven, y mucho)

- El escudo del colegio y sus colores oficiales.
- Billetes antiguos, diplomas, menús de restaurantes clásicos, etiquetas de perfume, portadas de libros viejos, sellos de lacre.
- Fotos de la arquitectura del colegio, si tiene detalles clásicos.

## Paso 2: toma las capturas

Lo ideal son entre 5 y 10. Captura **detalles**, no solo páginas completas: un encabezado, un adorno, una combinación de letras, un botón, un marco.

En Windows:

- **Una parte de la pantalla:** presiona `Windows + Shift + S` y arrastra sobre lo que quieres. En Windows 11 la captura se guarda sola en `Imágenes > Capturas de pantalla`. Muévela a la carpeta `capturas/`.
- **Una página completa:** en Microsoft Edge, presiona `Ctrl + Shift + S` y elige "Capturar página completa". Luego guárdala en `capturas/`.
- **Vista de celular:** también sirve tomar capturas desde tu teléfono, porque la mayoría de tus compañeros verán la página ahí. Pásalas al computador por WhatsApp Web o un cable.

Ponles nombres que digan qué son, sin espacios ni tildes. Por ejemplo:

```
01-buly-encabezado.png
02-tremezzo-portada.png
03-laduree-adornos.png
04-billete-antiguo-marco.jpg
05-escudo-colegio.png
```

## Paso 3: escribe tus notas

Abre `notas.md` y, por cada captura, escribe una o dos líneas: qué te gusta y qué no. Esto vale tanto como la captura misma.

Incluye también una o dos **anti-referencias**: cosas que NO quieres, para que Claude Code sepa qué evitar.

## Opción automática

Si tienes Playwright instalado en Claude Code, él puede visitar los sitios y tomar las capturas por ti. Escríbele:

> Visita los sitios de referencias/LEEME.md con Playwright, toma capturas a 390 px y a 1440 px y guárdalas en referencias/capturas. Después muéstramelas para que yo elija cuáles me gustan.

Aun así, las notas debes escribirlas tú: Claude Code no puede adivinar tu gusto.
