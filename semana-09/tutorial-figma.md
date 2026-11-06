# Tutorial Figma · Semana 9 — Maqueta final y capturas para la EFT
**Prototipos Navegables (DUD2204) · Evaluación Final Transversal · Clase del miércoles 16 de diciembre**

> 🧭 **Último tramo.** Este tutorial no introduce herramientas nuevas: te ayuda a **cerrar** tu archivo, aplicar el resultado del A/B test y sacar todas las capturas que pide el informe de la EFT, sin olvidar nada.
>
> 🔗 Resumen de la clase: [resumen-clase.md](resumen-clase.md) · Tutorial anterior: [semana 8](../semana-08/tutorial-figma.md) · Volver al [README](../README.md)

**Tiempo estimado:** 3 a 4 horas para la maqueta y las capturas. El informe va aparte.

## Qué vas a lograr

- Una **maqueta final** responsiva, ordenada y navegable.
- La **versión ganadora del A/B test** aplicada en móvil y escritorio.
- **Capturas** de cada etapa del bimestre, listas para el informe.
- Tu archivo **guardado y comprimido** para la entrega.

## Antes de comenzar

- [ ] Tu archivo `Apple Store — Proyecto PI` con las versiones `v1` y `v2` en el historial (semana 8).
- [ ] Los resultados de tu A/B test.
- [ ] La **rúbrica de la EFT**, descargada desde AVA. Léela antes de empezar.

---

## Paso 1 — Revisa qué debe tener la maqueta

Copia esta lista en un frame de tu archivo y ve marcándola:

| Elemento | Desktop 1440 | Mobile 375 |
| --- | :-: | :-: |
| Home (landing) actualizada | ☐ | ☐ |
| Ficha de producto | ☐ | ☐ |
| Carrito de compras | ☐ | ☐ |
| Check out | ☐ | ☐ |
| Flujos conectados y probados | ☐ | ☐ |
| Mejoras del A/B test aplicadas | ☐ | ☐ |
| Anotaciones de accesibilidad | ☐ | ☐ |
| Guía de estilos actualizada | ☐ | — |

---

## Paso 2 — Aplicar la versión ganadora del A/B test

**Meta:** que la decisión del A/B test quede en **toda** la maqueta, no solo en la página `🅰️🅱️ A/B test`.

### Haz esto

1. Revisa qué cambió entre A y B.
2. Si la ganadora cambia un **componente** (por ejemplo, el botón de compra queda fijo), hazlo en el componente principal o en la plantilla, para que llegue a todas las fichas.
3. Aplica el cambio también en la otra versión del sitio: si testeaste en móvil, piensa cómo se traduce a escritorio (o justifica por qué no aplica).
4. En la página `🅰️🅱️ A/B test`, agrega una etiqueta grande en la versión elegida: «✅ Versión aplicada en la maqueta final».

> **Error frecuente:** aplicar el cambio solo en la pantalla del test. La maqueta final debe ser **coherente**: la misma solución en todas las páginas donde corresponda.

---

## Paso 3 — Actualizar la guía de estilos

**Meta:** que la guía muestre el sistema **tal como quedó**, con las mejoras de la semana 8.

### Haz esto

1. Revisa que los colores corregidos aparezcan con su **nuevo** valor y contraste.
2. Agrega a la guía los estados nuevos de tus componentes (`Presionado`, `Foco`) y los patrones que creaste (toast, modal de confirmación).
3. Agrega un texto breve: «Cambios respecto de la v1» con una línea por cada mejora.

---

## Paso 4 — Ordenar el archivo

**Meta:** que quien abra tu archivo entienda todo sin preguntarte.

### Haz esto

1. Crea una página `📌 Portada` y déjala **primera**. Dentro, un frame de `1920 × 1080` con: nombre del proyecto, tu nombre, asignatura, fecha y una captura de la home. Clic derecho sobre el frame → **Establecer como miniatura / Set as thumbnail**.
2. Revisa el orden final de las páginas:

```
📌 Portada
🎨 Guía de estilos
🧩 Sistema de diseño
📱 Páginas · Mobile 375
💻 Páginas · Desktop 1440
🔍 Evaluación heurística
🧪 Test con usuarios
🅰️🅱️ A/B test
📝 Iteraciones
```

3. En las páginas de diseño, revisa que los frames tengan nombres claros (`Ficha iPhone Pro · Mobile`, no `Frame 238`).
4. Borra elementos sueltos o de prueba que ya no sirvan.

> **Tip:** en el panel de Capas, los nombres genéricos como «Frame 12» o «Rectangle 4» indican piezas que nadie nombró. Renombra al menos los frames de pantallas y secciones.

---

## Paso 5 — Revisar los flujos

**Meta:** flujos que funcionen en cada versión (recomendamos al menos **3**).

### Haz esto

1. Define tres recorridos con nombre claro, por ejemplo:
   - `Mobile · Compra` (home → ficha → carrito → check out)
   - `Mobile · Búsqueda` (home → búsqueda → ficha)
   - `Mobile · Soporte` (home → menú → soporte)
2. Crea los mismos tres en escritorio.
3. Recorre cada uno en **Presentar**. Revisa: ¿puedo volver siempre?, ¿el menú abre y cierra?, ¿el toast y la confirmación funcionan?
4. Copia el **enlace del prototipo** (**Compartir → Copiar enlace**, con acceso **Cualquier persona con el enlace · Puede ver**). Lo pondrás en el informe.

---

## Paso 6 — Revisión final de accesibilidad

Pasa rápido por cada página con esta lista:

- [ ] Contraste de todos los textos (mínimo 4,5:1; texto grande 3:1).
- [ ] Texto de cuerpo de 17 px, también en móvil.
- [ ] Botones, links y chips con área táctil de 44 × 44.
- [ ] Ninguna información solo por color.
- [ ] Alt de las imágenes y nombre accesible de los botones de ícono, en las anotaciones.
- [ ] Estado de foco definido en los componentes interactivos.

---

## Paso 7 — Capturas para el informe

**Meta:** una carpeta con todas las imágenes del informe, con nombres que digan qué son.

**Concepto: versiones anteriores.** Para mostrar cómo empezó tu diseño, puedes recuperar estados antiguos del archivo desde el **historial de versiones**.

### Haz esto — capturas de etapas anteriores

1. **Archivo → Mostrar historial de versiones.**
2. Busca la versión que quieres mostrar (por ejemplo, la de la semana 4 o la `v1` de la semana 8). Si no guardaste versiones con nombre, Figma igual guarda versiones automáticas por fecha.
3. Haz clic derecho sobre esa versión → **Duplicar / Duplicate**. Se crea un archivo nuevo con ese estado.
4. En ese archivo, selecciona las pantallas y exporta en **PNG 2x**.

### Haz esto — capturas de la maqueta final

5. En tu archivo actual, selecciona cada pantalla final y exporta en **PNG 2x**.
6. Usa nombres que sigan la estructura del informe:

| Sección del informe | Capturas sugeridas |
| --- | --- |
| Primera versión (S4 · AF3) | `01-v1-home-mobile.png`, `01-v1-home-desktop.png` |
| Diseño de páginas (S5 · AS2) | `02-sistema-atomos.png`, `02-carrito-mobile.png`, `02-ficha-desktop.png` |
| Proceso de iteración (S8 · AS3) | `03-iteracion-1-antes-despues.png`, `03-ab-test.png` |
| Evaluación de accesibilidad | `04-contraste-antes-despues.png`, `04-anotaciones.png` |
| Versión final | `05-final-home-mobile.png`, `05-final-ficha-desktop.png`… |

> **Tip:** para la portada del informe o para mostrar el flujo, exporta también la **página completa** de prototipo con las flechas: en **Prototipo**, las conexiones se ven al seleccionar los frames. Una captura de pantalla de tu computador sirve para eso.

---

## Paso 8 — Guardar y entregar

1. **Archivo → Guardar en el historial de versiones** → `Versión final EFT`.
2. **Archivo → Guardar copia local** → se descarga el `.fig`.
3. Comprime el `.fig` en un ZIP y nómbralo como indique la rúbrica.
4. Pega el **enlace de revisión** del diseño en el documento del enunciado, donde dice «ingresa aquí la URL». Inclúyelo también en el informe.
5. Sube el **ZIP**, el **documento con el enlace** y el **informe** a AVA antes del **domingo 20 de diciembre a las 23:59**.

## Checklist final

- [ ] Versión ganadora del A/B test aplicada en toda la maqueta.
- [ ] Guía de estilos actualizada.
- [ ] Páginas ordenadas, con portada y miniatura.
- [ ] Flujos probados en cada versión (recomendado: al menos 3).
- [ ] Revisión final de accesibilidad hecha.
- [ ] Capturas exportadas y nombradas por sección del informe.
- [ ] Versión final guardada, `.fig` en ZIP y enlace del prototipo en el informe.

---

## Mira todo lo que hiciste

| Semana | Lo que aprendiste en Figma |
| --- | --- |
| 1 | Variables, Auto Layout, componentes, variantes e instancias |
| 2 | Estilos de texto, guía de estilos, Navbar, Footer, Desplazarse a |
| 3 | Frames móviles, fold, áreas táctiles, Cambiar a, desbordamiento, posición fija |
| 4 | Guías de columnas, Mobile First, acordeón, overlay, flujos por dispositivo |
| 5 | Atomic Design, propiedades de componente, plantillas, Navegar a y Atrás |
| 6 | Fichas de hallazgo, comentarios, priorización |
| 7 | Flujos por tarea, compartir prototipo, test con usuarios, accesibilidad |
| 8 | Historial de versiones, estados Presionado y Foco, toast, modal, A/B test |
| 9 | Archivo final, capturas por etapa y entrega |

Empezaste con un botón y terminas con un prototipo completo, navegable, responsivo, accesible y evaluado. ¡Mucho éxito en la EFT!
