# Actividades Prácticas: Diagramas de Secuencia UML

## Objetivo

Aplicar los conceptos aprendidos sobre diagramas de secuencia UML identificando:

- Actores
- Participantes
- Mensajes
- Fragmentos combinados (`alt`, `loop`, `opt`)
- Flujo temporal de eventos

Para cada ejercicio se deberá:

1. Identificar los actores.
2. Identificar los participantes internos del sistema.
3. Determinar los mensajes intercambiados.
4. Construir el diagrama de secuencia utilizando Mermaid.
5. Incorporar fragmentos combinados cuando corresponda.

---

# Ejercicio 1: Inicio de Sesión

## Descripción

Un usuario desea acceder al sistema.

### Flujo Principal

1. El usuario ingresa nombre de usuario y contraseña.
2. El sistema recibe las credenciales.
3. El sistema consulta la base de datos.
4. La base de datos valida las credenciales.
5. El sistema permite el acceso.

### Escenario Alternativo

Si las credenciales son incorrectas:

1. La base de datos informa el error.
2. El sistema muestra un mensaje de autenticación fallida.

### Consigna

- Identificar actores y participantes.
- Construir el diagrama de secuencia.
- Utilizar un fragmento `alt` para representar ambas posibilidades.

---

# Ejercicio 2: Compra en Tienda Online

## Descripción

Un cliente realiza una compra a través de una tienda online.

### Flujo Principal

1. El cliente selecciona productos.
2. El sistema verifica el stock.
3. El sistema calcula el total.
4. El cliente confirma la compra.
5. El sistema solicita el procesamiento del pago.
6. El pago es aprobado.
7. El sistema registra la venta.
8. El sistema descuenta el stock.
9. El sistema informa la compra exitosa.

### Escenario Alternativo

Si el pago es rechazado:

1. El sistema cancela la operación.
2. Se informa el error al cliente.

### Consigna

- Construir el diagrama completo.
- Utilizar un fragmento `alt` para el resultado del pago.

---

# Ejercicio 3: Reserva de Turno Médico

## Descripción

Un paciente solicita un turno médico mediante una aplicación.

### Flujo Principal

1. El paciente consulta los turnos disponibles.
2. El sistema consulta la agenda.
3. Se muestran los horarios disponibles.
4. El paciente selecciona un horario.
5. El sistema registra la reserva.
6. El sistema confirma el turno.

### Escenario Alternativo

Si el horario ya fue reservado por otro paciente:

1. El sistema informa que el turno no está disponible.
2. El paciente debe seleccionar otro horario.

### Consigna

- Identificar todos los participantes.
- Modelar la reserva exitosa.
- Utilizar un fragmento `alt` para representar la indisponibilidad del turno.

---

# Ejercicio 4: Préstamo de Libro en Biblioteca

## Descripción

Un socio solicita un libro en una biblioteca.

### Flujo Principal

1. El bibliotecario ingresa el número de socio.
2. El sistema valida la existencia del socio.
3. El bibliotecario selecciona un libro.
4. El sistema verifica disponibilidad.
5. El sistema registra el préstamo.
6. El sistema confirma la operación.

### Escenario Alternativo

Si el libro no se encuentra disponible:

1. El sistema informa que el libro está prestado.
2. No se registra el préstamo.

### Requisito Adicional

Si el socio desea retirar más de un libro:

- El proceso de selección de libros debe repetirse para cada libro solicitado.

### Consigna

- Modelar el escenario completo.
- Utilizar un fragmento `alt` para disponibilidad del libro.
- Utilizar un fragmento `loop` para múltiples libros.

---

# Ejercicio 5: Sistema de Cajero Automático

## Descripción

Un cliente realiza una extracción de dinero.

### Flujo

1. Inserta tarjeta.
2. Ingresa PIN.
3. El cajero valida el PIN con el banco.
4. El banco verifica la cuenta.
5. El cliente solicita una extracción.
6. El banco verifica saldo.
7. Si hay saldo suficiente, autoriza la operación.
8. El cajero entrega el dinero.
9. El sistema registra la transacción.

### Escenarios Alternativos

- PIN incorrecto.
- Saldo insuficiente.

### Consigna

Construir un diagrama de secuencia completo utilizando múltiples fragmentos `alt`.