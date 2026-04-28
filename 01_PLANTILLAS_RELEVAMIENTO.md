
# 1. Planilla de Relevamiento General (vista global)
## Ficha de Relevamiento

- Organización:
- Área:
- Fecha:
- Analista:

### 👥 Usuarios entrevistados
| Nombre | Rol | Área |
|--------|-----|------|

### Procesos relevados
| Proceso | Descripción breve | Responsable |
|---------|------------------|-------------|

### Entradas del sistema
| Entrada | Origen | Formato |
|--------|--------|---------|

### Salidas del sistema
| Salida | Destino | Formato |
|--------|---------|---------|

### Problemas detectados
- 
- 
-

### Observaciones
-


___
# 2. Guía de Entrevista (semi-estructurada)
##  Guía de Entrevista

### Datos
- Entrevistado:
- Rol:
- Fecha:

###  Proceso actual
1. ¿Qué tareas realiza diariamente?
2. ¿Cómo inicia el proceso?
3. ¿Qué herramientas utiliza?
4. ¿Qué información necesita?

###  Problemas
5. ¿Qué problemas encuentra en su trabajo?
6. ¿Qué tareas son más lentas?
7. ¿Qué errores son frecuentes?

### Flujo de información
8. ¿De dónde recibe información?
9. ¿A quién entrega resultados?

### Mejora
10. ¿Qué le gustaría mejorar?
11. ¿Qué haría más rápido su trabajo?

### Notas del analista
-

___

# 3. Cuestionario (para múltiples usuarios)
## Cuestionario de Relevamiento

Marque la opción correcta:

### Rendimiento
¿El sistema actual es lento?
[ ] Nunca  
[ ] A veces  
[ ] Frecuentemente  

### Errores
¿Se producen errores?
[ ] Nunca  
[ ] Ocasionalmente  
[ ] Frecuentemente  

### Información
¿La información es clara?
[ ] Sí  
[ ] No  

### Procesos
¿Hay tareas repetitivas?
[ ] Sí  
[ ] No  

### Sugerencias
¿Qué mejoraría del sistema?
_________________________

# 4. Planilla de Observación Directa
## Observación del proceso

- Proceso observado:
- Usuario:
- Fecha:
- Duración:

### Secuencia de actividades
| Paso | Acción | Tiempo | Problema |
|------|--------|--------|----------|

###  Tiempos muertos
-
-

### Problemas detectados
-
-

### Comentarios del analista
-


___
# 5. Identificación de Problemas (formal)
## Lista de Problemas

| ID | Problema | Impacto | Frecuencia | Área |
|----|----------|---------|------------|------|
| P1 |          | Alto/Medio/Bajo | Alta/Media/Baja | |

### Causa probable
-

___
# 6. Planilla PIECES (Yourdon + Pressman)
## Análisis PIECES

| Categoría | Problema detectado | Ejemplo |
|----------|------------------|---------|
| Performance | | Sistema lento |
| Information | | Datos incorrectos |
| Economics | | Costos altos |
| Control | | Falta de seguridad |
| Efficiency | | Tareas manuales |
| Service | | Mala atención al usuario |

___
# 7. Fuentes de Información
## Fuentes de Información

### 👥 Personas
- Usuarios finales
- Administradores
- Gerentes

### 📄 Documentos
- Formularios
- Reportes
- Planillas Excel

### 🖥️ Sistemas existentes
- Software actual
- Base de datos

### 👀 Observación directa
- Procesos en ejecución





___

# Cómo se conectan todas estas herramientas
Entrevistas + Cuestionarios + Observación
                ↓
        Relevamiento
                ↓
   Identificación de problemas
                ↓
        Análisis PIECES
                ↓
        Requerimientos


___
# EJEMPLO

## 1. Descripción del negocio

El sistema analizado corresponde a un kiosco barrial llamado **“Maxi Kiosco 24”**, ubicado en una zona residencial con tránsito constante de vecinos y estudiantes.

El negocio funciona todos los días de 7:00 a 23:00 y es atendido principalmente por su dueño, aunque ocasionalmente lo ayuda un familiar. Ofrece productos como:

- Bebidas
- Snacks
- Golosinas
- Cigarrillos
- Artículos básicos (pan, leche, etc.)

Actualmente, el kiosco no utiliza ningún sistema informático. Todas las operaciones se realizan de manera manual, basadas en la memoria del dueño y observación directa del stock.

---

## 2. Relevamiento general

- Organización: Maxi Kiosco 24  
- Área: Ventas y control de stock  
- Usuario principal: Dueño  

### Procesos principales

| Proceso           | Descripción                         | Responsable |
|------------------|-------------------------------------|-------------|
| Venta            | Atención al cliente y cobro         | Dueño       |
| Control de stock | Verificación de productos disponibles | Dueño       |
| Reposición       | Compra de productos a proveedores   | Dueño       |

### Entradas del sistema

| Entrada            | Origen    | Formato |
|--------------------|-----------|---------|
| Pedido del cliente | Cliente   | Verbal  |
| Productos comprados| Proveedor | Físico  |

### Salidas del sistema

| Salida             | Destino  | Formato |
|--------------------|----------|---------|
| Producto vendido   | Cliente  | Físico  |
| Cobro              | Dueño    | Dinero  |

---

## 3. Entrevista

**Entrevistado:** Dueño del kiosco  
**Rol:** Responsable total del negocio  

### Preguntas y respuestas relevantes

- ¿Cómo registra las ventas?  
  → “No las registro, todo queda en el momento.”

- ¿Cómo sabe qué productos tiene disponibles?  
  → “Miro las estanterías o me acuerdo.”

- ¿Qué sucede cuando un producto se agota?  
  → “Me doy cuenta cuando un cliente lo pide y no está.”

- ¿Cómo decide qué comprar?  
  → “Cuando veo que falta algo o me lo piden.”

- ¿Qué problemas encuentra en el día a día?  
  → “A veces pierdo ventas porque no tengo lo que me piden.”

- ¿Qué le gustaría mejorar?  
  → “Saber mejor qué tengo y qué me falta.”

---

## 4. Observación del proceso

**Proceso observado:** Venta de productos  

| Paso | Acción                          | Tiempo estimado | Problema detectado                  |
|------|----------------------------------|-----------------|------------------------------------|
| 1    | Cliente solicita producto        | Inmediato       | —                                  |
| 2    | Búsqueda del producto            | 10-30 segundos  | A veces no se encuentra fácilmente |
| 3    | Confirmación de disponibilidad   | Variable        | No hay certeza de stock            |
| 4    | Cobro                            | 10 segundos     | No se registra la venta            |
| 5    | Entrega del producto             | Inmediato       | —                                  |

### Observaciones adicionales

- No existe ningún tipo de registro de ventas.
- El control de stock es visual y depende de la memoria.
- Se detectan momentos de demora cuando el producto no está visible.

---

## 5. Identificación de problemas

| ID | Problema                                      | Impacto | Frecuencia | Área |
|----|-----------------------------------------------|---------|------------|------|
| P1 | No existe registro de ventas                  | Alto    | Alta       | Ventas |
| P2 | No hay control formal de stock                | Alto    | Alta       | Stock |
| P3 | Pérdida de ventas por falta de productos      | Alto    | Media      | Ventas |
| P4 | Dificultad para encontrar productos           | Medio   | Media      | Operación |
| P5 | Dependencia total del conocimiento del dueño  | Alto    | Alta       | General |

### Causas probables

- Ausencia de sistema informático
- Procesos completamente manuales
- Falta de registro histórico de información

---

## 6. Análisis PIECES

| Categoría   | Problema identificado |
|-------------|----------------------|
| Performance | Demora en la búsqueda de productos |
| Information | No existe información de stock ni ventas |
| Economics   | Pérdidas económicas por faltantes |
| Control     | Falta de control sobre ventas y productos |
| Efficiency  | Procesos manuales y repetitivos |
| Service     | Mala experiencia del cliente cuando no hay stock |

---

## 7. Conclusión del relevamiento

El sistema actual presenta múltiples deficiencias principalmente relacionadas con la falta de información y control. La ausencia de registros impide tomar decisiones informadas y genera pérdidas económicas.

Se concluye que existe una clara necesidad de implementar un sistema que permita:

- Registrar ventas
- Controlar stock
- Mejorar la organización de productos
- Reducir pérdidas y mejorar la atención al cliente

Este relevamiento servirá como base para la definición de requerimientos en la siguiente etapa del desarrollo del sistema.
