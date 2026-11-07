# Tutorial Figma · Semana 4 — Landing page responsiva
**Prototipos Navegables (DUD2204) · Experiencia 2 · Clase del miércoles 11 de noviembre**

> 🧭 **Hoy tu landing aprende a vivir en el celular.** No vas a «achicar» la versión de escritorio: vas a diseñar la versión móvil con los mismos componentes y el mismo contenido, reorganizado para una pantalla chica.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 3](../semana-03/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 2 horas (puedes dividirlo: pasos 1 a 6 y pasos 7 a 11).

> 📌 **Sobre la AF3:** el caso pide una landing **móvil** (mínimo 350 px de ancho) para una tienda de distribución de productos Apple, con un **catálogo de 5 productos**, columnas, tipografía y espaciado accesibles, interacciones móviles y contenido sobre y bajo el fold. Este tutorial te lleva por todo eso; la versión de escritorio es un paso extra que te servirá en las semanas siguientes.

## 📎 Ejemplo de la clase en Figma

[▶ Abrir el ejemplo de la Clase 04 en Figma](https://www.figma.com/design/eWj1T2gmUaWlSM3tMLGhad)

Es el mismo proyecto Apple Store que construimos en clase, tal como queda al terminar esta semana. Úsalo **después** de hacer el tutorial: compara tu archivo con el ejemplo, revisa cómo están armadas las capas y los componentes, y presiona **▶ Presentar** para probar el prototipo. Si quieres desarmarlo, duplícalo en tus borradores: el original no cambia. Si tienes una duda, déjala como comentario (tecla **C**) sobre el elemento.

---

## Qué vas a aprender

- Usar **cuadrículas de columnas** de 4 (móvil) y 12 (escritorio).
- Diseñar la home móvil de **375 px** con Mobile First.
- Apilar el hero, pasar la grilla de productos a **1 columna** y el footer a **acordeón**.
- Abrir el menú hamburguesa como **superposición (overlay)**.
- Dejar el menú **fijo** mientras la página hace scroll.
- Crear **dos flujos**, uno móvil y uno de escritorio, para presentarlos por separado.

## Antes de comenzar

Abre **`Apple Store — Proyecto PI`**. Necesitas:

- [ ] La landing `Home · Desktop 1440` de la semana 2.
- [ ] `Navbar/Mobile` y los estilos `Mobile/H1`, `Mobile/H2`, `Mobile/H3` de la semana 3.
- [ ] `Botón/Primario`, `Botón/Secundario` (si lo hiciste) y `Card/Producto`.

## La idea en una tabla

Esto es lo que cambia entre escritorio y móvil. Tenla a la vista mientras trabajas.

| Elemento | Desktop 1440 | Mobile 375 |
| --- | --- | --- |
| Columnas | 12 · margen 80 · separación 24 | 4 · margen 20 · separación 16 |
| Hero | Texto e imagen lado a lado | Apilado: texto arriba, imagen abajo |
| Título H1 | 72 px | 40 px |
| **Texto de cuerpo** | **17 px** | **17 px (no se reduce)** |
| Productos | 4 columnas | 1 columna |
| Navegación | Links visibles | Menú ☰ que abre un panel |
| Botones del hero | En línea, 160 × 44 | Uno sobre otro, ancho completo, 50 de alto |
| Footer | 4 columnas | Acordeón |
| Padding lateral | 80 | 20 |

---

## Paso 1 — Preparar la página

**Meta:** las dos versiones de la landing en la misma página.

**Concepto: flujos en una página.** Los flujos de prototipo (Paso 10) se crean entre frames de **la misma página**. Por eso juntamos ambas versiones.

### Haz esto

1. Crea la página `Landing · Responsiva`.
2. Ve a `Landing · Desktop`, selecciona el frame `Home · Desktop 1440`, cópialo (**Ctrl + C** / **Cmd + C**) y pégalo en la página nueva (**Ctrl + V** / **Cmd + V**).
3. Deja espacio a la izquierda para el frame móvil.

---

## Paso 2 — Cuadrículas de columnas

**Meta:** ver las columnas sobre cada frame, para alinear todo.

**Concepto: cuadrícula.** Son columnas guía que no se ven en el prototipo, pero ayudan a alinear. Móvil usa 4 columnas, tablet 8 y escritorio 12.

**Dónde está:** selecciona un frame. En el panel derecho, sección **Guías de diseño / Layout guide** (antes «Layout grid»), pulsa **+**.

### Haz esto

1. Selecciona `Home · Desktop 1440` y agrega una guía. Haz clic en su ícono para editarla: **Columnas / Columns**, cantidad `12`, margen `80`, separación (gutter) `24`.
2. Crea un frame de **375 × 812** y nómbralo `Home · Mobile 375`.
3. Agrégale una guía de **4 columnas**, margen `20` y separación `16`.

### Comprueba

Ves franjas rojas suaves sobre ambos frames. En el móvil, el contenido útil mide 375 − 2 × 20 = **335 px**.

> **Tip:** para ocultar o mostrar las guías, usa el menú **Ver / View → Guías de diseño / Layout guides**.

---

## Paso 3 — La estructura del frame móvil

**Meta:** un frame de pantalla con su contenido adentro y el menú arriba.

**Concepto:** la pantalla mide 812 de alto, pero la página completa mide mucho más. El frame será la **ventana** del celular y adentro pondremos una columna larga que se moverá con el scroll.

### Haz esto

1. Dentro de `Home · Mobile 375` (que **no** tiene Auto Layout), crea un frame con Auto Layout vertical llamado `Contenido`. Ancho `375`, separación `0`, padding superior `52` (el alto del menú).
2. Pon una instancia de `Navbar/Mobile` directamente dentro de `Home · Mobile 375`, arriba de todo (x `0`, y `0`), con ancho `375`.
3. Selecciona `Home · Mobile 375` y activa **Recortar contenido / Clip content**.

### Comprueba

```
Home · Mobile 375          (375 × 812, sin Auto Layout)
├── Contenido              (Auto Layout vertical)
└── Navbar/Mobile          (instancia)
```

> **Error frecuente:** poner el navbar dentro de `Contenido`. Así no podrás dejarlo fijo en el Paso 9.

---

## Paso 4 — Hero apilado

**Meta:** el hero de la landing reorganizado para una columna.

### Haz esto

1. Dentro de `Contenido`, crea `Sección · Hero`: Auto Layout **vertical**, centrado, separación `12`, padding `20` a los lados, `32` arriba y `40` abajo. Relleno `Color/Primario`. Ancho **Llenar contenedor**.
2. Agrega: «Nuevo» (`Eyebrow`), «iPhone Pro» (`Mobile/H1`, blanco) y la frase corta (`Body/Regular`, `Color/Texto suave sobre oscuro`, centrada).
3. Agrega la imagen reservada: un rectángulo de **335 × 260**, radio `20`.
4. Agrega los botones uno **debajo** del otro: en un Auto Layout vertical con separación `12`, una instancia de `Botón/Primario` («Comprar») y una de `Botón/Secundario` («Conocer más»).
5. En cada botón: ancho **Llenar contenedor** y alto `50`.

### Comprueba

Los botones ocupan los 335 px útiles. El título mide 40 px y la frase 17 px.

> **¿Por qué 50 de alto y ancho completo?** En móvil el CTA principal debe ser fácil de tocar con el pulgar. Más grande = menos errores.

> **Error frecuente:** reducir el texto de cuerpo a 13 o 12 px para que quepa más. La guía recomienda trabajar con textos de **14 a 18 puntos**; en el curso usamos **17 px** también en móvil.

---

## Paso 5 — Productos en una columna

**Meta:** las cards de producto, una debajo de otra.

### Haz esto

1. Crea `Sección · Productos`: vertical, separación `20`, padding `48` arriba y abajo y `20` a los lados, relleno `Color/Secundario`.
2. Agrega el título «Explora nuestra línea» (`Mobile/H2`).
3. Agrega **5** instancias de `Card/Producto` (el catálogo de 5 productos que pide la AF3) y ponles ancho **Llenar contenedor**.

### Comprueba

Cada card mide 335 de ancho y crece hacia abajo sin superponerse.

> **¿Por qué 1 columna y no 2?** En 375 px, dos cards quedarían de unos 168 px: muy chicas para ver bien la foto. Desde 428 px (celulares grandes) sí caben dos.

---

## Paso 6 — Beneficios, CTA y footer en acordeón

**Meta:** terminar la página y crear el componente `Acordeón/Footer`.

**Concepto: acordeón.** Un título que al tocarlo muestra u oculta su contenido. En móvil, ahorra mucho espacio en el footer.

### Haz esto — beneficios y CTA

1. `Sección · Beneficios`: las 3 columnas de escritorio, ahora **apiladas** (vertical, separación `28`, padding `20`). Títulos en `Mobile/H3`.
2. `Sección · CTA final`: fondo negro, pregunta en `Mobile/H2` (centrada) y botón «Ver productos» de ancho completo.

### Haz esto — el acordeón

3. En la página `Componentes`, crea una fila de **375 × 50**: el título `Tienda` (`Body/Semibold`, blanco) a la izquierda y un ícono de flecha hacia abajo a la derecha. Auto Layout horizontal, separación **Automático**, padding `20`. Fondo `Color/Superficie oscura`. Nombra la fila `Encabezado`.
4. Envuelve el `Encabezado` en un Auto Layout vertical y conviértelo en componente: `Acordeón/Footer`.
5. **Añadir variante.** Propiedad `Estado`: `Cerrado` y `Abierto`.
6. En `Abierto`: cambia la flecha para que apunte hacia arriba y agrega, debajo del encabezado, los links (iPhone, Mac, iPad…) en filas de **44** de alto.
7. Haz que el título sea editable: selecciona el texto `Tienda` y, en el panel derecho, pulsa el ícono de **propiedad de componente** junto al contenido del texto. Crea la propiedad `Título`.
8. En `Cerrado`, selecciona el `Encabezado` → **Prototipo** → **Al hacer clic** → **Cambiar a** → `Abierto` → **Smart animate**, `250 ms`. En `Abierto`, lo mismo hacia `Cerrado`.

### Haz esto — el footer

9. En `Contenido`, crea `Footer · Acordeón` con 4 instancias del acordeón: Tienda, Soporte, Nosotros y Contacto (cambia el título desde la propiedad `Título`). Debajo, el texto del copyright.

### Comprueba

En **Presentar**, al tocar «Soporte» se despliegan sus links y el resto del footer baja.

---

## Paso 6.5 — Carrusel con variantes (la interacción de la guía)

**Meta:** un carrusel de imágenes del hero que cambia al tocar la flecha o al deslizar.

**Concepto: estados de un componente.** La guía crea el carrusel con «estados de componente» en Adobe XD. En Figma, los estados son **variantes**: una variante por cada imagen.

### Haz esto

1. Crea un frame de **335 × 260** con **Recortar contenido / Clip content**: es la «máscara».
2. Dentro, pon dos rectángulos de imagen de 335 × 260, uno al lado del otro: el primero visible y el segundo afuera, a la derecha (x `335`).
3. Agrega dos botones de flecha de **44 × 44** sobre la imagen.
4. Selecciona el frame y conviértelo en componente: `Carrusel`. **Añadir variante**: propiedad `Foto`, valores `1` y `2`.
5. En `Foto=2`, mueve las dos imágenes a la izquierda (x `-335` y `0`), para que se vea la segunda.
6. **Prototipo:** en `Foto=1`, selecciona la flecha derecha → **Al hacer clic** → **Cambiar a** → `Foto=2` → **Smart animate**, **Ease in and out**, **600 ms**.
7. Agrega también en `Foto=1`, sobre el frame completo, **Al arrastrar / On drag** → **Cambiar a** → `Foto=2`, para que funcione deslizando.
8. Repite en `Foto=2` hacia `Foto=1` con la flecha izquierda.
9. Reemplaza la imagen del hero por una instancia de `Carrusel`.

### Comprueba

En **Presentar**, la imagen se desliza al tocar la flecha o al arrastrar con el mouse (con el dedo, en el celular).

> **Error frecuente:** la animación «salta» en vez de deslizarse. **Smart animate** necesita que las capas se llamen igual en ambas variantes: no las renombres en una sola.

> **Pista visual:** agrega puntos indicadores debajo (como en la semana 3). Un gesto sin pista es un gesto que nadie descubre.

---

## Paso 7 — El menú que se abre (overlay)

**Meta:** que el botón ☰ abra un panel lateral y que se pueda cerrar.

**Concepto: superposición / overlay.** Es un frame que aparece **encima** de la pantalla actual, sin reemplazarla. Ideal para menús, avisos y ventanas de confirmación.

### Haz esto

1. Crea un frame de **375 × 812** llamado `Overlay · Menú`, sin relleno.
2. Dentro, un rectángulo de 375 × 812 negro con **opacidad 40 %**: `Fondo atenuado`.
3. Encima, a la izquierda, un panel blanco de **300 × 812** llamado `Drawer` con: un botón ícono **X** de 44 × 44 (`Botón ícono · Cerrar`) y los links Productos, Beneficios, Soporte y Mi cuenta, cada uno en una fila de **52** de alto.
4. En `Home · Mobile 375`, selecciona el `Botón ícono · Menú` del navbar (doble clic hasta llegar a él).
5. **Prototipo → +**: **Al hacer clic** → **Abrir superposición / Open overlay** → `Overlay · Menú`. Animación: **Desplazar hacia dentro / Move in**, desde la izquierda, `300 ms`.
6. En la configuración del overlay, activa **Cerrar al hacer clic fuera / Close when clicking outside**.
7. En el overlay, selecciona `Botón ícono · Cerrar` → **Al hacer clic** → **Cerrar superposición / Close overlay**. Haz lo mismo con el `Fondo atenuado` y con cada link.

### Comprueba

Al tocar ☰, el panel entra desde la izquierda y el resto de la pantalla se oscurece. La X, el fondo oscuro o cualquier link lo cierran.

> **Error frecuente:** usar **Navegar a** en vez de **Abrir superposición**. Con «Navegar a», el menú reemplaza la pantalla y al cerrar no vuelves al mismo lugar.

---

## Paso 8 — Navegación por anclas en móvil

### Haz esto

1. Botón **Comprar** del hero → **Al hacer clic** → **Desplazarse a** → `Sección · Productos`.
2. Botón **Ver productos** del CTA final → lo mismo.

> Igual que en la semana 2: si el botón pierde el hover, no importa en móvil. **En táctil no hay hover.**

---

## Paso 9 — Scroll con el menú fijo

**Meta:** que la página baje y el menú quede arriba.

### Haz esto

1. Selecciona `Home · Mobile 375` → **Prototipo** → **Comportamiento de desplazamiento / Scroll behavior** → **Desbordamiento / Overflow**: **Vertical**.
2. Selecciona la instancia del `Navbar/Mobile` → **Posición / Position**: **Fija / Fixed (stay in place)**.

### Comprueba

En **Presentar**, la página baja hasta el footer y el menú sigue visible arriba.

> **Error frecuente:** la página no baja. Revisa que `Home · Mobile 375` mida **812** de alto (fijo) y que `Contenido` sea más alto que eso.

---

## Paso 10 — Dos flujos: móvil y escritorio

**Meta:** presentar cada versión por separado, como espera el equipo de desarrollo.

**Concepto: flujo.** Es un recorrido del prototipo con su propio punto de inicio. Un archivo puede tener varios.

### Haz esto

1. Selecciona `Home · Mobile 375`. En **Prototipo**, junto a **Punto de inicio de flujo / Flow starting point**, pulsa **+**. Nómbralo `Mobile 375`.
2. Haz lo mismo con `Home · Desktop 1440`: flujo `Desktop 1440`.
3. Con nada seleccionado, en **Prototipo**, elige un **Dispositivo / Device** para ver la versión móvil dentro de un celular.

### Comprueba

Al presentar, en el panel izquierdo aparecen los dos flujos y puedes cambiar entre ellos.

> **Revisa también la versión de escritorio:** al copiarla, sus links pueden seguir apuntando a la página anterior. Haz clic en un link: si no baja, vuelve a conectar sus **Desplazarse a** (Paso 9 de la semana 2).

---

## Paso 11 — Probar en tu celular y entregar

### Haz esto

1. En la app **Figma** de tu celular, abre el archivo y el flujo `Mobile 375`. Prueba el menú, el acordeón y el scroll.
2. Para pedir opinión: botón **Compartir / Share** → **Copiar enlace del prototipo**.
3. Revisa la **rúbrica** de la AF3 en AVA.
4. **Archivo → Guardar copia local** → comprime el `.fig` como `PN_S4_NombreApellido.zip`.
5. Pega el **enlace de revisión** (acceso «Cualquier persona con el enlace · Puede ver») en el documento de la actividad.
6. Sube **los dos** (ZIP y documento) a AVA antes del **lunes 16 de noviembre a las 23:59**.

## Checklist final

- [ ] Página `Landing · Responsiva` con ambas versiones.
- [ ] Guías de 4 columnas (móvil) y 12 columnas (escritorio).
- [ ] Hero apilado, productos en 1 columna, beneficios apilados.
- [ ] Texto de cuerpo en 17 px también en móvil.
- [ ] Botones del hero de ancho completo y 50 de alto.
- [ ] Componente `Acordeón/Footer` con Cerrado y Abierto.
- [ ] Carrusel con variantes que cambia al tocar y al deslizar.
- [ ] Catálogo de 5 productos.
- [ ] Menú ☰ que abre un overlay y se cierra.
- [ ] Menú fijo y página con scroll vertical.
- [ ] Flujos `Mobile 375` y `Desktop 1440`.

---

## Preguntas de repaso

1. ¿Qué significa diseñar **Mobile First**?
2. ¿Cuántas columnas usa la guía en móvil y en escritorio?
3. ¿Por qué el texto de cuerpo no se reduce en móvil?
4. ¿Cuándo usas **Abrir superposición** en vez de **Navegar a**?
5. ¿Por qué el navbar móvil no va dentro del frame `Contenido`?
6. ¿Qué ventaja tiene tener dos flujos separados?

## Respuestas

1. Diseñar primero para la pantalla más chica, con lo esencial, y luego ampliar hacia tablet y escritorio.
2. 4 columnas en móvil y 12 en escritorio (8 en tablet).
3. Porque achicarlo dificulta la lectura justo en la pantalla más pequeña. La guía recomienda textos de 14 a 18 puntos, y las WCAG piden que el usuario pueda agrandarlos sin que el diseño se rompa.
4. Cuando algo debe aparecer **encima** de la pantalla actual sin reemplazarla: menús, avisos, confirmaciones.
5. Porque para dejarlo fijo debe ser hijo directo del frame de la pantalla. Si está dentro de `Contenido`, se mueve con el scroll.
6. Puedes mostrar y probar cada versión por separado, y el equipo de desarrollo ve exactamente cómo funciona cada dispositivo.

## Glosario

| Término | En una frase |
| --- | --- |
| Mobile First | Diseñar primero para móvil y luego escalar |
| Breakpoint | Ancho en que el diseño cambia (375, 428, 768, 1024, 1280, 1440) |
| Guía de columnas | Columnas de referencia para alinear el contenido |
| Acordeón | Título que muestra u oculta su contenido al tocarlo |
| Overlay | Frame que aparece encima de la pantalla actual |
| Posición fija | Elemento que no se mueve al hacer scroll |
| Flujo | Recorrido del prototipo con su propio punto de inicio |

## Cómo sigue

En la **semana 5** pasarás de una página a un **sitio**: con Atomic Design ordenarás tus componentes en átomos, moléculas y organismos, y diseñarás las páginas interiores (catálogo, ficha de producto y una más), primero en móvil y luego en escritorio.
