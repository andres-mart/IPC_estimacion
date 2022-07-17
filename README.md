## Análisis y modelado predictivo sobre IPC Argentina

CONTENIDOS DE ESTE REPORTE

Lo que encontraremos en este resumen ejecutivo:

● Descripción del caso.
● Definición del objetivo del proyecto.
● Etapas del proceso para concluir en la elaboración del modelo.
● Comparación de los resultados obtenidos en modelo de clasificación.
● Comparación de resultados obtenidos de los modelos de optimización.
● Conclusiones finales.

### DESCRIPCIÓN DEL PROBLEMA

El problema que se nos plantea, es la volatilidad
presente en los registros de las variaciones de
los índices de precios al consumidor. Dicha
información es provista por INDEC (Argentina) y,
se desarrolla en un entorno imprevisible
afectado por variables macroeconómicas,
políticas y sociales.

### OBJETIVO

El objetivo del presente proyecto es plantear un
modelo de clasificación que nos permita saber de
forma aproximada si las variaciones porcentuales
en niveles de precios medidos por INDEC,
aumentarán o disminuirán.

### ETAPAS DEL DESARROLLO

  1. DATOS: Se cargan las librerías y set de datos con los cuales vamos a trabajar.
  2. EDA: Analizamos tamaño y dimensiones, cant. datos por columnas, tipos, medidas estadísticas, outliers, faltantes, etc.
  3. HEATMAP: Análisis de las correlaciones entre las variables en estudio. Este gráfico es clave en cuanto al armado y modelo a seleccionar. 
  4. PREPARACIÓN DE MODELOS: Filtramos y reordenamos datos. Armamos nuevos datasets con información enmascarada para nuestro modelo de clasificación.
  5. ALGORITMOS: A partir de la manipulación de nuestros datos, estamos en condiciones de aplicar los distintos modelos. Se aplicó: Logistic Regression, Decision Tree, Random Forest, Support Vector Machine, XGBoost.
  6. OPTIMIZACIONES: Se aplican técnicas de optimización -GridSearhCV y RandomSerchCV- para mejorar las métricas de ‘accuracy’ obtenidas en los modelos. 
  7. CONCLUSIONES FINALES: Se detallan las decisiones tomadas a partir de los resultados obtenidos. Se determina el mejor camino a seguir. 
  
### COMPARACIÓN DE LOS MODELOS

Vemos que para los modelos utilizados para realizar nuestra clasificación, solo la regresión
logística y el modelo por árboles aleatorios son los que mejor se adaptan a nuestro set de
datos. La máquina de soporte vectorial, tiene una clara falta de información ya que arroja
una coincidencia del 100% en las probabilidades.

### OPTIMIZACIONES

Las optimizaciones realizadas sobre los modelos planteados presenta mejoras en algunos casos y para
otros empeora. Como los casos de Random Forest y SVM

### CONCLUSIONES FINALES

Concluimos finalmente, que para el problema planteado, el análisis de una región presenta información escasa y
modelos robustos arrojan predicciones 100% precisas. Para no incurrir en estos errores, es necesario -luego de un
análisis macroeconómico- generalizar las mediciones tomadas para todas las regiones sin incurrir en sesgos ni
errores groseros. Esto puede hacerse de esta forma ya que, todas las mediciones fueron tomadas en la República
Argentina y guardan correlación a nivel general.
