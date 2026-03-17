# Proyecto Final — Data Science I  
## Estudio de integridad financiera en datasets comerciales

**Autor:** Amílcar Fernández  
**Curso:** Data Science I  
**Tipo de proyecto:** Auditoría de datos, reconstrucción determinista, clustering y clasificación supervisada

---

## Resumen

Este proyecto analiza un dataset sintético de ventas minoristas con inconsistencias estructurales en variables financieras clave, como subtotales, descuentos, totales finales y márgenes de beneficio.

A diferencia de un análisis exploratorio tradicional centrado únicamente en visualizaciones, este trabajo prioriza la **auditoría de la calidad de los datos** antes de cualquier interpretación de negocio. A lo largo del proyecto se detectan errores matemáticos, se reconstruyen variables de forma determinista, se comparan datos originales contra datos corregidos y se evalúa el impacto de dichas inconsistencias sobre distintas lecturas analíticas.

Posteriormente, se aplican técnicas de **clustering** para segmentar clientes y productos, se analiza la relación entre ambos grupos mediante cruces y visualizaciones, y finalmente se entrena un **modelo supervisado de clasificación** para validar la segmentación de clientes.

---

## Objetivo del proyecto

Demostrar la importancia de la auditoría de datos en escenarios de negocio, mostrando cómo errores aparentemente menores en datasets transaccionales pueden derivar en interpretaciones financieras equivocadas y afectar decisiones estratégicas.

---

## Principales etapas del análisis

- Exploración inicial del dataset
- Auditoría de calidad de datos
- Reconstrucción determinista de variables financieras
- Comparación entre datos originales y corregidos
- Visualización del impacto de las inconsistencias
- Segmentación de clientes mediante clustering
- Segmentación de productos mediante clustering
- Cruce entre clusters de clientes y productos
- Entrenamiento de un modelo de clasificación con Decision Tree
- Evaluación del modelo con Accuracy y Confusion Matrix

---

## Hallazgos principales

- Se detectaron inconsistencias matemáticas en columnas derivadas como **Sub Total**, **Discount $**, **Order Total**, **Total** y **Profit Margin**.
- La reconstrucción determinista permitió corregir dichas variables y evidenciar que los errores no alteraban completamente la estructura macro del negocio, pero sí distorsionaban métricas sensibles.
- Se identificaron tres tipos de clientes:
  - clientes chicos
  - clientes frecuentes
  - clientes fuertes
- Se identificaron tres tipos de productos:
  - productos de bajo impacto
  - productos de rotación
  - productos clave
- El análisis cruzado mostró que los **clientes fuertes** concentran gran parte de sus compras en **productos clave**, mientras que los segmentos chicos y frecuentes se apoyan más en productos de rotación.
- El modelo supervisado alcanzó una precisión muy alta al predecir el tipo de cliente a partir de variables de comportamiento de compra, reforzando la consistencia de la segmentación obtenida mediante clustering.

---

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Estructura del repositorio

```text
data/
notebooks/
README.md
requirements.txt