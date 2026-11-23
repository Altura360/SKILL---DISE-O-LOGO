# KontrolPagos · Logo (concepto B: K y moneda)

**Idea:** la K (Kontrol) sostiene la moneda amarilla (el pago). Los brazos de la K recuerdan el arriostre en K de las estructuras de acero.

## Qué archivo usar
| Uso | Archivo |
|---|---|
| Fondo blanco o claro | `final/kontrolpagos-horizontal-color.svg` (o `-vertical-`, `-simbolo-color`) |
| Fondo oscuro (grafito) | `final/kontrolpagos-horizontal-invertido.svg` |
| Una sola tinta (sellos, fax, bordado) | `final/una-tinta/*-black.svg` / `*-white.svg` |
| Página web (favicon, app, redes) | `final/web/` (copiar el contenido de `head-snippet.html` en el `<head>`) |

## Colores
| Nombre | HEX | Uso |
|---|---|---|
| Grafito | `#1F2A33` | K, nombre, textos, fondos oscuros |
| Amarillo oro | `#FFB800` | Moneda, botones de acción, resaltados (texto encima en grafito) |
| Acero | `#5B6B78` | Textos secundarios, íconos |
| Niebla | `#F1F4F6` | Fondos claros |
| Pagado / Por pagar / Vencido | `#16794C` / `#2F6FB5` / `#C8382F` | Estados en la plataforma |

Los CMYK de `final/paleta-de-colores.png` son aproximados; antes de imprimir pide una prueba de color a la imprenta.

## Reglas rápidas
- Espacio libre alrededor del logo: al menos el diámetro de la moneda.
- Tamaño mínimo: símbolo 16 px en pantalla; logo horizontal 96 px de ancho.
- Sobre fondo amarillo usa solo la versión en negro. El amarillo sobre blanco tiene poco contraste (1.7:1): la moneda siempre va junto a la K oscura, y el texto sobre amarillo siempre en grafito.
- No estirar, no girar, no agregar sombras, no cambiar los colores.
- El nombre está dibujado con la tipografía Inter (licencia libre), convertida a curvas. No lo reescribas con texto.

## Otras opciones
En `opciones/` hay variantes de la moneda (lisa, con borde, con check) y de color de la K (azul marino, verde petróleo). El paquete `final/` usa la moneda con borde.

## Pendiente
Búsqueda de marca registrada del nombre, y una revisión final del nombre dibujado (kerning) con un diseñador si se va a imprimir en grande.
