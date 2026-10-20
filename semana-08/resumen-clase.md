# Semana 8 — Importancia de la iteración y mejora en un diseño de interfaz
**Prototipos Navegables (DUD2204) · Experiencia 3**
**Clase sincrónica:** Miércoles 9 de diciembre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Esta semana aprendemos a aplicar las mejoras encontradas en el test heurístico. Descubriremos cómo identificar áreas de mejora en nuestros diseños, implementar soluciones efectivas para optimizar la usabilidad y la experiencia del usuario, y entenderemos qué es la **iteración** y cuándo aplicarla. También aprenderemos a aplicar mejoras de **accesibilidad** de manera sistemática.

> 💡 **Preguntas activadoras:** ¿Qué es iterar? ¿Cómo sé cuándo iterar? ¿Cómo aplico las mejoras del test heurístico a mi prototipo?

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

`Iteración` · `Mejoras del prototipo` · `Accesibilidad` · `A/B Testing` · `Proceso de iteración` · `Evaluación continua`

---

## Contenidos

### 1. Aplicar las Mejoras a partir del Test Heurístico

El proceso de mejora tiene tres fases:

**Fase 1 — Análisis:**
- Revisar todos los hallazgos documentados en la AF5
- Priorizar por severidad (críticos primero: severidad 3 y 4)
- Agrupar hallazgos relacionados que puedan resolverse juntos

**Fase 2 — Propuesta de solución:**
- Para cada hallazgo prioritario, proponer una solución específica
- La solución debe ser directamente trazable al problema detectado
- Documentar el "por qué" de cada cambio (qué heurística o criterio resuelve)

**Fase 3 — Implementación:**
- Aplicar los cambios en Figma
- Documentar el "antes y después" con capturas
- Verificar que la solución realmente resuelve el problema original

---

### 2. ¿Qué es una Iteración?

Una **iteración** es un ciclo de mejora continua del diseño basado en **evidencia** — resultados de tests, feedback de usuarios o datos de uso.

> 🔑 **Diferencia clave:** Un rediseño dice "no me gusta, lo hago de nuevo". Una iteración dice "encontré evidencia de que esto no funciona — lo corrijo específicamente".

**Una iteración es:**
- Quirúrgica: toca solo lo que debe cambiar
- Basada en evidencia: cada cambio responde a un hallazgo documentado
- Trazable: se puede rastrear qué problema resuelve
- Medible: se puede verificar si la solución funcionó

**Una iteración NO es:**
- Rediseñar desde cero por preferencias estéticas
- Cambios sin justificación en el test heurístico
- Modificar lo que funciona bien

---

### 3. ¿Cuándo Iterar?

**Iterar cuando:**
- Los datos del test muestran que los usuarios no pueden completar una tarea
- Un hallazgo tiene severidad 3 o 4
- El cliente da feedback específico después de ver el prototipo
- Los indicadores de uso muestran abandono en un punto específico del flujo

**No iterar cuando:**
- Solo hay preferencias estéticas sin datos que las respalden
- El cambio propuesto no tiene origen en un problema documentado
- Los recursos no son proporcionales al impacto del cambio

**Proceso de iteración:**
```
Analizar hallazgos → Priorizar por severidad → Proponer solución
        ↓
Implementar en Figma → Documentar antes/después → Validar
```

---

### 4. ¿Cómo Aplicar Mejoras de Accesibilidad?

Las mejoras de accesibilidad identificadas en el test se aplican actualizando los **componentes** en la biblioteca de Figma, lo que propaga el cambio automáticamente a todas las instancias.

**Mejoras comunes de accesibilidad y cómo implementarlas en Figma:**

| Problema | Solución en Figma |
|---------|------------------|
| Contraste insuficiente | Actualizar el color del átomo "Texto secundario" en la biblioteca |
| Área táctil pequeña | Redimensionar el componente de botón a mínimo 44×44px |
| Sin feedback al hacer clic | Agregar variante "Active" al componente botón con animación Smart Animate |
| Sin indicador de foco | Agregar variante "Focus" con borde de 3px azul al componente |
| Solo color como indicador | Agregar ícono o texto como indicador adicional |
| Sin alt text documentado | Actualizar las anotaciones de accesibilidad en la capa de notas |

---

### 5. A/B Testing

El **A/B testing** es una forma específica de iteración: se crean **dos versiones** de la misma solución para comparar cuál funciona mejor.

**Cómo hacer A/B testing en Figma:**
1. Crear dos artboards paralelos: "Versión A" y "Versión B"
2. Cambiar solo la **variable a testear** (una sola diferencia entre A y B)
3. Crear dos Flows separados en Prototype mode: "Flow A" y "Flow B"
4. Mostrar cada versión a distintos evaluadores
5. Comparar cuál versión tiene mejor performance en la tarea objetivo

**Ejemplo práctico:**
```
Variable a testear: posición del botón CTA en la ficha de producto móvil

Versión A: Botón dentro del flujo normal (requiere scroll para llegar)
Versión B: Botón sticky fijo en la parte inferior (siempre visible)

Métrica: cantidad de pasos para completar "Agrega al carrito"
Resultado: Versión B → 0 scrolls adicionales vs. Versión A → 3 scrolls
```

---

### 6. Documentación del Proceso de Iteración

El **formato de respuesta** de la AS3 debe incluir:

**Para cada iteración aplicada:**
```
1. Heurística o criterio que motivó el cambio
2. Descripción del problema original
3. Impacto en el usuario si no se corrige
4. Solución implementada (descripción + captura Figma)
5. Comparación antes/después (capturas)
6. Heurística/criterio resuelto
7. Resultado esperado para el usuario
```

**Para el A/B test:**
```
Variable testeada:
Descripción Versión A:
Descripción Versión B:
Criterio de evaluación:
Resultado:
Versión elegida y justificación:
```

---

## Actividad de la Semana

> 📝 **AS3: Aplicando el proceso de iteración** · Cuestionario con formato de respuesta

Aplica las mejoras del test heurístico a tu prototipo y documenta el proceso en el **formato de respuesta descargable** desde AVA.

- 📅 **Fecha límite:** Lunes 14 de diciembre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Formato de respuesta completado + ZIP con Figma actualizado, subidos a AVA
- ⚠️ Esta actividad es **sumativa** — revisar la rúbrica

---

## Cierre de Semana

El proceso iterativo es el corazón del Diseño Centrado en el Usuario. Un prototipo nunca está "terminado" — está en constante mejora basada en evidencia. Lo que distingue a un diseñador profesional no es hacer el diseño perfecto a la primera, sino tener el proceso para identificar qué no funciona, documentarlo con precisión y mejorarlo sistemáticamente.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
