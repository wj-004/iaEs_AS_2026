# Estimación de Esfuerzo, Costos y Gestión de Proyectos de Software

## Basado en "Ingeniería del Software: Un enfoque práctico" – Roger S. Pressman

---

# 📌 1. Estimación de esfuerzo y costos

La estimación en ingeniería de software busca determinar:

- **Esfuerzo**: cantidad de trabajo requerido (personas/mes)
- **Duración**: tiempo calendario del proyecto
- **Costo**: inversión económica necesaria

### 🔹 Relación fundamental
Costo = Esfuerzo × Costo por recurso

### 🔹 Cómo se realiza la estimación
Se basa en:
- El **tamaño del software**
- La **productividad del equipo**

### 🔹 Métodos de estimación
- Juicio experto
- Analogía con proyectos similares
- Modelos matemáticos (como COCOMO)

### 🔹 Dificultades habituales
- Requisitos incompletos o cambiantes
- Subestimación por optimismo
- Falta de datos históricos

---

# 📌 2. Modelo COCOMO

COCOMO (Constructive Cost Model) es un modelo que estima el esfuerzo a partir del tamaño del software.

### 🔹 Fórmula básica
Esfuerzo = a × (KLOC)^b

Donde:
- **KLOC**: miles de líneas de código
- **a y b**: constantes empíricas según el tipo de proyecto

---

## 🔹 Tipos de proyecto y constantes

| Tipo | Características | a | b |
|------|---------------|---|---|
| Orgánico | Proyectos pequeños, simples, con equipos experimentados | 2.4 | 1.05 |
| Semi-acoplado | Proyectos intermedios, con complejidad moderada | 3.0 | 1.12 |
| Empotrado | Sistemas complejos con restricciones estrictas | 3.6 | 1.20 |

### 🔹 Interpretación
- A mayor complejidad → mayores valores de **a** y **b**
- Esto incrementa el esfuerzo estimado

---

## 🔹 Selección del tipo de proyecto
Se determina según:
- Complejidad del sistema
- Experiencia del equipo
- Restricciones técnicas y operativas

---

## 🔹 COCOMO II
Versión extendida que incorpora factores adicionales mediante multiplicadores, tales como:
- Capacidad del equipo
- Herramientas utilizadas
- Reutilización de software
- Estabilidad de los requisitos

Estos factores ajustan el esfuerzo calculado.

---

# 📌 3. Métricas de software

Las métricas permiten cuantificar el tamaño del software, que es la base de la estimación.

---

## 🔹 Líneas de código (LOC)

Mide la cantidad de líneas del programa.

### Ventajas:
- Fácil de entender
- Directamente utilizable en modelos como COCOMO

### Desventajas:
- Depende del lenguaje
- Difícil de estimar en etapas tempranas

---

## 🔹 Puntos de función (FP)

Miden la funcionalidad del sistema desde el punto de vista del usuario.

### 🔹 Componentes considerados:
- Entradas
- Salidas
- Consultas
- Archivos internos
- Interfaces externas

### 🔹 Procedimiento general:
1. Identificar y contar los componentes
2. Asignar pesos según complejidad
3. Calcular el total de puntos de función

### Ventajas:
- Independiente del lenguaje
- Aplicable en etapas iniciales

### Desventajas:
- Requiere mayor análisis
- Más complejo de calcular

---

## 🔹 Uso de las métricas
Permiten:
- Estimar el tamaño del sistema
- Servir como entrada para modelos de estimación
- Comparar productividad entre proyectos

---

# 📌 4. Planificación y gestión de proyectos

Una vez estimado el esfuerzo, se organiza el desarrollo del proyecto.

---

## 🔹 Planificación

### Actividades principales:
1. Descomposición del sistema en tareas (WBS)
2. Estimación de esfuerzo por tarea
3. Asignación de recursos
4. Definición de dependencias

---

## 🔹 Herramientas de planificación

- Diagramas de Gantt
- Redes PERT/CPM

---

## 🔹 Gestión del proyecto

Incluye:
- Seguimiento del progreso
- Comparación entre lo planificado y lo real
- Gestión de cambios
- Coordinación del equipo

---

## 🔹 Gestión de riesgos

Consiste en:
- Identificar posibles problemas
- Evaluar su impacto
- Definir estrategias de mitigación

---

# 🧠 Conclusión

- La estimación debe basarse en métricas objetivas
- El tamaño del software es la base para estimar esfuerzo
- Modelos como COCOMO permiten sistematizar la estimación
- La planificación organiza el trabajo a partir de esas estimaciones
- La gestión continua permite controlar desviaciones y reducir riesgos



# Ejemplo de estimación de costo con COCOMO

Basado en Ingeniería del Software: Un enfoque práctico – Roger S. Pressman

---

## 📌 Datos del problema

Se desea desarrollar un sistema con las siguientes características:

- Tamaño estimado: 10.000 líneas de código  
- KLOC = 10  
- Tipo de proyecto: orgánico (sistema simple, equipo experimentado)

---

## 📌 Modelo utilizado

COCOMO (Constructive Cost Model)

### Fórmula base:
Esfuerzo = a × (KLOC)^b

Para proyectos orgánicos:
- a = 2.4  
- b = 1.05  

---

## 🧮 Cálculo del esfuerzo

Esfuerzo = 2.4 × (10)^1.05

10^1.05 ≈ 11.22

Esfuerzo ≈ 2.4 × 11.22 = 26.93

---

## 👨‍💻 Resultado

- Esfuerzo aproximado: **27 personas/mes**

Interpretación:
- 1 persona → 27 meses  
- 3 personas → 9 meses  
- 5 personas → ~5–6 meses  

---

## 💰 Estimación de costo

Supongamos un costo mensual por persona de USD 3.000:

Costo = 27 × 3000 = 81.000 USD

---

## 📊 Resumen

| Concepto | Valor |
|----------|------|
| Tamaño | 10 KLOC |
| Esfuerzo | 27 persona/mes |
| Duración | Variable según equipo |
| Costo estimado | USD 81.000 |

---

## 🧠 Conclusión

- El tamaño del software es la base de la estimación
- COCOMO transforma tamaño en esfuerzo
- El esfuerzo permite calcular costo y duración
- Es un modelo aproximado, no exacto
