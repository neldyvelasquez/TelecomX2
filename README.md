#  Telecom X Predicción de Cancelación

Este proyecto tiene como propósito **predecir la cancelación o retiro de clientes (churn)** utilizando técnicas de análisis de datos y modelado predictivo. Se identifican las variables más influyentes en la decisión de un cliente de abandonar el servicio, y se proponen estrategias de retención basadas en los resultados obtenidos.

##  Objetivo principal

Desarrollar un modelo de clasificación que permita anticipar qué clientes tienen mayor probabilidad de cancelar su contrato, para que la empresa (Telecom X) pueda actuar de forma preventiva y mejorar la fidelización.

##  Estructura del proyecto

```plaintext
 TelecomX2/
│
├──  README.md                                      # Este archivo
├──  Telecom X Predicción de Cancelación.ipynb      # Notebook principal con análisis y visualizaciones
├──  LICENSE
```

##  Preparación y tratamiento de datos

###  Clasificación de Variables

- **Variables Categóricas**: Tipo_Contrato, Servicio_Internet, Metodo_Pago, Genero_Cliente y Cliente_Pareja
- **Variables Numéricas**: Antiguedad_Meses, Cargos_Mensuales, Cargos_Totales

###  Procesos eealizados

1. **Limpieza de datos**:
   - Eliminación de registros con datos faltantes o inválidos.
   - Conversión de columnas numéricas mal tipadas (ej. `Cargos_Totales`).

2. **Codificación**:
   - Uso de One-Hot Encoding para variables categóricas con múltiples niveles.

3. **Normalización**:
   - Aplicación de `StandardScaler` a variables numéricas para mejorar el desempeño de modelos como KNN.

4. **Separación de datos**:
   - División en conjunto de entrenamiento (80%) y prueba (20%) utilizando `train_test_split` de `sklearn`.

###  Justificaciones

- Se priorizó la eliminación de ruido y escalado para asegurar la calidad del entrenamiento.
- Se aplicaron dos modelos complementarios (KNN y Random Forest) para comparar rendimiento en distintos enfoques: proximidad vs. ensamble.
- Se eligió `Random Forest` por su superioridad general en exactitud y precisión.


##  Análisis Exploratorio (EDA)

Durante el EDA, se generaron varias visualizaciones clave:

-  **Mapa de calor de correlación**: Identificó la antigüedad, tipo de contrato y método de pago como variables clave.
  <img width="2185" height="1978" alt="Untitled" src="https://github.com/user-attachments/assets/ba331f12-ab3d-42d8-98fe-e613d7950ae5" />

-  **Relación entre antigueda y churn**: Mostró que clientes nuevos son más propensos a cancelar.
  <img width="1189" height="490" alt="Untitled-1" src="https://github.com/user-attachments/assets/437bbaaa-a61e-4a82-8066-bf4ffb07702e" />


##  Instrucciones para ejecutar el notebook

-   **Clonar el repositorio** en tu entorno local o abrirlo en [Google Colab](https://colab.research.google.com/).
   git clone https://github.com/tu-usuario/alura-store-analysis.git
   cd alura-store-analysis


##  Requisitos

-  Python 3.8+
-  Pandas
-  Matplotlib / Seaborn
-  Jupyter o Google Colab


##  Contribuciones

Si deseas colaborar o extender el análisis a otras áreas (marketing, predicciones, etc.), ¡las contribuciones son bienvenidas!


##  Contacto

Para dudas, sugerencias o mejoras, puedes abrir un issue o enviar un pull request.
