# Semana 5 — Diseñando una interfaz con sistemas de diseño
**Prototipos Navegables (DUD2204) · Experiencia 2**
**Clase sincrónica:** Miércoles 18 de noviembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana aprendemos sobre los elementos fundamentales para iniciar un diseño de interfaz y las metodologías que permiten construir prototipos escalables y coherentes. Exploramos cómo iniciar un proyecto de interfaz con una **arquitectura sólida**, la metodología **Mobile First**, los **sistemas de diseño** y el **Atomic Design**.

> 💡 **Preguntas activadoras:** ¿Qué elementos debemos tener en cuenta para iniciar un diseño de interfaz? ¿Qué metodologías para diseñar conoces? ¿Cuál es la importancia de los sistemas de diseño?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL1** | Utiliza componentes para el diseño de una interfaz interactiva, de acuerdo a la experiencia de usuario y requerimientos del proyecto. |
| **IL2** | Utiliza elementos gráficos para la correcta composición de un diseño de interfaz, aplicando interacciones y considerando elementos de accesibilidad y usabilidad. |
| **IL3** | Implementa una maqueta de interfaz responsiva para múltiples dispositivos, según los requerimientos del proyecto. |
| **IL4** | Aplica guía de estilo, considerando criterios de accesibilidad y usabilidad. |
| **IL5** | Compone prototipo interactivo, considerando elementos de accesibilidad y usabilidad. |

---

## Conceptos Clave de la Semana

`Mobile First` · `Sistemas de diseño` · `Atomic Design` · `Átomos` · `Moléculas` · `Organismos` · `Plantillas` · `Páginas`

---

## Contenidos

### 1. ¿Cómo iniciar un proyecto de interfaz?

Antes de comenzar a diseñar se debe contar con la **arquitectura del proyecto**:

```
✅ Diagrama de flujos (flujo de usuario)
✅ Arquitectura de la información (mapa de navegación)
✅ Wireframes de baja fidelidad
✅ Inventario de contenido
✅ Componentes definidos (Semana 1-2)
✅ Guía de estilo (colores, tipografía, espaciado)
```

**Elementos esenciales para diseño responsivo:**
- Tamaños tipográficos acordes a WCAG 2.1
- Resoluciones de pantalla definidas (breakpoints)
- Criterios de accesibilidad establecidos

---

### 2. Mobile First: ¿Qué es y para qué sirve?

**Mobile First** es una metodología donde se diseña primero para dispositivos móviles y luego se escala progresivamente a resoluciones mayores.

**¿Por qué Mobile First?**
- Prioriza el contenido esencial (la pantalla pequeña obliga a eliminar lo innecesario)
- Según NN Group, ocultar la navegación bajo menú hamburguesa disminuye el uso en desktop — diseñar para móvil primero evita llevar malas prácticas a desktop
- El mismo contenido y funcionalidad presentes en todas las pantallas, reorganizado según el espacio

**Proceso Mobile First:**
```
Diseño Mobile (375px) → Tablet (768px) → Desktop (1280px) → Desktop Large (1440px)
```

---

### 3. Sistemas de Diseño

Un **sistema de diseño** es un conjunto de normas, componentes y patrones reutilizables destinados a gestionar el diseño a escala. Incluye:

- Principios de diseño y valores de marca
- Guía de estilos (colores, tipografía, espaciado, íconos)
- Biblioteca de componentes
- Documentación de patrones y comportamientos
- Guías de accesibilidad

**Ventajas de un sistema de diseño:**
- Coherencia visual en todo el producto
- Velocidad de desarrollo (no se reinventa la rueda)
- Colaboración eficiente entre diseñadores y desarrolladores
- Escalabilidad del producto

**Ejemplos de sistemas de diseño reales:**
- Apple Human Interface Guidelines (HIG)
- Google Material Design
- IBM Carbon Design System

---

### 4. Metodología Atomic Design

Brad Frost propuso en 2013 una metodología que compara el diseño con la química. Toda interfaz se construye desde elementos mínimos hasta composiciones completas:

```
Átomos → Moléculas → Organismos → Plantillas → Páginas
```

#### Átomos
Los elementos más básicos e indivisibles de la interfaz.

```
Ejemplos: botón, input de texto, label, ícono, imagen, 
color, tipografía, badge, separador, tooltip
```

Cada átomo es un **componente** en Figma con sus variantes (estados: normal, hover, active, disabled, error).

---

#### Moléculas
Grupos simples de átomos que funcionan juntos como una unidad.

```
Ejemplos:
- Campo de búsqueda = input + botón buscar
- Combo precio-CTA = precio + botón comprar
- Rating = estrellas + número de reseñas
- Breadcrumb = link > link > texto activo
- Chip de filtro = ícono + etiqueta + botón cerrar
```

---

#### Organismos
Componentes más complejos formados por moléculas y/o átomos.

```
Ejemplos:
- Card de producto = imagen + badge + nombre + precio + botón
- Header = logo + navegación + carrito + búsqueda
- Barra de filtros = múltiples chips + dropdown "Ordenar"
- Hero section = imagen + título + subtítulo + CTA
- Footer = logo + columnas de links + redes sociales
```

---

#### Plantillas
La disposición de organismos que define la estructura de una página, sin contenido real.

```
Ejemplos:
- Template Catálogo: navbar + breadcrumb + filtros + grid + footer
- Template Ficha: navbar + breadcrumb + 2 columnas + relacionados + footer
- Template Checkout: navbar + formulario + resumen + footer
```

---

#### Páginas
Instancias específicas de las plantillas con contenido real.

```
Template Catálogo → Catálogo iPhone 16 (con datos reales: imágenes, precios, nombres)
Template Ficha   → iPhone 16 Pro, 256GB, Negro Volcán, $1.199.990
```

---

### 5. Aplicando Atomic Design en Figma

**Organización recomendada del archivo Figma:**

```
📄 Página: 🧩 Sistema de Diseño
  Sección: Átomos
    - Botones (variantes: tipo × estado)
    - Inputs (variantes: tipo × estado)
    - Badges, chips, íconos
  
  Sección: Moléculas
    - Combo precio-CTA
    - Campo de búsqueda
    - Rating + reseñas
  
  Sección: Organismos
    - Card de producto
    - Header (desktop + mobile)
    - Footer
    - Barra de filtros

📄 Página: 📋 Plantillas
  - Template Catálogo
  - Template Ficha
  - Template Carrito

📄 Página: 📱 Páginas Mobile 375px
  - Catálogo iPhone
  - Ficha Producto

📄 Página: 💻 Páginas Desktop 1440px
  - Catálogo iPhone
  - Ficha Producto
```

---

## Actividad de la Semana

> 📁 **AS2: Diseñando las páginas interiores del prototipo** · Actividad (ZIP)

Continúa trabajando con el diseño de interfaz responsiva de la semana anterior. Diseña todas las páginas interiores que requiere el prototipo aplicando **Mobile First** y **Atomic Design**.

- 📅 **Fecha límite:** Lunes 23 de noviembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Archivo ZIP con nomenclatura `PN_S5_NombreApellido.zip`
- ⚠️ Esta actividad es **sumativa** — revisar la rúbrica

---

## Cierre de Semana

Con el Atomic Design y los sistemas de diseño, el prototipo deja de ser una colección de pantallas y se convierte en un sistema coherente. Cada cambio en un átomo se propaga a todas las páginas automáticamente — eso es lo que hace que los sistemas de diseño sean tan poderosos a escala.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
