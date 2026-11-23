# KontrolPagos · Marca oficial

**Combinación elegida:** color 2 (azul marino + amarillo oro) · tipografía 5 (Sora + DM Sans) · logo opción 2 (K con moneda con borde).

**Idea del logo:** la K (Kontrol) sostiene la moneda amarilla (el pago). Los brazos de la K recuerdan el arriostre en K de las estructuras de acero.

## Qué archivo usar (carpeta `final/`)
| Uso | Archivo |
|---|---|
| Fondo blanco o claro | `kontrolpagos-horizontal-color.svg` (o `-vertical-`, `-simbolo-color`) |
| Fondo marino | `kontrolpagos-horizontal-invertido.svg` (o `-vertical-`, `-simbolo-invertido`) |
| Una sola tinta (sellos, bordado) | `una-tinta/*-black.svg` / `*-white.svg` |
| Fondo amarillo | `una-tinta/kontrolpagos-horizontal-black.svg` |
| Ícono de la página, de la app y redes | `web/` (pega `head-snippet.html` en el `<head>`) |
| Colores y tipografías para programar | `web/kontrolpagos-tokens.css` + carpeta `fonts/` |
| Resumen visual | `guia-de-marca.png` |

## Colores
| Nombre | HEX | Uso |
|---|---|---|
| Marino | `#14263F` | K, nombre, textos, menú oscuro |
| Amarillo oro | `#FFB800` | Moneda, botones de acción, resaltados (texto encima en marino) |
| Acero | `#5B6B78` | Textos secundarios, íconos |
| Niebla | `#F2F5F9` | Fondo de pantallas |
| Pagado / Por pagar / Vencido | `#16794C` / `#2F6FB5` / `#C8382F` | Estados en la plataforma |

Los CMYK de `guia-de-marca.png` son aproximados; antes de imprimir pide una prueba de color.

## Tipografía (uso libre, licencia OFL)
- **Sora**: títulos y cifras grandes (SemiBold / Bold).
- **DM Sans**: textos, tablas y botones (Regular / Medium / Bold).
- En tablas con importes usa `font-variant-numeric: tabular-nums` para que los números se alineen.
- El nombre del logo está dibujado con Sora, convertido a curvas. No lo reescribas con texto.

## Reglas rápidas
- Espacio libre alrededor del logo: al menos el diámetro de la moneda.
- Tamaño mínimo: símbolo 16 px en pantalla; logo horizontal 96 px de ancho.
- El amarillo sobre blanco tiene poco contraste (1.7:1): la moneda siempre va junto a la K oscura, y el texto sobre amarillo siempre en marino.
- En botones: fondo amarillo con texto marino. El rojo se reserva para alertas y errores.
- No estirar, no girar, no agregar sombras, no cambiar los colores.

## Otras carpetas
`opciones/`, `colores/`, `tipografias/` guardan las alternativas que se revisaron. `mockups/` tiene la maqueta de tu pantalla con la marca final.

## Pendiente
- Búsqueda de marca registrada del nombre.
- Si se imprime en grande (letrero, lona), que un diseñador revise el espaciado del nombre.
- Aplicar los cambios en el código de la plataforma (logo del menú, colores y fuentes).
