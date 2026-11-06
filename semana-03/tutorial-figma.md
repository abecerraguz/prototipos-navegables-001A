# Tutorial Figma · Semana 3 — Patrones de interacción en móviles
**Prototipos Navegables (DUD2204) · Experiencia 2 · Clase del miércoles 4 de noviembre**

> 🧭 **Esta semana no construyes una pantalla completa: practicas patrones.** Cada paso es un ejercicio corto que usarás la semana 4 para armar la versión móvil de tu landing.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 2](../semana-02/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 75–90 minutos.

## Qué vas a aprender

- Crear frames con medidas de celular (**points**, no píxeles físicos).
- Marcar el **fold** y decidir qué va sobre él.
- Revisar tu diseño con la **ley del pulgar**.
- Construir botones con **área táctil de 44 × 44**.
- Crear un menú hamburguesa y una **navegación inferior** con pestañas que cambian al tocarlas.
- Hacer un **carrusel horizontal** y un **botón fijo** (sticky CTA) que acompaña el scroll.
- Probar el prototipo **en tu propio celular**.

## Antes de comenzar

Abre tu archivo **`Apple Store — Proyecto PI`**. Vas a reutilizar `Botón/Primario`, `Card/Producto`, las variables de color y los estilos de texto de las semanas 1 y 2.

1. Crea una página nueva: `Móvil · Patrones`.
2. Crea dos estilos de texto nuevos para móvil (igual que en la semana 2):

| Estilo | Tamaño | Peso | Interlineado |
| --- | --- | --- | --- |
| `Mobile/H1` | 40 | Bold | 44 |
| `Mobile/H2` | 32 | Bold | 37 |
| `Mobile/H3` | 21 | Semi Bold | 26 |

> El texto de cuerpo **no** cambia en móvil: sigue siendo `Body/Regular` de 17 px.

---

## Paso 1 — Un frame del tamaño de un celular

**Meta:** un frame de `393 × 852`.

**Concepto: points.** Un iPhone 14 Pro tiene 1179 píxeles físicos de ancho, pero en Figma se diseña en **393 points**. El teléfono multiplica por su densidad (@3x). Si diseñas en 1179, todo quedará diminuto al probar.

**Dónde está:** herramienta **Frame** (**F**). En el panel derecho aparece una lista de tamaños: abre **Teléfono / Phone**.

### Haz esto

1. Presiona **F** y elige un preset de **393 × 852** (por ejemplo, un iPhone 15 o 16). Si no lo encuentras, dibuja un frame y escribe W `393`, H `852`.
2. Nómbralo `Fold · Home móvil`.

### Comprueba

El frame mide 393 × 852. Al hacer zoom al 100 %, el tamaño en pantalla se parece al de tu celular.

> **Tip:** en clase usamos 393 como base. Revisa también cómo se vería en 360 (Android chico) y 430 (celular grande).

---

## Paso 2 — Marcar el fold

**Meta:** una home móvil más alta que la pantalla, con una línea que muestra dónde termina la primera vista.

**Concepto: fold.** Es el límite entre lo que se ve sin hacer scroll y lo que queda abajo. Cerca del 74 % de la atención se concentra en las primeras pantallas.

### Haz esto

1. Selecciona el frame y aplica **Shift + A** (vertical, separación `0`). En la altura elige **Ajustar contenido / Hug**: el frame crecerá con su contenido.
2. Agrega dentro, en orden:
   - Un **hero** (Auto Layout vertical, fondo `Color/Primario`, padding `20` a los lados y `32` arriba y abajo) con: «Nuevo» (`Eyebrow`), «iPhone Pro» (`Mobile/H1`, blanco), el precio (`Body/Regular`), un rectángulo de `353 × 300` como imagen y una instancia de `Botón/Primario` con ancho **Llenar contenedor / Fill container**.
   - Una **sección de productos** (fondo `Color/Secundario`, padding `20`) con el título «Explora nuestra línea» (`Mobile/H2`) y dos instancias de `Card/Producto` con ancho **Llenar contenedor**.
3. Dibuja una línea (**L**) roja, horizontal, a la altura **852** del frame. Nómbrala `Fold`.

### Comprueba

Sobre la línea quedan el título, el precio y el botón **Comprar**. Bajo la línea **asoma** la parte superior de una card: eso invita a seguir bajando.

> **Error frecuente: el falso final.** Si justo en el fold hay un espacio vacío o una línea horizontal gruesa, el usuario cree que la página terminó. Haz que algo asome.

> **Error frecuente:** achicar textos y botones para que «todo quepa» sobre el fold. Prioriza, no comprimas.

---

## Paso 3 — Revisar con la ley del pulgar

**Meta:** comprobar que el botón principal está donde el pulgar llega fácil.

**Concepto: ley del pulgar.** Con el teléfono en una mano, el pulgar alcanza fácil la parte de **abajo y al centro**. Las esquinas de arriba son difíciles.

### Haz esto

1. Duplica tu frame (**Ctrl + D** / **Cmd + D**) y nómbralo `Ley del pulgar`. Cambia su alto a **Fijo / Fixed** de `852` y activa **Recortar contenido / Clip content**.
2. Dentro del frame dibuja tres formas, una encima de otra:
   - Un rectángulo arriba, de color `Estado/Error`, con **opacidad 15 %**: zona **difícil**.
   - Una elipse grande al centro, color `Estado/Alerta`, opacidad 15 %: zona **alcanzable**.
   - Una elipse más chica abajo, color `Estado/Éxito`, opacidad 25 %: zona **fácil**.
3. Escribe «Difícil», «Alcanzable» y «Fácil» en cada zona.
4. Bloquea las formas (**Ctrl + Shift + L** / **Cmd + Shift + L**) para no moverlas sin querer.

### Comprueba

¿El botón **Comprar** cae en la zona verde? Si no, piensa: ¿qué pasaría si estuviera fijo abajo? (Lo harás en el Paso 7.)

> **Tip:** guarda este frame. Puedes copiar las zonas encima de cualquier pantalla móvil para revisarla.

---

## Paso 4 — Áreas táctiles de 44 × 44

**Meta:** un botón de ícono cómodo de tocar.

**Concepto: área táctil.** Es la zona que responde al dedo. **No es el ícono**: un ícono de 24 px puede vivir dentro de un frame tocable de 44 × 44.

| Referencia | Tamaño mínimo |
| --- | --- |
| Guía del curso y Apple | 44 × 44 |
| Material Design (Android) | 48 × 48 |
| WCAG 2.2 | 24 × 24 (AA) · 44 × 44 (AAA) |

### Haz esto

1. Inserta un ícono de bolsa de 24 px con el plugin **Iconify** (**Recursos / Resources → Plugins**).
2. Selecciónalo y presiona **Shift + A**. En el frame nuevo: ancho y alto **Fijo**, `44 × 44`, alineación **centro**, sin relleno.
3. Nómbralo `Botón ícono · Bolsa`.
4. Para medir, selecciona el frame y mantén **Alt** (Windows) u **Option** (macOS) mientras pasas el cursor sobre otro elemento: Figma muestra las distancias en rojo.

### Comprueba

En Capas: un frame de 44 × 44 que contiene un ícono de 24 × 24, centrado.

---

## Paso 5 — Menú hamburguesa (sitio web)

**Meta:** el componente `Navbar/Mobile`.

**Concepto: menú hamburguesa.** El ícono ☰ abre un panel con las secciones. En un **sitio web** se pone en la cabecera, porque el navegador ya ocupa el borde inferior.

### Haz esto

1. Crea dos botones ícono de 44 × 44 como en el Paso 4: `Botón ícono · Menú` (ícono ☰) y `Botón ícono · Bolsa`.
2. Pon el `Logo` de la semana 2 entre ambos.
3. Selecciona los tres y presiona **Shift + A**: horizontal, separación **Automático / Auto**, padding lateral `8`, alto fijo `52`, ancho `393`.
4. Relleno `Color/Fondo` y borde inferior de 1 px `Color/Borde`.
5. Conviértelo en componente: `Navbar/Mobile`.

### Comprueba

```
Navbar/Mobile        ◆
├── Botón ícono · Menú     (44 × 44)
├── Logo
└── Botón ícono · Bolsa    (44 × 44)
```

> En la semana 4 harás que el botón ☰ abra el menú.

---

## Paso 6 — Navegación inferior (app)

**Meta:** una barra con 4 pestañas que cambia la pestaña activa al tocarla.

**Concepto: navegación inferior.** Una **app** controla toda la pantalla y puede poner sus secciones abajo, en la zona fácil del pulgar. Funciona bien con 3 a 5 secciones.

### Haz esto — una pestaña

1. Inserta un ícono de 24 px (casa) y debajo un texto `Inicio` con estilo `Label`.
2. Selecciona ambos y presiona **Shift + A**: vertical, separación `2`, centrado, tamaño fijo `72 × 56`. Nombra el frame `Pestaña · Inicio`.
3. Duplícala tres veces: `Tienda`, `Buscar` y `Bolsa`, cada una con su ícono.

### Haz esto — la barra y sus variantes

4. Junta las 4 pestañas con **Shift + A**: horizontal, separación **Automático**, padding lateral `16`, alto `64`, ancho `393`. Fondo `Color/Fondo` y borde superior `Color/Borde`.
5. Conviértela en componente y nómbrala `TabBar/App`.
6. Pulsa **Añadir variante** tres veces. Nombra la propiedad `Activa` y los valores `Inicio`, `Tienda`, `Buscar` y `Bolsa`.
7. En cada variante, pinta la pestaña activa (ícono y texto) con `Color/Acento`. Las demás, con `Color/Texto suave`.

### Haz esto — que cambie al tocar

8. En la variante `Activa=Inicio`, selecciona `Pestaña · Tienda`. En **Prototipo**: **Al hacer clic / On click** → **Cambiar a / Change to** → `Tienda`.
9. Repite para las otras pestañas y en las otras variantes.

### Comprueba

Pon una instancia de la barra al fondo de un frame de 393 × 852 y presiona **Presentar**. Al tocar «Buscar», esa pestaña se vuelve azul.

> **Accesibilidad:** la pestaña activa no se distingue **solo por el color**: también tiene su texto. Una persona que no distingue el azul igual sabe dónde está.

> **Error frecuente:** usar **Navegar a** en vez de **Cambiar a**. «Navegar a» cambia toda la pantalla; «Cambiar a» solo cambia la variante del componente.

---

## Paso 7 — Carrusel horizontal y botón fijo

**Meta:** una ficha de producto donde las cards relacionadas se deslizan de lado y el botón **Agregar a la bolsa** siempre está visible.

**Concepto: desbordamiento (overflow).** Cuando el contenido es más grande que su frame, Figma puede dejar que el usuario haga scroll dentro de él en el prototipo.

**Concepto: sticky CTA.** Un botón de acción que queda fijo en pantalla mientras el resto se mueve.

### Haz esto — la ficha

1. Crea un frame `393 × 852` llamado `Ficha · Sticky CTA`. Activa **Recortar contenido**. **No** le pongas Auto Layout.
2. Dentro, crea un Auto Layout vertical llamado `Contenido` con: el `Navbar/Mobile`, un rectángulo de `353 × 353` como imagen, el nombre del producto (`Mobile/H2`), el precio, el texto «● En stock» en `Estado/Éxito` y una descripción corta. Deja `120` de padding abajo, para que el botón no tape el final.

### Haz esto — el carrusel

3. Dentro de `Contenido`, agrega el título «También te puede interesar» (`Mobile/H3`).
4. Agrega 4 cards en un Auto Layout **horizontal** con separación `16` y padding lateral `20`. Nómbralo `Carrusel`.
5. Pon el ancho del `Carrusel` en **Llenar contenedor** y activa **Recortar contenido**. La cuarta card queda escondida a la derecha.
6. Con el `Carrusel` seleccionado, pestaña **Prototipo** → **Comportamiento de desplazamiento / Scroll behavior** → **Desbordamiento / Overflow**: **Horizontal**.

### Haz esto — el botón fijo

7. Fuera de `Contenido`, pero dentro del frame `Ficha · Sticky CTA`, crea una barra blanca de `393 × 90` con una instancia de `Botón/Primario` («Agregar a la bolsa», ancho completo, alto `50`). Ubícala abajo del frame.
8. Selecciona la barra. En **Prototipo → Comportamiento de desplazamiento**, elige **Posición: Fija / Fixed (stay in place)**.
9. Selecciona el frame `Ficha · Sticky CTA` y pon **Desbordamiento: Vertical**.

### Comprueba

En **Presentar**: al bajar, la ficha se mueve y el botón se queda abajo. En el carrusel, las cards se arrastran de lado y la segunda **asoma** por el borde derecho.

> **Error frecuente: el carrusel no se mueve.** Revisa que tenga **Recortar contenido** y **Desbordamiento: Horizontal**, y que sus cards sumen más ancho que él.

> **Error frecuente: el botón se mueve con todo.** La barra debe estar directamente dentro del frame de la ficha, no dentro de `Contenido`.

> **Recuerda:** en táctil **no existe el hover**. Todo lo que dependía de pasar el cursor debe funcionar con un toque.

---

## Paso 8 — Probarlo en tu celular

**Meta:** sentir el diseño en la mano.

### Haz esto

1. Descarga la app **Figma** en tu celular (iOS o Android). Reemplazó a la antigua «Figma Mirror».
2. Inicia sesión con tu cuenta, abre tu archivo y entra a la página `Móvil · Patrones`.
3. Abre el prototipo de la ficha. Prueba con **una sola mano**: ¿alcanzas el botón? ¿Y el ☰ de arriba a la izquierda?

> **Sin celular a mano:** con nada seleccionado, en **Prototipo** elige un **Dispositivo / Device** (por ejemplo, iPhone 15) y presenta en el computador.

## Checklist final

- [ ] Página `Móvil · Patrones` con frames de 393 de ancho.
- [ ] Fold marcado en 852 y contenido que asoma.
- [ ] Revisión con zonas del pulgar.
- [ ] Botones ícono de 44 × 44.
- [ ] Componentes `Navbar/Mobile` y `TabBar/App` (con 4 variantes que cambian al tocar).
- [ ] Ficha con carrusel horizontal y botón fijo.
- [ ] Probado en el celular o con un dispositivo en Presentar.

> **AF2:** esta semana la actividad es un **cuestionario en AVA** (lunes 9 de noviembre, 23:59). No hay archivo que entregar, pero todo lo que practicaste aquí lo usarás en la AF3.

---

## Preguntas de repaso

1. ¿Por qué un frame de iPhone mide 393 de ancho en Figma si la pantalla tiene 1179 píxeles?
2. ¿Qué es el «falso final» y cómo se evita?
3. ¿Dónde ubicarías un botón de «Eliminar» y por qué?
4. ¿Por qué un sitio web usa menú hamburguesa arriba y una app usa navegación inferior?
5. ¿Qué diferencia hay entre **Cambiar a** y **Navegar a**?
6. Tu carrusel no avisa que hay más cards. ¿Qué puedes hacer?

## Respuestas

1. Porque Figma trabaja en **points**. El teléfono multiplica por su densidad (@3x): 393 × 3 = 1179.
2. Es un espacio vacío o una línea justo en el fold que hace creer que la página terminó. Se evita haciendo que algo asome bajo el fold.
3. Lejos de la zona fácil del pulgar (por ejemplo, arriba), y con confirmación, para que no se toque por accidente.
4. En la web, el navegador ya ocupa los bordes, sobre todo el de abajo. Una app controla toda la pantalla y puede usar la zona inferior, la más cómoda.
5. **Cambiar a** cambia la variante de un componente (la pestaña activa). **Navegar a** cambia a otra pantalla completa.
6. Dejar que la siguiente card **asome** por el borde, o agregar puntos indicadores.

## Glosario

| Término | En una frase |
| --- | --- |
| Point | Unidad de diseño; el dispositivo la multiplica por su densidad |
| Fold | Límite entre lo que se ve sin scroll y lo que queda abajo |
| Ley del pulgar | Zonas de la pantalla fáciles o difíciles de alcanzar con una mano |
| Área táctil | Zona que responde al dedo (mínimo 44 × 44) |
| Menú hamburguesa | Ícono ☰ que abre las secciones del sitio |
| Navegación inferior | Barra de pestañas fija abajo, típica de apps |
| Desbordamiento | Permite hacer scroll dentro de un frame en el prototipo |
| Sticky CTA | Botón de acción que queda fijo en la pantalla |

## Cómo sigue

En la **semana 4** juntarás todo: tomarás la landing de la semana 2 y crearás su **versión móvil de 375 px**, con menú que se abre, footer en acordeón y flujos separados para móvil y escritorio.
