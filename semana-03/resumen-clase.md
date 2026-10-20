# Semana 3 — Reconociendo patrones de interacción en dispositivos móviles
**Prototipos Navegables (DUD2204) · Experiencia 2**
**Clase sincrónica:** Miércoles 4 de noviembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana iniciamos la **Experiencia 2** aprendiendo los distintos patrones y gestos en el diseño de interacción para dispositivos móviles. El concepto central es el **Fold**: término heredado de los diarios impresos, donde el contenido "bajo el pliegue" no era visible hasta abrir el diario. En web móvil, el Fold es el límite de lo visible sin hacer scroll.

> 💡 **Preguntas activadoras:** ¿Conoces las interacciones en móviles? ¿Cuáles son los patrones de diseño más utilizados? ¿Cuáles son las resoluciones más utilizadas en diseño de interfaz?

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

`Fold` · `Patrones de interacción` · `Resolución de pantalla` · `Desplazamientos vertical y horizontal` · `Patrones de diseño` · `Pruebas de usabilidad móvil`

---

## Contenidos

### 1. Patrones de Interacción en Dispositivos Móviles

La interacción táctil es distinta al mouse: el pulgar mide entre 7 y 10mm, lo que obliga a diseñar elementos más grandes y en zonas de alcance cómodo.

**Consideraciones fundamentales:**
- **Tamaño de elementos interactivos:** mínimo **44×44px** (Apple HIG + WCAG)
- **Retroalimentación táctil (Feedback):** efectos visuales al tocar (cambio de color, animación)
- **Navegación intuitiva:** patrones conocidos (navbar inferior, hamburguesa)
- **Gestos táctiles:** coherentes y significativos
- **Animaciones suaves:** 200–400ms para transiciones entre estados

---

### 2. Gestos Táctiles Principales

| Gesto | Descripción | Ejemplo de uso |
|-------|-------------|---------------|
| **Tap** | Toque simple | Botones, links, cards — el más accesible |
| **Swipe horizontal** | Deslizar izquierda/derecha | Carruseles, galería de imágenes |
| **Scroll vertical** | Deslizar arriba/abajo | Navegación por contenido |
| **Pulsación larga** | Mantener presionado | Menú contextual, selección múltiple |
| **Doble tap** | Dos toques rápidos | Zoom, "me gusta" (conflicto con zoom del sistema) |
| **Pellizco (pinch)** | Acercar/alejar con dos dedos | Zoom en mapas e imágenes |
| **Deslizar (swipe en elemento)** | Arrastrar elemento | Eliminar, archivar (patrón iOS) |
| **Magnificar/Reducir/Girar** | Gestos multitouch | Galería de fotos, mapas |

---

### 3. El Concepto Fold y el Contenido Visual

**¿Qué es el Fold?**
En una página web, el Fold es la línea imaginaria que separa el contenido visible sin hacer scroll del contenido que requiere desplazamiento.

- **Sobre el fold:** lo que el usuario ve inmediatamente al cargar la página
- **Bajo el fold:** requiere scroll para verse

**¿Qué debe ir sobre el fold en un ecommerce móvil?**
- El producto/propuesta de valor principal (hero)
- El título y precio
- El botón de acción principal (CTA)
- Indicadores de que hay más contenido (imagen ligeramente cortada, puntos de paginación)

---

### 4. Patrones de Diseño para Móvil

| Patrón | Descripción | Cuándo usar |
|--------|-------------|------------|
| **Hamburguesa** | Ícono ≡ que despliega el menú | Navegación secundaria en móvil |
| **Bottom navigation** | Tabs fijos en la parte inferior | Cuando hay 3-5 secciones principales |
| **Card con swipe** | Tarjetas que se deslizan | Galería de productos, contenidos relacionados |
| **Full-width button** | Botón a todo el ancho | CTA principal en pantallas pequeñas |
| **Sticky CTA** | Botón fijo al scrollear | "Comprar", "Agregar al carrito" en ficha de producto |
| **Pull to refresh** | Deslizar hacia abajo para recargar | Listas de contenido dinámico |
| **Infinite scroll** | Carga automática al llegar al final | Catálogos, feeds de contenido |

---

### 5. Formas de Sostener el Dispositivo

| Forma | Implicación para el diseño |
|-------|--------------------------|
| **Una mano (pulgar)** | Zona inferior central es la más accesible (zona "verde") |
| **Dos manos (pulgares)** | Zonas inferiores de ambos lados accesibles |
| **Cuna + índice** | Toda la pantalla accesible |

> 🎯 Los elementos de acción críticos (CTA principal) deben estar en la **zona de fácil alcance del pulgar**: parte inferior central de la pantalla.

---

### 6. Limitaciones Técnicas — Resoluciones de Pantalla

| Dispositivo | Resolución física | Points en Figma |
|-------------|-----------------|----------------|
| iPhone SE (3ª gen) | 750×1334 | 375×667 |
| iPhone 14 | 1170×2532 | 390×844 |
| iPhone 14 Pro | 1179×2556 | 393×852 |
| iPhone 14 Pro Max | 1284×2778 | 428×926 |
| Samsung Galaxy S22 | 1080×2340 | 360×780 |
| iPad (10ª gen) | 1640×2360 | 820×1180 |

> ⚠️ En Figma siempre se trabaja en **points** (no píxeles físicos). El sistema retina/super-retina multiplica automáticamente la resolución al exportar.

---

### 7. Pruebas de Usabilidad en Móviles

**¿Por qué es importante probar específicamente en móvil?**
- Las interacciones táctiles son distintas al mouse
- El contexto de uso es diferente (movilidad, luz solar, una mano ocupada)
- La resolución y tamaño de pantalla limitan el contenido visible

**Cómo probar el prototipo móvil en Figma:**
1. **Figma Mirror** (app mobile): ver el prototipo en el dispositivo real en tiempo real
2. **Prototype preview** con DeviceFrame activado en Figma
3. **Compartir enlace** del prototipo para que el tester lo pruebe en su celular

---

## Actividad de la Semana

> 📝 **AF2: Reconociendo patrones de interacción en dispositivos móviles** · Cuestionario en AVA

Identifica los patrones de interacción para interfaces móviles, reconoce las resoluciones para diseño responsivo y planifica el uso de los patrones de interacción en los componentes diseñados.

- 📅 **Fecha límite:** Lunes 9 de noviembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Cuestionario directo en la plataforma AVA (sin archivo ZIP)

---

## Cierre de Semana

Los patrones de interacción móvil no son convenciones arbitrarias — responden a cómo los usuarios sostienen y operan físicamente sus teléfonos. Diseñar ignorando estos patrones genera fricción y abandono. El conocimiento de breakpoints, resoluciones y zonas de alcance es la base técnica sobre la que construiremos la interfaz responsiva de las próximas semanas.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
