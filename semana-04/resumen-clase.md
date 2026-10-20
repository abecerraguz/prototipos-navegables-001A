# Semana 4 — Diseñando una interfaz responsiva
**Prototipos Navegables (DUD2204) · Experiencia 2**
**Clase sincrónica:** Miércoles 11 de noviembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana aprendemos a usar los flujos de mesas de trabajo en Figma, las interacciones necesarias y los componentes para diseñar interfaces responsivas. Según datos del INE de Chile (2022), el número de teléfonos móviles asciende a **33.437.286** — más de uno por persona. Con el creciente uso de dispositivos móviles, el diseño responsivo se vuelve esencial.

> 💡 **Preguntas activadoras:** ¿Puedo probar mi prototipo en un móvil? ¿Cuáles son las resoluciones para diseñar en móvil? ¿Cuántas columnas se ocupan en una mesa de trabajo móvil? ¿Qué tamaño de texto debo ocupar en diseño de interfaz móvil?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL1** | Utiliza componentes para el diseño de una interfaz interactiva, de acuerdo a la experiencia de usuario y requerimientos del proyecto. |
| **IL2** | Utiliza elementos gráficos para la correcta composición de un diseño de interfaz, aplicando interacciones y considerando elementos de accesibilidad y usabilidad. |
| **IL3** | Aplica guía de estilo, considerando criterios de accesibilidad y usabilidad. |
| **IL4** | Compone prototipo interactivo, considerando elementos de accesibilidad y usabilidad. |
| **IL5** | Implementa una maqueta de interfaz responsiva para múltiples dispositivos, según los requerimientos del proyecto. |

---

## Conceptos Clave de la Semana

`Vista previa` · `Componentes interactivos` · `Accesibilidad` · `Breakpoints` · `Columnas` · `Resolución` · `Flujos entre mesas de trabajo`

---

## Contenidos

### 1. Diseñar una Interfaz Responsiva en Figma

Al diseñar una interfaz responsiva es necesario:
- Tener claras las **mesas de trabajo** (artboards) para móvil, tablet y desktop
- Partir de la resolución mínima (Mobile First)
- Adaptar el proyecto a distintas resoluciones con coherencia visual

**Mesas de trabajo recomendadas (breakpoints principales):**

| Dispositivo | Ancho artboard Figma |
|-------------|---------------------|
| Mobile S | 375px |
| Mobile L | 428px |
| Tablet portrait | 768px |
| Tablet landscape | 1024px |
| Desktop estándar | 1280px |
| Desktop grande | 1440px |

---

### 2. Flujo entre Mesas de Trabajo en Figma

Cuando trabajamos en un proyecto de diseño de interfaz, es importante comprender los **flujos de interacción entre las mesas de trabajo** para crear una navegación coherente entre pantallas.

**Cómo crear flujos en Figma:**

1. En el modo Prototype, cada clic sobre un elemento de la mesa de trabajo genera un **manejador** (handler) de flujo.
2. Al arrastrar el manejador hacia otra mesa de trabajo, se activa el **panel de interacción**.
3. El panel de interacciones contiene:
   - **Trigger:** el disparador (On Click, Hover, Mouse Enter, etc.)
   - **Action:** la acción (Navigate To, Scroll To, Overlay, etc.)
   - **Destination:** el destino (artboard de destino)
   - **Animation:** el tipo y duración de la animación

4. Se pueden tener múltiples manejadores: uno desde la mesa de trabajo y otro desde los objetos dentro de ella.

> 🔑 **Buena práctica:** crear **Flows** separados para Mobile y Desktop. Al presentar, se puede cambiar entre flows para mostrar ambas versiones del prototipo.

---

### 3. Aspectos Gráficos — Tipografía Accesible

#### Tamaños tipográficos mínimos (WCAG 2.1)

| Elemento | Desktop | Tablet | Mobile | Mínimo WCAG |
|----------|---------|--------|--------|------------|
| H1 | 72px | 56px | 40px | — |
| H2 | 48px | 40px | 32px | — |
| H3 | 28px | 24px | 21px | — |
| Body | 17px | 17px | **17px** | 16px |
| Small | 15px | 15px | 13px | — |
| Label | 12px | 12px | 11px | — |

> ⚠️ **El cuerpo de texto NO se reduce en móvil.** WCAG 2.1 establece mínimo 16px para texto de cuerpo. Apple HIG recomienda 17px. Reducir a 12px genera problemas de legibilidad.

#### Propiedades de espaciado e interlineado

**Espaciado entre letras (tracking):**
- No comprimir el tracking — genera pérdida de legibilidad
- Se puede ampliar levemente en móvil para mayor claridad

**Interlineado (line-height):**
- WCAG 2.1 recomienda mínimo **1.5× el tamaño de fuente**
- Para 17px de cuerpo: interlineado mínimo = **25.5px** (en práctica, usar 28px)
- Para títulos grandes: 1.1×–1.2× es suficiente

---

### 4. Breakpoints — Tamaños de Pantalla

Los breakpoints definen los puntos donde el diseño cambia para adaptarse a distintos dispositivos:

```
Mobile First: diseñar desde 375px y escalar hacia arriba

375px  → Mobile Small (base)
428px  → Mobile Large
768px  → Tablet portrait
1024px → Tablet landscape
1280px → Desktop
1440px → Desktop large
```

**Columnas por breakpoint (sistema estándar):**
- Mobile: **4 columnas**
- Tablet: **8 columnas**
- Desktop: **12 columnas**

---

### 5. Interacciones Móviles en el Prototipo

Las interacciones para móvil se configuran igual que en desktop, pero usando triggers táctiles:

| Interacción | Trigger en Figma | Uso en prototipo |
|-------------|-----------------|-----------------|
| Tap → navegar | On Click | Navegar entre páginas |
| Swipe → siguiente | On Drag (right/left) | Carrusel de imágenes |
| Scroll → sección | Scroll To | Navegación por anclas |
| Tap → drawer | On Click → Overlay | Menú hamburguesa |
| Long press → opciones | After Delay | Menú contextual |

---

### 6. Visualización y Preview del Prototipo en Figma

**Para previsualizar el prototipo en dispositivo:**
1. En Figma, activar modo Prototype
2. En la barra lateral derecha, seleccionar el tipo de dispositivo (iPhone 14, Samsung, iPad...)
3. Activar **Figma Mirror** en el celular real para ver en tiempo real
4. Compartir el link del prototipo para testeo remoto

---

## Actividad de la Semana

> 📁 **AF3: Creando una landing page interactiva y responsiva** · Actividad (ZIP)

Crea un prototipo interactivo para dispositivos móviles, considerando requerimientos del proyecto, experiencia del usuario y elementos de accesibilidad y usabilidad. Diseña una interfaz responsiva, aplica gestos táctiles como interacciones y crea una guía de estilo con criterios de accesibilidad.

- 📅 **Fecha límite:** Lunes 16 de noviembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Archivo ZIP con nomenclatura `PN_S4_NombreApellido.zip`
- ⚠️ Esta actividad es **formativa** — tiene rúbrica de retroalimentación

---

## Cierre de Semana

El diseño responsivo no es adaptar el desktop para que "quepa" en el celular — es diseñar con Mobile First, desde la resolución mínima hacia arriba. Los flujos entre mesas de trabajo en Figma nos permiten mostrar al cliente y al equipo de desarrollo exactamente cómo se verá el sitio en cada dispositivo, con interacciones reales.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
