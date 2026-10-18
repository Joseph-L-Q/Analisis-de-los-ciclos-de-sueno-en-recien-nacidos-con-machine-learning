# Pipeline de razonamiento, búsqueda y resultados

## Problema

Representar los posibles recorridos desde un sueño irregular hasta un descanso adecuado, usando el espacio de estados que planteé en el examen.

## Razonamiento

1. Identificar el estado inicial: S0.
2. Revisar las transiciones permitidas.
3. Explorar los estados disponibles.
4. Buscar un camino hacia el estado objetivo: S4.
5. Mostrar el recorrido encontrado.

Usaré búsqueda en anchura (BFS), porque explora por niveles y permite encontrar un camino con el menor número de transiciones cuando todas tienen el mismo costo.

Este ejercicio utiliza un grafo conceptual. Encontrar un camino hacia S4 no demuestra que las acciones garanticen una mejora real del sueño.

## Interpretación de resultados

La búsqueda encontró el camino S0 → S1 → S3 → S4, con tres transiciones. En este recorrido primero se establece una rutina, luego se adecua el ambiente y finalmente se considera el escenario donde se observa una mejora.

También existe el camino S0 → S2 → S3 → S4, que tiene la misma cantidad de transiciones. El algoritmo devuelve el primero porque S1 aparece antes que S2 en el grafo.

Durante la exploración también se visitó S5, pero ese estado no forma parte del camino hacia el objetivo.

El resultado muestra una ruta posible dentro del modelo. La transición de S3 a S4 depende de observar una mejora; BFS no puede asegurar que ocurra ni calcular su probabilidad.
