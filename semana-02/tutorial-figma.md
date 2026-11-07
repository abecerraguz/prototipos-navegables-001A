# Tutorial Figma · Semana 2 — Landing page navegable
**Prototipos Navegables (DUD2204) · Experiencia 1 · Clase del miércoles 28 de octubre**

> 🧭 **Sigue el tutorial en orden.** Cada paso usa lo que hiciste en el anterior. Si algo no resulta, revisa el recuadro «Error frecuente» antes de seguir.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 1](../semana-01/tutorial-figma.md) · Volver al [README](../README.md)

En este tutorial convertirás los componentes de la semana 1 en una **landing page que se puede navegar**: el menú lleva a cada sección, los botones reaccionan al cursor y cada parte de la página tiene sus indicaciones de accesibilidad.

**Tiempo estimado:** 90–120 minutos (puedes dividirlo en dos sesiones: pasos 1 a 5 y pasos 6 a 10).

> 📌 **Sobre la AS1:** aquí practicas las técnicas con el proyecto Apple Store. La **AS1** pide aplicar estas mismas técnicas (header, nav y footer como componentes, interacciones, anclas y anotaciones de accesibilidad) al **rediseño del line-up del festival Lollapalooza**. Lee el enunciado en AVA; el Paso 11 te explica cómo entregar.

## 📎 Ejemplo de la clase en Figma

[▶ Abrir el ejemplo de la Clase 02 en Figma](https://www.figma.com/design/RYgItRByqHdlogloS5dLEj)

Es el mismo proyecto Apple Store que construimos en clase, tal como queda al terminar esta semana. Úsalo **después** de hacer el tutorial: compara tu archivo con el ejemplo, revisa cómo están armadas las capas y los componentes, y presiona **▶ Presentar** para probar el prototipo. Si quieres desarmarlo, duplícalo en tus borradores: el original no cambia. Si tienes una duda, déjala como comentario (tecla **C**) sobre el elemento.

---

## Qué vas a aprender

- Crear una **guía de estilos** con variables de color y **estilos de texto**.
- Construir los componentes **Navbar** y **Footer**, que la AS1 exige.
- Agregar una variante **Hover** a la card de producto.
- Armar una landing de **1440 px** con secciones ordenadas por Auto Layout.
- Crear **navegación por anclas** con la acción **Desplazarse a / Scroll to**.
- Dejar **anotaciones de accesibilidad** dentro del diseño.

## Antes de comenzar

Abre tu archivo **`Apple Store — Proyecto PI`** de la semana 1. Debe tener:

- [ ] La colección de variables `Apple Store · Colores` con las 8 variables.
- [ ] El componente `Botón/Primario` con las variantes `Normal` y `Hover`.
- [ ] El componente `Card/Producto` con un botón anidado.

> Si no terminaste la semana 1, hazla primero: [tutorial de la semana 1](../semana-01/tutorial-figma.md). Todo lo de hoy se construye encima.

## Cómo leer este tutorial

Igual que la semana pasada, cada paso tiene: **Concepto** (qué vas a usar), **Dónde está** (en qué parte de Figma), **Haz esto** (acciones en orden), **Comprueba** (cómo debe verse) y **Error frecuente** (qué revisar si falla). Los nombres de Figma aparecen en español e inglés: **Prototipo / Prototype**.

---

## Paso 1 — Ordenar el archivo

**Meta:** tres páginas con nombres claros.

**Concepto:** en un proyecto real el archivo crece rápido. Separar la guía, los componentes y las pantallas te ayuda a encontrar todo y es parte de lo que se evalúa.

### Haz esto

1. En **Páginas**, pulsa **+** y crea la página `Guía de estilos`. Arrástrala para dejarla primera.
2. Deja tu página `Componentes` como está.
3. Renombra la página `Landing Page` como `Landing · Desktop`.

### Comprueba

```
Apple Store — Proyecto PI
├── Guía de estilos
├── Componentes
└── Landing · Desktop
```

---

## Paso 2 — Completar la paleta de colores

**Meta:** 6 variables nuevas, para fondos oscuros, bordes y estados del sistema.

**Concepto: estados del sistema.** Son los colores que comunican qué pasó: un error, un éxito o una advertencia. Una guía de estilos completa los incluye aunque hoy no los uses.

**Dónde está:** botón **Variables** (ícono hexagonal) con nada seleccionado.

### Haz esto

1. Abre la colección `Apple Store · Colores` y crea estas variables de tipo **Color**:

| Nombre | Valor | Dónde se usa |
| --- | --- | --- |
| `Color/Superficie oscura` | #1D1D1F | Fondo del footer |
| `Color/Texto suave sobre oscuro` | #A1A1A6 | Textos secundarios sobre fondo negro |
| `Color/Borde` | #D1D1D6 | Bordes y separadores claros |
| `Estado/Error` | #D70015 | Mensajes de error |
| `Estado/Éxito` | #1D8348 | «En stock», confirmaciones |
| `Estado/Alerta` | #B25000 | Avisos (stock bajo) |

2. Verifica el contraste de cada color de texto en [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/): escribe el color del texto y el del fondo.

### Comprueba

Tu colección tiene **14 variables**. Anota el contraste de los pares que usarás:

| Texto | Fondo | Contraste | ¿Cumple AA? |
| --- | --- | --- | --- |
| #1D1D1F | #FFFFFF | 16,8:1 | ✅ |
| #6E6E73 | #FFFFFF | 5,1:1 | ✅ |
| #FFFFFF | #0071E3 | 4,7:1 | ✅ |
| #A1A1A6 | #1D1D1F | 6,6:1 | ✅ |

> **Regla WCAG AA:** texto normal, mínimo **4,5:1**. Texto grande (24 px o más, o 19 px en negrita), mínimo **3:1**.

> **Error frecuente:** usar `Color/Texto suave` (#6E6E73) sobre negro. Ahí el contraste baja a 4,1:1 y no cumple. Para fondos oscuros existe `Color/Texto suave sobre oscuro`.

---

## Paso 3 — Estilos de texto

**Meta:** 7 estilos de texto que usarás en toda la landing.

**Concepto: estilo de texto.** Guarda fuente, tamaño, peso e interlineado bajo un nombre. Si cambias el estilo, cambian todos los textos que lo usan. Es lo mismo que una variable, pero para la tipografía.

**Dónde está:** selecciona un texto. En el panel derecho, sección **Tipografía / Typography**, pulsa el ícono de cuatro puntos **Estilos / Styles** y luego **+**.

### Haz esto

1. En la página `Guía de estilos`, crea un texto (**T**) que diga `H1 · Título principal`.
2. Ponle fuente **Inter** (o SF Pro), tamaño `72`, peso **Bold**, interlineado `79`.
3. Pulsa el ícono **Estilos** → **+** y nombra el estilo `Desktop/H1`.
4. Repite con esta tabla:

| Estilo | Tamaño | Peso | Interlineado |
| --- | --- | --- | --- |
| `Desktop/H1` | 72 | Bold | 79 |
| `Desktop/H2` | 48 | Bold | 55 |
| `Desktop/H3` | 28 | Semi Bold | 34 |
| `Eyebrow` | 17 | Semi Bold | 24 |
| `Body/Regular` | 17 | Regular | 28 |
| `Small` | 15 | Regular | 23 |
| `Label` | 12 | Semi Bold | 17 |

### Comprueba

Con nada seleccionado, el panel derecho muestra **Estilos de texto / Text styles** con las 7 entradas. Si haces clic en un texto, en Tipografía aparece el nombre del estilo, no números sueltos.

> **¿Por qué el cuerpo mide 17 px y el interlineado 28?** La guía del curso recomienda textos de 14 a 18 puntos, y el criterio WCAG 1.4.12 pide que el contenido funcione con un interlineado de al menos 1,5 veces el tamaño de la fuente: 17 × 1,5 = 25,5. Usamos 28 para leer con más aire.

> **Error frecuente:** cambiar el tamaño de un texto **después** de aplicarle el estilo. Eso lo «despega» del estilo. Si necesitas otro tamaño, crea otro estilo.

---

## Paso 4 — La página Guía de estilos

**Meta:** una página que cualquier persona del equipo pueda leer para saber qué colores, textos y espacios usar.

### Haz esto

1. Crea un frame (**F**) de `1440` de ancho y nómbralo `Guía de estilos`. Aplícale **Auto Layout** vertical (**Shift + A**) con separación `56` y padding `80`.
2. **Sección Colores:** por cada variable, un rectángulo de `240 × 96` con su relleno conectado a la variable y, debajo, un texto con el nombre, el HEX y el contraste.
3. **Sección Tipografía:** un texto de ejemplo por cada estilo de texto.
4. **Sección Espaciado:** cuadrados de 8, 16, 24, 32, 48, 64 y 80 px.

> **Espaciado en múltiplos de 8.** Todos los paddings y separaciones de la landing serán 8, 16, 24, 32, 48, 64 u 80. Así el diseño se ve ordenado aunque no sepas explicar por qué.

### Comprueba

Al cambiar el valor de `Color/Acento` en Variables, la muestra azul de la guía también cambia. Deshaz el cambio.

---

## Paso 5 — Componente Navbar

**Meta:** una barra de navegación de `1440 × 52` con logo, tres enlaces y dos íconos, convertida en componente.

**Concepto: espaciado automático.** En Auto Layout, la opción **Automático / Auto** reparte el espacio entre los elementos: el primero queda a la izquierda, el último a la derecha y el resto al centro.

### Haz esto

1. En la página `Componentes`, crea el **logo** como espacio reservado: un texto `LOGO` (estilo `Label`) dentro de un frame con borde de 1,5 px y radio 6. Nómbralo `Logo`.
2. Crea tres textos (`Productos`, `Beneficios`, `Soporte`) con estilo `Small`. Envuelve **cada uno** en su propio frame con **Shift + A**, alto fijo `44` y padding lateral `12`. Nómbralos `Link · Productos`, `Link · Beneficios` y `Link · Soporte`.
3. Selecciona los tres links y presiona **Shift + A**. Nombra el grupo `Links`.
4. Para los íconos usa el plugin **Iconify** (menú **Recursos / Resources → Plugins**): busca «search» y «bag». Pon cada ícono de 24 px dentro de un frame de **44 × 44** y nómbralos `Botón ícono · Buscar` y `Botón ícono · Bolsa`.
5. Selecciona `Logo`, `Links` y los dos íconos, y presiona **Shift + A**. En Auto Layout: dirección **horizontal**, separación **Automático / Auto**, padding lateral `80`, ancho fijo `1440`, alto fijo `52`.
6. Relleno: `Color/Fondo`. Borde inferior de 1 px con `Color/Borde`.
7. Conviértelo en componente (**Ctrl + Alt + K** / **Option + Cmd + K**) y nómbralo `Navbar/Desktop`.

### Comprueba

```
Navbar/Desktop          ◆
├── Logo
├── Links
│   ├── Link · Productos
│   ├── Link · Beneficios
│   └── Link · Soporte
├── Botón ícono · Buscar
└── Botón ícono · Bolsa
```

> **¿Por qué cada link mide 44 de alto si el texto mide 23?** El área que se puede tocar debe ser cómoda (44 px), aunque el texto sea más chico. Lo verás en detalle en la semana 3.

> **Error frecuente:** nombrar mal los links. En el Paso 9 los buscarás por nombre para conectarlos.

---

## Paso 6 — Componente Footer

**Meta:** un footer oscuro con 4 columnas y una barra inferior.

### Haz esto

1. Crea 4 columnas. Cada una es un Auto Layout **vertical** con separación `12`: un título (estilo `Body/Regular` en negrita o `Body/Semibold`, color `Color/Texto sobre acento`) y 3 a 5 enlaces (estilo `Small`, color `Color/Texto suave sobre oscuro`).
   - **Tienda:** iPhone, Mac, iPad, Watch, Accesorios
   - **Soporte:** Envíos, Garantía, Cambios y devoluciones
   - **Nosotros:** Quiénes somos, Tiendas
   - **Contacto:** correo, teléfono y horario
2. Junta las 4 columnas en un Auto Layout **horizontal** con separación `40`. Nómbralo `Columnas`.
3. Debajo, una línea de 1 px (`Color/Separador oscuro` o `#424245`) y un texto: `© 2026 Proyecto PI · Prototipo académico`.
4. Envuelve todo en un Auto Layout **vertical**: ancho `1440`, padding `64` arriba, `80` a los lados, `40` abajo. Relleno: `Color/Superficie oscura`.
5. Conviértelo en componente: `Footer/Desktop`.

### Comprueba

El texto gris del footer se lee bien sobre el fondo oscuro (6,6:1).

---

## Paso 7 — Hover en la card de producto

**Meta:** que la card se «eleve» cuando pasas el cursor.

**Concepto: microinteracción.** Una respuesta pequeña y rápida del diseño a una acción del usuario. Le confirma que ese elemento se puede usar.

### Haz esto

1. Selecciona el componente `Card/Producto` y pulsa **Añadir variante / Add variant**.
2. Al conjunto, ponle la propiedad `Estado`. La original es `Normal` y la nueva `Hover`.
3. En la variante **Hover**, cambia la sombra: Y `16`, desenfoque `40`, opacidad `18%`.
4. En la variante **Normal**, pestaña **Prototipo**: **+** → **Al pasar el cursor / While hovering** → **Cambiar a / Change to** → `Hover` → **Smart animate**, `250 ms`.

### Comprueba

En modo Presentar, la card gana sombra al pasar el cursor y vuelve a la normalidad al salir.

> **Error frecuente:** la animación «salta». **Smart animate** solo funciona bien si las capas tienen los **mismos nombres** en ambas variantes. Si duplicaste con Añadir variante, ya los tienen.

---

## Paso 8 — Armar la landing de 1440 px

**Meta:** una página con 6 partes, una debajo de otra, todas hechas con instancias.

**Concepto: sección.** Cada bloque horizontal de la landing (hero, productos, beneficios…) es un frame con nombre propio. El nombre es importante: en el Paso 9 el menú «saltará» a esos frames.

### Haz esto

1. En `Landing · Desktop`, crea un frame de ancho `1440`, aplica **Shift + A** (vertical, separación `0`) y nómbralo `Home · Desktop 1440`. Alto: **Ajustar contenido / Hug**.
2. Agrega dentro, en este orden:

| Orden | Nombre del frame | Contenido |
| --- | --- | --- |
| 1 | (instancia) | `Navbar/Desktop` |
| 2 | `Sección · Hero` | Fondo `Color/Primario`. «Nuevo» (`Eyebrow`, `Color/Acento`), «iPhone Pro» (`Desktop/H1`, blanco), una frase corta (`Body/Regular`, `Color/Texto suave sobre oscuro`), botones **Comprar** y **Conocer más**, y un rectángulo de `600 × 400` como imagen. Alto `680`. |
| 3 | `Sección · Productos` | Fondo `Color/Secundario`, padding `80`. Título «Explora nuestra línea» (`Desktop/H2`) y 4 instancias de `Card/Producto` en fila, separación `24`. |
| 4 | `Sección · Beneficios` | 3 columnas: ícono de 48 px, título (`Desktop/H3`) y texto (`Body/Regular`). Envío, garantía y soporte. |
| 5 | `Sección · CTA final` | Fondo negro, una pregunta en `Desktop/H2` blanco y un botón **Ver productos**. |
| 6 | (instancia) | `Footer/Desktop` |

3. En cada sección (menos navbar y footer), pon el ancho en **Llenar contenedor / Fill container**.
4. Cambia los textos de las cards: iPhone Pro, MacBook Air, iPad, AirPods, con precios ficticios en pesos chilenos.

### Comprueba

Al mover una sección en el panel de Capas, las demás se reacomodan solas. La landing mide unos 1440 × 2400.

> **Error frecuente:** cuatro cards de 300 px no caben si el padding es mayor que 80. Cuenta: 4 × 300 + 3 × 24 = 1272, y 1440 − 2 × 80 = 1280. Calza justo.

> **Error frecuente:** usar la imagen o el logo reales de la marca. Usa espacios reservados (rectángulos) y escribe en la anotación qué imagen iría ahí.

---

## Paso 9 — Navegación por anclas

**Meta:** que cada link del menú y los botones principales lleven a su sección haciendo scroll.

**Concepto: ancla.** Es un punto de la misma página al que se puede saltar. **Navegar a / Navigate to** cambia de pantalla; **Desplazarse a / Scroll to** se mueve dentro de la misma pantalla. Para una landing usamos **Desplazarse a**.

**Dónde está:** pestaña **Prototipo / Prototype** del panel derecho.

### Haz esto

1. En la landing, haz **doble clic** varias veces sobre el link `Productos` del navbar hasta seleccionar el frame `Link · Productos` (mira el panel de Capas).
2. Pestaña **Prototipo** → **+** en Interacciones.
3. Configura: **Al hacer clic / On click** → **Desplazarse a / Scroll to** → `Sección · Productos`. Animación: **Ease in and out**, `400 ms`.
4. Repite:

| Elemento | Acción | Destino |
| --- | --- | --- |
| `Link · Productos` | Desplazarse a | `Sección · Productos` |
| `Link · Beneficios` | Desplazarse a | `Sección · Beneficios` |
| `Link · Soporte` | Desplazarse a | Footer |
| Botón **Comprar** del hero | Desplazarse a | `Sección · Productos` |
| Botón **Ver productos** del CTA final | Desplazarse a | `Sección · Productos` |

5. **Menú fijo:** selecciona la instancia del navbar. En **Prototipo**, busca **Comportamiento de desplazamiento / Scroll behavior** y elige **Fija / Sticky**. Así el menú sigue visible al bajar.
6. **Punto de inicio:** selecciona el frame `Home · Desktop 1440` y, en **Prototipo**, agrega un **Punto de inicio de flujo / Flow starting point**. Llámalo `Landing · Desktop`.

### Comprueba

Pulsa **Presentar / Present** (▶ arriba a la derecha). Haz clic en «Beneficios»: la página baja hasta esa sección y el menú sigue arriba.

> **Error frecuente:** el botón **Comprar** pierde su hover al agregarle el clic. Una instancia con interacciones propias deja de usar las del componente. Agrégale también **Al pasar el cursor → Cambiar a → Hover**.

> **Error frecuente:** la interacción quedó en el texto y no en el frame del link. Funciona igual, pero el área clicable es más chica. Selecciona el frame `Link · …`.

---

## Paso 10 — Anotaciones de accesibilidad

**Meta:** que el equipo de desarrollo sepa, sin preguntarte, cómo hacer accesible cada parte.

**Dónde está:** tienes dos opciones.

- **Comentarios / Comments** (tecla **C**): haz clic sobre la sección y escribe la nota.
- **Anotaciones / Annotations** en **Dev Mode** (**Shift + D**, luego **Shift + T** sobre el elemento), si tu plan lo permite.

### Haz esto

Agrega una nota en cada sección. Usa este checklist:

| Elemento | Qué anotar |
| --- | --- |
| Imágenes | Texto alternativo (alt). Ej.: «iPhone Pro, vista frontal». |
| Botones de solo ícono | Nombre accesible: «Buscar», «Bolsa de compras». |
| Textos | Contraste verificado (Paso 2). |
| Botones y links | Área táctil mínima 44 × 44. |
| Teclado | Estado de foco visible: borde de 2 px `Color/Acento`. |
| Adaptación | Qué pasa en móvil: «4 columnas → 1 columna», «menú → hamburguesa». |

### Comprueba

Cada sección de la landing tiene al menos una nota visible.

---

## Paso 11 — Preparar la entrega (AS1)

La AS1 se hace en un **archivo nuevo**, con el rediseño del line-up de Lollapalooza. Aplica ahí todo lo que practicaste en este tutorial.

1. Revisa el **enunciado** y la **rúbrica** en AVA. Se evalúan componentes, interacciones, accesibilidad, **responsividad** (versión desktop **y** mobile) y guía de estilos.
2. **Archivo / File → Guardar copia local / Save local copy**. Se descarga un `.fig`.
3. Comprime el `.fig` en un ZIP con el nombre `PN_S2_NombreApellido.zip`.
4. Copia el **enlace de revisión** del diseño (**Compartir / Share** → acceso «Cualquier persona con el enlace · Puede ver» → **Copiar enlace**) y pégalo en el documento del enunciado, donde dice «ingresa aquí la URL». Pruébalo en una ventana de incógnito.
5. Sube **los dos** (ZIP y documento) a AVA antes del **lunes 2 de noviembre a las 23:59**.

## Checklist final

- [ ] Página `Guía de estilos` con colores, tipografía y espaciado.
- [ ] 14 variables de color y 7 estilos de texto.
- [ ] Componentes: `Botón/Primario`, `Card/Producto` (con hover), `Navbar/Desktop`, `Footer/Desktop`.
- [ ] Landing de 1440 px armada solo con instancias y estilos.
- [ ] Links del menú y botones con **Desplazarse a**.
- [ ] Anotaciones de accesibilidad en cada sección.
- [ ] Probado en modo Presentar.

---

## Preguntas de repaso

1. ¿Cuál es la diferencia entre **Navegar a** y **Desplazarse a**?
2. ¿Por qué el footer usa `Color/Texto suave sobre oscuro` y no `Color/Texto suave`?
3. Cambias el tamaño del estilo `Body/Regular` de 17 a 18. ¿Qué pasa con los textos de la landing?
4. ¿Por qué conviene que el navbar sea un componente y no un grupo?
5. ¿Qué heurística de Nielsen aplica el hover de la card?

## Respuestas

1. **Navegar a** cambia a otra pantalla (otro frame). **Desplazarse a** baja o sube dentro de la misma pantalla hasta un punto: es la navegación por anclas.
2. Porque #6E6E73 sobre el fondo del footer (#1D1D1F) tiene un contraste de apenas 3,3:1 y no cumple AA. #A1A1A6 sobre #1D1D1F llega a 6,6:1.
3. Todos los textos con ese estilo pasan a 18 px de una vez. Ese es el valor de los estilos.
4. Porque se repetirá en todas las páginas. Si cambias un link en el componente, cambia en todas.
5. La n.º 1, **Visibilidad del estado del sistema**: el usuario ve que el elemento responde.

## Glosario

| Término | En una frase |
| --- | --- |
| Estilo de texto | Fuente, tamaño, peso e interlineado guardados con un nombre |
| Guía de estilos | Página que documenta colores, tipografía, espaciado y componentes |
| Microinteracción | Respuesta pequeña del diseño a una acción (hover, clic) |
| Ancla | Punto de la misma página al que se puede saltar |
| Desplazarse a / Scroll to | Acción de prototipo que hace scroll hasta un elemento |
| Sticky | Elemento que se queda fijo arriba al hacer scroll |
| Anotación | Nota para desarrollo dentro del diseño |

## Cómo sigue

En la **semana 3** dejaremos el escritorio y miraremos el celular: el fold, la zona del pulgar, el tamaño de lo que se toca y los menús móviles. Tu landing de hoy será la base de la versión móvil de la semana 4.
