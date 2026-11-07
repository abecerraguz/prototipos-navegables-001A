# Tutorial Figma · Semana 6 — Tu primera evaluación heurística
**Prototipos Navegables (DUD2204) · Experiencia 3 · Clase del miércoles 25 de noviembre**

> 🧭 **Esta semana cambias de rol: dejas de diseñar y pasas a evaluar.** Vas a preparar en Figma un espacio para registrar problemas de usabilidad y practicarás revisando tu propio prototipo con las 10 heurísticas de Nielsen.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 5](../semana-05/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 90 minutos.

## 📎 Ejemplo de la clase en Figma

[▶ Abrir el ejemplo de la Clase 06 en Figma](https://www.figma.com/design/g6QQkYAwk2pqVesSKcKb59)

Es el mismo proyecto Apple Store que construimos en clase, tal como queda al terminar esta semana. Úsalo **después** de hacer el tutorial: compara tu archivo con el ejemplo, revisa cómo están armadas las capas y los componentes, y presiona **▶ Presentar** para probar el prototipo. Si quieres desarmarlo, duplícalo en tus borradores: el original no cambia. Si tienes una duda, déjala como comentario (tecla **C**) sobre el elemento.

---

## Qué vas a aprender

- Crear una página de **evaluación** dentro de tu archivo.
- Construir un componente **Ficha de hallazgo** con severidad del 0 al 4.
- Recorrer el prototipo con **tareas** y registrar problemas con **comentarios**.
- Pegar **capturas** del problema junto a cada hallazgo.
- **Priorizar** los hallazgos por severidad.

## Antes de comenzar

Abre **`Apple Store — Proyecto PI`** con las páginas interiores de la semana 5. Ten a mano la tabla de las 10 heurísticas de tu [resumen de la clase](resumen-clase.md).

> **AF4:** la actividad de esta semana es un **cuestionario en AVA** sobre una plataforma de cursos en línea (lunes 30 de noviembre, 23:59). Este tutorial es práctica: te prepara para el cuestionario y para la AF5 de la semana 7, donde evaluarás tu prototipo «en serio».

---

## Paso 1 — La página de evaluación

**Meta:** un lugar ordenado para los hallazgos, separado del diseño.

### Haz esto

1. Crea la página `🔍 Evaluación heurística`.
2. Crea tres secciones (**Shift + S**): `Referencia`, `Hallazgos` y `Priorización`.

> **¿Por qué en el mismo archivo?** Así cada hallazgo queda al lado de las pantallas que evalúa, y en la semana 8, cuando corrijas, sabrás exactamente qué cambiar.

---

## Paso 2 — Tarjeta de referencia: las 10 heurísticas

**Meta:** tener las heurísticas a la vista mientras evalúas.

### Haz esto

1. En la sección `Referencia`, crea un frame con Auto Layout vertical, ancho `600`, padding `32`, fondo `Color/Secundario`.
2. Escribe las 10 heurísticas, una por línea, con su número en negrita:

```
1. Visibilidad del estado del sistema
2. Relación entre el sistema y el mundo real
3. Control y libertad del usuario
4. Consistencia y estándares
5. Prevención de errores
6. Reconocer antes que recordar
7. Flexibilidad y eficiencia de uso
8. Diseño estético y minimalista
9. Ayudar a reconocer, diagnosticar y recuperarse de errores
10. Ayuda y documentación
```

3. Debajo, la escala de severidad:

| Nivel | Nombre | ¿Qué hacer? |
| --- | --- | --- |
| 0 | No es problema | Nada |
| 1 | Cosmético | Solo si hay tiempo |
| 2 | Menor | Baja prioridad |
| 3 | Mayor | Corregir antes de publicar |
| 4 | Catastrófico | Corregir sí o sí antes de publicar |

---

## Paso 3 — Componente Ficha de hallazgo

**Meta:** una tarjeta reutilizable para documentar cada problema siempre igual.

**Concepto:** si todos los hallazgos tienen los mismos campos, es fácil compararlos, ordenarlos y pasarlos luego a la plantilla de la semana 7.

### Haz esto — la tarjeta

1. Crea un frame con Auto Layout vertical: ancho fijo `360`, alto **Ajustar contenido**, padding `20`, separación `8`, radio `12`, borde 1 px `Color/Borde`, fondo blanco.
2. Agrega estos textos, cada uno con un rótulo en `Label` y su contenido en `Small`:

| Rótulo | Ejemplo de contenido |
| --- | --- |
| ID | H1 |
| Heurística | #8 Diseño estético y minimalista |
| Elemento | Ficha · botones de compra |
| Descripción | El CTA compite con otros 3 botones en la misma vista. |
| Propuesta | Dejar un solo botón primario y los demás como secundarios. |

3. Para los textos largos (Descripción y Propuesta): ancho **Llenar contenedor** y crecimiento **Alto automático / Auto height**, para que hagan salto de línea.
4. Arriba de todo, agrega una **pastilla de severidad**: texto `Severidad 2` dentro de un Auto Layout con radio `999` y padding `4 × 10`.
5. Conviértela en componente: `Ficha de hallazgo`.

### Haz esto — propiedades

6. Crea **propiedades de texto** para `ID`, `Heurística`, `Elemento`, `Descripción` y `Propuesta` (ícono de propiedad junto al contenido de cada texto, como en la semana 5).
7. **Añadir variante** cuatro veces. Propiedad `Severidad`: `1`, `2`, `3` y `4`. Cambia el color de la pastilla:

| Severidad | Color de la pastilla | Texto |
| --- | --- | --- |
| 1 | `Color/Secundario` | `Color/Texto` |
| 2 | `Color/Borde` | `Color/Texto` |
| 3 | `Estado/Alerta` | blanco |
| 4 | `Estado/Error` | blanco |

### Comprueba

Al poner una instancia de `Ficha de hallazgo`, en el panel derecho cambias la severidad con un menú y escribes los textos sin entrar al componente.

> **Accesibilidad también aquí:** la pastilla dice «Severidad 3» con palabras. No dependas solo del color.

---

## Paso 4 — Definir el alcance y las tareas

**Meta:** saber qué vas a revisar antes de empezar.

**Concepto: tarea.** Algo concreto que un usuario quiere lograr. Evaluar por tareas te obliga a recorrer los flujos reales, no solo a mirar pantallas sueltas.

### Haz esto

En la sección `Referencia`, escribe 3 tareas para tu prototipo. Por ejemplo:

1. «Encuentra un iPad y entra a su ficha.»
2. «Elige un color y una capacidad, y agrégalo a la bolsa.»
3. «Busca cómo contactar a soporte.»

---

## Paso 5 — Recorrer el prototipo y comentar

**Meta:** encontrar problemas mientras usas el prototipo como lo haría un cliente.

**Concepto: comentario.** Una nota anclada a un punto exacto del diseño (o del prototipo). Queda visible para todo el equipo.

### Haz esto

1. Abre el flujo `Mobile · Compra` en **Presentar**.
2. Haz la **tarea 1** de principio a fin. Cada vez que algo te haga dudar, detenerte o equivocarte, presiona **C** y haz clic sobre el elemento.
3. Escribe el comentario con este formato corto:

```
#4 · Sev 2 · El botón dice «Comprar» aquí y «Agregar a la bolsa» en la ficha.
```

4. Repite con las tareas 2 y 3. Luego haz el mismo recorrido en el flujo de escritorio.

> **Tip: mira con ojos de cliente.** Pregúntate en cada pantalla: ¿sé dónde estoy?, ¿sé qué pasó cuando toqué algo?, ¿puedo volver?, ¿entiendo las palabras?

> **Tip:** revisa cada heurística al menos una vez. Si una nunca aparece, vuelve a recorrer pensando solo en ella.

---

## Paso 6 — Pasar los hallazgos a fichas

**Meta:** cada comentario convertido en una ficha con su captura.

### Haz esto

1. Selecciona en el diseño la parte donde está el problema (por ejemplo, la barra de compra de la ficha).
2. Cópiala como imagen: **Ctrl + Shift + C** (Windows) o **Cmd + Shift + C** (macOS) — **Copiar como PNG / Copy as PNG**.
3. Ve a la sección `Hallazgos` y pégala (**Ctrl + V** / **Cmd + V**).
4. Al lado, pon una instancia de `Ficha de hallazgo` y complétala.
5. Si quieres señalar el punto exacto, dibuja una flecha (**Shift + L**) desde la ficha hasta la captura.
6. Agrupa captura, flecha y ficha en un Auto Layout horizontal. Nómbralo con el ID: `H1`, `H2`…

### Comprueba

Cada hallazgo tiene: ID, heurística, elemento, descripción, **severidad**, **propuesta** y captura.

> **Error frecuente: hallazgos vagos.** «El botón se ve mal» no sirve. Escribe **qué** está mal, **dónde** y **por qué** afecta al usuario. Ejemplo: «Heurística #8, severidad 2: el CTA compite visualmente con 3 botones más en la misma vista».

> **Error frecuente: propuestas vagas.** «Mejorar el contraste» no sirve. Escribe cómo: «Cambiar el texto del precio de #A1A1A6 a #6E6E73 sobre blanco para pasar de 2,6:1 a 5,1:1».

---

## Paso 7 — Priorizar

**Meta:** saber qué corregir primero.

### Haz esto

1. En la sección `Priorización`, crea 4 columnas con Auto Layout vertical: `Severidad 4`, `Severidad 3`, `Severidad 2` y `Severidad 1`.
2. Duplica cada ficha (**Ctrl + D** / **Cmd + D**) y arrástrala a su columna.
3. Pon las columnas una al lado de otra con un Auto Layout horizontal.
4. Marca las fichas de severidad **3 y 4**: son las que deberías corregir en la semana 8.

### Comprueba

De un vistazo se ve cuántos problemas graves tiene tu prototipo.

---

## Checklist final

- [ ] Página `🔍 Evaluación heurística` con secciones Referencia, Hallazgos y Priorización.
- [ ] Tarjeta con las 10 heurísticas y la escala de severidad.
- [ ] Componente `Ficha de hallazgo` con propiedades y 4 severidades.
- [ ] 3 tareas escritas.
- [ ] Al menos **5 hallazgos** con captura, heurística y propuesta.
- [ ] Hallazgos ordenados por severidad.

---

## Preguntas de repaso

1. ¿Por qué Nielsen recomienda entre 3 y 5 evaluadores?
2. Al tocar «Agregar a la bolsa», no pasa nada visible. ¿Qué heurística se vulnera?
3. El producto se elimina del carrito sin preguntar. ¿Qué heurística y qué severidad le darías?
4. ¿Qué diferencia hay entre severidad 3 y 4?
5. ¿Por qué conviene evaluar con tareas y no solo mirando pantallas?

## Respuestas

1. Porque cada evaluador detecta solo una parte de los problemas: uno encuentra cerca del 35 %, cinco llegan a cerca del 75 %.
2. La n.º 1, **Visibilidad del estado del sistema**: el usuario no sabe si su acción funcionó.
3. La n.º 5, **Prevención de errores** (también la n.º 3, Control y libertad). Al menos severidad 3: puede hacer perder una compra.
4. Severidad 3 (mayor) es importante corregir antes de publicar. Severidad 4 (catastrófico) **impide** usar el sitio y debe corregirse sí o sí.
5. Porque obliga a recorrer los flujos completos. Muchos problemas solo aparecen al pasar de una pantalla a otra.

## Glosario

| Término | En una frase |
| --- | --- |
| Heurística | Principio general de usabilidad |
| Evaluación heurística | Revisión experta de una interfaz usando heurísticas |
| Hallazgo | Problema de usabilidad encontrado y documentado |
| Severidad | Gravedad del hallazgo, del 0 al 4 |
| Tarea | Objetivo concreto de un usuario dentro del prototipo |
| Copiar como PNG | Copia una selección del diseño como imagen |

## Cómo sigue

En la **semana 7** evaluarás tu prototipo con **otras personas** (test guiado y no guiado), revisarás los criterios de accesibilidad y pasarás todo a la **plantilla de Torres Burriel** para la AF5.
