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
