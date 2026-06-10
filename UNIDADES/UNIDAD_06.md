# Requerimientos de Sistemas

## Objetivos de la clase

Al finalizar la clase, el alumno será capaz de:

- Comprender qué es un requerimiento y cuál es su función dentro del desarrollo de sistemas.
- Diferenciar requerimientos funcionales y no funcionales.
- Identificar el origen de los requerimientos.
- Aplicar una metodología para obtener requerimientos a partir del relevamiento.
- Redactar requerimientos de forma clara y verificable.
- Relacionar requerimientos con el problema, los objetivos y los modelos del sistema.

---

# 1. Introducción

Uno de los errores más comunes en el desarrollo de sistemas es comenzar a diseñar o programar sin comprender correctamente qué necesita el usuario.

Los requerimientos constituyen el puente entre el problema detectado y la solución que se desarrollará.

Todo sistema existe para satisfacer una necesidad. Los requerimientos describen de manera precisa qué debe hacer el sistema y bajo qué condiciones debe operar.

---

# 2. ¿Qué es un requerimiento?

Un requerimiento es una condición o capacidad que debe poseer un sistema para satisfacer una necesidad del usuario o resolver un problema identificado.

En términos simples:

> Un requerimiento describe algo que el sistema debe hacer o una característica que debe cumplir.

---

# 3. ¿De dónde surgen los requerimientos?

Los requerimientos no se inventan.

Se obtienen a partir del análisis de la situación actual.

## Flujo general

```text
Problema
    ↓
Relevamiento
    ↓
Análisis del sistema actual
    ↓
Identificación de problemas
    ↓
Definición de objetivos
    ↓
Requerimientos
```

---

# 4. Fuentes de requerimientos

Los requerimientos pueden surgir de múltiples fuentes.

## Usuarios

Son quienes utilizan el sistema.

Ejemplos:

- Operarios
- Administrativos
- Gerentes
- Clientes

---

## Observación directa

Permite conocer cómo se realizan realmente las tareas.

Muchas veces existe diferencia entre:

- Lo que el usuario dice que hace.
- Lo que realmente hace.

---

## Documentación existente

Ejemplos:

- Formularios
- Planillas Excel
- Informes
- Procedimientos escritos

---

## Sistemas existentes

Cuando existe un sistema anterior.

Permite identificar:

- Funciones útiles
- Problemas actuales
- Oportunidades de mejora

---

# 5. Relación entre problema, objetivo y requerimiento

Es importante comprender que los requerimientos no aparecen aislados.

## Ejemplo

### Problema

La empresa registra pagos en cuadernos.

### Consecuencia

Se producen errores y pérdidas de información.

### Objetivo

Mejorar el control de pagos.

### Requerimiento

RF01:
El sistema deberá permitir registrar pagos realizados por los clientes.

---

# 6. Tipos de requerimientos

Los requerimientos se clasifican principalmente en:

- Funcionales
- No funcionales

---

# 7. Requerimientos funcionales

Describen qué debe hacer el sistema.

Representan funcionalidades.

---

## Ejemplos

RF01:
El sistema deberá permitir registrar clientes.

RF02:
El sistema deberá permitir registrar pagos.

RF03:
El sistema deberá permitir consultar el saldo de un cliente.

RF04:
El sistema deberá generar reportes de deuda.

---

## Características

Un requerimiento funcional:

- Describe una función.
- Produce una acción observable.
- Puede verificarse mediante pruebas.

---

# 8. Requerimientos no funcionales

Describen restricciones o condiciones que debe cumplir el sistema.

No indican qué hace el sistema.

Indican cómo debe comportarse.

---

## Categorías frecuentes

### Rendimiento

RNF01:
El sistema deberá responder en menos de 3 segundos.

---

### Seguridad

RNF02:
El acceso deberá requerir autenticación mediante usuario y contraseña.

---

### Disponibilidad

RNF03:
El sistema deberá estar disponible durante el horario comercial.

---

### Usabilidad

RNF04:
La interfaz deberá permitir realizar las operaciones principales en un máximo de tres pasos.

---

### Tecnológicos

RNF05:
La información deberá almacenarse en una base de datos relacional.

---

# 9. Cómo redactar requerimientos

Un requerimiento debe ser:

- Claro
- Preciso
- Completo
- Verificable
- Sin ambigüedades

---

## Redacción recomendada

Utilizar la estructura:

```text
El sistema deberá...
```

---

## Correcto

RF01:
El sistema deberá permitir registrar clientes.

---

## Incorrecto

RF01:
El sistema debería registrar clientes fácilmente.

Problemas:

- No es verificable.
- La palabra "fácilmente" es subjetiva.

---

# 10. Metodología para obtener requerimientos

## Paso 1: Relevar

Preguntas típicas:

- ¿Qué tareas realiza?
- ¿Qué información utiliza?
- ¿Qué documentos genera?
- ¿Qué problemas encuentra?

Resultado:

Descripción del sistema actual.

---

## Paso 2: Identificar problemas

Preguntas típicas:

- ¿Qué demora más tiempo?
- ¿Qué genera errores?
- ¿Qué información es difícil de obtener?

Resultado:

Lista de problemas.

---

## Paso 3: Definir objetivos

Preguntas típicas:

- ¿Qué se quiere mejorar?
- ¿Qué se quiere controlar?
- ¿Qué se quiere automatizar?

Resultado:

Objetivos del sistema.

---

## Paso 4: Derivar requerimientos

Preguntarse:

¿Qué debe hacer el sistema para alcanzar los objetivos?

Resultado:

Requerimientos funcionales.

---

## Paso 5: Identificar restricciones

Preguntarse:

¿Qué condiciones debe cumplir?

Resultado:

Requerimientos no funcionales.

---

# 11. Ejemplo completo

## Caso

Una ferretería lleva las cuentas corrientes de los clientes en un cuaderno.

---

## Problemas detectados

- Errores de cálculo.
- Dificultad para conocer saldos.
- Información repetida.
- Pérdida de registros.

---

## Objetivo general

Mejorar el control de cuentas corrientes de clientes.

---

## Objetivos específicos

- Registrar movimientos.
- Consultar saldos.
- Generar reportes.

---

## Requerimientos funcionales

RF01:
El sistema deberá permitir registrar clientes.

RF02:
El sistema deberá permitir registrar débitos.

RF03:
El sistema deberá permitir registrar créditos.

RF04:
El sistema deberá calcular automáticamente el saldo de cada cliente.

RF05:
El sistema deberá emitir reportes de deuda.

---

## Requerimientos no funcionales

RNF01:
El acceso deberá requerir usuario y contraseña.

RNF02:
La información deberá almacenarse en una base de datos.

RNF03:
El sistema deberá responder en menos de tres segundos.

RNF04:
La interfaz deberá estar disponible en idioma español.

---

# 12. Relación con el resto del análisis

Los requerimientos son la base para construir los modelos posteriores.

```text
Problema
    ↓
Relevamiento
    ↓
Análisis
    ↓
Objetivos
    ↓
Requerimientos
    ↓
DFD
    ↓
DER
    ↓
Diseño
    ↓
Implementación
```

---

# 13. Actividad práctica

## Consigna

Una veterinaria registra las consultas en planillas de papel.

Problemas detectados:

- Dificultad para encontrar historiales.
- Pérdida de fichas.
- Demoras en la atención.

Objetivo:

Mejorar la gestión de consultas médicas.

---

## Actividad

Identificar:

1. Tres requerimientos funcionales.
2. Tres requerimientos no funcionales.

---

## Posible solución

### Requerimientos funcionales

RF01:
El sistema deberá permitir registrar mascotas.

RF02:
El sistema deberá permitir registrar consultas médicas.

RF03:
El sistema deberá permitir consultar el historial clínico de una mascota.

---

### Requerimientos no funcionales

RNF01:
El acceso deberá requerir autenticación.

RNF02:
La información deberá almacenarse en una base de datos.

RNF03:
El sistema deberá responder en menos de tres segundos.

---

# 14. Preguntas para cierre

1. ¿Qué diferencia existe entre un problema y un requerimiento?
2. ¿De dónde surgen los requerimientos?
3. ¿Qué diferencia hay entre requerimientos funcionales y no funcionales?
4. ¿Por qué los requerimientos deben ser verificables?
5. ¿Qué consecuencias puede tener un requerimiento ambiguo?
