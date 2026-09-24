# 📡 Líneas y Comunicaciones Ópticas

## 🔬 Análisis y Simulación de Líneas de Transmisión Ideales

![ADS](https://img.shields.io/badge/Software-Keysight%20ADS-red)
![Telecomunicaciones](https://img.shields.io/badge/Programa-Ingenier%C3%ADa%20en%20Telecomunicaciones-blue)
![UMNG](https://img.shields.io/badge/Universidad-UMNG-green)

---

## 📋 Descripción

Este repositorio contiene el desarrollo del laboratorio de **Líneas y Comunicaciones Ópticas**, correspondiente al periodo académico **2026-2** de Ingeniería en Telecomunicaciones de la **Universidad Militar Nueva Granada (UMNG)**.

El proyecto estudia mediante **Keysight Advanced Design System (ADS)** el comportamiento de una línea de transmisión ideal sin pérdidas para dos condiciones de terminación:

🔴 **Cortocircuito (Short Circuit)**
🔵 **Circuito abierto (Open Circuit)**

Se analiza la variación de la **impedancia de entrada, voltaje y corriente** en función de la longitud eléctrica de la línea.

---

## 🎯 Objetivos

### Objetivo general

Analizar mediante simulación el comportamiento de una línea de transmisión ideal sin pérdidas bajo diferentes condiciones de terminación.

### Objetivos específicos

* 🔌 Simular una línea de transmisión terminada en **cortocircuito**.
* 🔓 Simular una línea de transmisión terminada en **circuito abierto**.
* 📈 Analizar la variación de la **reactancia de entrada**.
* ⚡ Analizar la magnitud del **voltaje y la corriente**.
* 📊 Comparar los resultados obtenidos para ambas terminaciones.
* 🔄 Relacionar los resultados de simulación con el comportamiento teórico de la línea.

---

## 🛠️ Herramientas utilizadas

| Herramienta         | Uso                                                    |
| ------------------- | ------------------------------------------------------ |
| 📡 **Keysight ADS** | Diseño y simulación de la línea de transmisión         |
| 📊 **Data Display** | Visualización y análisis de resultados                 |
| 💻 **MATLAB**       | Análisis y representación de resultados, cuando aplica |

---

## ⚙️ Parámetros de simulación

La simulación se realizó utilizando una línea de transmisión ideal **TLIN** con una impedancia característica de **50 Ω**.

| Parámetro                    |     Valor |
| ---------------------------- | --------: |
| ⚡ Fuente AC                  |       2 V |
| 🔧 Resistencia del generador |      50 Ω |
| 📡 Impedancia característica |      50 Ω |
| 📶 Frecuencia                |     1 GHz |
| 🔄 Barrido de `θ`            | 0° – 360° |
| 📐 Incremento                |        1° |

El barrido permite analizar el comportamiento de la línea a lo largo de una longitud de onda completa.

---

## 🔴 1. Terminación en cortocircuito

Para esta configuración, el extremo de la línea de transmisión se conecta directamente a tierra, representando una condición de **cortocircuito**.

Se analizan:

* 📈 Reactancia de entrada.
* ⚡ Magnitud del voltaje.
* 🔌 Magnitud de la corriente.
* 📐 Impedancia de entrada.

La simulación muestra que la impedancia de entrada tiende a **0 Ω** en `0λ`, `0.5λ` y `1λ`, mientras que tiende a valores muy elevados en `0.25λ` y `0.75λ`.

---

## 🔵 2. Terminación en circuito abierto

Para representar el circuito abierto se utiliza una resistencia de valor elevado, del orden de los **megaohmios (MΩ)**.

Los demás parámetros de la simulación se mantienen iguales para permitir una comparación directa entre ambas configuraciones.

En este caso, el comportamiento es complementario al cortocircuito:

* `0λ` → impedancia muy elevada.
* `0.25λ` → impedancia cercana a 0 Ω.
* `0.5λ` → impedancia muy elevada.
* `0.75λ` → impedancia cercana a 0 Ω.

---

## 📊 Comparación de resultados

| Longitud eléctrica | 🔴 Cortocircuito                | 🔵 Circuito abierto             |
| ------------------ | ------------------------------- | ------------------------------- |
| **0λ**             | Z → 0 Ω<br>V mínimo<br>I máximo | Z → ∞ Ω<br>V máximo<br>I mínimo |
| **0.25λ**          | Z → ∞ Ω<br>V máximo<br>I mínimo | Z → 0 Ω<br>V mínimo<br>I máximo |
| **0.5λ**           | Z → 0 Ω<br>V mínimo<br>I máximo | Z → ∞ Ω<br>V máximo<br>I mínimo |
| **0.75λ**          | Z → ∞ Ω<br>V máximo<br>I mínimo | Z → 0 Ω<br>V mínimo<br>I máximo |

Los resultados evidencian un comportamiento complementario entre ambas terminaciones, con un desplazamiento de **λ/4** en los máximos y mínimos de las variables analizadas.

---

## 🌊 Reflexión y ondas estacionarias

En las terminaciones de **cortocircuito** y **circuito abierto** se presenta reflexión total de la onda.

Esto genera la formación de **ondas estacionarias**, produciendo máximos y mínimos de voltaje y corriente a lo largo de la línea.

### 🔴 Cortocircuito

* 📉 Voltaje mínimo.
* 📈 Corriente máxima.
* Γ = −1.

### 🔵 Circuito abierto

* 📈 Voltaje máximo.
* 📉 Corriente mínima.
* Γ = +1.

La diferencia en la fase de la onda reflejada produce el desplazamiento de los máximos y mínimos entre ambas configuraciones.

---

## 📈 Variables analizadas

Durante el desarrollo del laboratorio se obtuvieron gráficas de:

* 📊 Reactancia de entrada vs. longitud eléctrica.
* ⚡ Magnitud de voltaje vs. longitud eléctrica.
* 🔌 Magnitud de corriente vs. longitud eléctrica.
* 🔄 Comparación entre cortocircuito y circuito abierto.

Estas gráficas permiten observar directamente el comportamiento periódico de la línea de transmisión.

---

## 🧠 Conclusiones

La simulación realizada en **Keysight ADS** permitió comprobar el comportamiento de una línea de transmisión ideal sin pérdidas.

Se identificó que la **impedancia de entrada depende de la longitud eléctrica y de la condición de terminación**. Además, las magnitudes de voltaje y corriente presentan comportamientos complementarios.

La comparación entre cortocircuito y circuito abierto permitió identificar un desplazamiento de **λ/4** en los patrones de reactancia, voltaje y corriente, asociado a la reflexión total y a la formación de ondas estacionarias.

---

##  Autores

Harol Felipe Riveros Sierra 

 Ingeniería en Telecomunicaciones
 Universidad Militar Nueva Granada

Miguel Ángel Plazas Llanes

 Ingeniería en Telecomunicaciones
 Universidad Militar Nueva Granada

---

## Docente

**Ing. Gilma Inés Ángel Castillo**

---

## 📚 Asignatura

**Líneas y Comunicaciones Ópticas**

 **Periodo:** 2026-2
 **Universidad Militar Nueva Granada**



