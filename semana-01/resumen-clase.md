# Semana 1 — Aprendiendo a crear componentes de diseño
**Prototipos Navegables (DUD2204) · Experiencia 1**
**Clase sincrónica:** Miércoles 21 de octubre de 2026 · 19:00 hrs

---

> 🖼️ *Infografía de clase — agregar a `material-clase/infografia.png` cuando esté disponible.*

---

## Introducción

Bienvenidos a la primera experiencia de **Prototipos Navegables**. En asignaturas anteriores adquiriste habilidades en diseño de interfaces: levantamiento de brief, investigación de usuarios, arquitectura de información y wireframes. También desarrollaste conocimientos en diseño responsive.

Durante este bimestre aprenderemos a crear **diseños de interfaces interactivas** mediante componentes usando software de prototipado (Figma), y abordaremos cómo realizar entregas considerando la **usabilidad** y **accesibilidad**. Los componentes te ayudarán a construir interfaces siguiendo principios de usabilidad y criterios de accesibilidad para entregarlos al equipo de desarrollo Front-end.

> 💡 **Preguntas activadoras:** ¿Sabías que puedes crear componentes en un software de prototipado? ¿Cómo se puede crear una guía de estilo efectiva que incluya criterios de accesibilidad y usabilidad? ¿Cómo influyen los componentes en la accesibilidad de una interfaz?

---

## Resultado de Aprendizaje e Indicadores de Logro

**RA1.** Implementar prototipo interactivo de un proyecto digital, considerando códigos gráficos y elementos de usabilidad y accesibilidad.

| IL | Indicador |
|----|-----------|
| **IL1** | Utiliza componentes para el diseño de una interfaz interactiva, de acuerdo a la experiencia de usuario y requerimientos del proyecto. |
| **IL2** | Utiliza elementos gráficos para la correcta composición de un diseño de interfaz, aplicando interacciones y considerando elementos de accesibilidad y usabilidad. |

---

## Conceptos Clave de la Semana

`Usabilidad` · `Accesibilidad` · `Componentes` · `WCAG 2.1` · `Leyes de Nielsen` · `WAI`

---

## Contenidos

### 1. Usabilidad y Accesibilidad

**Usabilidad:** facilidad con que los usuarios pueden interactuar con un producto, sistema o aplicación y lograr sus objetivos de manera **eficiente, efectiva y satisfactoria**. Una debilidad de usabilidad es cualquier aspecto que dificulte o entorpezca la experiencia del usuario.

**Accesibilidad Web:** acceso universal a la Web, independientemente del tipo de hardware, software, infraestructura de red, idioma, cultura, localización geográfica y capacidades de los usuarios.

La **WAI (Web Accessibility Initiative)** es una actividad del W3C que facilita el acceso de personas con discapacidad, desarrollando las **pautas WCAG**.

> 📌 En Chile las normativas que regulan la accesibilidad digital son las **Leyes 21.180** (Transformación Digital del Estado) y **20.422** (igualdad de oportunidades e inclusión social de personas con discapacidad). Exigen el cumplimiento de WCAG 2.1 nivel AA.

---

### 2. Las 10 Leyes Heurísticas de Nielsen

| # | Ley | Descripción resumida |
|---|-----|---------------------|
| 1 | **Visibilidad del estado del sistema** | Retroalimentación adecuada en tiempo razonable |
| 2 | **Relación sistema/mundo real** | Lenguaje familiar, no terminología técnica |
| 3 | **Control y libertad del usuario** | Poder deshacer acciones no deseadas |
| 4 | **Consistencia y estándares** | Elementos y acciones consistentes con estándares |
| 5 | **Prevención de errores** | Diseño que minimiza o previene errores |
| 6 | **Reconocer antes que recordar** | Información visible, sin requerir recordar |
| 7 | **Flexibilidad y eficiencia** | Atajos para usuarios avanzados |
| 8 | **Diseño estético y minimalista** | Solo información relevante, sin sobrecarga visual |
| 9 | **Ayuda a recuperarse de errores** | Mensajes claros y opciones de resolución |
| 10 | **Ayuda y documentación** | Ayuda contextual y documentación accesible |

> 🔗 Video recomendado: [Conoce los principios (leyes) del diseño UX UI](https://www.youtube.com/watch?v=9FxIt_XlLn8)

---

### 3. Componentes en el Diseño de Interfaces

Un **componente** es un elemento visual **reutilizable** que se utiliza para construir la interfaz de usuario. Pueden ser botones, menús desplegables, campos de entrada, gráficos, tablas, entre otros.

Los componentes estandarizan la apariencia y funcionalidad de la interfaz, simplificando la creación de diseños coherentes y fáciles de usar. Se pueden combinar para crear diseños más complejos.

**Un componente bien diseñado debe:**
- Ser fácil de usar y entender
- Tener apariencia consistente con el resto de la interfaz
- Cumplir con las expectativas del usuario en cuanto a funcionalidad

---

### 4. Ventajas de Crear Componentes

| Ventaja | Descripción |
|---------|-------------|
| **Consistencia visual** | Apariencia coherente en toda la interfaz — mismos botones, mismos cards |
| **Ahorro de tiempo** | Reutilización sin re-diseñar. Cambios en el maestro se propagan automáticamente |
| **Eficiencia en el flujo** | Biblioteca de componentes para arrastrar y soltar rápidamente |
| **Colaboración** | Todo el equipo usa los mismos elementos; cambios rastreables |
| **Prototipado ágil** | Crear y testear interacciones con componentes reutilizables |

---

### 5. Elementos Constitutivos de una Interfaz Web

Los siguientes elementos son comunes en interfaces web y deben construirse como **componentes** en el software de diseño:

- **Encabezado (Header):** logotipo + menú principal + login/búsqueda
- **Barra de navegación:** links a secciones del sitio
- **Contenido principal:** texto, imágenes, videos, elementos interactivos
- **Barra lateral (Sidebar):** contenido adicional, menús secundarios
- **Pie de página (Footer):** información de contacto, links legales, redes sociales
- **Botones y enlaces:** acciones del usuario (enviar, abrir, navegar)
- **Formularios:** campos de texto, checkboxes, selects, botones de envío
- **Menús desplegables:** listas de opciones seleccionables
- **Imágenes y multimedia:** fotos, videos, gráficos, animaciones
- **Íconos y elementos de diseño:** redes sociales, indicadores de estado

---

### 6. Criterios de Accesibilidad WCAG 2.1

La W3C establece tres niveles de cumplimiento:

| Nivel | Descripción |
|-------|-------------|
| **A** | Requisitos mínimos básicos |
| **AA** | Estándar recomendado (obligatorio en Chile) |
| **AAA** | Nivel máximo de accesibilidad |

**Los 4 principios POUR:**

- **Perceptible:** alternativas textuales para imágenes y videos, contraste adecuado
- **Operable:** tiempo suficiente para leer y usar el contenido, navegación por teclado
- **Comprensible:** lenguaje claro, estructura lógica, menus consistentes
- **Robusto:** compatible con tecnologías asistivas, HTML semántico válido

**Buenas prácticas básicas:**
- Contraste mínimo de texto: **4.5:1** (AA) para texto normal / **3:1** para texto grande
- Área táctil mínima: **44×44px** para elementos interactivos
- Alt text en todas las imágenes informativas
- Estados de foco visibles (teclado y lector de pantalla)
- No depender del color como único indicador de información

---

## Actividad de la Semana

> 📝 **AF1: Utilizando componentes para desarrollar un ecommerce** · Cuestionario en AVA

Responde el cuestionario sobre el diseño de componentes y su utilización en el diseño de interfaz. Leerás un breve caso y responderás preguntas sobre cómo crear componentes para una interfaz atractiva, funcional y accesible.

- 📅 **Fecha límite:** Lunes 26 de octubre de 2026 a las 23:59 hrs
- 📤 **Entrega:** Cuestionario directo en la plataforma AVA (sin archivo ZIP)
- 🔗 Recursos Figma disponibles en el **CRAED**

---

## Cierre de Semana

Esta semana sentamos los fundamentos del bimestre: los componentes son la unidad básica de construcción de cualquier interfaz profesional. La usabilidad y la accesibilidad no son "extras" — son los criterios que determinan si un diseño funciona para todos los usuarios. Las 10 leyes de Nielsen son la lente que usaremos para evaluar nuestros diseños a lo largo del semestre.

---

> 📄 *Presentación de clase — agregar a `material-clase/presentacion.pdf` cuando esté disponible.*
