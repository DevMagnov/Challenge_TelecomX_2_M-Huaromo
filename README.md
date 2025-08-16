# 📡 Análisis de Abandono de Clientes - TelecomX

## 🧾 Descripción del Proyecto

Este proyecto se enfoca principalmente en el análisis de evación de clientes (churn) en una empresa de telecomunicaciones llamada **TelecomX**. El objetivo principal es desarrollar un flujo completo de trabajo que abarque desde la **extracción de datos desde una API**, hasta la **limpieza, transformación, análisis exploratorio y visualización**. Finalmente obtener conocimiento relevante que ayude a la emprersa elaborar un plan de acción para reducir la tasa de abandono de clentes.

---

## 🎯 Objetivos

El objetivo principal de este proyecto es **analizar la cancelación de clientes** en una empresa de telecomunicaciones, identificando los factores más relevantes que influyen en la decisión de abandono y proponiendo estrategias de retención basadas en evidencia.

### Objetivos específicos:

1. **Exploración de Datos**  
   - Comprender la distribución de clientes activos y cancelados.  
   - Evaluar la existencia de desbalance de clases en la variable objetivo (cancelación).  

2. **Preprocesamiento de Datos**  
   - Tratamiento de valores nulos y codificación de variables categóricas.  
   - Aplicación de técnicas de balanceo (oversampling, undersampling, SMOTE) cuando sea necesario.  
   - Evaluar la necesidad de normalización/estandarización para modelos sensibles a la escala.  

3. **Análisis Exploratorio**  
   - Visualizar correlaciones entre variables numéricas y la cancelación.  
   - Identificar patrones en variables clave como tiempo de contrato, gasto total y método de pago.  

4. **Modelado Predictivo**  
   - Construcción y evaluación de modelos supervisados (ej. Regresión Logística, KNN, Random Forest, SVM).  
   - Comparar métricas de desempeño: Exactitud, Precisión, Recall, F1-score y matriz de confusión.  

5. **Interpretación de Resultados**  
   - Determinar las variables más influyentes en la cancelación (coeficientes, importancia de variables).  
   - Identificar señales tempranas de riesgo de cancelación.  

6. **Estrategias de Negocio**  
   - Proponer acciones de retención basadas en los hallazgos del análisis, tales como:  
     - Incentivar contratos de mayor permanencia.  
     - Mejorar la experiencia de clientes de alto gasto con onboarding y soporte.  
     - Promover el uso de métodos de pago automáticos.  
     - Ofrecer bundles de servicios que aumenten el valor percibido.  

---
📌 Este proyecto combina **análisis exploratorio**, **técnicas de machine learning** y **estrategia de negocio** para abordar un problema clave en la industria de telecomunicaciones: **la retención de clientes**.

---

## 📦 Estructura del Dataset

Los datos extraídos contienen información demográfica, de servicios contratados, comportamiento de pago y abandono. A continuación se presenta la estructura del dataset:

| Columna                | Tipo de Dato | Descripción                                       |
|------------------------|--------------|---------------------------------------------------|
| `Id_Cliente`           | object       | Identificador único del cliente                   |
| `Abandono`             | int64        | Indicador de abandono (1 = sí, 0 = no)            |
| `Genero`               | object       | Género del cliente                                |
| `Adulto_Mayor`         | int64        | Si el cliente es adulto mayor (1 = sí)            |
| `Con_Pareja`           | int64        | Estado civil (1 = con pareja)                     |
| `Dependientes`         | int64        | Si tiene dependientes (1 = sí)                    |
| `Antiguedad`           | int64        | Meses de antigüedad como cliente                  |
| `Servicio_Telefonico`  | int64        | Si tiene servicio telefónico (1 = sí)             |
| `Lineas_Multiples`     | object       | Indica si tiene múltiples líneas telefónicas      |
| `Internet_Tipo`        | object       | Tipo de conexión a internet                       |
| `Seguridad_Linea`      | object       | Servicio de seguridad en línea contratado         |
| `Respaldo_Linea`       | object       | Servicio de respaldo de datos contratado          |
| `Proteccion_Equipo`    | object       | Protección para equipos contratada                |
| `Soporte_Tecnico`      | object       | Servicio de soporte técnico contratado            |
| `Tv_Streaming`         | object       | Acceso a TV por streaming                         |
| `Peliculas_Streaming`  | object       | Acceso a películas por streaming                  |
| `Tipo_Contrato`        | object       | Tipo de contrato (mensual, anual, etc.)           |
| `Factura_Digital`      | int64        | Si recibe factura digital                         |
| `Metodo_Pago`          | object       | Método de pago utilizado                          |
| `Cargo_Mensual`        | float64      | Monto mensual que paga el cliente                 |
| `Cargo_Total`          | float64      | Total facturado durante su tiempo como cliente    |
| `Cargo_Diario`         | float64      | Estimación del cargo diario                       |

---

## 🛠️ Proceso del Proyecto

### 1. Extracción de Datos
- Conexión a la API de TelecomX.
- Conversión de los datos en formato JSON a un DataFrame de pandas.

### 2. Limpieza de Datos
- Revisión y tratamiento de valores nulos.
- Conversión de tipos de datos apropiados.
- Normalización de variables categóricas.
- Detección y corrección de inconsistencias.

### 3. Transformación
- Creación de nuevas variables como `Cargo_Diario`.
- Codificación binaria y one-hot encoding según sea necesario.
- Segmentación de clientes por perfil.

### 4. Análisis Exploratorio (EDA)
- Distribución general del abandono.
- Análisis por género, edad, tipo de contrato, servicios contratados.
- Visualización de relaciones entre variables y abandono.

### 5. Visualización
- Gráficos de barras, histogramas, mapas de calor.
- Comparativas entre clientes que abandonaron y los que no.
- Dashboards exploratorios (opcional: Power BI o Plotly).

---

## 📈 Ejemplos de Visualizaciones

- 📊 **Tasa de abandono genetral**
- 📉 **Distribución de abandono por variables categóricas**
- 📉 **Distribución de abandono por variables numéricas**
- 📌 **Mapa de calor de correlaciones**

---

## 💡 Hallazgos Clave (ejemplos)

- Los clientes con **contrato mensual** tienen una tasa de abandono significativamente mayor.
- Los clientes con múltiples servicios (internet + streaming + protección) tienden a permanecer más tiempo.
- El **cargo mensual elevado** sin servicios adicionales se asocia con mayor abandono.

---

## 📚 Herramientas Utilizadas

- **Lenguaje**: Python
- **Librerías**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `requests`, `json`
- **Entorno**: Google colab / VS Code / Git Hub
- **Fuente de Datos**: API de TelecomX

---

## 👤 Autor

**Magno Gabriel Huaromo Montañez**  
Proyecto realizado como parte de un desafío de análisis de datos con enfoque en retención de clientes.  
[LinkedIn](http://www.linkedin.com/in/magno-huaromo)

