# Semana 2 — Aplicando interacción a un landing page
**Prototipos Navegables (DUD2204) · Experiencia 1**
**Clase sincrónica:** Miércoles 28 de octubre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana creamos el primer prototipo navegable aplicando **diseño de interacción** a un landing page. El diseño de interacción se refiere al proceso de crear interacciones significativas y efectivas entre los usuarios y un sistema digital. Se centra en cómo los usuarios interactúan con la interfaz y cómo el sistema **responde** a esas interacciones.

Para realizar nuestro prototipo navegable retomamos las guías de estilo, ahora construidas directamente desde el software de prototipado mediante el uso de **componentes**.

> 💡 **Preguntas activadoras:** ¿Sabías que puedes agregar interacción a tu documento? ¿Qué tipo de interacciones conoces?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL1** | Utiliza componentes para el diseño de una interfaz interactiva, de acuerdo a la experiencia de usuario y requerimientos del proyecto. |
| **IL2** | Utiliza elementos gráficos para la correcta composición de un diseño de interfaz, aplicando interacciones y considerando elementos de accesibilidad y usabilidad. |
| **IL3** | Implementa una maqueta de interfaz responsiva para múltiples dispositivos, según los requerimientos del proyecto. |
| **IL4** | Aplica guía de estilo, considerando criterios de accesibilidad y usabilidad. |

---

## Conceptos Clave de la Semana

`Interacción` · `Guía de estilos` · `Landing page` · `Microinteracciones` · `Navegación por anclas` · `Prototipo navegable`

---

## Contenidos

### 1. ¿Qué es el Diseño de Interacción?

El diseño de interacción crea y define cómo los usuarios interactúan con una interfaz digital. Su objetivo es crear una experiencia **intuitiva, eficiente y satisfactoria**. Se basa en:
- Usabilidad y accesibilidad
- Retroalimentación visual
- Estructura de la información
- Respuesta del sistema a las acciones del usuario

**Al definir la interacción en un prototipo se considera:**

| Aspecto | Descripción |
|---------|-------------|
| **Objetivos de interacción** | ¿Qué acción o resultado se espera de cada elemento? |
| **Flujos de usuario** | ¿Cómo navegará el usuario entre elementos y pantallas? |
| **Estado de los elementos** | ¿Cómo cambia visualmente un elemento antes/durante/después de la interacción? |
| **Transiciones y animaciones** | ¿Cómo se realizan los cambios entre pantallas o estados? |
| **Herramientas de prototipado** | Figma, InVision, Proto.io |

---

### 2. Diseño de Prototipo — Guía de Estilos

La guía de estilos construida con componentes en Figma garantiza la **coherencia visual** en todo el prototipo. Sus elementos básicos son:

**Colores:**
- Definir paleta completa con variables de color en Figma
- Incluir: primario, secundario, acento, texto, fondo, estados (error, éxito, alerta)
- Verificar contraste de cada combinación (WebAIM Contrast Checker)

**Tipografía:**
- Definir familias tipográficas (máximo 2)
- Establecer escala: H1, H2, H3, H4, body, label, caption
- Definir tamaños mínimos respetando WCAG (≥16px para body)

**Espaciado:**
- Sistema de espaciado en múltiplos de 8px (8, 16, 24, 32, 48, 64, 80...)
- Padding y márgenes consistentes

**Componentes base:**
- Botones (primario, secundario, fantasma, disabled)
- Campos de formulario (normal, enfocado, error, correcto)
- Cards y contenedores
- Iconografía

**¿Cómo construir la guía de estilos en Figma?**
1. Crear una página dedicada "Guía de Estilos" en el archivo
2. Definir colores como Styles (panel Colores → + nuevo estilo)
3. Definir tipografías como Text Styles
4. Crear los componentes base con variantes (estados: normal, hover, active, disabled)
5. Organizar en secciones: Colores / Tipografía / Componentes / Íconos

---

### 3. Diseño de Interacción en Figma

**Tipos de interacción disponibles en Figma:**

| Trigger | Descripción | Uso típico |
|---------|-------------|-----------|
| On Click | Al hacer clic | Botones, links, menús |
| Mouse Enter | Al entrar el cursor | Hover states de botones y cards |
| Mouse Leave | Al salir el cursor | Restaurar estado normal |
| On Drag | Al arrastrar | Sliders, carruseles |
| Key Down | Al presionar tecla | Atajos de teclado |
| On Hover | Estado de hover | Efectos visuales de feedback |

**Tipos de animación:**
- **Instant:** cambio inmediato, sin transición
- **Dissolve:** fundido entre estados
- **Smart Animate:** Figma interpola automáticamente entre estados similares
- **Move In/Out/Slide:** el elemento entra/sale desde un borde
- **Push:** el elemento nuevo "empuja" al anterior

**Duración recomendada:** 200–400ms para la mayoría de las transiciones. 300ms es el punto dulce.

---

### 4. Navegación por Anclas en el Prototipo

La **navegación por anclas** permite ir de un punto a otro de la misma página sin navegar a una nueva pantalla — el equivalente al `scroll to` del código.

**Cómo crear navegación por anclas en Figma:**
1. Seleccionar el elemento trigger (ej. link "Productos" en el navbar)
2. En el panel Prototype: arrastrar el conector al artboard o sección de destino
3. En Action: seleccionar **Scroll To** (no Navigate To)
4. Elegir la animación y duración

> 🔑 **Diferencia clave:** `Navigate To` lleva a un artboard diferente. `Scroll To` hace scroll dentro del mismo artboard — esto es la navegación por anclas.

---

### 5. La Actividad Sumativa AS1 — Landing Page

**Entregable AS1 — componentes requeridos:**
Los elementos que **deben** construirse como componentes:
- **Header:** logo + navegación
- **Nav:** barra de navegación con links
- **Footer:** información de contacto + redes + links

**Indicaciones de accesibilidad:** agregarlas como anotaciones o comentarios dentro del propio diseño en Figma. Incluir:
- Alt text de todas las imágenes
- Ratios de contraste verificados
- Áreas táctiles mínimas (44×44px)
- Indicadores de foco para navegación por teclado

---

## Actividad de la Semana

> 📁 **AS1: Creando componentes en un landing page** · Actividad (ZIP)

Crea un landing page usando componentes y proporciona las indicaciones de accesibilidad necesarias para que sea responsivo y se adapte a diferentes tamaños de pantalla y dispositivos.

- 📅 **Fecha límite:** Lunes 2 de noviembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Archivo ZIP con nomenclatura `PN_S2_NombreApellido.zip`
- ⚠️ Esta actividad es **sumativa** — revisar la rúbrica

---

## Cierre de Semana

Con la AS1 cerramos la Experiencia 1. El primer prototipo navegable ya existe: tiene componentes reutilizables, una guía de estilos aplicada, interacciones de hover y navegación por anclas. Este es el punto de partida sobre el que construiremos las próximas experiencias.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
