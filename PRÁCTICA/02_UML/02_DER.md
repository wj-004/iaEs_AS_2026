# Actividad Práctica – Diagrama Entidad-Relación (DER)

## Consigna

A partir del escenario presentado a continuación, elaborar un **Diagrama Entidad-Relación (DER)** que represente conceptualmente la información que necesita gestionar la organización.

El modelo deberá identificar las **entidades**, sus **atributos principales**, las **relaciones existentes entre ellas** y las **cardinalidades correspondientes**.

No se debe diseñar todavía la estructura de tablas de una base de datos. El objetivo es representar el **modelo conceptual de los datos**.

---

# Escenario: Taller Mecánico "El Pistón"

El taller mecánico **El Pistón** se dedica al mantenimiento y reparación de vehículos particulares.

Para solicitar un trabajo, el cliente debe encontrarse registrado. De cada cliente se almacenan su nombre, apellido, DNI, teléfono, correo electrónico y domicilio.

Un cliente puede tener registrados varios vehículos. Cada vehículo pertenece a un único cliente. De los vehículos se registra la patente, marca, modelo, año de fabricación, color y kilometraje actual.

Cuando un cliente lleva un vehículo al taller, se genera una **orden de trabajo**. Cada orden posee un número identificador, fecha de ingreso, kilometraje del vehículo al momento del ingreso, descripción del problema informado por el cliente y estado de la orden. También puede registrarse una fecha estimada y una fecha real de finalización.

Un vehículo puede ingresar al taller en diferentes oportunidades, por lo que puede tener varias órdenes de trabajo a lo largo del tiempo. Cada orden de trabajo corresponde a un único vehículo.

En el taller trabajan varios mecánicos. De cada mecánico se registran su legajo, nombre, apellido, teléfono y especialidad.

Una orden de trabajo puede ser atendida por uno o varios mecánicos y un mismo mecánico puede participar en distintas órdenes de trabajo. Para cada participación interesa registrar la cantidad de horas trabajadas por el mecánico en esa orden.

Durante una reparación pueden realizarse diferentes **servicios**, por ejemplo: cambio de aceite, alineación, cambio de frenos, reparación del motor o diagnóstico electrónico.

De cada servicio se mantiene un código, nombre, descripción y precio de referencia.

Una orden de trabajo puede incluir varios servicios y un mismo tipo de servicio puede realizarse en diferentes órdenes de trabajo. Para cada servicio realizado dentro de una orden se registra el precio efectivamente cobrado y una observación sobre el trabajo efectuado.

Durante los trabajos también pueden utilizarse **repuestos**. De cada repuesto se conoce su código, descripción, marca, precio de venta y cantidad disponible en stock.

Una orden de trabajo puede requerir varios repuestos y un mismo repuesto puede utilizarse en diferentes órdenes. Para cada repuesto utilizado se debe conocer la cantidad empleada y el precio unitario aplicado en ese momento.

Los repuestos son adquiridos a diferentes proveedores. De cada proveedor se registra la razón social, CUIT, teléfono, correo electrónico y domicilio.

Un proveedor puede suministrar diferentes repuestos y un mismo repuesto puede ser comercializado por varios proveedores. El taller necesita conocer qué proveedores pueden suministrar cada repuesto.

Cuando finalizan los trabajos correspondientes a una orden, se determina el importe total considerando los servicios realizados y los repuestos utilizados. Posteriormente, el cliente puede efectuar uno o varios pagos hasta completar el importe adeudado.

De cada pago se registra la fecha, el importe y el medio utilizado, que puede ser efectivo, transferencia, tarjeta u otro medio habilitado.

Una orden de trabajo puede no poseer pagos mientras se encuentra en reparación, pero una vez finalizada puede registrar uno o varios pagos. Cada pago corresponde exclusivamente a una orden de trabajo.

---

# Actividades

A partir del escenario:

1. Identificar las **entidades** necesarias para representar la información.
2. Determinar los **atributos principales** de cada entidad.
3. Identificar un atributo que pueda funcionar como **identificador** de cada entidad.
4. Establecer las **relaciones** existentes entre las entidades.
5. Determinar las **cardinalidades mínimas y máximas** de cada relación.
6. Analizar especialmente las relaciones de tipo **muchos a muchos (N:M)** y determinar si poseen información propia que deba ser representada en el modelo.
7. Elaborar el **Diagrama Entidad-Relación conceptual** completo.

## Importante

El escenario debe analizarse desde el punto de vista de los **datos que necesita conservar el sistema**, no solamente desde las acciones que realizan las personas.

No se solicita:

* Crear tablas.
* Definir tipos de datos SQL.
* Escribir sentencias SQL.
* Diseñar interfaces o pantallas.

La entrega debe representar un **DER conceptual**, indicando claramente entidades, atributos, relaciones y cardinalidades.
