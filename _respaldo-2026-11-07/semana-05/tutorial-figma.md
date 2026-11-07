# Tutorial Figma · Semana 5 — Sistema de diseño y páginas interiores
**Prototipos Navegables (DUD2204) · Experiencia 2 · Clase del miércoles 18 de noviembre**

> 🧭 **Hasta ahora tenías una página. Hoy empiezas un sitio.** Ordenarás tus componentes con Atomic Design y los usarás para diseñar las páginas interiores, primero en móvil y luego en escritorio.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 4](../semana-04/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 2,5 a 3 horas. Te recomendamos hacerlo en tres sesiones: pasos 1 a 4 (sistema), pasos 5 a 7 (páginas móviles) y pasos 8 a 11 (escritorio y flujos).

## Qué vas a aprender

- Ordenar el archivo como un **sistema de diseño**.
- Clasificar componentes en **átomos, moléculas y organismos**.
- Usar **propiedades de componente**: texto, booleana (mostrar u ocultar) y variantes.
- Armar **plantillas** y convertirlas en **páginas** con contenido real.
- Diseñar con **Mobile First**: 375 primero, 1440 después.
- Conectar páginas con **Navegar a** y **Atrás**.

## Antes de comenzar

Abre **`Apple Store — Proyecto PI`** con la landing responsiva de la semana 4.

> **Esto es para la AS2 (sumativa).** El enunciado pide estas páginas, en móvil (mínimo 350 px) y escritorio (máximo 1366 × 768): **Home** (la landing de la AF3), **Ficha de producto**, **Carrito de compras** y **Check out** (tentativa). La arquitectura y el inventario de contenidos están en el [tablero de Miro de la actividad](https://miro.com/app/board/uXjVM5YvNgk=/).
>
> El tutorial te enseña el **método** con un catálogo (práctica) y la ficha. En el Paso 9 diseñas el carrito y el check out. Revisa el enunciado y la rúbrica en AVA antes de empezar.

## Atomic Design en una imagen

```
Átomos  →  Moléculas  →  Organismos  →  Plantillas  →  Páginas
botón      barra de       card de         estructura     la plantilla
chip       búsqueda       producto        sin contenido  con contenido
input      selector       panel de        real           real
           de color       compra
```

---

## Paso 1 — Reorganizar el archivo

**Meta:** que el archivo se lea como un sistema.

**Concepto: sección.** Una **sección** (**Shift + S**) es un área con título que agrupa frames en el lienzo. Sirve para separar átomos, moléculas y organismos dentro de una misma página.

### Haz esto

1. Renombra las páginas y crea las que faltan:

```
🎨 Guía de estilos
🧩 Sistema de diseño        (antes «Componentes»)
📋 Plantillas
📱 Páginas · Mobile 375
💻 Páginas · Desktop 1440
🏠 Landing · Responsiva     (semana 4)
```

2. En `🧩 Sistema de diseño`, crea tres secciones: `Átomos`, `Moléculas` y `Organismos`.
3. Arrastra cada componente principal a su sección según la tabla del Paso 2.

### Comprueba

Tus instancias de la landing siguen conectadas. Mover un componente principal **dentro del mismo archivo** no rompe sus instancias.

> **Error frecuente:** copiar y pegar un componente principal en otra página. Eso crea un **componente nuevo** y desconectado. Para moverlo, arrástralo o usa clic derecho → **Mover a página / Move to page**.

---

## Paso 2 — Clasificar lo que ya tienes

**Meta:** saber qué es cada pieza.

**Pregunta clave:** ¿se puede dividir en piezas más chicas que también se reutilizan?

| Componente | Nivel | Por qué |
| --- | --- | --- |
| `Botón/Primario`, `Botón/Secundario` | Átomo | No se puede dividir más |
| `Badge/Nuevo` | Átomo | Una etiqueta sola |
| `Botón ícono · …` (44 × 44) | Átomo | Un ícono con su área táctil |
| `Card/Producto` | Organismo | Imagen + textos + botón (un átomo adentro) |
| `Navbar/Desktop`, `Navbar/Mobile` | Organismo | Logo + links + botones ícono |
| `Footer/Desktop`, `Acordeón/Footer` | Organismo | Varios grupos de links |
| `TabBar/App` | Organismo | Varias pestañas |

> Los colores, la tipografía y el espaciado (variables y estilos) son la base de los átomos. En algunos libros los llaman «tokens».

---

## Paso 3 — Átomos nuevos

**Meta:** las piezas mínimas que necesitarán el catálogo y la ficha.

### 3.1 Chip

Se usa para filtros («Todos», «iPhone», «Mac») y para elegir capacidad («128 GB», «256 GB»).

1. Texto `128 GB` (`Small`). **Shift + A**: padding `16` a los lados, alto fijo `44`, radio `999` (queda como píldora). Borde de 1 px `Color/Borde`, relleno `Color/Fondo`.
2. Conviértelo en componente: `Chip`.
3. **Añadir variante**. Propiedad `Estado`: `Normal` y `Seleccionado`.
4. En `Seleccionado`: relleno `Color/Texto` (casi negro) y texto blanco.
5. Selecciona el texto → en el panel derecho, junto al contenido, pulsa el ícono de **propiedad de componente** y crea la propiedad de texto `Etiqueta`.

> **Concepto: propiedad de texto.** Permite cambiar el texto de cada instancia desde el panel derecho, sin hacer doble clic dentro del componente.

### 3.2 Chip de color

1. Un círculo de **28 px** con el color del producto, dentro de un frame de **44 × 44** (área táctil).
2. Componente `Chip de color`, con variante `Seleccionado`: `No` / `Sí`. En `Sí`, agrega un anillo de 2 px `Color/Acento` alrededor.

### 3.3 Campo de texto (input)

1. Frame de `335 × 48`, radio `12`, borde `Color/Borde`, con un texto gris «Buscar productos» (`Body/Regular`, `Color/Texto suave`).
2. Componente `Input`, con variantes `Estado`: `Normal`, `Foco` (borde de 2 px `Color/Acento`) y `Error` (borde `Estado/Error` y un mensaje debajo).

> **Accesibilidad:** el estado `Foco` muestra dónde está el usuario cuando navega con teclado. El error no se marca **solo** con rojo: lleva un mensaje.

### Comprueba

En la sección `Átomos` tienes `Chip` (2 variantes), `Chip de color` (2) e `Input` (3).

---

## Paso 4 — Moléculas y organismos

**Meta:** combinar átomos en piezas con una función.

### 4.1 Molécula · Barra de búsqueda

Un `Input` + un `Botón ícono · Buscar`, en Auto Layout horizontal con separación `8`. Componente `Búsqueda`.

### 4.2 Molécula · Selector de color

Un texto «Color: Negro» (`Body/Regular`) y, debajo, 4 instancias de `Chip de color` en fila (separación `8`). Componente `Selector de color`.

> **Heurística n.º 6 (Reconocer antes que recordar):** el selector muestra **el nombre** del color elegido, no solo el círculo.

### 4.3 Molécula · Combo precio-CTA

Precio «$999.990» (`Desktop/H3` o `Mobile/H3`) + `Botón/Primario` «Agregar a la bolsa», en vertical. Componente `Precio + CTA`.

### 4.4 Organismo · Barra de filtros

Varias instancias de `Chip` en fila horizontal (separación `8`), dentro de un frame con **Recortar contenido** y **Desbordamiento horizontal** (lo aprendiste en la semana 3). Componente `Barra de filtros`.

### 4.5 Mejorar la card con una propiedad booleana

1. Abre el componente `Card/Producto` y agrega una instancia de `Badge/Nuevo` arriba del nombre.
2. Con el badge seleccionado, en el panel derecho, en **Capa / Layer**, pulsa el ícono de propiedad junto a la visibilidad y crea la propiedad booleana `Mostrar badge`.

> **Concepto: propiedad booleana.** Un interruptor sí/no para mostrar u ocultar una capa. Así no necesitas una variante «con badge» y otra «sin badge».

### Comprueba

Arrastra una `Card/Producto` al lienzo: en el panel derecho aparecen `Nombre`, `Precio`, `Estado` y el interruptor `Mostrar badge`.

---

## Paso 5 — Plantillas

**Meta:** la estructura del catálogo y de la ficha, sin contenido real.

**Concepto: plantilla.** Es el esqueleto de una página: qué organismos van y en qué orden. Usa textos genéricos («Nombre del producto») y rectángulos grises.

### Haz esto

En `📋 Plantillas`, crea dos frames de **375** de ancho con Auto Layout vertical:

| Template Catálogo · Mobile | Template Ficha · Mobile |
| --- | --- |
| `Navbar/Mobile` | `Navbar/Mobile` |
| Breadcrumb («Inicio › Categoría») | Breadcrumb |
| Título de la categoría | Galería (imagen + puntos) |
| `Barra de filtros` | Nombre y precio |
| Grilla de `Card/Producto` | `Selector de color` |
| Footer en acordeón | Chips de capacidad |
| | `Precio + CTA` |
| | «También te puede interesar» (carrusel) |
| | Footer en acordeón |

### Comprueba

Una persona que mira la plantilla entiende la página aunque no haya ni un precio real.

---

## Paso 6 — Página móvil: catálogo

**Meta:** la plantilla con contenido real.

### Haz esto

1. Duplica `Template Catálogo · Mobile` y arrástralo a `📱 Páginas · Mobile 375`. Renómbralo `Catálogo iPhone · Mobile`.
2. Cambia los textos: breadcrumb «Inicio › iPhone», título «iPhone» (`Mobile/H1`), filtros «Todos», «iPhone Pro», «iPhone», «iPhone SE».
3. Marca el primer chip como `Seleccionado`.
4. En las cards, pon modelos y precios ficticios en pesos chilenos. Activa `Mostrar badge` solo en el modelo más nuevo.

### Comprueba

El catálogo se ve como un sitio real y **todo** son instancias: si cambias el radio del chip en el sistema, cambia aquí.

---

## Paso 7 — Página móvil: ficha de producto

### Haz esto

1. Duplica `Template Ficha · Mobile` → `📱 Páginas · Mobile 375` → `Ficha iPhone Pro · Mobile`.
2. Completa: nombre, precio, «● En stock» (`Estado/Éxito`), color seleccionado con su nombre, chips de capacidad (uno `Seleccionado`).
3. Pon el `Precio + CTA` como **botón fijo** abajo (Paso 7 de la semana 3).

### Comprueba

El botón «Agregar a la bolsa» queda en la zona fácil del pulgar y siempre visible.

---

## Paso 8 — Escalar a escritorio

**Meta:** las mismas páginas en 1440, con el mismo contenido reorganizado.

### Haz esto

1. En `💻 Páginas · Desktop 1440`, crea `Catálogo iPhone · Desktop` de 1440 de ancho con la guía de 12 columnas.
2. Usa `Navbar/Desktop` y `Footer/Desktop`. La grilla de cards pasa a **3 columnas** (separación `24`).
3. Crea `Ficha iPhone Pro · Desktop` en **dos columnas**: galería a la izquierda y la información de compra a la derecha.

| Elemento | Mobile 375 | Desktop 1440 |
| --- | --- | --- |
| Grilla del catálogo | 1 columna | 3 columnas |
| Filtros | Fila con scroll horizontal | Fila completa visible |
| Ficha | Todo apilado | 2 columnas |
| Botón de compra | Fijo abajo | Dentro de la columna derecha |

> **Mobile First no es «achicar».** El contenido y las funciones son los mismos en ambas versiones; solo cambia cómo se ordenan.

> 📌 **Para la AS2:** el enunciado pide mesas de escritorio de **máximo 1366 × 768**. En tu entrega usa **1366** de ancho en vez de 1440 (la guía de 12 columnas se ajusta sola).

---

## Paso 9 — Carrito y check out

La AS2 pide estas dos páginas. Diséñalas en móvil y escritorio, solo con instancias del sistema:

- **Carrito de compras:** lista de productos agregados (imagen, nombre, variante, cantidad y opción de eliminar), resumen con subtotal, envío y total, y un botón **Ir a pagar**.
- **Check out (tentativa):** datos de envío, método de pago y un resumen de la orden, con un botón **Confirmar compra** y una pantalla o mensaje de confirmación.

Revisa en el Miro qué contenido debe ir en cada una.

> **Pista:** antes de diseñar, escribe qué átomos, moléculas y organismos necesitas. Si falta alguno, créalo primero en `🧩 Sistema de diseño`.

---

## Paso 10 — Conectar las páginas

**Meta:** que se pueda recorrer Home → Ficha → Carrito → Check out, y volver.

**Concepto: Navegar a y Atrás.** **Navegar a / Navigate to** lleva a otro frame. **Atrás / Back** vuelve al anterior, sea cual sea.

### Haz esto

Las páginas deben estar en la **misma página de Figma** para conectarlas. Junta en `📱 Páginas · Mobile 375` la home móvil (cópiala desde la semana 4), la ficha, el carrito, el check out y, si lo hiciste, el catálogo.

| Desde | Interacción | Hacia |
| --- | --- | --- |
| Home: una card del catálogo | Al hacer clic → Navegar a | Ficha |
| Ficha: «Agregar a la bolsa» | Al hacer clic → Navegar a | Carrito |
| Carrito: «Ir a pagar» | Al hacer clic → Navegar a | Check out |
| Check out: «Confirmar compra» | Al hacer clic → Navegar a | Confirmación |
| Breadcrumb «Inicio» | Al hacer clic → Navegar a | Home |
| Flecha o link «Volver» | Al hacer clic → **Atrás** | (vuelve solo) |

Animación sugerida: **Desplazar hacia dentro / Slide in** desde la derecha, `300 ms`. Al volver, desde la izquierda.

Crea el flujo `Mobile · Compra` en la home móvil. Repite en escritorio con el flujo `Desktop · Compra`.

### Comprueba

En **Presentar**, puedes hacer la compra completa sin quedarte «atrapado» en ninguna pantalla.

> **Error frecuente:** al tocar una card, también se activa el botón «Comprar» de adentro. Pon la interacción en la card **o** en el botón, no en ambos.

---

## Paso 11 — Revisar y entregar (AS2)

1. **Anotaciones:** alt de las imágenes, contraste de los textos nuevos, áreas táctiles de chips y botones (44 × 44).
2. **Orden:** páginas con nombre, capas con nombre, sin elementos sueltos.
3. **Archivo → Guardar copia local** → comprime el `.fig` como `PN_S5_NombreApellido.zip`.
4. Pega el **enlace de revisión** (acceso «Cualquier persona con el enlace · Puede ver») en el documento de la actividad.
5. Sube **los dos** (ZIP y documento) a AVA antes del **lunes 23 de noviembre a las 23:59**.

## Checklist final

- [ ] Páginas: Guía de estilos, Sistema de diseño, Plantillas, Páginas Mobile 375, Páginas Desktop 1440.
- [ ] Sistema con secciones Átomos, Moléculas y Organismos.
- [ ] Componentes nuevos: `Chip`, `Chip de color`, `Input`, `Búsqueda`, `Selector de color`, `Precio + CTA`, `Barra de filtros`.
- [ ] Al menos una propiedad de texto y una booleana.
- [ ] Plantillas de las páginas.
- [ ] Home, ficha, carrito y check out en móvil (mín. 350) y escritorio (máx. 1366).
- [ ] Flujos de compra conectados en móvil y escritorio.
- [ ] Anotaciones de accesibilidad.

---

## Preguntas de repaso

1. ¿Por qué `Card/Producto` es un organismo y no un átomo?
2. ¿Qué diferencia hay entre una plantilla y una página?
3. ¿Cuándo conviene una propiedad booleana en vez de una variante?
4. ¿Qué pasa con tus páginas si cambias el borde del átomo `Chip`?
5. ¿Qué hace la acción **Atrás**?

## Respuestas

1. Porque está formada por otras piezas reutilizables: una imagen, textos y un `Botón/Primario` (un átomo).
2. La plantilla es la estructura con contenido genérico. La página es esa misma estructura con contenido real.
3. Cuando solo necesitas mostrar u ocultar algo (un badge, un ícono). Las variantes son para estados distintos (Normal, Seleccionado, Error).
4. Cambia en todas las instancias: filtros, capacidades y cualquier otro lugar donde uses el chip.
5. Vuelve a la pantalla anterior del recorrido, sin importar cuál fue.

## Glosario

| Término | En una frase |
| --- | --- |
| Sistema de diseño | Reglas, estilos y componentes reutilizables de un producto |
| Átomo | Pieza mínima: botón, chip, input |
| Molécula | Átomos que funcionan juntos: barra de búsqueda |
| Organismo | Bloque complejo: card, navbar, panel de compra |
| Plantilla | Estructura de una página sin contenido real |
| Página | Plantilla con contenido real |
| Propiedad booleana | Interruptor para mostrar u ocultar una capa |
| Atrás / Back | Acción que vuelve a la pantalla anterior |

## Cómo sigue

Con la **semana 5** cierras la Experiencia 2: tu prototipo ya es un sitio completo. En la **semana 6** aprenderás a **evaluarlo** con las 10 heurísticas de Nielsen.
