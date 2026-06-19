# Modelado de Procesos (DFD)
# Clase: Diagramas de Flujo de Datos (DFD)

## Asignatura
Análisis de Sistemas

## Unidad
Modelado de Procesos

## Bibliografía base

- Kendall, K. & Kendall, J. (2011). *Análisis y Diseño de Sistemas*.
- Yourdon, E. (1989). *Análisis Estructurado Moderno*.
- Pressman, R. (2010). *Ingeniería del Software*.

---

# Objetivos de la clase

Al finalizar la clase, el alumno será capaz de:

- Comprender el propósito de un DFD.
- Identificar los elementos que lo componen.
- Diferenciar Diagrama de Contexto, DFD Nivel 0 y DFD Nivel 1.
- Aplicar las reglas de construcción propuestas por el análisis estructurado.
- Construir diagramas coherentes y balanceados.
- Utilizar el DFD como herramienta de análisis y comunicación.

---

# 1. Introducción

Uno de los principales objetivos del análisis de sistemas es comprender cómo circula la información dentro de una organización.

Para ello se utilizan los Diagramas de Flujo de Datos (DFD), una técnica desarrollada dentro del análisis estructurado que permite representar:

- El movimiento de la información.
- Los procesos que transforman datos.
- Los almacenes donde se guarda información.
- Las entidades que interactúan con el sistema.

---

## ¿Qué es un DFD?

Un Diagrama de Flujo de Datos es una representación gráfica que muestra:

> Cómo los datos ingresan al sistema, cómo son procesados, dónde se almacenan y cómo salen del sistema.

---

## ¿Qué NO muestra un DFD?

Un DFD no representa:

- Algoritmos
- Código fuente
- Decisiones lógicas
- Estructuras de programación
- Interfaces gráficas

Para eso existen otras herramientas.

---

# 2. Objetivos del DFD

Los DFD permiten:

- Comprender sistemas complejos.
- Documentar sistemas existentes.
- Diseñar nuevos sistemas.
- Detectar redundancias y problemas.
- Facilitar la comunicación entre usuarios y analistas.

---

# 3. Componentes del DFD

Un DFD está compuesto por cuatro elementos fundamentales.

---

## 3.1 Procesos

Representan transformaciones de datos.

Reciben información de entrada y generan información de salida.

### Ejemplos

- Registrar Cliente
- Emitir Factura
- Generar Reporte

---

### Regla fundamental

Todo proceso debe tener:

- Al menos una entrada.
- Al menos una salida.

---

### Incorrecto

```text
Cliente → Registrar Cliente
```

No existe salida.

---

### Correcto

```text
Cliente → Registrar Cliente → Cliente Registrado
```

---

## 3.2 Flujos de datos

Representan información que circula entre componentes.

---

### Ejemplos

```text
Pedido
Factura
Datos del Cliente
Comprobante
```

---

### Regla

Todo flujo debe tener:

- Origen
- Destino

---

## 3.3 Entidades externas

Son personas, organizaciones o sistemas que interactúan con el sistema.

---


### Características

- Se encuentran fuera del sistema.
- Generan o reciben información.

---

## 3.4 Almacenes de datos

Representan lugares donde se guarda información.

---


# 4. Reglas de construcción

Según Yourdon y Kendall:

---

## Regla 1

Todo proceso debe transformar datos.

---

### Incorrecto

```text
Pedido → Proceso → Pedido
```

No existe transformación.

---

## Regla 2

No pueden existir flujos sin origen o destino.

---

## Regla 3

No puede existir comunicación directa entre entidades externas.

---

### Incorrecto

```text
Cliente → Proveedor
```

---

## Regla 4

No puede existir comunicación directa entre almacenes.

---

### Incorrecto

```text
CLIENTES → FACTURAS
```

---

## Regla 5

Todo flujo debe tener nombre.

---

### Incorrecto

```text
Cliente ─────►
```

---

### Correcto

```text
Cliente ── Pedido ──►
```

---

# 5. Niveles de los DFD

Los DFD se construyen jerárquicamente.

---

## Nivel 1: Diagrama de Contexto

Representa al sistema como una única caja negra.

Su objetivo es definir:

- El límite del sistema.
- Las entidades externas.
- Los principales flujos de entrada y salida.

---


## Características

- Un único proceso.
- No existen almacenes.
- No existen procesos internos.

---

# 6. DFD Nivel 0

El Nivel 0 descompone el sistema en procesos principales.


---

## Características

- Aparecen procesos internos.
- Aparecen almacenes.
- Se mantiene el mismo límite definido en el contexto.

---

# 7. DFD Nivel 1

Consiste en descomponer uno de los procesos del Nivel 0.

---

# 8. Balanceo de diagramas

El balanceo garantiza la consistencia entre niveles.

---

## Regla

Todo flujo que entra o sale de un proceso en un nivel debe aparecer en su descomposición.

---


## Error de balanceo

Nivel 0:

```text
Cliente → Registrar Pedido
```

Nivel 1:

```text
No aparece Cliente
```

Esto rompe el balanceo.

---

# 9. Metodología para construir un DFD

---

## Paso 1

Identificar entidades externas.

Preguntas:

- ¿Quién utiliza el sistema?
- ¿Quién envía información?
- ¿Quién recibe información?

---

## Paso 2

Construir el Diagrama de Contexto.

---

## Paso 3

Identificar procesos principales.

---

## Paso 4

Construir el Nivel 0.

---

## Paso 5

Agregar almacenes de datos.

---

## Paso 6

Descomponer procesos complejos.

---

## Paso 7

Verificar balanceo.

---

## Paso 8

Documentar mediante Diccionario de Datos.

---

# Preguntas de cierre

1. ¿Qué diferencia existe entre un DFD y un diagrama de flujo?
2. ¿Qué diferencia existe entre Diagrama de Contexto y Nivel 0?
3. ¿Qué función cumple el balanceo?
4. ¿Qué elementos componen un DFD?
5. ¿Qué relación existe entre el DFD y el Diccionario de Datos?

