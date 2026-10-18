# Pipeline de predicción y visualización

## Objetivo

Estimar la duración del ciclo de sueño de un bebé según su edad, trabajando entre los 3 y 12 meses.

## Modelo elegido

Usaré aprendizaje supervisado con regresión lineal simple:

- **Entrada (X):** edad en meses.
- **Salida (y):** duración del ciclo de sueño en minutos.

Elegí este modelo porque permite representar e interpretar una tendencia de aumento de la duración del ciclo con la edad.

## Datos

Utilizaré 120 registros sintéticos. Para generarlos, asumiré un aumento promedio de 10 minutos entre los 3 y 12 meses y agregaré variación aleatoria.

Esta fórmula es una simplificación para el ejercicio. Los registros no pertenecen a bebés reales ni reproducen la base original del estudio.

Link de colab: https://colab.research.google.com/drive/1dzRb_l58dK7HUhypMhzswMdgIKoF66Ba#scrollTo=XpL47eVi_FgP&line=10&uniqifier=1

## Interpretación de los resultados

En el primer gráfico, los puntos representan los datos sintéticos y la línea roja muestra la tendencia aprendida. La dispersión alrededor de la línea representa la variación agregada al generar los datos.

En el segundo gráfico, los puntos más cercanos a la línea roja corresponden a predicciones con menor error.

El MAE indica cuántos minutos se equivoca el modelo en promedio sobre los datos de prueba. Un valor menor representa menos error. El R² compara el error cuadrático del modelo con el de usar el promedio de los valores de prueba: cuanto más cercano a 1, mejor es el ajuste; también puede ser negativo.

## Conclusión

El pipeline permite generar datos, separarlos, entrenar una regresión y evaluar sus predicciones. Además, compara el modelo con una referencia básica que siempre predice el promedio.

La tendencia de aumento fue incluida al crear los datos, por lo que el modelo está aprendiendo una relación simulada. Estos resultados no permiten afirmar que prediga correctamente el sueño de bebés reales.
