# Trabajo Práctico Final – Seminario

## Información General

* **Materia:** Seminario
* **Carrera:** Tecnicatura en Análisis de Sistemas
* **Año:** 2026
* **Alumno/s:**
* **Docente:**
* **Título del Proyecto:**

---

# 1. Definición del Proyecto

## 1.1 Definición del problema

Describir claramente la situación actual indicando:

* Qué ocurre.
* A quién afecta.
* Cuáles son sus consecuencias.
* Por qué representa un problema para la organización.

## 1.2 Contexto organizacional

Describir la organización y el entorno donde se implementará el sistema.

* Tipo de organización.
* Área o sector involucrado.
* Usuarios participantes.
* Procesos relacionados.

## 1.3 Objetivos del sistema

### Objetivo general

Descripción del propósito principal del sistema.

### Objetivos específicos

Listado de objetivos concretos y medibles.

## 1.4 Alcance y límites

### Alcance

Definir las funcionalidades y procesos que serán cubiertos por el sistema.

### Límites

Definir explícitamente qué procesos o funcionalidades quedan fuera del proyecto.

---

# 2. Relevamiento y Análisis del Sistema Actual

## 2.1 Descripción del sistema actual

### Organización relevada

* Organización:
* Área:
* Fecha del relevamiento:
* Analista:

### Procesos principales

| Proceso | Descripción | Responsable |
| ------- | ----------- | ----------- |
|         |             |             |
|         |             |             |

### Entradas del sistema

| Entrada | Origen |
| ------- | ------ |
|         |        |
|         |        |

### Salidas del sistema

| Salida | Destino |
| ------ | ------- |
|        |         |
|        |         |

### Problemas detectados inicialmente

* ...
* ...
* ...

---

## 2.2 Técnicas de relevamiento utilizadas

### Entrevistas realizadas

| Entrevistado | Rol | Área |
| ------------ | --- | ---- |
|              |     |      |
|              |     |      |

### Observación directa

| Proceso observado | Usuario |
| ----------------- | ------- |
|                   |         |
|                   |         |

### Documentación analizada

* Formularios.
* Planillas.
* Reportes.
* Sistemas existentes.
* Reglamentos o procedimientos internos.

### Principales hallazgos

* ...
* ...
* ...

---

## 2.3 Narrativa del sistema actual

Realizar una descripción textual y secuencial del funcionamiento actual de la organización o del proceso objeto de estudio.

La narrativa debe permitir comprender:

* Cómo se inicia el proceso.
* Qué actividades se realizan.
* Qué actores intervienen.
* Qué información se utiliza.
* Qué documentos o registros se generan.
* Cómo finaliza el proceso.

La descripción debe reflejar el flujo real de trabajo y servirá como base para la elaboración de los DFD del sistema actual y la posterior identificación de problemas.

### Narrativa

> Redactar aquí la descripción completa del proceso actual.

---

## 2.4 Modelado de Procesos del Sistema Actual

Los diagramas incluidos en esta sección deben representar exclusivamente el funcionamiento del sistema actual relevado.

No deben representar la solución informática que será desarrollada posteriormente.

### 2.4.1 Diagrama de Contexto

Representar el sistema actual como un único proceso, identificando:

* Entidades externas.
* Entradas de información.
* Salidas de información.
* Límites del sistema analizado.

### 2.4.2 DFD Nivel 0

Representar los principales procesos que componen el sistema actual, incluyendo:

* Procesos principales.
* Entidades externas.
* Flujos de datos.
* Almacenes de datos, cuando correspondan.

El DFD Nivel 0 deberá mantener el balanceo con el Diagrama de Contexto.

### 2.4.3 Diccionario de procesos

Describir brevemente los procesos identificados en el DFD del sistema actual.

| Proceso | Descripción |
| ------- | ----------- |
|         |             |
|         |             |

### 2.4.4 Diccionario de datos del DFD

Definir los principales flujos y estructuras de datos representados en los diagramas.

| Flujo | Descripción |
| ----- | ----------- |
|       |             |
|       |             |

---

## 2.5 Identificación de problemas

A partir del relevamiento y del modelado realizado, identificar los principales problemas del sistema actual.

| ID | Problema | Impacto         | Frecuencia      |
| -- | -------- | --------------- | --------------- |
| P1 |          | Alto/Medio/Bajo | Alta/Media/Baja |
| P2 |          | Alto/Medio/Bajo | Alta/Media/Baja |
| P3 |          | Alto/Medio/Bajo | Alta/Media/Baja |

### Causas probables

* ...
* ...
* ...

---

## 2.6 Análisis del problema

### Análisis PIECES

| Categoría   | Problema detectado |
| ----------- | ------------------ |
| Performance |                    |
| Information |                    |
| Economics   |                    |
| Control     |                    |
| Efficiency  |                    |
| Service     |                    |

### Conclusiones del análisis

Analizar cómo los problemas detectados afectan el funcionamiento de la organización y qué necesidades deberán ser atendidas por la solución propuesta.

---

# 3. Requerimientos del Nuevo Sistema

Los requerimientos deberán surgir de las necesidades identificadas durante el relevamiento y análisis del sistema actual y deberán ser coherentes con los objetivos, alcance y límites definidos para el proyecto.

## 3.1 Actores del sistema

Identificar los usuarios o sistemas externos que interactuarán con la nueva solución.

| Actor | Descripción |
| ----- | ----------- |
|       |             |
|       |             |

---

## 3.2 Requerimientos funcionales

Listado numerado de las funcionalidades que deberá proporcionar el sistema.

* RF01:
* RF02:
* RF03:

---

## 3.3 Requerimientos no funcionales

Definir las condiciones, restricciones y atributos de calidad que deberá cumplir el sistema.

* RNF01:
* RNF02:
* RNF03:

---

## 3.4 Matriz de trazabilidad (Opcional)

| Requerimiento | Problema o necesidad | Funcionalidad implementada |
| ------------- | -------------------- | -------------------------- |
|               |                      |                            |
|               |                      |                            |

---

# 4. Modelado del Nuevo Sistema

## 4.1 Diagramas de secuencia

Desarrollar al menos dos diagramas correspondientes a procesos o funcionalidades críticas del nuevo sistema.

Los diagramas deberán ser coherentes con los requerimientos funcionales definidos.

---

# 5. Diseño de Datos

## 5.1 DER (Diagrama Entidad-Relación)

Representar el modelo de datos correspondiente al nuevo sistema.

## 5.2 Modelo relacional

Para cada tabla indicar:

* Nombre.
* Campos.
* Clave primaria.
* Claves foráneas.

## 5.3 Normalización

Aplicar hasta Tercera Forma Normal (3FN) cuando corresponda.

## 5.4 Diccionario de datos

| Campo | Tipo de dato | Descripción |
| ----- | ------------ | ----------- |
|       |              |             |
|       |              |             |

---

# 6. Construcción del Sistema

## 6.1 Arquitectura de la solución

Describir:

* Arquitectura utilizada.
* Componentes principales.
* Diagrama de arquitectura (opcional).

## 6.2 Tecnologías utilizadas

* Lenguaje de programación.
* Framework.
* Motor de base de datos.
* Herramientas complementarias.

## 6.3 Funcionalidades implementadas

Listado de funcionalidades desarrolladas.

Las funcionalidades implementadas deberán mantener correspondencia con los requerimientos funcionales definidos.

## 6.4 Capturas del sistema

Pantallas principales acompañadas de una breve descripción.

---

# 7. Despliegue y Uso

## 7.1 Requisitos técnicos

### Software

* Sistema operativo.
* Servidor web o de aplicaciones.
* Base de datos.

### Dependencias

* Librerías.
* Frameworks.
* Herramientas externas.

## 7.2 Instalación y ejecución

Procedimiento paso a paso para ejecutar el sistema.

## 7.3 Manual de usuario

### Descripción general

Objetivo y alcance del sistema.

### Uso básico

Procedimiento para utilizar las funcionalidades principales.

---

# 8. Validación y Pruebas

## 8.1 Casos de prueba

| Caso de prueba | Resultado esperado | Resultado obtenido |
| -------------- | ------------------ | ------------------ |
|                |                    |                    |
|                |                    |                    |

## 8.2 Resultados de validación

Presentar evidencia del cumplimiento de los requerimientos definidos.

---

# 9. Conclusiones

## 9.1 Resultados obtenidos

Analizar el grado de cumplimiento de los objetivos establecidos para el proyecto.

## 9.2 Problemas encontrados

Describir las principales dificultades surgidas durante el desarrollo.

## 9.3 Mejoras futuras

Indicar funcionalidades o mejoras que podrían incorporarse en versiones posteriores.

---

# Criterios obligatorios

* El sistema debe funcionar correctamente.
* Debe existir persistencia en base de datos.
* Los requerimientos definidos deben estar implementados.
* El Diagrama de Contexto y el DFD Nivel 0 deben representar correctamente el sistema actual relevado.
* Los DFD deberán ser coherentes con la narrativa y las evidencias obtenidas durante el relevamiento.
* El DER debe representar el modelo de datos del sistema desarrollado y coincidir con la base de datos implementada.
* Debe existir coherencia entre los problemas detectados, los requerimientos definidos y la solución desarrollada.

---

# Motivos de desaprobación

* Sistema no funcional.
* Ausencia de base de datos.
* Inconsistencia entre análisis, requerimientos e implementación.
* Diagramas inexistentes o incorrectos.
* DFD que no represente el sistema actual relevado.
* Trabajo copiado o genérico.
* Falta de evidencia del desarrollo realizado.

---

# Consideraciones finales

El Trabajo Práctico Final debe demostrar la capacidad del alumno para aplicar de forma integrada las etapas de:

* Relevamiento.
* Análisis.
* Definición de requerimientos.
* Diseño.
* Construcción.
* Validación.
* Implementación.

Se evaluará especialmente la trazabilidad y coherencia del proyecto:

**Sistema actual relevado → Problemas detectados → Requerimientos → Diseño de la solución → Sistema implementado**

El sistema actual deberá ser comprendido y documentado mediante el relevamiento y los DFD correspondientes. A partir de los problemas y necesidades identificados se definirán los requerimientos que darán origen al nuevo sistema.

La solución desarrollada deberá responder a una necesidad real y mantener coherencia con el análisis realizado durante el proyecto.
