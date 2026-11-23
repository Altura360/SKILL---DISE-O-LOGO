# Instrucciones para Claude: aplicar la marca nueva de KontrolPagos

Eres un asistente trabajando en el código de la plataforma **KontrolPagos** (control de pagos de obra: estimaciones, avance físico, proyectos y casas, ampliaciones, descuentos, destajistas, reportes). La persona que te lo pide es ingeniera/ingeniero civil y está empezando en programación: **explica cada paso en español, con palabras simples**, y muéstrale qué cambiaste.

Esta carpeta trae la marca ya terminada. **No rediseñes nada**: solo aplícala.

## Reglas de seguridad (léelas primero)
1. Trabaja en una **rama nueva** (por ejemplo `marca-nueva`). No toques la rama principal.
2. Cambia **solo apariencia**: logo, íconos, colores y tipografías. **No cambies lógica, datos, rutas ni cálculos de dinero.**
3. Antes de editar, revisa cómo está hecho el proyecto (framework, dónde están los estilos, cómo se carga el logo) y dime qué encontraste.
4. Haz cambios pequeños y verificables. Al terminar, corre el build/lint/tests del proyecto y dime el resultado real (si algo falla, dilo).
5. No subas ni publiques nada sin que la persona lo apruebe. La plataforma está en Vercel; si la rama se publica sola como vista previa, pídele que la revise antes de unirla a la principal.
6. Conserva el nombre de la empresa/tenant ("TRACOTAMSA") y su logo redondo si existe: la plataforma es del cliente, el logo de KontrolPagos es del producto.

## Qué hay en esta carpeta
| Carpeta | Contenido | Dónde ponerlo en el proyecto |
|---|---|---|
| `logo/` | Logo en SVG: horizontal, vertical, solo símbolo, versión invertida (fondo oscuro) y `una-tinta/` | `public/brand/` (o donde el proyecto guarde imágenes) |
| `iconos-web/` | favicon, ícono de app, `site.webmanifest`, `head-snippet.html` | Archivos de ícono en la **raíz pública** (`public/`), porque el snippet los llama como `/favicon.ico`, etc. |
| `fonts/` | Sora (títulos) y DM Sans (textos), variables, uso libre (OFL) | `public/fonts/` |
| `estilos/kontrolpagos-tokens.css` | Colores como variables CSS, `@font-face`, estilos base | Importarlo en los estilos globales; **ajusta las rutas `../fonts/`** a donde copies las fuentes |
| `referencia/` | `guia-de-marca.png` y `maqueta-pantalla-proyectos.png`: así debe verse | Solo para mirar (no se copia) |

## Marca (valores exactos)
| Nombre | HEX | Uso |
|---|---|---|
| Marino | `#14263F` | Textos principales, logo, barras de progreso, menú oscuro si lo hay |
| Amarillo oro | `#FFB800` | Botones de acción, indicador del menú activo, resaltados (**texto encima siempre en Marino**) |
| Acero | `#5B6B78` | Textos secundarios, íconos, etiquetas |
| Niebla | `#F2F5F9` | Fondo de pantallas |
| Blanco | `#FFFFFF` | Tarjetas, menú lateral |
| Pagado | `#16794C` | Estado "Autorizada/Pagado" |
| Por pagar | `#2F6FB5` | Estado pendiente/por pagar |
| Vencido / alerta | `#C8382F` | Solo alertas y errores |

Tipografías: **Sora** para títulos y cifras grandes (peso 600-700); **DM Sans** para textos, tablas y botones. En tablas e importes usa `font-variant-numeric: tabular-nums`.

## Qué cambiar, paso a paso
1. **Logo del menú lateral**: donde hoy aparece el texto/imagen "KONTROLPAGOS" arriba a la izquierda, usa `logo/kontrolpagos-horizontal-color.svg` (ancho aprox. 200-215 px). Debajo deja el nombre del tenant ("TRACOTAMSA") como está. En fondos oscuros usa `kontrolpagos-horizontal-invertido.svg`.
2. **Favicon y app instalable ("Instalar app")**: copia `iconos-web/*` a la raíz pública, pega `head-snippet.html` en el `<head>` global (en Next.js, en `layout`/metadata) y reemplaza el manifest existente por `site.webmanifest` (si ya hay uno, conserva sus campos propios). `theme_color` = `#14263F`.
3. **Colores**: importa `estilos/kontrolpagos-tokens.css` y reemplaza los colores actuales:
   - Botones principales (hoy rojos, p. ej. "Nueva estimación", "Nuevo proyecto"): fondo Amarillo oro, texto Marino, esquinas igual que ahora.
   - Indicador del ítem activo del menú (hoy una barra roja a la izquierda): Amarillo oro. Fondo del ítem activo: gris-azul muy claro (`#E7EDF5`).
   - Enlaces tipo "Ver todas", "Ver las estimaciones": Marino (subrayado al pasar el cursor), ya no rojos.
   - Barras de progreso: relleno Marino sobre pista `#E3E9F0`.
   - Gráfica "Pagado por semana": barras en gris azulado; la semana actual en Marino.
   - Fondo general: Niebla `#F2F5F9` (hoy es un blanco cálido).
   - **El rojo se queda solo para alertas**: bloque "Pagado de más", insignia roja de "Descuentos", estados vencidos, errores. No lo uses en botones principales.
   - Insignias de conteo: "Ampliaciones" se queda ámbar; "Descuentos" se queda roja.
4. **Tipografías**: carga Sora y DM Sans (con `@font-face` apuntando a `public/fonts/` o con el sistema de fuentes del framework). Los títulos de página y tarjetas pasan a Sora (hoy son condensados en mayúsculas; mantén las mayúsculas si el diseño actual las usa). Texto general, menús, tablas y botones en DM Sans.
5. **Revisión final**: recorre estas pantallas y compáralas con `referencia/maqueta-pantalla-proyectos.png`: Inicio (Bandeja de costos), Estimaciones (tabla), Avance físico, Proyectos y casas, Ampliaciones, Descuentos, Destajistas, Reporte semanal, Control de costos, Usuarios. Revisa también en pantalla de celular.

## Criterios de "terminado"
- [ ] Logo nuevo en el menú lateral y en la pantalla de inicio de sesión (si existe).
- [ ] Favicon nuevo en la pestaña; ícono nuevo al instalar la app.
- [ ] Ningún botón principal rojo; el rojo solo en alertas.
- [ ] Texto sobre amarillo siempre en Marino (contraste legible).
- [ ] Sora en títulos y DM Sans en textos; importes alineados en tablas.
- [ ] Build y lint sin errores nuevos; ninguna pantalla se ve rota.
- [ ] Resumen en español de los archivos que cambiaste y capturas/antes-después si es posible.

## Si algo no está claro
Pregunta a la persona antes de adivinar. Si el proyecto ya usa Tailwind, CSS Modules u otro sistema, adapta las variables de `kontrolpagos-tokens.css` a ese sistema en lugar de forzar CSS global nuevo.
