# Estimación de costos en proyectos de software

**Asignatura:** Análisis de Sistemas — 3.er año  
**Tema:** Métodos tradicionales y actuales de estimación de esfuerzo, duración, costos y precios.

## Objetivos de aprendizaje

Al finalizar el tema, se espera que puedas:

- Diferenciar tamaño, esfuerzo, duración, costo y precio de un proyecto.
- Reconocer los principales métodos tradicionales de estimación de software.
- Comprender las técnicas ágiles y los enfoques basados en datos históricos.
- Analizar cómo influye el uso de inteligencia artificial en las estimaciones.
- Elaborar y justificar un presupuesto básico de desarrollo.

---

## 1. ¿Cómo se estima el costo de desarrollar un sistema?

Una empresa necesita un sistema para administrar clientes, productos, stock, ventas y reportes. Antes de contratar el desarrollo, desea conocer **cuánto costará** y **cuándo estará terminado**.

Para responder, es necesario conocer el alcance del proyecto, la complejidad de las funcionalidades, las tecnologías involucradas, los recursos disponibles y los riesgos. A partir de esa información pueden estimarse el esfuerzo, la duración y el costo.

### 1.1. Conceptos fundamentales

| Concepto | Definición | Ejemplo |
|---|---|---|
| **Tamaño** | Magnitud del software que se debe construir. | 20 funcionalidades |
| **Esfuerzo** | Cantidad de trabajo necesaria para completar el proyecto. | 160 horas-persona |
| **Duración** | Tiempo calendario que transcurre hasta la entrega. | 5 semanas |
| **Costo** | Recursos económicos necesarios para realizar el proyecto. | $3.000.000 |
| **Precio** | Importe que se ofrece o cobra al cliente. | $4.000.000 |

**Esfuerzo y duración no son equivalentes.** Un trabajo de 160 horas-persona podría distribuirse entre varios integrantes, pero incorporar más personas no reduce necesariamente el plazo de manera proporcional. Existen dependencias entre tareas y costos de coordinación.

**¿Qué significa «persona-mes»?** Es una unidad de *esfuerzo*: equivale al trabajo de una persona durante un mes laboral. Si se adopta como supuesto un mes de 160 horas, entonces **1 persona-mes = 160 horas-persona**. Un proyecto estimado en 6 personas-mes requiere aproximadamente 960 horas de esfuerzo. Ese trabajo podría repartirse entre varias personas, pero eso no garantiza que la duración se reduzca en la misma proporción.

Del mismo modo, **costo y precio no son equivalentes**. El precio puede incluir una ganancia, una reserva comercial y otras condiciones contractuales.

### 1.2. ¿Qué factores influyen en una estimación?

- Cantidad y complejidad de las funcionalidades.
- Reglas de negocio y requisitos no funcionales, como seguridad y rendimiento.
- Integraciones con servicios o sistemas externos.
- Experiencia y disponibilidad de quienes desarrollan el software.
- Reutilización de componentes, bibliotecas y herramientas existentes.
- Pruebas, documentación, capacitación, despliegue y mantenimiento previsto.
- Incertidumbres, dependencias y posibles cambios en los requisitos.

**Para reflexionar:** ¿dos sistemas con diez pantallas deberían tener necesariamente el mismo costo? Justificá tu respuesta.

---

## 2. Métodos tradicionales de estimación

Los métodos tradicionales buscan construir estimaciones sistemáticas utilizando el tamaño del software, sus características y la experiencia acumulada en proyectos anteriores. Varios de ellos siguen utilizándose en la actualidad.

### 2.1. Líneas de código (LOC y KLOC)

Consiste en estimar cuántas líneas de código serán necesarias para implementar el software.

- **LOC** (*Lines of Code*): líneas de código.
- **KLOC**: miles de líneas de código.

**Ejemplo:** se estima que un sistema tendrá 10.000 líneas de código y que una persona produce, en promedio, 500 líneas terminadas y verificadas por mes.

$$
\text{Esfuerzo} = \frac{10.000\ \text{líneas}}{500\ \text{líneas/persona-mes}} = 20\ \text{personas-mes}
$$

**Ventaja:** es una medida fácil de comprender y puede medirse una vez escrito el código.

**Limitaciones:** depende del lenguaje, los frameworks y las bibliotecas. La cantidad de líneas no representa por sí sola el valor, la calidad ni la dificultad del software.

### 2.2. COCOMO

COCOMO (*Constructive Cost Model*) fue propuesto por Barry Boehm en 1981. Su modelo básico estima el esfuerzo a partir del tamaño previsto del software.

$$
E = a \times (KLOC)^b
$$

Donde:

- **$E$:** esfuerzo estimado, expresado en personas-mes.
- **$KLOC$:** cantidad de miles de líneas de código. Por ejemplo, 10.000 líneas equivalen a **10 KLOC**.
- **$a$:** *coeficiente multiplicador*. Ajusta la escala del esfuerzo estimado según el tipo de proyecto.
- **$b$:** *exponente*. Determina cómo crece el esfuerzo cuando aumenta el tamaño del software. En COCOMO básico es mayor que 1, por lo que el esfuerzo crece más que proporcionalmente al tamaño.

**¿De dónde salen $a$ y $b$?** Son **parámetros empíricos**: números determinados al analizar datos de proyectos de software anteriores. **No los inventa ni los elige libremente el desarrollador.** En COCOMO básico se seleccionan de la siguiente tabla, según la categoría del proyecto:

| Categoría del proyecto | $a$ | $b$ | Características generales |
|---|---:|---:|---|
| **Orgánico** | 2,4 | 1,05 | Proyectos relativamente pequeños, con requisitos conocidos y equipos familiarizados con el tipo de trabajo. |
| **Semiacoplado** (*semidetached*) | 3,0 | 1,12 | Proyectos de complejidad intermedia, con mayor diversidad de requisitos o experiencia en el equipo. |
| **Empotrado** (*embedded*) | 3,6 | 1,20 | Proyectos sujetos a restricciones exigentes de hardware, software, operación o tiempo real. |

**Ejemplo resuelto.** Se estima que un sistema de gestión clasificado como **orgánico** tendrá 10.000 líneas de código.

1. Convertimos a KLOC: $10.000 / 1.000 = 10$ KLOC.
2. Buscamos en la tabla los parámetros del proyecto orgánico: $a = 2,4$ y $b = 1,05$.
3. Reemplazamos en la fórmula:

$$
E = 2,4 \times 10^{1,05} \approx 26,9\ \text{personas-mes}
$$

**Interpretación:** el modelo estima un esfuerzo total equivalente a unos 26,9 meses de trabajo de una persona. **No significa necesariamente que el proyecto tardará 26,9 meses**, porque la duración depende de cómo se organice el equipo, las dependencias entre tareas y otros factores.

**¿Por qué importa $b$?** Si el tamaño se duplica y el exponente es $b = 1,20$, el esfuerzo se multiplica por $2^{1,20} \approx 2,30$, no solamente por 2. Esto representa que los proyectos más grandes pueden incorporar dificultades adicionales de coordinación e integración.

**Importante:** la fórmula, las categorías y los coeficientes de esta sección corresponden a **COCOMO básico (1981)**. Otras variantes, como COCOMO intermedio y **COCOMO II**, emplean ajustes y parámetros diferentes. COCOMO II considera, entre otros factores, la complejidad del producto, la experiencia del equipo, la reutilización y las condiciones de desarrollo.

**Ventaja:** ofrece un procedimiento formal y repetible.

**Limitación:** requiere estimar el tamaño del software, identificar correctamente el tipo de proyecto y reconocer que los coeficientes históricos pueden no representar la productividad del equipo actual sin una calibración apropiada.

### 2.3. Puntos de función (FPA)

La técnica de **Puntos de Función** mide el tamaño funcional del sistema, en lugar de basarse en líneas de código.

Considera distintos tipos de funciones, como entradas, salidas, consultas y archivos lógicos, aplicando reglas específicas de clasificación y ponderación.

Ejemplos de funcionalidades que podrían analizarse:

- Registrar un cliente.
- Registrar una venta.
- Consultar el stock disponible.
- Generar un reporte de ventas.

Una vez calculado el tamaño funcional, puede estimarse el esfuerzo utilizando datos históricos de productividad, por ejemplo, horas por punto de función.

**Ventaja:** permite estimar con menor dependencia del lenguaje de programación.

**Limitación:** exige contar con requisitos suficientemente definidos y aplicar las reglas de medición.

### 2.4. Puntos de casos de uso (UCP)

Los **Puntos de Casos de Uso** parten del modelo de requisitos, considerando los actores, los casos de uso y factores técnicos y ambientales.

Es útil cuando el sistema ya cuenta con casos de uso documentados.

**Ventaja:** aprovecha información elaborada durante el análisis de requisitos.

**Limitación:** depende de la calidad del modelo y de una productividad de referencia apropiada.

### 2.5. Estimación por analogía y juicio de expertos

La **estimación por analogía** compara un nuevo proyecto con otros similares ya realizados. El **juicio de expertos** utiliza la experiencia de profesionales para estimar el esfuerzo.

**Ejemplo:** si un sistema de inventario parecido requirió dos meses de trabajo, ese resultado puede utilizarse como referencia, ajustándolo por diferencias de alcance y complejidad.

**Ventaja:** permite aprovechar experiencias reales.

**Limitación:** las estimaciones pueden estar sesgadas si los proyectos comparados son muy diferentes o si no existen registros confiables.

### 2.6. Comparación de métodos tradicionales

| Método | ¿En qué se basa? | Principal limitación |
|---|---|---|
| LOC / KLOC | Cantidad prevista de código | Depende del lenguaje y las herramientas |
| COCOMO | Tamaño del software y factores de esfuerzo | Requiere supuestos y calibración |
| Puntos de función | Tamaño de la funcionalidad ofrecida | Requiere reglas de conteo y requisitos definidos |
| Puntos de casos de uso | Actores, casos de uso y factores de ajuste | Depende de la calidad del modelado |
| Analogía / expertos | Experiencia y proyectos anteriores | Puede ser subjetivo |

---

## 3. Métodos actuales de estimación

Los métodos modernos no sustituyeron por completo a los tradicionales. En numerosos proyectos se combinan estimaciones iniciales con mediciones del trabajo real y revisiones periódicas del pronóstico.

### 3.1. Story Points: estimación relativa

En algunos equipos ágiles se usan **Story Points** para comparar el esfuerzo relativo de las funcionalidades. Se tienen en cuenta la complejidad, el trabajo y la incertidumbre, según los criterios del equipo.

Una escala frecuente utiliza valores como 1, 2, 3, 5, 8, 13 y 21.

| Funcionalidad | Story Points (ejemplo) |
|---|---:|
| Registro de clientes | 3 |
| Inicio de sesión y roles | 5 |
| Gestión de productos | 8 |
| Facturación electrónica | 13 |

Si un equipo completa aproximadamente 15 puntos por sprint y tiene 30 puntos pendientes, podría prever unos dos sprints, siempre que la productividad y las características del trabajo sigan siendo comparables.

**Importante:** un Story Point no equivale universalmente a una cantidad de horas o de dinero. Los valores son relativos al equipo que los utiliza. Scrum no exige adoptar Story Points.

### 3.2. Estimación basada en métricas de flujo

Este enfoque utiliza datos de tareas realmente terminadas, en lugar de depender solamente de predicciones iniciales.

Algunas métricas son:

- **Throughput:** cantidad de tareas completadas por período.
- **Cycle Time:** tiempo transcurrido desde el inicio de una tarea hasta su finalización.
- **WIP** (*Work in Progress*): cantidad de tareas que están en ejecución.
- **Work Item Age:** tiempo que lleva abierta una tarea que aún no finalizó.

**Ejemplo:** si históricamente se completan cinco tareas comparables por semana y quedan veinte tareas:

$$
\text{Duración aproximada} = \frac{20\ \text{tareas}}{5\ \text{tareas/semana}} = 4\ \text{semanas}
$$

Este resultado representa una aproximación, no una fecha garantizada. Los bloqueos, la variación en complejidad y las dependencias pueden modificar el plazo.

### 3.3. Simulación Monte Carlo

#### ¿Qué es una simulación?

**Simular** significa representar de manera simplificada cómo podría comportarse una situación real. Por ejemplo, antes de construir un puente se puede simular cómo respondería ante distintas cargas. En un proyecto de software podemos simular **cuánto tardaríamos en terminar el trabajo pendiente**.

La **simulación Monte Carlo** consiste en generar muchos escenarios posibles utilizando valores elegidos al azar de acuerdo con unos datos o supuestos. Luego se observa cuántas veces ocurre cada resultado. Así se obtiene un **pronóstico probabilístico**, en lugar de una única fecha supuestamente segura.

El nombre *Monte Carlo* hace referencia al uso del azar en el método. **No significa que se estén adivinando las fechas**: los resultados dependen de los datos utilizados y de los supuestos del modelo.

#### ¿Qué información necesitamos?

Para estimar **cuántas semanas faltan para terminar** un proyecto utilizando tareas completadas por semana, necesitamos:

1. **Trabajo pendiente:** cuántas tareas quedan por finalizar.
2. **Historial de entregas:** cuántas tareas terminó el equipo en semanas anteriores.
3. **Condiciones comparables:** las tareas pendientes deben tener tamaños razonablemente similares a las tareas del historial, y la capacidad del equipo no debería cambiar de manera importante.

No es obligatorio utilizar tareas como unidad. Según el proyecto, también pueden modelarse historias terminadas, elementos de trabajo comparables u otras medidas de entrega.

#### Ejemplo completo: ¿cuándo terminaremos 12 tareas?

Supongamos que un equipo tiene **12 tareas pendientes** y registró las siguientes entregas en sus últimas ocho semanas:

| Semana anterior | Tareas terminadas |
|---|---:|
| 1 | 2 |
| 2 | 3 |
| 3 | 4 |
| 4 | 5 |
| 5 | 3 |
| 6 | 4 |
| 7 | 2 |
| 8 | 5 |

Su rendimiento **no es idéntico todas las semanas**. Algunas veces completa 2 tareas; otras, 3, 4 o 5.

El promedio es:

$$
\text{Promedio semanal}=\frac{2+3+4+5+3+4+2+5}{8}=3{,}5\ \text{tareas/semana}
$$

Si dividimos directamente las 12 tareas pendientes entre ese promedio, obtenemos:

$$
\frac{12}{3{,}5}\approx 3{,}43\ \text{semanas}
$$

Pero **3,43 semanas no es una garantía**. El promedio no muestra cómo podría variar el plazo si aparecen semanas más lentas o más productivas. Ahí es donde sirve Monte Carlo.

#### Paso 1. Simular una semana

Para representar una semana futura, elegimos al azar **uno de los ocho valores históricos**: 2, 3, 4, 5, 3, 4, 2 o 5 tareas.

Por ejemplo, si sale **3**, suponemos que esa semana se terminan 3 tareas. Para representar la semana siguiente, volvemos a elegir al azar entre los mismos ocho valores.

Esta elección se hace **con reposición**: cada semana simulada puede volver a tomar cualquiera de los valores históricos, incluso uno que ya haya aparecido. En este ejemplo, los rendimientos de 2, 3, 4 y 5 tareas tienen la misma frecuencia histórica.

#### Paso 2. Repetir hasta completar las tareas

Se siguen simulando semanas y se acumulan las tareas terminadas. Cuando se alcanzan o superan las 12 tareas pendientes, anotamos **cuántas semanas fueron necesarias**.

Estos son tres escenarios posibles:

| Escenario | Tareas completadas en cada semana simulada | Acumulado | Duración |
|---|---|---:|---:|
| A | 5, 3, 4 | 5 + 3 + 4 = 12 | 3 semanas |
| B | 2, 3, 2, 5 | 2 + 3 + 2 + 5 = 12 | 4 semanas |
| C | 2, 2, 2, 2, 4 | 2 + 2 + 2 + 2 + 4 = 12 | 5 semanas |

Los tres escenarios utilizan valores que aparecieron en el historial. **Ninguno asegura qué ocurrirá realmente**.

#### Paso 3. Ejecutar miles de escenarios

Tres escenarios son insuficientes para estimar probabilidades. Por eso una computadora repite el procedimiento muchas veces, por ejemplo, **10.000 simulaciones**.

El procedimiento lógico es:

```text
Repetir 10.000 veces:
    tareas_terminadas = 0
    semanas = 0

    Mientras tareas_terminadas < 12:
        elegir al azar un valor del historial
        tareas_terminadas = tareas_terminadas + valor_elegido
        semanas = semanas + 1

    guardar semanas como resultado de esta simulación

Contar cuántas simulaciones terminaron en 3, 4, 5, etc. semanas.
```

**Resultado reproducible del ejemplo:** al ejecutar 10.000 simulaciones con los ocho valores anteriores y una semilla aleatoria fija, se obtuvo:

| Duración necesaria | Simulaciones | Porcentaje de simulaciones | Probabilidad acumulada de terminar **dentro** de ese plazo |
|---|---:|---:|---:|
| 3 semanas | 3.063 | 30,63 % | 30,63 % |
| 4 semanas | 5.624 | 56,24 % | 86,87 % |
| 5 semanas | 1.255 | 12,55 % | 99,42 % |
| 6 semanas | 58 | 0,58 % | 100 % |
| **Total** | **10.000** | **100 %** | — |

*Estos porcentajes provienen de una simulación del ejemplo, no de datos de un proyecto real. Si se modifica la secuencia de números aleatorios o se usan otros datos históricos, los resultados de una ejecución pueden variar.*

#### Paso 4. Interpretar los resultados

La última columna es la más útil para planificar:

- **30,63 % dentro de 3 semanas:** aproximadamente 3 de cada 10 simulaciones completaron las 12 tareas en ese plazo.
- **86,87 % dentro de 4 semanas:** casi 9 de cada 10 simulaciones terminaron en 4 semanas o menos.
- **99,42 % dentro de 5 semanas:** prácticamente todas las simulaciones terminaron en 5 semanas o menos.

**¿Por qué no aparece un plazo de 2 semanas?** En este ejemplo, el mayor rendimiento observado fue de 5 tareas por semana. Incluso dos semanas de 5 tareas solo sumarían 10, menos de las 12 necesarias.

Si se necesitara informar al cliente un plazo con al menos **85 % de confianza según el modelo**, se elegirían **4 semanas**, porque la probabilidad acumulada simulada supera el 85 %. Para exigir al menos **95 %**, se elegirían **5 semanas**.

Esto no significa que exista una garantía real del 85 % o del 95 %: son probabilidades **condicionadas a que los datos y supuestos representen razonablemente el trabajo futuro**.

#### Paso 5. Convertir el pronóstico de duración en un costo

Monte Carlo estima aquí **duración**, no dinero directamente. Para obtener un costo necesitamos conocer cuánto cuesta mantener el proyecto en funcionamiento cada semana.

Supongamos:

- Costo del equipo: **$300.000 por semana**.
- Herramientas e infraestructura: **$100.000 en total**, como costo fijo.

Entonces:

$$
\text{Costo estimado}=\text{Semanas}\times\$300.000+\$100.000
$$

| Nivel de confianza buscado | Plazo tomado de la simulación | Costo asociado |
|---|---:|---:|
| Al menos 85 % | 4 semanas | $1.300.000 |
| Al menos 95 % | 5 semanas | $1.600.000 |

Estos importes son **costos hipotéticos**, no precios de venta. Para presupuestar al cliente todavía habría que considerar ganancia, impuestos, riesgos adicionales y las condiciones del contrato.

#### ¿Qué limitaciones tiene Monte Carlo?

Los resultados pueden resultar engañosos cuando los datos no reflejan el proyecto futuro. Por ejemplo:

- Si las tareas pendientes son mucho más complejas que las anteriores, contar tareas sin distinguir tamaños puede producir un pronóstico optimista.
- Si el equipo pierde integrantes o incorpora nuevos desarrolladores, el rendimiento futuro puede cambiar.
- Si una integración externa bloquea varias tareas a la vez, las semanas ya no se comportan necesariamente como observaciones independientes.
- Si el historial no registra semanas con **cero** tareas terminadas, la simulación de este ejemplo nunca contempla una semana completamente bloqueada.
- Si solo tenemos unas pocas observaciones históricas, las probabilidades pueden ser poco representativas.

Por lo tanto, **Monte Carlo no predice el futuro con certeza**. Ayuda a evaluar muchos escenarios posibles y a seleccionar plazos con una confianza explícita, siempre que los supuestos sean razonables.

**Para comprobar que lo entendiste:**

1. ¿Por qué es más informativo decir «86,87 % de probabilidad de terminar dentro de cuatro semanas» que afirmar «el proyecto termina en cuatro semanas»?
2. ¿Qué cambiaría si durante las semanas anteriores hubieran existido varias semanas sin tareas terminadas?
3. Si el cliente necesita una fecha con mayor confianza, ¿convendría usar el plazo de cuatro o el de cinco semanas? ¿Por qué?
4. ¿Por qué el resultado de Monte Carlo no representa directamente el precio que debe pagar el cliente?

### 3.4. Métodos tradicionales y enfoques actuales

| Aspecto | Métodos tradicionales | Enfoques actuales |
|---|---|---|
| Datos habituales | Tamaño del software, requisitos y factores de esfuerzo | Historial de entregas, tareas, capacidades y riesgos |
| Técnicas representativas | LOC, COCOMO, puntos de función | Story Points, métricas de flujo, Monte Carlo |
| Manejo de incertidumbre | Supuestos, intervalos y contingencias | Rangos y probabilidades explícitas |
| Actualización | Ante nuevas fases o cambios relevantes | Frecuente, con datos del desarrollo en curso |

---

## 4. Inteligencia artificial y estimación de costos

Las herramientas de inteligencia artificial pueden acelerar algunas tareas de programación. Sin embargo, desarrollar un sistema incluye otras actividades:

- Relevar y validar requisitos.
- Diseñar la arquitectura y las estructuras de datos.
- Implementar e integrar funcionalidades.
- Revisar el código producido, incluso cuando se genera con IA.
- Ejecutar pruebas, corregir errores y verificar seguridad.
- Preparar el despliegue, la documentación y el mantenimiento.

**Ejemplo hipotético de esfuerzo:**

| Actividad | Sin IA | Con IA |
|---|---:|---:|
| Programación | 50 h | 30 h |
| Otras actividades | 30 h | 30 h |
| Revisión adicional de resultados generados por IA | 0 h | 8 h |
| **Total** | **80 h** | **68 h** |

En este escenario, las horas de programación disminuyeron un **40 %**, pero el esfuerzo total disminuyó un **15 %**.

Esto muestra que **reducir el tiempo de generación de código no implica una reducción idéntica del esfuerzo global**. La productividad debe evaluarse sobre funcionalidades completas, probadas y listas para entregar.

Al estimar un proyecto que usa IA también pueden considerarse suscripciones, consumo de API, infraestructura, tiempo de supervisión y posibles correcciones.

---

## 5. Del esfuerzo al presupuesto

Una estimación técnica del esfuerzo no constituye todavía un presupuesto comercial. Para obtenerlo, se deben incorporar los costos y decidir el margen de ganancia.

### 5.1. Calcular el esfuerzo total

Cuando se utiliza una contingencia porcentual sobre las horas:

$$
\text{Horas presupuestadas} = \text{Horas estimadas} \times (1 + \text{Contingencia})
$$

La contingencia se expresa como decimal: por ejemplo, 20 % equivale a $0{,}20$.

### 5.2. Calcular el costo laboral

$$
\text{Costo laboral} = \text{Horas presupuestadas} \times \text{Costo por hora}
$$

El costo por hora debe reflejar los costos reales del trabajo, no necesariamente el precio de venta de una hora al cliente.

### 5.3. Calcular el costo total

$$
\text{Costo total} = \text{Costo laboral} + \text{Otros costos}
$$

Los otros costos pueden incluir infraestructura, licencias, APIs, servicios externos, herramientas y gastos indirectos.

### 5.4. Definir el precio de venta

Si se desea obtener un **margen de ganancia** sobre el precio final:

$$
\text{Precio de venta} = \frac{\text{Costo total}}{1 - \text{Margen}}
$$

Un margen del 25 % se expresa como $0{,}25$.

**Atención:** margen y recargo no son lo mismo. Agregar un 25 % al costo es un *recargo* del 25 %, pero no produce un margen del 25 % sobre el precio de venta.

Un presupuesto real también debe contemplar impuestos, condiciones de cobro, cambios de alcance, garantías, soporte y mantenimiento, cuando correspondan.

---

## 6. Actividad práctica: estimación y presupuesto de un sistema comercial

### Situación

Una pequeña empresa solicita un sistema web para gestionar sus operaciones comerciales. El alcance inicial incluye:

1. Gestión de clientes.
2. Administración de productos y stock.
3. Registro de ventas.
4. Consultas y reportes.
5. Integración, pruebas y puesta en producción.

Después de analizar el proyecto, se realiza esta estimación preliminar:

| Módulo | Horas estimadas |
|---|---:|
| Clientes | 8 |
| Productos y stock | 16 |
| Ventas | 24 |
| Reportes | 12 |
| Integración, pruebas y despliegue | 20 |
| **Total** | **80** |

**Datos para calcular el presupuesto:**

- Costo interno del trabajo: **$15.000 por hora**.
- Reserva de contingencia: **20 % del esfuerzo estimado**.
- Infraestructura y herramientas: **$60.000 en total**.
- Margen de ganancia deseado: **25 % del precio de venta**.

> Los importes y las horas son hipotéticos y se utilizan con fines educativos; no representan una cotización de mercado.

### Consignas

1. Calculá cuántas horas deben presupuestarse incluyendo la contingencia.
2. Calculá el costo laboral del proyecto.
3. Determiná el costo total, incorporando infraestructura y herramientas.
4. Calculá el precio de venta que permita alcanzar el margen de ganancia solicitado.
5. Explicá qué diferencia habría entre aplicar un margen del 25 % sobre el precio y agregar un recargo del 25 % sobre el costo.
6. Supongamos que el cliente solicita una nueva integración externa que no estaba contemplada. ¿Qué información necesitarías y cómo afectaría la estimación?
7. Indicá al menos tres riesgos que podrían provocar cambios en el esfuerzo o el presupuesto.

---

## 7. Preguntas de repaso

1. ¿Cuál es la diferencia entre tamaño, esfuerzo y duración?
2. ¿Por qué el costo de un proyecto no es necesariamente igual a su precio de venta?
3. ¿Qué desventajas tiene estimar únicamente a partir de líneas de código?
4. ¿Qué diferencia existe entre los puntos de función y los puntos de casos de uso?
5. ¿En qué consiste una estimación por analogía?
6. ¿Por qué los Story Points no deben convertirse directamente a una cantidad fija de horas o dinero?
7. ¿Qué aportan las métricas de flujo cuando ya existe un historial de trabajo?
8. ¿Cómo se obtiene e interpreta una probabilidad del 95 % de finalizar dentro de un plazo mediante Monte Carlo?
9. ¿Por qué el uso de IA no garantiza una reducción proporcional del costo del software?
10. ¿Qué debería hacerse ante un cambio de alcance solicitado por el cliente?

---

## 8. Trabajo de aplicación

Elegí el sistema de tu Trabajo Práctico Final u otro proyecto para el cual dispongas de requisitos suficientemente detallados.

Elaborá una **estimación inicial de desarrollo** que incluya:

1. Descripción breve del sistema y del problema que resuelve.
2. Alcance y listado de módulos o funcionalidades.
3. Método de estimación seleccionado y justificación de la elección.
4. Esfuerzo estimado y duración aproximada.
5. Costos laborales, infraestructura y herramientas.
6. Riesgos, supuestos y contingencia.
7. Precio de venta propuesto y criterio utilizado para calcularlo.
8. Aspectos excluidos del presupuesto y posibles condiciones de mantenimiento.

La estimación debe ser **coherente, verificable y fundamentada**. No se espera un importe exacto, sino un procedimiento que permita comprender y justificar cómo se llegó al resultado.

---

## 9. Bibliografía y recursos

- Boehm, B. W. (1981). *Software Engineering Economics*. Prentice Hall.
- Boehm, B. y otros (2000). *Software Cost Estimation with COCOMO II*. Prentice Hall.
- ISO/IEC 20926:2009. *Software and systems engineering — Software measurement — IFPUG functional size measurement method 2009*.
- Schwaber, K. y Sutherland, J. (2020). [*The Scrum Guide*](https://scrumguides.org/scrum-guide.html).
- [*The Kanban Guide*](https://kanbanguides.org/the-kanban-guide/).
- U.S. Government Accountability Office. [*Cost Estimating and Assessment Guide*](https://www.gao.gov/products/gao-20-195g).
