# ProyectoM_VIH_SIDA

![image](https://github.com/user-attachments/assets/17ef6bcd-ebee-4eab-aa38-1cc8a6545f65)


El objetivo principal de este proyecto fue identificar variables relevantes que influyen en el diagnóstico de VIH/SIDA y entrenar un modelo predictivo que permita estimar la probabilidad de infección a partir de datos clínicos y demográficos.

---

##  Descripción del conjunto de datos

Este dataset proviene de un estudio clínico realizado en la década de 1990, enfocado en la progresión del SIDA en pacientes tratados con diferentes esquemas antirretrovirales. Contiene información valiosa en tres grandes dimensiones:

- **Demográficas:**  Género , Raza , Edad, Peso, Orientación sexual  

- **Clínicas:**  Escala de Karnofsky (estado funcional)  , Conteo de glóbulos blancos CD40, CD4, CD8 y CD80  , Presencia de hemofilia  , Historial de tratamientos previos  

- **Conductuales:**  Uso de drogas intravenosas , Tipo de terapia previa  

Este conjunto de datos permite analizar cómo estas variables se relacionan con la presencia o ausencia de infección por VIH/SIDA.

---

##  Descripción del problema

El VIH/SIDA sigue siendo una de las enfermedades más críticas en salud pública global debido a su impacto sobre el sistema inmunológico. La detección temprana y la predicción de su progresión son fundamentales para mejorar la atención y calidad de vida de los pacientes.

### Pregunta de investigación:
> ¿Qué variables pueden ser relevantes para determinar si una persona tiene la infección del SIDA?

---

##  Objetivo general

- Analizar la relación entre diferentes variables clínicas y de comportamiento con el diagnóstico de infección por VIH/SIDA, y desarrollar un modelo predictivo basado en árboles de decisión que estime la probabilidad de infección.

---

##  Objetivos específicos

- Observar la relación entre la ausencia de glóbulos blancos CD40 y el diagnóstico de infección por SIDA.
- Determinar si la escala de Karnofsky, junto con otras variables, puede utilizarse para predecir el estado de infección.
- Aplicar técnicas de minería de datos para entrenar un modelo de árbol de decisión que clasifique a los pacientes como infectados o no infectados.
- Evaluar la precisión y relevancia del modelo, identificando las variables más determinantes en la clasificación.

---

## Hallazgos

- Se realizaron análisis exploratorios, visualizaciones y pruebas estadísticas para detectar relaciones entre variables y diagnóstico.
- **Variables más influyentes**:
  - **Escala de Karnofsky**: a menor puntuación, mayor probabilidad de infección.
  - **CD40 y CD4**: su ausencia o niveles bajos se correlacionan directamente con un diagnóstico positivo.
  - **Género y orientación sexual**: mostraron influencia leve pero no determinante.

---

##  Modelo Predictivo

Se entrenó un modelo de **árbol de decisión** para predecir la infección por VIH/SIDA.

### Resultados del modelo:


| Clase | Precisión | Recall | F1-Score | Soporte |
|-------|-----------|--------|----------|---------|
| **0 (No infectado)** | 0.80 | 0.58 | 0.67 | 1025 |
| **1 (Infectado)**    | 0.43 | 0.68 | 0.53 | 475  |



El modelo mostró una buena capacidad para **identificar casos positivos (recall del 68 %)**, aunque con una **precisión baja (43 %)**, lo cual implica un número considerable de **falsos positivos**.

Este comportamiento es común en modelos entrenados con clases desbalanceadas. 

El modelo mostró una buena capacidad para **identificar casos positivos (recall alto)**, aunque con una precisión baja. Esto significa que **algunas personas fueron clasificadas incorrectamente como infectadas**, pero **se minimizó el riesgo de falsos negativos**, lo cual es favorable en contextos clínicos donde es preferible alertar incluso con cierto margen de error antes que no detectar una infección real a tiempo.

---

##  Conclusiónes


- Las variables clínicas como los conteos de células CD4 y CD8 demostraron ser  relevantes para el diagnóstico de infección por VIH/SIDA
- Factores demográficos como el género y la actividad homosexual también mostraron asociaciones significativas, especialmente en su relación con los niveles de CD4
- Aunque no es una herramienta diagnóstica definitiva, la escala de Karnofsky es valiosa en la evaluación integral del paciente, ayudando a los médicos a medir el impacto funcional del VIH.
- La implementación del modelo de árbol de decisión permitió clasificar a los pacientes infectados con un nivel aceptable de precisión, facilitando la interpretación de los factores de riesgo, aunque el modelo alcanzó una precisión del 61.4%, con un F1-Score promedio de 0.53, lo cual indica un rendimiento moderado. La clase 1 (infectados), que representa el caso de mayor interés clínico, fue predicha con recall del 68%, pero con una precisión baja del 43%, lo que implica una alta tasa de falsos positivos.
- El modelo predictivo destacó ciertas variables como prioritarias en el proceso de clasificación, entre ellas: el conteo de CD4, el estado sintomático, el tipo de tratamiento recibido y el historial de uso de drogas intravenosas, todos ellos con impacto significativo en la evolución de la enfermedad.

Aunque el rendimiento del modelo no es suficientemente alto, permitió identificar variables clave y sentar las bases para modelos más robustos. Es necesario explorar algoritmos más complejos y realizar técnicas de balanceo para mejorar el rendimiento.



---




