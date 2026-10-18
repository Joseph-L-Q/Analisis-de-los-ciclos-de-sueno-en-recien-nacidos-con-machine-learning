# Análisis de los ciclos de sueño en los recién nacidos con machine learning

## Presentación del caso

Este proyecto parte del caso sobre el sueño en los recién nacidos que trabajé en el examen parcial. La infografía muestra cómo cambian los ciclos de sueño durante los primeros meses de vida y qué variables se registraron, como la edad, la actividad motora y la duración del sueño.

El estudio presentado incluyó a 152 bebés y 100 padres, con seguimiento a los 3, 6 y 12 meses. Uno de los hallazgos fue que la duración de los ciclos de sueño aumenta con la edad.

## Problema

El sueño de los bebés cambia mientras crecen y no todos presentan los mismos patrones. Por eso, en este proyecto busco responder:

**¿Cómo podemos estimar la duración del ciclo de sueño de un bebé a partir de su edad?**

Aunque el caso se llama “Sueño en los recién nacidos”, para la predicción trabajaré con edades de 3 a 12 meses, según el seguimiento mostrado en la infografía.

## Objetivo

Desarrollar un modelo que estime la duración del ciclo de sueño en minutos según la edad del bebé y mostrar los resultados en un gráfico.

## ¿Por qué usar IA y Machine Learning?

La IA permitirá representar el problema mediante un espacio de estados y explorar caminos hacia un estado objetivo, tomando como base lo que planteé en el examen.

Para la predicción usaré aprendizaje supervisado con una regresión lineal simple, porque quiero predecir un valor numérico: los minutos que dura un ciclo de sueño.

- **Entrada:** edad del bebé en meses.
- **Salida:** duración estimada del ciclo de sueño en minutos.

Como no cuento con los registros originales del estudio, utilizaré datos sintéticos para desarrollar el ejercicio. Los resultados servirán para mostrar cómo funciona el modelo y no como una evaluación médica.

## Fuente

Infografía del examen parcial: “El Sueño en los Primeros Meses de Vida”.
