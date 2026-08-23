# Predicción-Clínica-y-Financiera-en-Salud

# 📌 Planteamiento del Problema
En los sistemas de salud actuales, los hospitales y aseguradoras enfrentan un dilema constante: **Cómo garantizar una atención médica oportuna y de calidad sin generar costos excesivos ni deudas impagables para los pacientes**.  

- Cuando un paciente no recibe atención rápida en casos urgentes, la estancia hospitalaria tiende a prolongarse, lo que incrementa los costos y aumenta el riesgo de complicaciones clínicas.  
- Por otro lado, las aseguradoras buscan minimizar gastos, pero si la cobertura es insuficiente, los pacientes con recursos limitados quedan endeudados y los hospitales enfrentan pérdidas financieras por servicios no pagados.  
- Aunque las instituciones hospitalarias y las cobradoras pueden recurrir a embargos para recuperar parte de la deuda, en la práctica esto **no cubre el monto total** y termina generando pérdidas adicionales, afectando tanto la estabilidad financiera del hospital como la confianza del paciente en el sistema.  

Actualmente, muchos hospitales carecen de herramientas predictivas que integren simultáneamente:  
1. La **clasificación de resultados clínicos** para priorizar la atención.  
2. La **estimación de costos hospitalarios** para anticipar la carga financiera.  
3. La **predicción del riesgo de hospitalización prolongada y cobertura de seguros** para equilibrar calidad y viabilidad económica.  

---

# 🎯 Objetivo del Proyecto
**Desarrollar un sistema predictivo integral que permita optimizar la atención hospitalaria y la gestión financiera en salud, combinando tres dimensiones clave:**

1. **Clasificación de resultados clínicos** para identificar de forma temprana condiciones anormales y priorizar la atención de pacientes con mayor urgencia.  
2. **Predicción de costos hospitalarios** con el fin de estimar la facturación asociada a cada ingreso y anticipar posibles escenarios financieros.  
3. **Evaluación del riesgo de hospitalización prolongada y cobertura de seguros**, buscando equilibrar la calidad del tratamiento con la sostenibilidad económica, evitando que los pacientes queden endeudados y que los hospitales enfrenten pérdidas.  

El propósito central es **priorizar la salud del paciente sin comprometer la viabilidad financiera del sistema sanitario**, generando un modelo que apoye la toma de decisiones clínicas y administrativas de manera ética, eficiente y transparente.

---

# 📖 Justificación
La atención hospitalaria enfrenta un reto crítico: **equilibrar la calidad del tratamiento con la sostenibilidad financiera**. En muchos casos, los pacientes con recursos limitados no pueden cubrir los costos derivados de estancias prolongadas o tratamientos complejos. Aunque los hospitales y las cobradoras pueden recurrir a embargos para recuperar parte de la deuda, en la práctica esto rara vez cubre el monto total, generando pérdidas económicas y debilitando la confianza en el sistema de salud.

Un sistema predictivo que integre la **clasificación de resultados clínicos**, la **estimación de costos hospitalarios**, el **riesgo de hospitalización prolongada** y la **probabilidad de cobertura de seguros** ofrece una solución innovadora y realista. Este enfoque permitiría:  
- **Priorizar la salud del paciente**, identificando rápidamente los casos urgentes para reducir complicaciones y estancias innecesarias.  
- **Optimizar la gestión financiera**, anticipando costos y ajustando recursos de manera más eficiente.  
- **Reducir el endeudamiento de los pacientes**, garantizando que la cobertura de seguros sea suficiente y evitando pérdidas para los hospitales.  
- **Apoyar la toma de decisiones clínicas y administrativas**, combinando datos médicos y financieros en un modelo integral.  

La relevancia social del proyecto radica en que contribuye a un sistema de salud más **justo, eficiente y sostenible**, donde los pacientes reciben atención adecuada sin quedar atrapados en deudas, y los hospitales mantienen estabilidad económica. Además, desde el punto de vista tecnológico, este proyecto demuestra cómo el **machine learning** puede ser aplicado de manera ética y práctica en el ámbito sanitario, generando valor tanto para la investigación como para la operación real.

---

# 📚 Marco Teórico
El proyecto se fundamenta en la aplicación de **Machine Learning (ML)** en el ámbito sanitario, combinando modelos de clasificación y regresión para apoyar la toma de decisiones clínicas y financieras.  

### 1. Machine Learning en Salud
El ML permite analizar grandes volúmenes de datos médicos y administrativos para encontrar patrones que apoyen:
- **Diagnóstico temprano**: identificar condiciones médicas a partir de síntomas y pruebas.  
- **Gestión hospitalaria**: optimizar recursos, reducir estancias prolongadas y anticipar costos.  
- **Cobertura financiera**: estimar riesgos y ajustar seguros de manera más justa.  

### 2. Clasificación
La clasificación es una técnica de ML que asigna una etiqueta a cada caso.  
En este proyecto se aplica para:
- **Resultados de pruebas médicas**: Normal, Anormal, Inconcluso.  
- **Cobertura de seguros**: Completa vs Parcial.  

Ejemplo sencillo:  
```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```
---
Markdown
### 3. Regresión de Costos y Riesgo de Hospitalización Prolongada
La regresión predice valores numéricos y se usa para estimar la **facturación hospitalaria**.  
Además, se modela el **riesgo de hospitalización prolongada** como un problema de clasificación binaria:  
- **Estancia corta** (≤ 7 días)  
- **Estancia prolongada** (> 7 días)  

Ejemplo:  
```python
from sklearn.ensemble import GradientBoostingRegressor

reg_model = GradientBoostingRegressor()
reg_model.fit(X_train, y_train)
cost_pred = reg_model.predict(X_test)
```

---
Markdown
### 4. Explicabilidad del Modelo
En salud no basta con predecir, hay que **explicar**.  
Se usan técnicas como **SHAP** o **LIME** para mostrar qué variables influyen más en cada predicción.  
Ejemplo: la edad y condición médica pueden ser determinantes en la duración de la estancia.  

Esto aporta transparencia y confianza, permitiendo que médicos y administradores comprendan las razones detrás de cada resultado.

---

### 5. Impacto Social y Financiero
- **Pacientes**: reciben atención adecuada sin quedar endeudados.  
- **Hospitales**: reducen pérdidas por deudas no cubiertas.  
- **Aseguradoras**: ajustan coberturas de forma más eficiente.  

Este enfoque busca un equilibrio entre la **prioridad clínica** y la **sostenibilidad económica**, generando beneficios para todos los actores del sistema de salud.

---

### 6. Conclusión del Marco Teórico
El uso de machine learning en salud permite integrar predicciones clínicas y financieras en un mismo sistema.  
Este proyecto demuestra cómo la combinación de **clasificación, regresión, explicabilidad e impacto social** puede transformar la gestión hospitalaria, priorizando la salud del paciente y asegurando la viabilidad económica de hospitales y aseguradoras.




