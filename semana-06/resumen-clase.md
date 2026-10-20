# Semana 6 — Comprendiendo un test heurístico
**Prototipos Navegables (DUD2204) · Experiencia 3**
**Clase sincrónica:** Miércoles 25 de noviembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana iniciamos la **Experiencia 3** aprendiendo cómo evaluar y mejorar nuestros diseños. Para medir la usabilidad y accesibilidad existen diversas herramientas y técnicas: pruebas con usuarios reales, análisis de datos, revisión de contenido, evaluación de accesibilidad y **evaluación heurística**.

La usabilidad y la accesibilidad son aspectos clave que deben trabajarse de manera constante — no solo al final del proceso de diseño.

> 💡 **Preguntas activadoras:** ¿Qué es un test heurístico? ¿Para qué sirve? ¿Cómo aplicar las 10 reglas heurísticas de Nielsen?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL6** | Aplica test heurístico en el diseño de interfaz, para evaluar la usabilidad y la experiencia del usuario en la navegación. |
| **IL7** | Implementa cambios a partir de los resultados del testeo para la mejora del diseño de interfaz. |

---

## Conceptos Clave de la Semana

`Test heurístico` · `Evaluación heurística` · `Usabilidad` · `Accesibilidad` · `Pautas de Accesibilidad` · `Mejoras de prototipos`

---

## Contenidos

### 1. Evaluación de Diseño de Sitios Web

La **evaluación de sitios web** es un proceso sistemático y objetivo para analizar y medir la calidad, usabilidad y efectividad de una interfaz. Métodos principales:

| Método | Descripción | Requiere usuarios |
|--------|-------------|:----------------:|
| **Evaluación Heurística** | Revisión experta con lista de principios | ❌ |
| **Pruebas de Usabilidad** | Observar usuarios reales completando tareas | ✅ |
| **Análisis de Métricas** | Datos de comportamiento (tiempo, tasa de rebote) | Indirecto |
| **Revisión de Contenido** | Calidad, relevancia, organización del contenido | ❌ |
| **Evaluación de Accesibilidad** | Cumplimiento WCAG 2.1 | ❌ |
| **Evaluación de SEO** | Estructura, metadatos, indexación | ❌ |

---

### 2. ¿Qué es la Evaluación Heurística?

Un **test heurístico** es una técnica de evaluación de usabilidad que identifica posibles problemas en el diseño de una interfaz mediante una revisión sistemática usando **heurísticas** (principios de usabilidad establecidos).

**Proceso del test heurístico:**
1. Un evaluador experto examina la interfaz
2. Busca violaciones a las heurísticas
3. Documenta cada problema encontrado
4. Asigna severidad a cada hallazgo
5. Propone soluciones

**¿Cuántos evaluadores se necesitan?**
- 1 evaluador detecta ≈35% de los problemas
- 3 evaluadores detectan ≈65%
- 5 evaluadores detectan ≈75%
- Nielsen recomienda **entre 3 y 5** evaluadores

---

### 3. Test Heurístico de Nielsen — Las 10 Reglas Aplicadas al Diseño de Interfaces

| # | Heurística | Cómo se aplica al diseño de interfaz |
|---|-----------|--------------------------------------|
| 1 | **Visibilidad del estado del sistema** | Feedback visual al hacer clic, indicadores de carga, estado del carrito |
| 2 | **Relación sistema/mundo real** | Usar "Comprar" no "Ejecutar transacción"; íconos reconocibles |
| 3 | **Control y libertad del usuario** | Botón "Deshacer", poder cancelar procesos |
| 4 | **Consistencia y estándares** | Mismos botones, misma paleta, mismo comportamiento en todas las páginas |
| 5 | **Prevención de errores** | Confirmar antes de eliminar, validar formularios en tiempo real |
| 6 | **Reconocer antes que recordar** | Imagen del producto en el carrito; mostrar el color seleccionado con su nombre |
| 7 | **Flexibilidad y eficiencia** | Filtros rápidos + búsqueda + categorías para distintos tipos de usuarios |
| 8 | **Diseño estético y minimalista** | Solo mostrar información relevante, sin elementos decorativos que compitan |
| 9 | **Ayudar a reconocer/recuperarse de errores** | Mensajes específicos: "Código de descuento expirado" (no "Error") |
| 10 | **Ayuda y documentación** | FAQ visible, chat de soporte accesible (no solo en el footer) |

---

### 4. Escala de Severidad de Nielsen

Al documentar hallazgos, se asigna severidad según:
- **Frecuencia:** ¿con qué frecuencia ocurre?
- **Impacto:** ¿qué tan difícil es para el usuario superarlo?
- **Persistencia:** ¿ocurre una vez o repetidamente?

| Nivel | Descripción | Prioridad de corrección |
|-------|-------------|------------------------|
| **0** | No es un problema de usabilidad | Ignorar |
| **1** | Cosmético | Solo si hay tiempo disponible |
| **2** | Menor | Baja prioridad |
| **3** | Mayor | Importante corregir antes del lanzamiento |
| **4** | Catastrófico | Debe corregirse **antes** de publicar |

---

### 5. Proceso de Evaluación Heurística

**Pasos:**

```
1. Definir alcance y tareas a evaluar
        ↓
2. Evaluación individual (cada evaluador de forma independiente)
        ↓
3. Registrar hallazgos (heurística, elemento, descripción, severidad, propuesta)
        ↓
4. Consolidar hallazgos de todos los evaluadores
        ↓
5. Priorizar por severidad
        ↓
6. Documentar propuestas de mejora
```

**Plantilla de registro de hallazgo:**
```
ID: [número]
Heurística vulnerada: [# y nombre]
Elemento: [componente o sección específica]
Descripción: [qué está mal y por qué]
Severidad: [0-4]
Propuesta: [cómo corregirlo]
```

---

## Actividad de la Semana

> 📝 **AF4: Utilizando las reglas de Nielsen para evaluar una interfaz** · Cuestionario en AVA

Lee y analiza una situación relacionada con una plataforma de cursos en línea (e-learning) y responde las preguntas sobre cómo se aplican las reglas heurísticas de Nielsen al diseño de esa plataforma.

- 📅 **Fecha límite:** Lunes 30 de noviembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Cuestionario directo en la plataforma AVA (sin archivo ZIP)

---

## Cierre de Semana

El test heurístico transforma la evaluación del diseño en un proceso sistemático y basado en evidencia. En lugar de "creo que está bien", ahora podemos decir "según el principio N°X de Nielsen, este elemento tiene un problema de severidad 3 y la solución es...". Esa es la diferencia entre un diseñador en formación y un profesional.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
