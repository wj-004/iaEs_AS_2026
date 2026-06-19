# Diccionario de Datos (DD)

---

# Objetivos de la clase

Al finalizar la clase, el alumno será capaz de:

- Comprender qué es un Diccionario de Datos.
- Reconocer su importancia dentro del análisis de sistemas.
- Documentar correctamente flujos de datos, estructuras de datos y elementos de datos.
- Relacionar el Diccionario de Datos con los DFD.
- Construir un Diccionario de Datos a partir de un caso práctico.

---

# 1. Introducción

Durante el modelado de procesos mediante Diagramas de Flujo de Datos (DFD), aparecen numerosos flujos de información entre procesos, entidades externas y almacenes de datos.

Sin embargo, el DFD únicamente muestra el nombre de dichos flujos, sin explicar detalladamente qué información contienen.

Por este motivo surge el Diccionario de Datos.

---

# 2. ¿Qué es un Diccionario de Datos?

El Diccionario de Datos es un catálogo que describe de manera detallada todos los datos utilizados por un sistema.

Su objetivo es eliminar ambigüedades y asegurar que todos los participantes del proyecto comprendan exactamente el significado de cada dato.

---

## Definición

> Un Diccionario de Datos es una colección organizada de definiciones que describen el contenido, estructura y significado de los datos que circulan o se almacenan dentro de un sistema.

---

# 3. ¿Para qué sirve?

Permite:

- Estandarizar nombres.
- Evitar interpretaciones incorrectas.
- Documentar el sistema.
- Facilitar el diseño de bases de datos.
- Facilitar el mantenimiento futuro.
- Verificar la consistencia de los DFD.

---

# 4. Relación con el DFD

Un DFD responde:

> ¿Cómo fluye la información?

Mientras que el Diccionario de Datos responde:

> ¿Qué contiene esa información?

---

## Ejemplo

En un DFD aparece el flujo:

```text
Pedido
```

El DFD no explica qué es un pedido.

El Diccionario de Datos sí lo hace:

```text
Pedido =
    Número de Pedido +
    Fecha +
    Cliente +
    Importe Total
```

---

# 5. Elementos del Diccionario de Datos

El Diccionario de Datos describe:

- Flujos de datos
- Estructuras de datos
- Elementos de datos
- Almacenes de datos

---

# 6. Elementos de datos

Son los datos más simples que no pueden descomponerse.

---

## Ejemplos

```text
Nombre
Apellido
DNI
Fecha
Saldo
Precio
Cantidad
```

---

## Características

- Son atómicos.
- Tienen significado propio.
- Constituyen la base de estructuras más complejas.

---

# 7. Estructuras de datos

Una estructura de datos está compuesta por varios elementos de datos.

---

## Ejemplo

```text
Cliente =
    DNI +
    Apellido +
    Nombre +
    Dirección +
    Teléfono
```

---

## Otro ejemplo

```text
Producto =
    Código +
    Descripción +
    Precio
```

---

# 8. Flujos de datos

Representan información que circula entre procesos.

Cada flujo debe estar documentado.

---

## Ejemplo

En el DFD:

```text
Datos del Cliente
```

En el Diccionario:

```text
Datos del Cliente =
    DNI +
    Apellido +
    Nombre +
    Dirección +
    Teléfono
```

---

# 9. Almacenes de datos

También pueden documentarse.

---

## Ejemplo

```text
CLIENTES =
    Datos del Cliente
```

---

## Otro ejemplo

```text
PEDIDOS =
    Pedido
```

---

# 10. Notación utilizada

La bibliografía clásica propone símbolos para describir estructuras.

---

## Concatenación

Símbolo:

```text
+
```

Significa:

"y"

Ejemplo:

```text
Cliente =
    DNI +
    Nombre +
    Apellido
```

---

## Selección

Símbolo:

```text
()
```

Representa alternativas.

Ejemplo:

```text
TipoPago =
    (Contado | Cuenta Corriente)
```

---

## Repetición

Símbolo:

```text
{}
```

Representa uno o varios elementos.

Ejemplo:

```text
Pedido =
    Número +
    Fecha +
    {Detalle}
```

---

## Elemento opcional

Símbolo:

```text
[]
```

Ejemplo:

```text
Cliente =
    DNI +
    Nombre +
    [Correo Electrónico]
```

---

# 11. Metodología para construir un Diccionario de Datos

## Paso 1

Identificar todos los flujos del DFD.

Ejemplo:

```text
Pedido
Factura
Pago
Datos del Cliente
```

---

## Paso 2

Definir qué contiene cada flujo.

Ejemplo:

```text
Factura =
    Número +
    Fecha +
    Cliente +
    Importe
```

---

## Paso 3

Descomponer estructuras complejas.

Ejemplo:

```text
Cliente =
    DNI +
    Nombre +
    Apellido +
    Dirección
```

---

## Paso 4

Definir elementos simples.

Ejemplo:

```text
DNI
Nombre
Apellido
Dirección
```

---

## Paso 5

Verificar consistencia.

Preguntarse:

- ¿Todos los flujos del DFD están documentados?
- ¿Todos los nombres son claros?
- ¿Existen duplicaciones?

---

# 12. Ejemplo completo

## Caso: Sistema de cuentas corrientes

---

### Flujo

```text
Movimiento
```

---

### Diccionario

```text
Movimiento =
    Fecha +
    TipoMovimiento +
    Importe +
    Observación
```

---

### Flujo

```text
Cliente
```

---

### Diccionario

```text
Cliente =
    CódigoCliente +
    Apellido +
    Nombre +
    Dirección +
    Teléfono
```

---

### Flujo

```text
Cuenta Corriente
```

---

### Diccionario

```text
Cuenta Corriente =
    Cliente +
    {Movimiento}
```

---

# 13. Ejemplo aplicado al DFD

Supongamos el siguiente flujo:

```text
Solicitud de Turno
```

---

## Diccionario

```text
Solicitud de Turno =
    Fecha +
    Hora +
    Paciente +
    Especialidad
```

---

## Paciente

```text
Paciente =
    DNI +
    Apellido +
    Nombre +
    Teléfono
```

---

# 14. Relación con la Base de Datos

El Diccionario de Datos ayuda posteriormente a:

- Diseñar entidades.
- Identificar atributos.
- Construir el DER.
- Construir tablas.

Ejemplo:

```text
Cliente =
    DNI +
    Apellido +
    Nombre
```

Posteriormente:

```text
CLIENTE
--------
dni
apellido
nombre
```

---

# 15. Errores frecuentes

## Error 1

Documentar solamente algunos flujos.

Incorrecto:

```text
Pedido
```

Correcto:

Todos los flujos del DFD deben estar definidos.

---

## Error 2

Usar nombres ambiguos.

Incorrecto:

```text
Información
Datos
Archivo
```

Correcto:

```text
Datos del Cliente
Datos de Facturación
Movimiento de Cuenta
```

---

## Error 3

No descomponer estructuras complejas.

Incorrecto:

```text
Cliente
```

Correcto:

```text
Cliente =
    DNI +
    Nombre +
    Apellido
```

---

# Actividad práctica

## Caso

Una veterinaria desea informatizar el registro de consultas.

El DFD posee los siguientes flujos:

```text
Mascota
Consulta
Veterinario
```

---

## Consigna

Construir el Diccionario de Datos para:

- Mascota
- Consulta
- Veterinario

---

# Posible solución

```text
Mascota =
    CódigoMascota +
    Nombre +
    Especie +
    Raza +
    FechaNacimiento
```

```text
Veterinario =
    Matrícula +
    Apellido +
    Nombre +
    Especialidad
```

```text
Consulta =
    Fecha +
    Diagnóstico +
    Tratamiento +
    Mascota +
    Veterinario
```

---

# Preguntas de cierre

1. ¿Cuál es la diferencia entre un DFD y un Diccionario de Datos?
2. ¿Qué información aporta el Diccionario que no aparece en el DFD?
3. ¿Qué es un elemento de dato?
4. ¿Qué es una estructura de datos?
5. ¿Por qué es importante documentar todos los flujos?

---

# Conclusión

El Diccionario de Datos complementa a los Diagramas de Flujo de Datos proporcionando una descripción precisa y estandarizada de la información utilizada por el sistema.

Mientras el DFD muestra cómo circulan los datos, el Diccionario de Datos describe exactamente qué contienen esos datos, convirtiéndose en una herramienta fundamental para el análisis, el diseño de bases de datos y la documentación del sistema.