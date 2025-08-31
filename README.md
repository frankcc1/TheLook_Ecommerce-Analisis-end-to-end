# TheLook_Ecommerce-Analisis-end-to-end
## 📌 Introducción: Problemática  
En el competitivo mundo del e-commerce, **retener a los clientes es más difícil que atraerlos**.  
Durante el periodo **2024 - 2025**, la plataforma **TheLook Ecommerce** enfrentó una serie de retos críticos:  

- 📉 **Altas tasas de churn (abandono de clientes).**  
- 🛑 **Productos sin rotación durante meses.**  
- 🎯 **Promociones poco efectivas.**

## 🛠️ Stack Tecnológico  
- ☁️ **BigQuery** → Extracción, modelado y análisis masivo de datos.  
- 🔥 **Databricks (ML)** → Modelos predictivos de churn.  
- 📊 **Looker Studio** → Reporte interactivo.

## 🔎 Análisis de Negocio  
### 1️⃣ Retención y Cohortes  
El análisis de cohortes reveló:  
- 🔻 **Caída consistente en la retención mensual** (>30% de churn promedio).  
- 👤 Segmentos como hombres de **45-54 años** tenían un **LTV_60m > 9500**, siendo los más valiosos en retenerlos.
  
### 2️⃣ Clientes en Riesgo  
Mediante clustering y segmentación, se determinó lo siguiente:  
- ⚠️ +34% de clientes en estado **“En Riesgo”**.  
- 📌 Mayor concentración en **hombres 45-54 años** (el grupo más rentable a largo plazo).

### 3️⃣ Productos y Canastas Inteligentes  
- 🛒 Identificación de **categorías sin ventas en los últimos 3 meses**.  
- 🔗 Análisis de **índice de afinidad entre categorías** → propuesta de **combos/promos cruzadas**.  

  📍 Ejemplo: *Jeans + Fashion en China* → alto ticket promedio y afinidad comprobada.  

  ➡️ **Objetivo:** evitar sobre-stock + aumentar ticket promedio.  

### 4️⃣ Efectividad por País, Canal y Horario  
Se identificaron patrones clave:  
- ⏰ **Horarios Premium** → Top 3 en clientes y ventas.  
- 💳 **Horarios de Valor Alto** → Top 3 en ticket promedio.
- 🔥 **Horarios Buenos** → Top 5 (En clientes y ventas totales)
- 💳 **Horarios Regulares** → Los demás.
- 👤 Diferencias claras por **país y canal de adquisición**.  

  ➡️ **Acción:** campañas segmentadas por **horario, país y canal**.

### 5️⃣ Modelo Predictivo de Churn (Databricks)  
Se construyó un modelo ML usando:  
📊 **Variables utilizadas en el entrenamiento:**  
- 👤 **Demográficas** → `age`, `gender`, `country`  
- 🌐 **Origen** → `traffic_source`  
- 📅 **Antigüedad y actividad** → `antiguedad_cliente`, `total_ordenes`, `dias_desde_ultima_compra`, `num_compras_0_30`  
- 💸 **Valor de compra** → `total_gastado`, `ticket_promedio`  
- 📦 **Diversidad** → `num_categorias_compradas`  
- 🎟️ **Comportamiento digital** → `uso_cupon`, `apertura_email_rate`, `visitas_web_mes`, `dispositivo_preferido`  
- 🔄 **Post-venta** → `ratio_devoluciones`  
- 🏷️ **Etiqueta (target)** → `EstadoCliente`
  
  👉 Clasificación: **Activo | Nuevo | Churned**  
  ➡️ **Impacto:** este modelo permite anticipar qué clientes tienen alta probabilidad de abandono y accionar campañas preventivas antes de perderlos.  

![](https://github.com/frankcc1/TheLook_Ecommerce-Analisis-end-to-end/blob/main/Reporte_TheLookEcommerce.jpg)
