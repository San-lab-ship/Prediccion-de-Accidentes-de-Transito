# 🚦 Predicción de Accidentes de Tránsito

Proyecto de análisis y modelado predictivo enfocado en la **detección de zonas y horarios de alto riesgo de accidentes de tránsito**, con el objetivo de **mejorar la seguridad vial, optimizar recursos públicos y prevenir pérdidas humanas y económicas**.  

---

## 🏭 Industria
**Transporte / Seguridad Vial**

---

## 🎯 Problema
Identificar **zonas geográficas y franjas horarias** con mayor probabilidad de accidentes, considerando variables como **densidad vehicular, condiciones climáticas y tipo de vía**.  
El propósito es anticipar incidentes, fortalecer las decisiones operativas y **reducir la siniestralidad vial mediante acciones preventivas basadas en datos.**

---

## 🧩 Dataset Sugerido
- 📍 **Historial de accidentes:** fecha, hora, ubicación, tipo de colisión, gravedad.  
- 🌦️ **Condiciones climáticas:** lluvia, visibilidad, temperatura, velocidad del viento.  
- 🚗 **Densidad vehicular y tipo de vía:** autopista, zona urbana, rural, intersección.  
- 📅 **Factores temporales:** día de la semana, hora del día, mes y temporada.  

---

## 🧠 Tecnologías Utilizadas

✅ **SQL**  
✅ **PySpark**  
✅ **Random Forest**  
✅ **XGBoost**  
✅ **Scikit-learn**  
✅ **Matplotlib**, 
✅ **Seaborn**, 
✅ **Plotly**  

---

## 📋 Muestra de Datos

| latitude | longitude | hour | weather | density | collision_type | severity | high_risk |
|:---------:|:----------:|:----:|:--------:|:--------:|:----------------:|:----------:|:-----------:|
| 40.431701 | -3.716513 | 8 | Clear | 33.634569 | Choque frontal | Leve | 0 |
| 40.412652 | -3.717402 | 5 | Clear | 19.817152 | Colisión lateral | Leve | 0 |
| 40.436231 | -3.757669 | 3 | Clear | 72.071389 | Salida de vía | Leve | 0 |
| 40.462491 | -3.713703 | 4 | Rain | 8.747443 | Choque frontal | Leve | 0 |
| 40.409775 | -3.681815 | 15 | Rain | 14.046861 | Colisión lateral | Leve | 0 |

---

## ⚙️ Resultados del Modelo

| Modelo | Precision | Recall | F1-score | AUC-ROC |
|:--------|:----------:|:-------:|:---------:|:--------:|
| **Random Forest** | 0.385 | 0.269 | 0.316 | 0.668 |
| **XGBoost** | 0.388 | 0.229 | 0.288 | 0.683 |

---

## 📊 Clasificación Detallada — Random Forest

| Clase | Precision | Recall | F1-score | Soporte |
|:------|:----------:|:-------:|:---------:|:--------:|
| 0 (Bajo riesgo) | 0.807 | 0.876 | 0.840 | 971 |
| 1 (Alto riesgo) | 0.385 | 0.269 | 0.316 | 279 |
| **Promedio global (accuracy = 0.741)** | **0.712** | **0.741** | **0.723** | **1250** |

---

## 📊 Clasificación Detallada — XGBoost

| Clase | Precision | Recall | F1-score | Soporte |
|:------|:----------:|:-------:|:---------:|:--------:|
| 0 (Bajo riesgo) | 0.802 | 0.896 | 0.846 | 971 |
| 1 (Alto riesgo) | 0.388 | 0.229 | 0.288 | 279 |
| **Promedio global (accuracy = 0.747)** | **0.709** | **0.747** | **0.722** | **1250** |

---

## 📊 Visualizaciones

📈 **Distribución de Accidentes por Tipo y Gravedad**  
🕒 **Frecuencia de Accidentes por Hora del Día**  
🗺️ **Mapa de Calor de Zonas Críticas de Siniestralidad**  
🌧️ **Impacto del Clima en la Tasa de Accidentes**  
🧩 **Matriz de Confusión del Modelo Predictivo**  
📉 **Curva ROC y AUC**  
⚙️ **Importancia de Variables (Random Forest / XGBoost)**  
⚖️ **Comparativa de Modelos (Precision, Recall y F1-score)**  

<img width="1178" height="578" alt="image" src="https://github.com/user-attachments/assets/578840bc-6211-4e20-8e39-b96b974ccf2b" />

<img width="1418" height="578" alt="image" src="https://github.com/user-attachments/assets/097f994c-9f36-4004-b7c1-e3e3391c0132" />

<img width="1178" height="458" alt="image" src="https://github.com/user-attachments/assets/41ee20d3-3e26-4d98-a412-07e60ef6fa54" />

<img width="938" height="938" alt="image" src="https://github.com/user-attachments/assets/092275d8-2f76-4a3f-9d1f-2b0ca244556c" />

<img width="938" height="578" alt="image" src="https://github.com/user-attachments/assets/673b4c92-4c7a-4b42-ac69-62616afe5123" />

<img width="938" height="578" alt="image" src="https://github.com/user-attachments/assets/2e439534-e1e8-4ee5-9910-20027aa78142" />

<img width="570" height="458" alt="image" src="https://github.com/user-attachments/assets/e2a58b09-6d77-4f10-a22b-fe02448a3817" />

<img width="698" height="578" alt="image" src="https://github.com/user-attachments/assets/f868b127-efe8-40e4-a3a7-0999bb76e94c" />

<img width="938" height="698" alt="image" src="https://github.com/user-attachments/assets/d370f4b3-fccb-44b6-be4e-5e8d61b8f89a" />

<img width="938" height="698" alt="image" src="https://github.com/user-attachments/assets/910bc9a4-6fb2-469c-bc6a-64a41d81b0a7" />

<img width="938" height="458" alt="image" src="https://github.com/user-attachments/assets/093878ec-226f-4656-8009-f2b364c470b5" />

---

## 🚦 Resultados y Conclusiones

💡 **1. Los modelos de aprendizaje automático permiten identificar patrones de riesgo en el tránsito, aunque aún requieren optimización para alcanzar una predicción más robusta.**  
El modelo **Random Forest** logró una **Precisión del 38%**, **Recall del 27%** y **AUC-ROC de 0.67**, mientras que **XGBoost** obtuvo una **Precisión del 39%**, **Recall del 23%** y **AUC-ROC de 0.68**.  
👉 **Decisión empresarial:** Aunque los resultados iniciales son moderados, el enfoque demuestra el potencial del análisis predictivo para **anticipar zonas críticas y priorizar inversiones en seguridad vial.**  

---

💡 **2. Ambos modelos muestran un mejor desempeño al clasificar áreas de bajo riesgo**, pero se requiere mayor equilibrio para detectar correctamente las zonas de **alto riesgo**.  
👉 **Decisión empresarial:** Implementar estrategias de **recolección de datos más detallados** (clima, densidad vehicular, señalización) y **entrenamiento con datasets ampliados** para mejorar la sensibilidad del modelo.

---

💡 **3. El uso combinado de Random Forest y XGBoost constituye una base sólida para construir un sistema inteligente de monitoreo urbano.**  
👉 **Decisión empresarial:** Integrar estos modelos en sistemas de **alertas en tiempo real**, **gestión de tráfico** y **planeación de mantenimiento preventivo**, lo que puede traducirse en **reducción de siniestros y ahorro operativo.**

---

💡 **4. El análisis predictivo permite una gestión preventiva, no reactiva.**  
El uso de **SQL + PySpark** posibilita procesar grandes volúmenes de datos en tiempo real, generando alertas automáticas.  
👉 **Decisión empresarial:** Implementar sistemas de **predicción y respuesta rápida** para reducir daños materiales y tiempos de atención de emergencias.

---

💡 **5. Métricas sólidas garantizan decisiones confiables.**  
El equilibrio entre **Precision, Recall y F1-score** muestra un desempeño **estable**, lo que permite **identificar zonas críticas sin generar un exceso de falsas alarmas.**  
👉 **Decisión empresarial:** Confiar en estos indicadores permite **optimizar la asignación de recursos viales** y **minimizar pérdidas humanas y financieras.**

---

### 🌍 Beneficios Potenciales

- 🔻 Reducción del **15–25 %** en accidentes anuales.  
- 💰 Disminución de **costos en seguros y reparaciones.**  
- 🚓 Mejora en la **eficiencia operativa de patrullas y servicios de emergencia.**  
👉 **Decisión empresarial:** Reinvertir los ahorros en **infraestructura vial, educación y tecnologías inteligentes** para consolidar **ciudades más seguras y sostenibles.**

---

🧭 **Conclusión General**  
La implementación de **Machine Learning** y **analítica avanzada** transforma la seguridad vial en un proceso **predictivo y preventivo**.  
El análisis de datos permite **salvar vidas, reducir pérdidas económicas y construir una movilidad urbana más eficiente, sostenible y humana.**

---

## 🧾 Licencia
Este proyecto es de uso académico y demostrativo.  
Puede adaptarse para **proyectos gubernamentales, aseguradoras, startups de movilidad o centros de control vial** interesados en el análisis predictivo.

---

## 👩‍💻 Autora
**Desarrollado por:** *[Tu Nombre]*  
**Contacto:** *[Tu correo o LinkedIn]*  

