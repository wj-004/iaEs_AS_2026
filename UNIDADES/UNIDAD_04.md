# Material de Estudio Extenso - UNIDAD 4: Etapa de Relevamiento

Este material profundiza en la etapa de relevamiento, integrando las metodologías de **Kendall & Kendall, Roger Pressman, Edward Yourdon** y guías de gestión de proyectos para proporcionar una visión técnica y detallada de la obtención de requerimientos.

---

## a) Relevamiento Preliminar y Relevamiento Detallado: Diferencias

El proceso de relevamiento no es un evento único, sino una progresión que va desde lo general a lo específico.

1.  **Relevamiento Preliminar (La Encuesta o Estudio de Factibilidad):** 
    *   **Objetivo:** Su propósito es identificar a los usuarios responsables y establecer un "campo de actividad" inicial [1]. 
    *   **Actividades:** Involucra una serie de entrevistas breves para determinar qué departamentos se verán afectados y el desarrollo de un **diagrama de contexto**, que representa al sistema como un proceso único para entender sus fronteras [1, 2]. 
    *   **Alcance:** Ocupa entre el 5% y el 10% de los recursos totales del proyecto [3]. Se centra en la viabilidad técnica, económica y operativa para decidir si el proyecto debe cancelarse o continuar [3, 4].
    
2.  **Relevamiento Detallado (Determinación de Requerimientos):** 
    *   **Objetivo:** Comprender exhaustivamente los requerimientos humanos de información y las interacciones de los usuarios con la tecnología (HCI) [5, 6]. 
    *   **Actividades:** El analista utiliza métodos interactivos (entrevistas, cuestionarios, JAD) y discretos (observación, muestreo) para descubrir el "quién, qué, dónde, cuándo, cómo y por qué" de los procedimientos actuales [7, 8].
    *   **Alcance:** Busca definir la **esencia del sistema** (lo que debe hacer) independientemente de la tecnología que se usará [9, 10].

---

## b) Información a Relevar

### Cantidad vs. Calidad
El analista debe ser selectivo. Recopilar datos irrelevantes es costoso y genera "ruido" en el análisis [11, 12]. La **calidad** de la información es superior a la cantidad; se busca información precisa que ayude a diferenciar los problemas reales de los síntomas superficiales [10]. Una sobrecarga de información puede impedir que los responsables tomen decisiones efectivas [13].

### Fuentes de Información Disponibles
Existen tres categorías principales de fuentes [6, 14, 15]:
*   **Fuentes Humanas:** Usuarios finales, gerentes de operaciones y administradores estratégicos. Son clave para obtener opiniones y sentimientos sobre el sistema actual [16].
*   **Documentación Organizacional:** Incluye datos "duros" (informes de rendimiento, registros de transacciones) y cualitativos (manuales de procedimientos, memorandos, correos electrónicos) [17, 18].
*   **Entorno Físico:** El análisis de la oficina y el espacio de trabajo revela la cultura organizacional y cómo se procesa la información en la práctica [19, 20].

---

## c) Muestreo (Sampling)

### Necesidad (Objeto del Muestreo)
El muestreo es la selección sistemática de elementos representativos para revelar información útil sobre la población total [21]. Sus objetivos fundamentales son [11]:
1.  **Contener Costos:** Evita el gasto masivo de examinar cada documento o entrevistar a cada empleado [11].
2.  **Agilizar la Recopilación:** Permite obtener una imagen válida del sistema en una fracción del tiempo necesario para un censo completo [22].
3.  **Mejorar la Efectividad:** Al tratar con menos elementos, el analista puede ser más minucioso y realizar un seguimiento detallado de cada dato obtenido [23].
4.  **Reducir Predisposición:** Seleccionar muestras de forma estadística (como el muestreo aleatorio complejo) evita que el análisis se distorsione por opiniones aisladas o datos atípicos [23, 24].

---

## d) El Plan de Acción

### Confección del Plan de Acción
La planificación crea un "mapa" que guía al equipo de ingeniería de software a través de tareas, riesgos y recursos [25].
*   **Determinación de Objetivos:** Deben ser lo más específicos posible para definir la extensión y duración del proyecto (ej: "Construir un sistema de ventas en línea") [26, 27].
*   **Descomposición de Actividades:** Se divide el proyecto en fases (análisis, diseño, implementación) y estas en tareas menores [28, 29].
*   **Establecimiento de Secuencia:** Se identifican tareas que dependen de otras y tareas que pueden ejecutarse en paralelo para optimizar el tiempo [27, 30].
*   **Herramientas de Control:** 
    *   **Diagramas de Gantt:** Muestran el calendario del proyecto con barras horizontales. Permiten ver qué tareas están completadas y cuáles presentan retrasos [31, 32].
    *   **Diagramas PERT:** Representan al proyecto como una red de nodos y flechas. Son fundamentales para identificar la **ruta crítica**, que es la secuencia de actividades cuyo retraso postergaría todo el proyecto [33-35].

---

## e) Entrevistas

### Planeación
Antes de la reunión, el analista debe seguir cinco pasos: leer antecedentes (informes anuales, sitios web), establecer objetivos claros, decidir a quién entrevistar (muestreo representativo), preparar al entrevistado y seleccionar la estructura de preguntas [15, 36, 37].

### Desarrollo: Tipos de Preguntas y Estructura
*   **Preguntas Abiertas:** Permiten respuestas extensas y espontáneas (ej: "¿Qué opina del nuevo portal?"). Ayudan a entender el vocabulario y sentimientos del usuario [38, 39].
*   **Preguntas Cerradas:** Limitan las opciones de respuesta (ej: "¿Cuántos pedidos procesa al día?"). Son útiles para obtener datos precisos y ahorrar tiempo [40, 41].
*   **Preguntas Bipolares:** Un tipo de cerrada con solo dos opciones (Sí/No, De acuerdo/En desacuerdo) [42].
*   **Sondeos:** Preguntas de seguimiento (ej: "¿Por qué piensa eso?") para profundizar en declaraciones ambiguas o superficiales [43, 44].

**Estructuras Lógicas:**
*   **Pirámide:** Inicia con preguntas cerradas y específicas para luego abrirse a temas generales [45, 46].
*   **Embudo:** Comienza con preguntas amplias y abiertas para luego restringirse a respuestas específicas [47, 48].
*   **Diamante:** Combina ambas; empieza específico, se amplía a temas generales y concluye con una resolución particularizada [49, 50].

### Escritura del Reporte
El reporte debe escribirse inmediatamente después de la entrevista para no perder calidad en los datos [51]. Debe incluir un resumen inicial de impresiones y un desarrollo detallado de los puntos principales [50]. Se recomienda revisar el reporte con el entrevistado para corregir malentendidos [50].

### Técnicas de Registro
*   **Grabación:** Captura exactamente lo dicho, pero requiere permiso y puede inhibir al usuario [52, 53].
*   **Toma de Notas:** Permite registrar señales no verbales y aspectos del entorno, aunque puede interrumpir el flujo si el analista se enfoca demasiado en escribir [52, 54].

---

## f) Cuestionarios

### Planeación
Se usan cuando los usuarios están geográficamente dispersos o cuando se necesita cuantificar opiniones de un grupo grande [55, 56]. Requieren una planeación meticulosa de la terminología, ya que no hay oportunidad de aclaración inmediata [57, 58].

### Uso de Escalas
*   **Nominal:** Clasifica elementos en categorías (ej: Ventas, Producción) [59].
*   **Intervalo:** Los intervalos entre puntos son iguales, permitiendo calcular promedios (ej: escala de 1 a 5 para medir utilidad) [60, 61].

### Diseño
*   **Preguntas Abiertas vs. Cerradas:** Las cerradas son preferibles en muestras grandes por su facilidad de análisis cuantitativo; las abiertas son ideales para explorar problemas no anticipados [62, 63].
*   **Orden de las Preguntas:** Las más importantes y menos controversiales deben ir al principio para motivar al encuestado [64, 65].

---

## g) Revisión de la Documentación

El analista debe investigar dos tipos de evidencia documental [17]:
1.  **Documentos Cuantitativos:** Informes para toma de decisiones, informes de rendimiento (brecha entre lo real y lo esperado), registros de transacciones y formularios de captura de datos [66, 67].
2.  **Documentos Cualitativos:** Memorandos, correos electrónicos, manuales de políticas y anuncios. Revelan las expectativas de los autores, la cultura organizacional y el lenguaje común de la empresa [18, 68].

---

## h) Observación Directa

### Guión del Analista (Playscript)
Es una técnica humanista para documentar actividades de toma de decisiones. El analista registra al "actor" y sus "acciones" usando verbos específicos (habla, decide, firma) para entender el flujo de trabajo real [19, 69].

### Técnica STROBE (Structured Observation of the Environment)
Permite observar sistemáticamente el entorno físico para interpretar cómo el encargado de decisiones usa la información [70]. Analiza 7 elementos clave [20, 71]:
1.  **Ubicación de la oficina.**
2.  **Colocación del escritorio.**
3.  **Equipo de oficina estacionario.**
4.  **Accesorios (dispositivos electrónicos).**
5.  **Fuentes externas de información (revistas, libros).**
6.  **Iluminación y colores.**
7.  **Vestimenta del personal.**

---

## i) Estructura PIECES para Detección de Problemas

Aunque no se detalla siempre como un acrónimo rígido, las fuentes sugieren evaluar estas dimensiones para justificar un proyecto [13, 72, 73]:
*   **P (Performance/Rendimiento):** Búsqueda de lentitud o cuellos de botella [67, 74].
*   **I (Information/Información):** Identificación de falta de datos, inexactitud o redundancia [75, 76].
*   **E (Economics/Economía):** Deseo de minimizar gastos operativos o aumentar beneficios [13, 72].
*   **C (Control/Seguridad):** Necesidad de mejores medidas de validación y acceso [73, 77].
*   **E (Efficiency/Eficiencia):** Cómo la computadora puede simplificar tareas manuales [78].
*   **S (Service/Servicio):** Mejora de la interacción con el cliente y resolución de quejas [79].

## Ejemplos

### 🅿️ P — Performance (Rendimiento)

Problemas relacionados con lentitud, cuellos de botella o tiempos de respuesta.

- El sistema tarda más de 10 segundos en cargar el listado de clientes.
- Las consultas a la base de datos se vuelven lentas cuando hay más de 100.000 registros.
- El servidor se satura en horarios pico, provocando caídas temporales.
- El proceso de generación de reportes mensuales demora demasiado y bloquea otras operaciones.

---

### ℹ️ I — Information (Información)

Problemas de datos incompletos, incorrectos, duplicados o mal estructurados.

- Existen clientes duplicados con diferentes formatos de nombre.
- Los reportes financieros muestran datos desactualizados.
- Falta información clave como correo electrónico o número de teléfono en registros de usuarios.
- La base de datos contiene inconsistencias entre el stock real y el sistema.

---

### 💰 E — Economics (Economía)

Problemas relacionados con costos, recursos o rentabilidad.

- El mantenimiento manual del sistema requiere demasiado tiempo del personal administrativo.
- Se están utilizando múltiples herramientas pagas para tareas que podrían centralizarse.
- El proceso actual genera altos costos operativos por errores humanos frecuentes.
- La falta de automatización incrementa la necesidad de contratar más empleados.

---

### 🔐 C — Control (Seguridad)

Problemas de acceso, validación, seguridad o control de procesos.

- Cualquier usuario puede acceder a información sensible sin autenticación adecuada.
- No existe historial de auditoría sobre cambios en los datos.
- Los permisos de usuario no están correctamente definidos.
- Se han detectado accesos simultáneos con credenciales compartidas.

---

### ⚙️ E — Efficiency (Eficiencia)

Problemas donde tareas manuales podrían ser automatizadas o simplificadas.

- Los empleados cargan datos manualmente en Excel en lugar de usar un sistema automatizado.
- Se repiten tareas administrativas que podrían ser procesadas por un flujo automático.
- El envío de correos se realiza uno por uno en lugar de usar notificaciones masivas.
- La conciliación de pagos se realiza manualmente todos los días.

---

### 🧩 S — Service (Servicio)

Problemas relacionados con la experiencia del usuario o la calidad del servicio.

- Los clientes no reciben confirmación de sus pedidos.
- El soporte tarda demasiado en responder consultas.
- La interfaz del sistema es confusa y dificulta la navegación.
- No existe un canal claro para reclamos o seguimiento de tickets.

---
**Referencias Bibliográficas Utilizadas:**
*   **Kendall & Kendall (2011).** *Análisis y Diseño de Sistemas*. 8va Edición. Pearson Educación.
*   **Pressman, R. (2010).** *Ingeniería del Software*. McGraw-Hill.
*   **Yourdon, E. (1993).** *Análisis Estructurado Moderno*. Prentice-Hall.