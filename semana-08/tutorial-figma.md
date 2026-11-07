# Tutorial Figma · Semana 8 — Iterar con evidencia y hacer un A/B test
**Prototipos Navegables (DUD2204) · Experiencia 3 · Clase del miércoles 9 de diciembre**

> 🧭 **Hoy corriges tu prototipo, pero no «a gusto»: cada cambio responde a un hallazgo de la semana 7.** Aprenderás a guardar el «antes», corregir desde el sistema de diseño para que el cambio llegue a todas las páginas, y comparar dos versiones con un A/B test.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 7](../semana-07/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 2,5 horas, más el tiempo del A/B test con 2 a 4 personas.

## 📎 Ejemplo de la clase en Figma

[▶ Abrir el ejemplo de las Clases 08 y 09 en Figma](https://www.figma.com/design/TYFZLFIFTpNbU0XGz7spEX)

Es el mismo proyecto Apple Store que construimos en clase, tal como queda al terminar esta semana. Úsalo **después** de hacer el tutorial: compara tu archivo con el ejemplo, revisa cómo están armadas las capas y los componentes, y presiona **▶ Presentar** para probar el prototipo. Si quieres desarmarlo, duplícalo en tus borradores: el original no cambia. Si tienes una duda, déjala como comentario (tecla **C**) sobre el elemento.

---

## Qué vas a aprender

- Guardar el estado **antes** de iterar (historial de versiones y capturas).
- Corregir **desde los componentes y las variables**, para que el cambio se propague.
- Agregar estados que faltan: **Presionado** y **Foco**.
- Crear patrones de **feedback**: un aviso que aparece y se va solo, y una confirmación antes de eliminar.
- Armar un **A/B test** con dos versiones y dos flujos.
- Documentar el **antes y después** de cada cambio.

## Antes de comenzar

- [ ] Tus hallazgos priorizados de la semana 7 (página `🔍 Evaluación heurística`).
- [ ] La plantilla de Torres Burriel completa.
- [ ] El **formato de respuesta de la AS3**, descargado desde AVA.

> **Iterar no es rediseñar.** Una iteración es **quirúrgica** (toca solo lo necesario), **basada en evidencia** (responde a un hallazgo), **trazable** (sabes qué problema resuelve) y **medible** (puedes comprobar si funcionó).

---

## Paso 1 — Guardar el «antes»

**Meta:** no perder la versión original, porque necesitas compararla.

### Haz esto

1. **Exporta las capturas del antes.** Por cada pantalla que vas a cambiar: selecciónala → **Exportar** → **PNG 2x** → nómbrala `antes-ficha-mobile.png`, etc.
2. **Guarda una versión.** Menú **Archivo / File → Guardar en el historial de versiones / Save to version history**. Título: `v1 · Antes de iterar`. Descripción: «Estado después de la AF5».

> **Error frecuente: duplicar las páginas para guardar el antes.** Las copias tienen **instancias**: cuando corrijas un componente, ¡la copia también cambiará! Por eso el «antes» se guarda como **captura** y en el **historial de versiones**.

> **Tip:** para volver a ver la v1, abre **Archivo → Mostrar historial de versiones / Show version history** y haz clic en `v1`. No pierdes nada de lo nuevo.

---

## Paso 2 — Elegir qué corregir

**Meta:** una lista corta y priorizada.

### Haz esto

1. En `Priorización`, toma todas las fichas de **severidad 4 y 3**.
2. Agrupa las que se resuelven con el mismo cambio (por ejemplo, dos problemas de contraste se corrigen ajustando una variable).
3. Elige **al menos 3 iteraciones**. Escribe cada una en una nota:

```
Iteración 1 → resuelve H?, H? · Heurística/criterio: #? · Qué cambiaré: …
```

> **No iteres** lo que solo es una preferencia tuya sin un hallazgo detrás.

---

## Paso 3 — Corregir desde el sistema de diseño

**Meta:** que cada corrección se haga **una vez** y llegue a todas las páginas.

**Concepto: propagación.** Si corriges el componente principal o la variable, todas las instancias cambian. Si corriges una instancia suelta, solo cambia esa.

Estas son correcciones frecuentes. Aplica las que respondan a **tus** hallazgos:

### 3.1 Contraste insuficiente

1. Abre **Variables** y busca la variable del color con problema.
2. Cambia su valor y verifica el nuevo contraste (plugin de contraste o WebAIM).
3. Revisa 2 o 3 páginas: el color cambió en todas.

### 3.2 Área táctil pequeña

1. Ve al componente principal (clic derecho en una instancia → **Ir al componente principal / Go to main component**).
2. Ajusta su alto o su frame contenedor a **44** como mínimo.
3. Revisa que las páginas no se hayan desarmado: el Auto Layout debería reacomodar todo.

### 3.3 Sin respuesta al presionar (variante Presionado)

1. En `Botón/Primario`, **Añadir variante** → `Estado=Presionado`. Oscurece un poco el relleno.
2. En la variante `Normal`, **Prototipo** → **Mientras se presiona / While pressing** → **Cambiar a** → `Presionado` → **Smart animate**, `100 ms`.

### 3.4 Sin indicador de foco (variante Foco)

1. **Añadir variante** → `Estado=Foco`.
2. Agrega un borde exterior de **3 px** `Color/Acento`, separado 2 px del botón.
3. Anota para desarrollo: «Foco visible al navegar con Tab».

### 3.5 Información solo por color

Agrega una segunda señal al componente: un ícono, un texto o un subrayado.

### Comprueba

Después de cada corrección, recorre el flujo afectado en **Presentar**.

---

## Paso 4 — Patrón de feedback: un aviso que se va solo

**Meta:** cuando el usuario hace algo importante (como agregar a la bolsa), el sistema le confirma que funcionó.

**Concepto: toast.** Un aviso breve que aparece encima de la pantalla y desaparece solo. Responde a la heurística n.º 1, **Visibilidad del estado del sistema**.

### Haz esto

1. Crea un frame de `335 × 56`, radio `12`, fondo `Color/Texto`, con un ícono ✓ y un texto blanco: «Agregado a tu bolsa». Nómbralo `Toast · Agregado`.
2. En la ficha, selecciona el botón «Agregar a la bolsa» → **Al hacer clic** → **Abrir superposición** → `Toast · Agregado`. Posición: **Arriba al centro / Top center**. Animación: **Desplazar hacia dentro**, desde arriba.
3. Selecciona el frame `Toast · Agregado` → **Prototipo** → **+** → **Después de un tiempo / After delay**: `3000 ms` → **Cerrar superposición**.

### Comprueba

Al tocar el botón, el aviso baja, se queda 3 segundos y se va solo.

---

## Paso 5 — Patrón de prevención: confirmar antes de borrar

**Meta:** evitar que un toque accidental borre algo importante (heurística n.º 5, **Prevención de errores**).

### Haz esto

1. Crea un frame de `335 × 200` llamado `Modal · Confirmar`: una pregunta clara («¿Eliminar este producto de tu bolsa?»), una frase con el detalle y dos botones: **Cancelar** (secundario) y **Eliminar** (fondo `Estado/Error`, texto blanco).
2. Desde el ícono de eliminar → **Al hacer clic** → **Abrir superposición** → `Modal · Confirmar`. Posición **Centro**. Activa **Añadir fondo / Add background** (negro, 40 %).
3. **Cancelar** → **Cerrar superposición**. **Eliminar** → **Navegar a** la versión del carrito sin ese producto (o **Cerrar superposición** si no la tienes).

> **Tip:** el botón destructivo dice **qué** hace («Eliminar»), no «Aceptar».

---

## Paso 6 — Armar el A/B test

**Meta:** comparar tu diseño actual (A) con el mejorado (B) y decidir con datos.

**Concepto: variantes A y B.** En la AS3, la **variante A** es tu diseño **actual** (el que evaluaste en la semana 7) y la **variante B** es el diseño **mejorado**. Las dos tienen los mismos elementos; cambia el diseño. Así compruebas si tus mejoras funcionan de verdad.

> 💡 **Si quieres saber qué cambio funcionó:** cambiar varias cosas te dice qué versión es mejor, pero no exactamente por qué. Si te interesa un cambio en particular (por ejemplo, botón de compra fijo abajo o dentro de la página), puedes hacer además un A/B de **un solo cambio**.

### Haz esto

1. Crea la página `🅰️🅱️ A/B test`.
2. Copia ahí las pantallas del recorrido que vas a probar **tal como estaban** antes de iterar: esa es la `Versión A`. Si ya corregiste los componentes, recupéralas desde el historial de versiones (**Archivo → Mostrar historial de versiones** → clic derecho en `v1` → **Duplicar**) y cópialas desde ese archivo.
3. Copia las mismas pantallas **ya mejoradas**: esa es la `Versión B`.
4. Conecta cada recorrido por separado y crea dos flujos: `Flujo A` y `Flujo B`.

### Comprueba

Las dos versiones tienen los mismos elementos y el mismo recorrido; lo que cambia es el diseño mejorado.

---

## Paso 7 — Hacer el A/B test

### Haz esto — datos cuantitativos

1. Elige una **métrica**: si completan la tarea, el tiempo, la cantidad de clics o pasos, los errores.
2. Prepara la misma tarea para todos: por ejemplo, «Agrega un producto al carrito y llega al check out».
3. Muestra la **versión A** a la mitad de las personas y la **B** a la otra mitad (comparte el enlace de cada flujo desde **Presentar**). El enunciado pide usar una **herramienta de pruebas A/B**: busca una que acepte prototipos de Figma para medir clics y tiempos; si no puedes usarla, mide tú y anótalo.
4. Anota los resultados en una tabla en la misma página:

| Participante | Versión | ¿Completó? | Métrica (tiempo / clics) | Comentario |
| --- | --- | --- | --- | --- |
| P1 | A | | | |
| P2 | B | | | |
| P3 | A | | | |
| P4 | B | | | |

5. Compara: ¿la variante B fue más efectiva? Escribe **por qué**.

### Haz esto — feedback cualitativo y ajustes finales

6. Muestra la **variante B** a usuarios reales y pregúntales cómo la perciben: qué les resultó fácil, qué les costó, si algo no se entiende o no se lee bien.
7. Con ese feedback, haz los **ajustes finales** en el diseño.

> **Con pocas personas, sé honesto:** 4 participantes dan una **señal**, no una prueba definitiva. Dilo en tu reporte.

---

## Paso 8 — Documentar el antes y después

**Meta:** que se vea, sin explicar mucho, qué cambió y por qué.

### Haz esto

1. Crea la página `📝 Iteraciones`.
2. Por cada iteración, crea un frame horizontal con:
   - La captura **antes** (del Paso 1; arrastra el PNG a Figma).
   - Una captura **después** (selecciona la pantalla corregida → **Copiar como PNG** → pega).
   - Una ficha de texto: hallazgo que resuelve, heurística o criterio, qué cambiaste y resultado esperado.
3. Exporta cada frame en **PNG 2x** para el formato de respuesta.
4. Guarda una versión nueva: **Archivo → Guardar en el historial de versiones** → `v2 · Después de iterar`.

---

## Paso 9 — Entrega (AS3)

1. Escribe el **reporte** en el documento de la actividad: cómo abordaste los problemas de la semana 7, cómo implementaste las mejoras, los resultados del A/B test (con capturas comparativas y gráficos) y cómo integraste el feedback de los usuarios en los ajustes finales.
2. Pega el **enlace de revisión** del diseño en el documento.
3. **Archivo → Guardar copia local** → comprime el `.fig` en un ZIP.
4. Revisa la **rúbrica** y sube **los dos** (documento y ZIP) a AVA antes del **lunes 14 de diciembre a las 23:59**.

## Checklist final

- [ ] Capturas del antes exportadas y versión `v1` guardada.
- [ ] Al menos 3 iteraciones basadas en hallazgos de severidad 3 o 4.
- [ ] Correcciones hechas en componentes o variables, no en instancias sueltas.
- [ ] Al menos un patrón de feedback y uno de prevención, si tus hallazgos los piden.
- [ ] A/B test con versión A (actual) y B (mejorada), dos flujos, datos cuantitativos y feedback de usuarios reales.
- [ ] Ajustes finales hechos y reporte con enlace de revisión.
- [ ] Página `📝 Iteraciones` con antes y después.
- [ ] Versión `v2` guardada.

---

## Preguntas de repaso

1. ¿Qué diferencia hay entre iterar y rediseñar?
2. ¿Por qué no sirve duplicar las páginas para guardar el «antes»?
3. ¿Dónde corriges un problema de contraste para que se arregle en todo el sitio?
4. ¿Qué heurística resuelve el aviso «Agregado a tu bolsa»?
5. En tu A/B test cambiaste el color **y** la posición del botón. ¿Qué problema tiene?

## Respuestas

1. Iterar es corregir algo específico porque hay evidencia de que falla. Rediseñar es rehacer, muchas veces por gusto.
2. Porque las copias tienen instancias: al corregir el componente principal, la copia también cambia y pierdes el «antes».
3. En la **variable** de ese color (o en el componente principal). El cambio llega a todas las instancias.
4. La n.º 1, **Visibilidad del estado del sistema**.
5. Sabrás qué versión funcionó mejor, pero no cuál de los dos cambios produjo el resultado. Si necesitas saberlo, prueba un cambio a la vez.

## Glosario

| Término | En una frase |
| --- | --- |
| Iteración | Ciclo de mejora basado en evidencia |
| Historial de versiones | Registro de estados guardados del archivo |
| Propagación | Un cambio en el componente principal llega a todas sus instancias |
| Toast | Aviso breve que aparece y desaparece solo |
| Modal de confirmación | Ventana que pide confirmar una acción riesgosa |
| A/B test | Comparar dos versiones con los mismos elementos y distinto diseño |
| Métrica | Lo que mides para decidir qué versión funciona mejor |

## Cómo sigue

En la **semana 9** cierras el bimestre: con la versión ganadora del A/B test armarás la **maqueta final** en móvil y escritorio y prepararás las capturas para el informe de la **EFT**.
