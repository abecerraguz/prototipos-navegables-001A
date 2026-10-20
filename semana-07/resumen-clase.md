# Semana 7 — Identificando elementos a evaluar con test heurístico y criterios de accesibilidad
**Prototipos Navegables (DUD2204) · Experiencia 3**
**Clase sincrónica:** Miércoles 2 de diciembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana aprendemos a crear una **lista de evaluación** para probar nuestros prototipos usando las 10 leyes heurísticas de Nielsen. Exploraremos cómo aplicar un **test guiado y uno no guiado**, usaremos la **plantilla Torres Burriel** y aprenderemos a seleccionar herramientas de testeo en Figma. También evaluaremos criterios de **accesibilidad** en nuestro prototipo y documentaremos los resultados.

> 💡 **Preguntas activadoras:** ¿Para qué sirve un test heurístico? ¿Cuáles son los elementos clave que debemos sumar a nuestro test? ¿Cuál es la pauta de accesibilidad que debemos seguir para testear el diseño?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL1** | Utiliza componentes para el diseño de una interfaz interactiva. |
| **IL2** | Utiliza elementos gráficos para la correcta composición de un diseño de interfaz. |
| **IL3** | Implementa una maqueta de interfaz responsiva para múltiples dispositivos. |
| **IL4** | Aplica guía de estilo, considerando criterios de accesibilidad y usabilidad. |
| **IL5** | Compone prototipo interactivo, considerando elementos de accesibilidad y usabilidad. |
| **IL6** | Aplica test heurístico en el diseño de interfaz, para evaluar la usabilidad y la experiencia del usuario. |
| **IL7** | Implementa cambios a partir de los resultados del testeo para la mejora del diseño de interfaz. |

---

## Conceptos Clave de la Semana

`Test heurístico` · `Test guiado` · `Test no guiado` · `Plantilla Torres Burriel` · `Criterios de accesibilidad` · `Documentación de resultados`

---

## Contenidos

### 1. Testeando el Diseño de Interfaz

Para evaluar un diseño creamos un **checklist** de elementos a revisar. Yusef Hassan (NoSoloUsabilidad) estableció criterios de evaluación clasificados en categorías:

**Criterios Generales:**
- ¿Los objetivos del sitio son concretos y bien definidos?
- ¿Los contenidos y servicios se corresponden con esos objetivos?
- ¿La estructura general está orientada al usuario?
- ¿El look & feel se corresponde con los objetivos del sitio?
- ¿Es coherente y reconocible el diseño general?

**Criterios de Identidad e Información:**
- ¿Se muestra claramente la identidad de la empresa en todas las páginas?
- ¿El logotipo es significativo, identificable y suficientemente visible?
- ¿Se proporcionan mecanismos de contacto?
- ¿Se informa sobre protección de datos?

**Criterios de Lenguaje y Redacción:**
- ¿Los textos son concisos y claros?
- ¿Se usa lenguaje cercano al usuario (no técnico)?

**Criterios de Rotulado:**
- ¿Los títulos y etiquetas son descriptivos y significativos?
- ¿Los rótulos son auto-evidentes para el usuario?

---

### 2. Test Guiado vs. Test No Guiado

| | Test Guiado | Test No Guiado |
|--|------------|----------------|
| **Descripción** | Se le da una tarea específica al evaluador | El evaluador navega libremente |
| **Ejemplo** | "Encuentra y compra un iPhone 16 Pro 256GB" | "Explora el sitio y dime qué encuentras" |
| **Detecta** | Problemas en flujos de tarea específicos | Problemas de descubrimiento y navegación general |
| **Ventaja** | Datos precisos sobre tareas concretas | Hallazgos inesperados, perspectiva fresca |
| **Recomendación** | Para evaluar flujos de compra | Para evaluar primera impresión y navegación |

> 🎯 Para una evaluación completa: combinar **ambos tipos** en la misma sesión.

---

### 3. Plantilla Test Heurístico de Torres Burriel

La plantilla de Torres Burriel es una herramienta estructurada para documentar la evaluación heurística de manera profesional.

**Estructura de la plantilla:**

```
DATOS DEL PROYECTO
  Nombre del proyecto:
  Evaluador/es:
  Fecha:
  Tareas evaluadas:
  URL / Prototipo:

RESUMEN EJECUTIVO
  Total de problemas por severidad:
    - Severidad 4 (Catastrófico): X
    - Severidad 3 (Mayor): X
    - Severidad 2 (Menor): X
    - Severidad 1 (Cosmético): X
  Top 3 problemas críticos:
    1. [Descripción breve]
    2. [Descripción breve]
    3. [Descripción breve]

HALLAZGOS DETALLADOS (tabla)
  ID | Heurística | Elemento | Descripción | Severidad | Propuesta

CONCLUSIONES
  Evaluación general:
  Próximos pasos:
```

---

### 4. Consideraciones al Diseñar y/o Testear

**Aspectos clave del prototipo a evaluar:**

| Aspecto | Qué revisar |
|---------|------------|
| **Navegación** | ¿Es intuitiva? ¿El usuario siempre sabe dónde está? |
| **Contenido** | ¿Es claro, conciso y orientado al usuario? |
| **Formularios** | ¿Tienen labels visibles? ¿Mensajes de error claros? |
| **Consistencia** | ¿Los mismos elementos se ven igual en todas las páginas? |
| **Feedback** | ¿El sistema responde visiblemente a las acciones del usuario? |
| **Accesibilidad** | ¿Contraste suficiente? ¿Alt text? ¿Área táctil mínima? |

---

### 5. Selección de Herramientas de Testeo en Figma

| Herramienta | Cómo usar | Para qué sirve |
|------------|-----------|---------------|
| **Prototype mode** | Activar en panel derecho | Navegar el prototipo como usuario real |
| **Figma Mirror** | App mobile + mismo WiFi | Ver el prototipo en dispositivo real en tiempo real |
| **Compartir enlace** | Share → Anyone with link → Can view | Testeo remoto con evaluadores externos |
| **Comments** | Ícono de burbuja en toolbar | Dejar notas sobre elementos específicos |
| **Maze.co** | Integración con Figma | Test remoto con métricas (click maps, tiempo de tarea) |

---

### 6. Aplicación de Criterios de Accesibilidad al Prototipo

Al evaluar el prototipo con criterios de accesibilidad, revisar:

**Perceptibilidad:**
- ¿Todas las imágenes tienen alt text anotado?
- ¿El contraste de texto cumple WCAG 2.1 AA (≥4.5:1 para texto normal)?
- ¿La información no se transmite SOLO por color?

**Operabilidad:**
- ¿Los elementos interactivos tienen área táctil ≥44×44px?
- ¿Los estados de foco están marcados en las anotaciones?
- ¿Hay suficiente tiempo para completar las tareas (no hay timeouts abruptos)?

**Comprensibilidad:**
- ¿El lenguaje es claro y sencillo?
- ¿Los mensajes de error son descriptivos y útiles?
- ¿La estructura de navegación es predecible?

**Robustez:**
- ¿Las anotaciones indican atributos ARIA necesarios?
- ¿Los formularios tienen labels correctamente asociados?

---

### 7. Documentación de Resultados

Una buena documentación del test debe incluir:
- **Descripción detallada** de cada elemento evaluado
- **Resultados del test heurístico** (todas las violaciones encontradas)
- **Resultados de criterios de accesibilidad** (qué cumple y qué no)
- **Propuestas de mejora** con especificidad (no solo "mejorar el contraste" — sino "cambiar el texto #6E6E73 a #4A4A4A sobre fondo blanco para cumplir 4.5:1")
- **Impacto esperado** de los cambios en usabilidad y accesibilidad

---

## Actividad de la Semana

> 📝 **AF5: Evaluando nuestro prototipo** · Cuestionario con plantilla descargable

Aplica las 10 heurísticas de Nielsen y los criterios de accesibilidad a tu proyecto de diseño de interfaz prototipado. Revisa cada página interior del prototipo (mínimo 5 páginas) y documenta tus hallazgos en la plantilla descargable desde AVA.

- 📅 **Fecha límite:** Lunes 7 de diciembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Descarga la plantilla desde AVA, complétala y sube el archivo
- ⚠️ Esta actividad tiene rúbrica

---

## Cierre de Semana

La plantilla Torres Burriel nos da un lenguaje común para hablar de problemas de usabilidad con el cliente y el equipo de desarrollo. "El botón no se ve bien" se convierte en "Heurística #8 (Diseño minimalista), severidad 2: el botón CTA compite visualmente con 3 otros botones en la misma vista. Propuesta: reducir a un solo CTA primario y hacer los demás secundarios."

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
