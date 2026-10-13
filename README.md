# sprint7-final-project
# 📞 ConnectaTel: Análisis de Uso y Segmentación de Clientes

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es realizar un análisis exploratorio de datos (EDA) integral para **ConnectaTel**, evaluando el comportamiento de uso de sus clientes de telecomunicaciones en Colombia y México. A través de la limpieza de datos, el perfilamiento estadístico y la segmentación estratégica, se identificaron patrones de consumo clave para respaldar decisiones comerciales y de fidelización.

---

## 📊 Datasets Utilizados
El análisis se fundamenta en tres datasets principales:
1. `plans.csv`: Información sobre los planes ofrecidos (Básico y Premium), tarifas e inclusiones.
2. `users_latam.csv`: Datos demográficos de los clientes (edad, ciudad, fecha de registro, tipo de plan y fecha de cancelación/churn).
3. `usage.csv`: Registro histórico de interacciones de los usuarios (duración de llamadas y cantidad de mensajes de texto).

---

## 🛠️ Etapas del Análisis Realizadas

1. **Carga y Exploración Inicial:** Inspección estructural y evaluación del estado inicial de los datos (`info()`, `shape`).
2. **Identificación de Calidad de Datos:** Detección de valores nulos, valores centinela (`-999` en edad, `?` en ciudad) y fechas futuras fuera del rango del estudio (posteriores a 2024).
3. **Limpieza y Estandarización:**
   * Imputación de centinelas de edad mediante la mediana.
   * Tratamiento de valores `?` y fechas imposibles convirtiéndolos a valores nulos válidos.
   * Confirmación y manejo de nulos tipo **MAR (Missing At Random)** en métricas de consumo de llamadas vs. mensajes.
4. **Agrupación y Perfil de Usuario:** Creación del DataFrame `user_profile` consolidando métricas de mensajes, número de llamadas y minutos totales consumidos por usuario.
5. **Visualización y Detección de Outliers:** Análisis de distribuciones mediante histogramas y boxplots con la regla del Rango Intercuartílico (IQR), optando por mantener a los *power users* para conservar representatividad comercial.
6. **Segmentación de Clientes:**
   * **Por nivel de uso:** Clasificación en `Bajo uso`, `Uso medio` y `Alto uso`.
   * **Por grupo de edad:** Clasificación en `Joven`, `Adulto` y `Adulto Mayor`.
7. **Insights Ejecutivos:** Formulación de conclusiones estratégicas y recomendaciones dirigidas a los stakeholders.

---

## 💻 Requisitos y Guía de Reproducción

### Requisitos Previos
* Python 3.8+
* Librerías: `pandas`, `numpy`, `matplotlib`, `seaborn`

### Pasos para Ejecutar Localmente
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITTORIO.git](https://github.com/TU_USUARIO/TU_REPOSITTORIO.git)
   cd TU_REPOSITORIO
