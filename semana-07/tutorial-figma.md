# Tutorial Figma · Semana 7 — Testear tu prototipo con personas y revisar su accesibilidad
**Prototipos Navegables (DUD2204) · Experiencia 3 · Clase del miércoles 2 de diciembre**

> 🧭 **La semana pasada evaluaste tú. Hoy evalúan otros.** Prepararás tu prototipo para que otra persona lo pruebe, harás un test guiado y uno no guiado, revisarás la accesibilidad y llevarás todo a la plantilla de Torres Burriel.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 6](../semana-06/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 2 horas, más 20 a 30 minutos por cada persona que pruebe tu prototipo.

## Qué vas a aprender

- Preparar **un flujo por tarea** para el test.
- **Compartir** el prototipo con un enlace.
- Conducir un **test no guiado** y uno **guiado**, y registrar lo que pasa.
- Revisar la **accesibilidad** del prototipo dentro de Figma.
- **Exportar capturas** y completar la **plantilla de Torres Burriel**.

## Antes de comenzar

- [ ] Tu prototipo con las páginas interiores (semana 5) y sus flujos.
- [ ] La página `🔍 Evaluación heurística` y el componente `Ficha de hallazgo` (semana 6).
- [ ] El **formato de respuesta de la AF5** descargado desde AVA y la [plantilla de test heurístico de Torres Burriel](https://torresburriel.com/weblog/plantilla-para-hacer-analisis-heuristicos-de-usabilidad/).
- [ ] La [tabla de cotejo WCAG nivel AA del CRAED](https://craed.cl/criterios-de-accesibilidad/).
- [ ] Una o dos personas que puedan probar tu prototipo (un familiar, un compañero de otra carrera, un amigo). Mejor si **no** conocen tu diseño.

| | Test no guiado | Test guiado |
| --- | --- | --- |
| Cómo es | Le explicas el contexto, pero **no lo guías**: observas y anotas todo lo que hace y no hace | **Guías** a la persona hacia una sección o tarea puntual |
| Qué le pides | «Explora el sitio y cuéntame qué ves» | «Encuentra unos audífonos y agrégalos a la bolsa» |
| Qué descubres | Dónde se estanca y dónde le resulta fácil navegar | Cómo funciona una sección o un elemento concreto |
| Tip de la guía | Grábalo, para revisar después lo que no alcanzaste a ver | Define antes las secciones o tareas a revisar |

> Lo ideal es hacer **los dos** en la misma sesión: primero el no guiado, después el guiado.

---

## Paso 1 — Un flujo por tarea

**Meta:** que cada tarea del test empiece en el lugar correcto.

### Haz esto

1. Escribe 3 tareas guiadas. Que sean concretas y no digan **dónde** hacer clic:
   - ✅ «Quieres comprar unos audífonos. Encuéntralos y agrégalos a la bolsa.»
   - ❌ «Haz clic en Productos y luego en AirPods.»
2. En `📱 Páginas · Mobile 375`, selecciona el frame donde empieza cada tarea (normalmente la home). En **Prototipo**, junto a **Punto de inicio de flujo**, pulsa **+** y nómbralo `Tarea 1 · Audífonos`, `Tarea 2 · …`, etc.
3. Crea también un flujo `Exploración libre` para el test no guiado.

### Comprueba

Al presentar, en el panel izquierdo aparecen tus flujos con esos nombres.

---

## Paso 2 — Revisar que nada esté roto

**Meta:** que el test mida tu diseño, no tus enlaces rotos.

### Haz esto

1. Recorre cada flujo en **Presentar** y haz las tareas tú mismo.
2. Si un botón no lleva a ningún lado, decide: ¿lo conectas o lo dejas así a propósito? Si lo dejas así, anótalo; no es un hallazgo de diseño.
3. Revisa el **botón Atrás** en cada pantalla: la persona nunca debe quedar atrapada.

> **Tip:** cuando alguien hace clic en una zona sin interacción, Figma destaca en azul las zonas clicables. Durante el test, si eso pasa, anótalo: la persona buscaba algo que no encontró.

---

## Paso 3 — Compartir el prototipo

**Meta:** que la otra persona pueda abrir el prototipo en su computador o celular.

### Haz esto

1. Abre el prototipo en **Presentar**.
2. Botón **Compartir / Share** (arriba a la derecha).
3. En el acceso, elige **Cualquier persona con el enlace / Anyone with the link** con permiso **Puede ver / Can view**.
4. Pulsa **Copiar enlace / Copy link** y envíalo.

> **Test a distancia:** comparte tu pantalla en una videollamada y pide a la persona que **te dicte** dónde hacer clic, o envíale el enlace y pídele que comparta **su** pantalla.

> **Error frecuente:** compartir el enlace del **archivo** en vez del **prototipo**. La persona vería capas y paneles. El enlace correcto se copia desde la vista Presentar.

---

## Paso 4 — Preparar el registro del test

**Meta:** una tabla en Figma para anotar mientras observas.

### Haz esto

1. Crea la página `🧪 Test con usuarios`.
2. Por cada persona, crea un frame con Auto Layout vertical llamado `Participante 1`, `Participante 2`… con esta tabla:

| Tarea | ¿La completó? | Tiempo aprox. | Dudas o errores | Lo que dijo |
| --- | --- | --- | --- | --- |
| Exploración libre | — | 2 min | | |
| Tarea 1 | Sí / Con ayuda / No | | | |
| Tarea 2 | | | | |
| Tarea 3 | | | | |

3. Escribe arriba un guion corto para leerle a la persona antes de empezar:

> «Gracias por ayudarme. Vamos a probar el **diseño**, no a ti: si algo te cuesta, es un problema del diseño. Por favor, piensa en voz alta: dime qué ves, qué buscas y qué esperas que pase. Yo no te voy a ayudar durante las tareas.»

---

## Paso 5 — Hacer el test

**Meta:** observar sin intervenir.

### Haz esto

1. Lee el guion.
2. **No guiado (2 a 3 minutos):** abre el flujo `Exploración libre` y di solo «Explora y cuéntame qué es este sitio».
3. **Guiado:** abre cada flujo `Tarea …` y lee la tarea en voz alta.
4. Mientras la persona trabaja, anota en la tabla. Si quieres marcar el punto exacto, deja un comentario (**C**) en el diseño que empiece con `P1 ·` (participante 1).
5. Al final, pregunta: «¿Qué fue lo más difícil?» y «¿Qué cambiarías?».

> **Regla de oro:** no expliques, no corrijas, no digas «es por allá». Si la persona pregunta, responde: «¿Dónde crees que estaría?». Lo que le cuesta es justo lo que necesitas saber.

---

## Paso 6 — Revisión de accesibilidad

**Meta:** revisar el prototipo con los criterios de WCAG 2.1, ordenados en sus cuatro principios.

Crea en `🔍 Evaluación heurística` un frame `Checklist de accesibilidad` y revisa cada punto en tus páginas.

### Perceptible

1. **Contraste.** En **Recursos / Resources → Plugins**, busca «contrast» e instala un plugin de revisión de contraste. Selecciona un texto y su fondo y revisa el resultado. También puedes usar [WebAIM](https://webaim.org/resources/contrastchecker/).
   - Texto normal: mínimo **4,5:1**. Texto grande: mínimo **3:1**.
2. **Texto alternativo.** ¿Cada imagen tiene su alt anotado?
3. **No solo color.** ¿Hay algo que se entienda **solo** por el color? (Un error en rojo sin mensaje, una pestaña activa solo en azul.)

### Operable

4. **Áreas táctiles.** Selecciona cada botón, chip y link y mira su tamaño en el panel derecho. ¿Mide al menos **44 × 44**? Para medir distancias, mantén **Alt** / **Option** y pasa el cursor.
5. **Foco.** ¿Tus componentes interactivos tienen una variante `Foco` o una anotación que indique cómo se ve el foco con teclado?

### Comprensible

6. **Lenguaje.** ¿Los textos son claros y sin tecnicismos? ¿Los botones dicen lo mismo en todas las páginas?
7. **Errores.** ¿Los mensajes de error explican qué pasó y cómo arreglarlo?

### Robusto

8. **Anotaciones para desarrollo.** ¿Los botones de solo ícono tienen nombre accesible? ¿Los campos de formulario tienen etiqueta visible?

### Comprueba

Cada punto que **no** se cumple se convierte en una `Ficha de hallazgo` nueva.

> **Propuestas específicas:** «Mejorar el contraste» no sirve. «Cambiar el texto del precio de #A1A1A6 a #6E6E73 sobre blanco para pasar de 2,6:1 a 5,1:1» sí sirve.

---

## Paso 7 — Juntar todos los hallazgos

**Meta:** una sola lista con lo que encontraste tú, lo que encontraron los participantes y lo de accesibilidad.

### Haz esto

1. Por cada problema del test y del checklist, agrega una `Ficha de hallazgo` en la sección `Hallazgos` con su captura (**Copiar como PNG**, como en la semana 6).
2. En la descripción, indica el origen: `[Heurístico]`, `[Test P1]` o `[Accesibilidad]`.
3. Si dos personas tuvieron el mismo problema, es **un** hallazgo, pero súbele la severidad: se repite.
4. Vuelve a ordenar todo en la sección `Priorización`.

### Comprueba

Tienes **al menos 8 hallazgos**, cada uno con heurística o criterio, severidad, propuesta y captura.

---

## Paso 8 — Exportar capturas

**Meta:** imágenes nítidas para la plantilla.

### Haz esto

1. Selecciona el grupo de un hallazgo (`H1`: captura + ficha).
2. En el panel derecho, sección **Exportar / Export**, pulsa **+**. Formato **PNG**, tamaño **2x**.
3. Pulsa **Exportar H1**. Repite con cada hallazgo.
4. Exporta también cada pantalla evaluada completa: te servirá en las semanas 8 y 9.

> **Tip:** selecciona varios grupos a la vez y exporta todos de una vez. Cada archivo toma el nombre de su capa.

---

## Paso 9 — Puntuar con Torres Burriel y escribir el reporte (AF5)

**La plantilla de Torres Burriel** es un test que **puntúa** tu prototipo, con preguntas de cotejo basadas en los criterios de Yusef Hassan:

1. Completa los **datos de tu proyecto** en la plantilla.
2. Revisa **cada pregunta de cotejo** mientras recorres tu prototipo (mínimo 5 y máximo 10 páginas).
3. **Asigna una puntuación** a cada pregunta.

**La tabla de cotejo WCAG (nivel AA)** del CRAED: marca qué criterios cumple cada elemento y cuáles no.

**El reporte**, en el formato de respuesta de la AF5:

1. **Introducción:** el proyecto, su objetivo y cómo hiciste la evaluación (heurística y de accesibilidad).
2. **Explicación del contexto:** por qué y para qué evaluaste.
3. **Hallazgos más importantes**, en orden de prioridad: primero los de severidad 4 y 3. Usa tus fichas de hallazgo.
4. **Test heurístico completo** (la plantilla de Torres Burriel puntuada), adjunto.
5. **Tabla de cotejo de accesibilidad**, adjunta.
6. **Lo que cumple y lo que necesita mejoras:** tablas o gráficos y tus **capturas** del Paso 8, con cómo implementarías cada cambio.
7. **Conclusiones:** hallazgos principales, recomendaciones y su impacto en la usabilidad y la accesibilidad.

**Entrega:** pega el **enlace de revisión** del diseño en el formato, comprime tu `.fig` en un **ZIP** y sube **los dos** a AVA antes del **lunes 7 de diciembre a las 23:59**. Revisa la **rúbrica** antes.

## Checklist final

- [ ] Flujos por tarea y flujo de exploración libre.
- [ ] Prototipo revisado sin enlaces rotos.
- [ ] Al menos 1 persona testeó (ideal: 2 o 3).
- [ ] Registro del test en `🧪 Test con usuarios`.
- [ ] Checklist de accesibilidad completo.
- [ ] Al menos 8 hallazgos consolidados y priorizados.
- [ ] Capturas exportadas en PNG 2x.
- [ ] Plantilla de Torres Burriel puntuada y tabla de cotejo WCAG AA completa.
- [ ] Reporte en el formato de respuesta, con enlace de revisión, y ZIP del proyecto.

---

## Preguntas de repaso

1. ¿Por qué el test no guiado se hace antes que el guiado?
2. Una tarea dice «Haz clic en el menú y elige Productos». ¿Qué tiene de malo?
3. ¿Por qué no debes ayudar a la persona durante el test?
4. ¿Cuál es el contraste mínimo para un texto de 17 px según WCAG AA?
5. Tu pestaña activa solo cambia de gris a azul. ¿Qué criterio no cumple y cómo lo arreglas?

## Respuestas

1. Porque las tareas le enseñan el sitio. Si primero haces el guiado, ya no verás su primera impresión real.
2. Le dice exactamente dónde hacer clic. La tarea debe describir el **objetivo**, no el camino.
3. Porque necesitas ver dónde se traba. Si ayudas, el problema queda escondido.
4. 4,5:1 (es texto normal; el texto grande empieza en 24 px, o 19 px en negrita).
5. «No usar solo el color» (Perceptible). Agrega otra señal: texto en negrita, un subrayado o un indicador.

## Glosario

| Término | En una frase |
| --- | --- |
| Test no guiado | La persona explora libremente |
| Test guiado | La persona cumple tareas concretas |
| Pensar en voz alta | Pedir a la persona que diga lo que piensa mientras usa el prototipo |
| Participante | Persona que prueba el prototipo |
| POUR | Los 4 principios de WCAG: Perceptible, Operable, Comprensible, Robusto |
| Plantilla de Torres Burriel | Formato para documentar una evaluación heurística |

## Cómo sigue

En la **semana 8** usarás estos hallazgos para **mejorar** tu prototipo: corregirás los más graves desde el sistema de diseño y harás un **A/B test** para decidir entre dos versiones.
