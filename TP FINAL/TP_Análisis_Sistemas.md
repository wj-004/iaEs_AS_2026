# Trabajo Práctico – Análisis del Sistema Actual

<div style="text-align: justify;">

El presente Trabajo Práctico tiene como objetivo aplicar los contenidos desarrollados en la materia **Análisis de Sistemas** mediante el relevamiento, análisis y modelado de una organización o situación problemática concreta.

El trabajo será de **carácter individual**. Cada estudiante deberá utilizar como escenario de análisis **el mismo proyecto o escenario trabajado en la materia Seminario**, pero deberá desarrollar y presentar individualmente la documentación solicitada.

El trabajo deberá describir inicialmente el problema y el contexto de la organización para luego analizar **cómo funciona actualmente**.

</div>

---

## 1. Definición del Proyecto

### 1.1. Definición del problema

<div style="text-align: justify;">

Describir claramente la situación problemática que da origen al proyecto. La descripción deberá permitir comprender **qué ocurre actualmente, a quiénes afecta, qué dificultades o consecuencias genera, por qué representa un problema para la organización y qué procesos o actividades se encuentran involucrados**.

En esta sección deberá describirse **el problema**, evitando anticipar funcionalidades o características de la solución informática propuesta.

</div>

### 1.2. Contexto organizacional

<div style="text-align: justify;">

Describir brevemente la organización en la cual se desarrolla el proyecto y el contexto en el que se presenta la problemática.

La descripción deberá contemplar, cuando corresponda, el nombre y actividad principal de la organización, el tipo de organización, el área o sector involucrado, su estructura organizacional básica, los puestos o roles que participan en los procesos analizados y las principales actividades relacionadas con el problema.

Cuando resulte necesario para comprender la organización, podrá incorporarse un **organigrama**.

</div>

### 1.3. Objetivos del sistema

<div style="text-align: justify;">

Definir el propósito que se pretende alcanzar mediante el desarrollo del nuevo sistema.

El **objetivo general** deberá expresar de manera clara el propósito principal del sistema y la mejora que se pretende conseguir en la organización.

Los **objetivos específicos** deberán establecer resultados concretos derivados del objetivo general. Deberán expresar las mejoras que se busca alcanzar, evitando convertirlos en una enumeración detallada de funcionalidades o características técnicas del sistema.

Los objetivos planteados deberán mantener relación directa con el problema previamente definido.

</div>

### 1.4. Alcance y límites

<div style="text-align: justify;">

El **alcance** deberá indicar qué procesos, áreas y actividades serán contemplados por el sistema propuesto.

Los **límites** deberán establecer expresamente qué procesos, áreas o funcionalidades quedarán fuera del proyecto.

La definición del alcance y los límites deberá permitir determinar claramente **hasta dónde llegará la solución desarrollada**.

</div>

---

# 2. Relevamiento y Análisis del Sistema Actual

<div style="text-align: justify;">

Esta etapa deberá representar **exclusivamente el funcionamiento actual de la organización**. No deberán incorporarse en esta sección procesos, datos, estructuras o funcionalidades pertenecientes al nuevo sistema que se pretende desarrollar.

</div>

## 2.1. Descripción del sistema actual

<div style="text-align: justify;">

Realizar una descripción general del funcionamiento actual del proceso analizado.

La descripción deberá permitir identificar la organización y el área relevada, las personas o puestos que participan, los principales procesos que se desarrollan, las entradas y salidas de información, los registros o medios utilizados actualmente y los problemas inicialmente observados.

Esta sección deberá brindar una visión general del funcionamiento actual que permita comprender posteriormente el relevamiento, la narrativa y los diagramas desarrollados.

</div>

## 2.2. Técnicas de relevamiento utilizadas

<div style="text-align: justify;">

Indicar y desarrollar las técnicas utilizadas para obtener información acerca del funcionamiento actual de la organización.

Podrán utilizarse, según corresponda, **entrevistas, observación directa, análisis de documentación, cuestionarios u otras técnicas justificadas**.

Para cada técnica deberá indicarse qué información se buscó obtener, a quién o sobre qué proceso se aplicó y cuáles fueron los principales resultados obtenidos.

</div>

### 2.2.1. Documentación analizada

<div style="text-align: justify;">

Incorporar ejemplos de los documentos, formularios, planillas, registros o comprobantes utilizados actualmente por la organización y que resulten relevantes para comprender los procesos estudiados.

Cada documento deberá presentarse **etiquetado**, identificando y numerando sus principales datos, campos o elementos de información.

Además de incorporar la imagen o representación del documento, deberá realizarse su correspondiente análisis, explicando el significado de cada elemento identificado.

</div>

**Ejemplo:**

**Documento: Pedido de cliente**

1. Fecha.
2. Nombre del cliente.
3. Producto solicitado.
4. Cantidad.
5. Forma de pago.

<div style="text-align: justify;">

No será suficiente incorporar únicamente una imagen del documento. El estudiante deberá identificar y explicar la información que contiene y su participación dentro del proceso actual.

</div>

## 2.3. Narrativa del sistema actual

<div style="text-align: justify;">

Redactar de manera textual, ordenada y secuencial **cómo funciona actualmente el proceso analizado**.

La narrativa deberá permitir comprender cómo se inicia cada proceso, qué actividades se realizan, qué personas, sectores u organizaciones intervienen, qué información se utiliza, qué documentos o registros se generan o consultan, qué decisiones pueden producir caminos alternativos y cómo finaliza el proceso.

La descripción deberá representar fielmente la realidad observada durante el relevamiento y constituirá la base para desarrollar posteriormente el **Diagrama de Contexto** y el **DFD Nivel 0**.

No deberán describirse en esta sección funcionalidades correspondientes al nuevo sistema.

</div>

---

## 2.4. Modelado de Procesos del Sistema Actual

<div style="text-align: justify;">

Los diagramas incluidos en esta sección deberán representar **el sistema actual relevado** y mantener coherencia con las entrevistas, observaciones, documentación y narrativa desarrolladas anteriormente.

No deberán representar la solución informática que se pretende desarrollar posteriormente.

</div>

### 2.4.1. Diagrama de Contexto

<div style="text-align: justify;">

Representar el sistema actual como **un único proceso**, identificando las entidades externas que interactúan con él, las entradas de información, las salidas de información y el límite del sistema analizado.

Las entidades externas deberán corresponder a personas, sectores, organizaciones u otros sistemas que intercambien información con el proceso estudiado.

Los flujos deberán representar **datos o información**, evitando representar acciones o movimientos físicos de objetos como si fueran flujos de datos.

</div>

### 2.4.2. DFD Nivel 0

<div style="text-align: justify;">

Descomponer el proceso general presentado en el Diagrama de Contexto en los principales procesos que componen el sistema actual.

El DFD deberá incluir los **procesos principales, entidades externas, flujos de datos y almacenes de datos existentes actualmente**, cuando corresponda.

El **DFD Nivel 0 deberá mantener balanceo con el Diagrama de Contexto**, conservando las entradas y salidas que atraviesan el límite del sistema.

Los almacenes representados deberán corresponder a registros que realmente existen en el funcionamiento actual, tales como cuadernos, planillas, archivos, formularios, bases de datos u otros medios relevados. No deberán incorporarse estructuras correspondientes a la futura solución informática.

</div>

### 2.4.3. Diccionario de procesos

<div style="text-align: justify;">

Describir cada uno de los procesos representados en el DFD Nivel 0.

Para cada proceso deberá indicarse su nombre, finalidad, información recibida, principales actividades realizadas e información generada.

La denominación de cada proceso deberá coincidir con la utilizada en el DFD Nivel 0.

</div>

### 2.4.4. Diccionario de datos del DFD

<div style="text-align: justify;">

Definir los principales flujos de información representados en el Diagrama de Contexto y en el DFD Nivel 0.

Para cada flujo deberá indicarse su **nombre, descripción y los principales datos que lo componen**.

La información definida deberá corresponder al **sistema actual relevado** y no al diseño de la futura base de datos o a estructuras pertenecientes al nuevo sistema.

</div>

---

## 2.5. Identificación de problemas

<div style="text-align: justify;">

A partir del relevamiento, la narrativa y los diagramas realizados, identificar los principales problemas existentes en el funcionamiento actual de la organización.

Para cada problema deberá indicarse un identificador, una descripción clara, su nivel de impacto, su frecuencia y, cuando corresponda, el área o proceso afectado.

Los problemas deberán estar respaldados por la información obtenida durante el relevamiento. No deberán incorporarse problemas que no hayan sido previamente observados, documentados o identificados.

Además, deberán indicarse brevemente las **causas probables** que originan los problemas detectados.

</div>

Ejemplo de estructura:

| ID | Problema | Impacto | Frecuencia | Área |
|---|---|---|---|---|
| P1 | Descripción del problema | Alto / Medio / Bajo | Alta / Media / Baja | Área afectada |
| P2 | Descripción del problema | Alto / Medio / Bajo | Alta / Media / Baja | Área afectada |

---

## 2.6. Análisis del problema

<div style="text-align: justify;">

Analizar los problemas identificados y explicar de qué manera afectan el funcionamiento de la organización.

Para organizar este análisis deberá utilizarse el modelo **PIECES**, clasificando los problemas detectados según corresponda en las categorías **Performance, Information, Economics, Control, Efficiency y Service**.

No será necesario incorporar problemas artificialmente en todas las categorías cuando el relevamiento realizado no proporcione evidencia suficiente para ello.

</div>

| Categoría | Aspecto a analizar |
|---|---|
| **Performance** | Rendimiento, tiempos de respuesta, demoras o capacidad de procesamiento. |
| **Information** | Calidad, precisión, disponibilidad, actualización o accesibilidad de la información. |
| **Economics** | Costos, pérdidas económicas, desperdicios o utilización innecesaria de recursos. |
| **Control** | Controles, seguridad, integridad, seguimiento y protección de la información. |
| **Efficiency** | Uso innecesario de tiempo o recursos, tareas repetidas o procedimientos redundantes. |
| **Service** | Calidad del servicio ofrecido a clientes, usuarios u otras personas relacionadas con la organización. |

<div style="text-align: justify;">

Finalmente, deberá incorporarse una **conclusión del análisis**, explicando cuáles son los principales problemas detectados, cómo afectan a la organización y qué necesidades deberían ser atendidas posteriormente mediante una solución.

En esta instancia podrán identificarse necesidades generales, pero no deberán definirse todavía en detalle las funcionalidades del nuevo sistema.

</div>

---

# Criterios de evaluación

<div style="text-align: justify;">

Se evaluará principalmente la **coherencia y trazabilidad del análisis realizado**, considerando la relación existente entre:

**Problema planteado → Relevamiento → Narrativa → Modelado del sistema actual → Problemas identificados → Análisis**

También se tendrá en cuenta la correcta aplicación de las técnicas de relevamiento y de las herramientas de modelado, la correspondencia entre la información obtenida y los diagramas presentados, la claridad de la redacción y la correcta diferenciación entre el **sistema actual** y el **nuevo sistema**.

</div>