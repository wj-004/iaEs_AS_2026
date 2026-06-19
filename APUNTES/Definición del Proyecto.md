# Definición del Proyecto

## Introducción

Todo proyecto de software comienza con una correcta comprensión del problema que se desea resolver. Antes de diseñar diagramas, definir requerimientos o escribir código, es necesario entender:

- Qué problema existe.
- Dónde ocurre.
- A quién afecta.
- Qué se espera lograr.
- Hasta dónde llegará la solución propuesta.

La definición del proyecto constituye la base sobre la cual se desarrollarán todas las etapas posteriores del análisis y diseño del sistema.

---

# 1. Definición del Problema

## ¿Qué es?

La definición del problema consiste en describir la situación actual que motiva el desarrollo del sistema.

No se trata de describir la solución, sino de explicar la necesidad que existe en la organización.

---

## ¿Qué debe responder?

Una buena definición del problema debe responder las siguientes preguntas:

### ¿Qué ocurre?

Describe la situación actual.

### ¿A quién afecta?

Identifica las personas, áreas o procesos afectados.

### ¿Cuáles son las consecuencias?

Explica los efectos negativos que produce la situación.

### ¿Por qué representa un problema?

Justifica la necesidad de intervenir mediante una solución informática.

---

## Ejemplo

### Incorrecto

> Se desarrollará un sistema de stock para una ferretería.

Este texto describe una solución, no un problema.

---

### Correcto

> Actualmente la ferretería registra las ventas y el stock de productos de manera manual mediante cuadernos y planillas impresas. Esta situación dificulta conocer la disponibilidad real de productos, genera errores en los registros y provoca pérdidas de ventas por faltantes no detectados a tiempo. El problema afecta principalmente a los empleados encargados de ventas y al propietario del negocio, quienes no disponen de información confiable para la toma de decisiones.

---

# 2. Contexto Organizacional

## ¿Qué es?

El contexto organizacional describe el entorno donde funcionará el sistema.

Permite comprender la organización, sus procesos y los actores involucrados.

---

## ¿Qué información debe incluir?

### Tipo de organización

Describe la naturaleza de la organización.

Ejemplos:

- Empresa comercial
- Industria
- Institución educativa
- Hospital
- Organismo público
- ONG

---

### Área o sector involucrado

Indica dónde se encuentra el problema.

Ejemplos:

- Ventas
- Recursos Humanos
- Compras
- Producción
- Biblioteca
- Administración

---

### Usuarios participantes

Personas que utilizarán o interactuarán con el sistema.

Ejemplos:

- Administradores
- Empleados
- Clientes
- Profesores
- Alumnos
- Pacientes

---

### Procesos relacionados

Procesos de negocio involucrados.

Ejemplos:

- Registro de ventas
- Gestión de turnos
- Control de stock
- Inscripción de alumnos
- Gestión de pedidos

---

## Ejemplo

### Contexto organizacional

La organización corresponde a una librería comercial dedicada a la venta minorista de libros y artículos escolares.

El área involucrada es el sector de ventas y control de stock.

Los usuarios participantes serán:

- Vendedores
- Encargado de stock
- Administrador

Los procesos relacionados son:

- Registro de ventas
- Control de inventario
- Reposición de productos

---

# 3. Objetivos del Sistema

## ¿Qué son?

Los objetivos describen lo que se pretende lograr mediante la implementación del sistema.

Deben expresar resultados esperados y no características técnicas.

---

# 3.1 Objetivo General

## ¿Qué es?

Representa la finalidad principal del proyecto.

Debe resumir el propósito global del sistema en una sola idea.

---

## Ejemplo

> Desarrollar un sistema informático que permita gestionar las ventas y controlar el stock de productos de una librería de manera eficiente y segura.

---

## Recomendaciones

Utilizar verbos como:

- Desarrollar
- Implementar
- Diseñar
- Automatizar
- Gestionar
- Optimizar

---

# 3.2 Objetivos Específicos

## ¿Qué son?

Son metas concretas que permiten alcanzar el objetivo general.

Deben ser claros y verificables.

---

## Ejemplo

Objetivo general:

> Desarrollar un sistema de gestión de ventas y stock.

Objetivos específicos:

- Registrar ventas realizadas.
- Gestionar el inventario de productos.
- Consultar existencias disponibles.
- Generar reportes de ventas.
- Reducir errores de registro manual.

---

## Recomendaciones

Cada objetivo específico debería responder a alguna necesidad identificada durante el relevamiento.

---

# 4. Alcance y Límites

Una de las tareas más importantes del analista consiste en definir claramente qué incluirá el sistema y qué quedará fuera del proyecto.

Esto evita malentendidos con los usuarios y reduce el riesgo de crecimiento descontrolado del proyecto.

---

# 4.1 Alcance

## ¿Qué es?

El alcance define las funcionalidades, procesos y responsabilidades que serán cubiertos por el sistema.

Describe aquello que el sistema hará.

---

## Pregunta clave

### ¿Qué hace el sistema?

---

## Características

- Describe funcionalidades.
- Se expresa en términos positivos.
- Define responsabilidades del sistema.
- Delimita el trabajo a realizar.

---

## Ejemplo

Sistema de gestión para una librería.

### Alcance

El sistema permitirá:

- Registrar productos.
- Gestionar categorías.
- Registrar ventas.
- Controlar stock.
- Consultar existencias.
- Generar reportes básicos de ventas.

---

## Observación

Todo lo incluido en el alcance debería reflejarse posteriormente en los requerimientos funcionales.

---

# 4.2 Límites

## ¿Qué son?

Los límites establecen las restricciones del proyecto y determinan qué aspectos quedan fuera de la solución propuesta.

Definen hasta dónde llega el sistema.

---

## Pregunta clave

### ¿Hasta dónde llega el sistema?

---

## Características

- Son restrictivos.
- Delimitan responsabilidades.
- Definen el contexto operativo.
- Evitan falsas expectativas.

---

## Ejemplo

Para el mismo sistema de librería:

### Límites

El sistema:

- Será utilizado en una única sucursal.
- Funcionará únicamente como aplicación web.
- No realizará facturación electrónica.
- No se integrará con sistemas externos.
- No incluirá una tienda online.
- No gestionará compras a proveedores.

---

# 4.3 Diferencia entre Alcance y Límites

| Concepto | Pregunta principal | Describe |
|-----------|-------------------|-----------|
| Alcance | ¿Qué hace el sistema? | Funcionalidades |
| Límites | ¿Hasta dónde llega el sistema? | Restricciones |

---

# Ejemplo Completo

## Sistema de Turnos Médicos

### Alcance

El sistema permitirá:

- Registrar pacientes.
- Gestionar médicos.
- Asignar turnos.
- Cancelar turnos.
- Consultar historial de turnos.

### Límites

El sistema:

- No almacenará historias clínicas.
- No realizará videollamadas.
- No se integrará con obras sociales.
- Será utilizado únicamente en una clínica.

---

# Errores Frecuentes

## Error 1: Confundir problema con solución

Incorrecto:

> Se desarrollará una aplicación web.

Correcto:

> Actualmente la información se registra manualmente generando errores y demoras.

---

## Error 2: Escribir funcionalidades en los objetivos

Incorrecto:

> El objetivo es registrar clientes.

Correcto:

> El objetivo es mejorar la gestión de clientes.

---

## Error 3: Confundir alcance con límites

Incorrecto:

### Alcance

- No tendrá aplicación móvil.

Esto es un límite.

Correcto:

### Límites

- No tendrá aplicación móvil.

---

# Conclusión

La definición del proyecto constituye el punto de partida del análisis de sistemas.

Una correcta definición permite:

- Comprender el problema.
- Conocer el contexto organizacional.
- Establecer objetivos claros.
- Delimitar adecuadamente el alcance.
- Definir los límites del proyecto.

Estos elementos servirán como base para el relevamiento, la identificación de requerimientos y el modelado posterior del sistema.