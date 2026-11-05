# Guía: pasar el mockup a Wix Studio

El diseño de referencia es `index.html` (abrilo en el navegador al lado del editor).
La idea es **reutilizar la tienda que ya existe** y cambiar solo la página de inicio.
Los nombres de los menús de Wix pueden variar un poco según la versión.

Antes de empezar: **duplicá la página de inicio** (clic derecho en la página → Duplicar)
y trabajá sobre la copia oculta. Cuando quede lista, la ponés como página de inicio.

## 1. Estilos del sitio (una sola vez)

En **Estilos del sitio → Colores**, cargá solo estos:

| Uso | Color |
|---|---|
| Fondo general | `#FFF8F1` (crema, nunca gris) |
| Texto y botón principal | `#6E3444` (ciruela) |
| Acento de marca (etiquetas, contacto) | `#E0576B` (rosa) |
| Naranja de la caja (detalles, hover de botones, títulos del footer) | `#E98B42` |
| Fondo de los precios | `#FDE4CC` (naranja claro) |
| Fondo de secciones con fotos rosadas | `#FEB7BF` |
| Fondo de secciones con fotos naranjas | `#F4B067` |
| Blanco | `#FFFFFF` |

Los dos fondos de sección son **el mismo color del fondo de las fotos**:
así el producto parece recortado y no se ve "un cuadrado sobre otro color".

**Tipografía:**
- Títulos: Fraunces (o una serif parecida que ofrezca Wix), en negrita.
- Texto: Nunito, 16–18 px.

**Botones:** dos estilos y no más.
- Lleno: fondo ciruela, texto blanco, totalmente redondeado. Al pasar el mouse: fondo naranja `#E98B42`.
- Borde: borde ciruela de 2 px, sin fondo.

## 2. Sacar lo que molesta

1. **Cursor:** se reemplaza por el iso de la marca con los colores de la caja (ver punto 5).
2. **Menú al bajar:** seleccioná el header → **Comportamiento al desplazar** → "Fijo" (sticky),
   con **fondo crema sólido** y sin efectos de "desaparece / se encoge".
3. **Efectos de scroll** de las secciones (parallax, revelar desde abajo, etc.):
   quitalos todos. Como mucho, "Aparecer" suave en las tarjetas.
4. **Texto en loop** "Melania en tu local": borrarlo.
5. **Burbuja "¿Cómo podemos ayudarte?"** del chat: en la app de WhatsApp/Chat, desactivar
   el mensaje automático. El botón verde se queda.

## 3. Página de inicio, sección por sección

Ancho de contenido: unos 1150 px centrado. Espacio vertical entre secciones: ~90 px.

1. **Inicio (hero):** fondo `#FEB7BF`.
   - Izquierda:
     - Etiqueta chica "COOKIES Y POSTRES ARTESANALES · MONTEVIDEO".
     - Título "Pequeños momentos que hacen *más dulces* tus días", con "más dulces" en blanco cursiva.
     - Una línea de texto y dos botones: "Ver la tienda" (lleno) y "Encargar por WhatsApp" (borde).
   - Derecha: foto "Pack de 6 cookies rosado".
   - Altura: que entre en una pantalla, no más.
2. **Nuestras cookies:** fondo crema.
   - Elemento **Galería de productos** de Wix Stores, filtrado a 4 productos.
   - Tarjetas sin borde, foto cuadrada con esquinas redondeadas, nombre y precio debajo.
   - Arriba a la derecha, un link "Ver todos los productos →". Un solo título; nada de "Todos los productos".
3. **Para regalar:** fondo `#F4B067`.
   - Foto "Pack de 6 cookies" (la naranja).
   - Título "Una caja que se abre con una sonrisa", precio "desde $ 250" y botón "Armar mi pack".
4. **Categorías:** fondo crema.
   - **Galería de categorías**, o 4 imágenes con link: Cookies, Tortas, Postres y Salados.
   - El nombre va en una píldora blanca sobre la foto. Sin marcos de otro color.
5. **Tu vitrina (mayoristas):** fondo blanco.
   - Foto del tres leches con el sello, título "Llevá nuestras delicias a tu vitrina" y 3 viñetas.
   - Botón "Quiero vender Melania".
6. **Nuestra historia:** fondo crema.
   - Texto corto y la línea 2024 / 2026; la foto a la derecha.
7. **Instagram:** fondo blanco.
   - El feed que ya tienen, en **una sola fila de 6 fotos** (3 + 3 en celular).
8. **Contacto:** fondo rosa `#E0576B`, texto blanco.
   - Botón "Escribir por WhatsApp" (blanco) y "Pedir presupuesto", que lleva al formulario.
   - El formulario largo de 5 campos va en la página de Mayoristas / Catering, no en el inicio.
9. **Footer:** fondo ciruela, texto crema, 3 columnas: logo, páginas y contacto.
   - Que el contacto se lea: nunca rosa sobre rosa.

## 4. Celular

En Wix Studio revisá la vista de **celular** por separado:
- Todo centrado.
- Productos y categorías en 2 columnas.
- Ocultar el menú de texto (queda el ícono de menú).
- Revisar que ningún título quede cortado.

## 5. Cursor con el iso de la marca

Los archivos están en `~/personal/repos/Melania/cursor/`:

| Archivo | Para qué |
|---|---|
| `cursor-32.svg` | Cursor normal: iso rosa y naranja con borde blanco, 32 px |
| `cursor-48.svg` | Mismo cursor, más grande (48 px) |
| `cursor-hover-48.svg` | Iso todo naranja, para cuando está sobre un link o botón |
| `iso-color.svg` | El iso en grande, para usar como decoración en la página |

El SVG original daba el error *"no tiene los atributos de tamaño adecuados"* porque le
faltaban `width` y `height`: solo tenía `viewBox`. Los nuevos los tienen, son cuadrados
y el iso está centrado.

En Wix Studio: seleccioná la **página** (o la sección) → panel derecho → **Cursor** →
**Agregar imagen o .svg** → subí `cursor-32.svg`. Si querés el de hover, repetí lo mismo
en los botones con `cursor-hover-48.svg`.

Para que no moleste como el anterior: un solo cursor, siempre igual, sin animación ni
cambios de color al azar.

## 6. Antes de publicar

- [ ] Ningún color fuera de la tabla del punto 1.
- [ ] El menú no tapa ni deja pasar contenido por detrás al bajar.
- [ ] Todos los botones llevan a algún lado (tienda, categoría, WhatsApp).
- [ ] Probado en celular real.
- [ ] Textos alternativos en las fotos (Wix: **Configuración de imagen → Texto alternativo**).
