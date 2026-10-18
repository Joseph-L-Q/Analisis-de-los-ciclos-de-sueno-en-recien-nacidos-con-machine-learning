## Espacio de estados

Para representar el problema, tomaré como base el esquema que hice en el examen. El estado inicial es un bebé con sueño irregular y el objetivo es llegar a un descanso adecuado a sus necesidades.

Este esquema es una representación conceptual. Las acciones planteadas no garantizan una mejora real del sueño.

### Estados

| Estado | Descripción |
| --- | --- |
| S0 | Sueño irregular: estado inicial. |
| S1 | Rutina establecida. |
| S2 | Ambiente adecuado para el descanso. |
| S3 | Rutina establecida y ambiente adecuado. |
| S4 | Descanso adecuado a sus necesidades: estado objetivo. |
| S5 | Dificultad de sueño persistente. |

### Operadores

Los operadores representan las acciones o evaluaciones que permiten pasar de un estado a otro.

| Operador | Transición |
| --- | --- |
| Establecer una rutina | S0 → S1 |
| Adecuar el ambiente | S0 → S2 |
| Adecuar el ambiente cuando ya existe una rutina | S1 → S3 |
| Establecer una rutina cuando el ambiente ya está adecuado | S2 → S3 |
| Evaluar el descanso y observar una mejora | S3 → S4 |
| Evaluar el descanso y observar que la dificultad continúa | S3 → S5 |

Las últimas dos transiciones dependen del resultado observado; no son resultados que el sistema pueda elegir.

### Restricciones

- Solo se permiten las transiciones definidas en el esquema.
- Se considera la edad del bebé al interpretar sus patrones de sueño.
- Tener una rutina y un ambiente adecuado no garantiza llegar a S4.
- S5 representa una dificultad persistente, no un diagnóstico.
- Para esta simulación, S4 y S5 son estados finales y no tienen transiciones de salida.

### Representación visual

<img width="788" height="648" alt="image" src="https://github.com/user-attachments/assets/24e53ef4-f415-4293-915a-8d63693e1465" />

### Relación con el modelo predictivo

El espacio de estados representa posibles recorridos dentro del problema. La regresión se utilizará para estimar la duración del ciclo de sueño según la edad. Esa predicción, por sí sola, no determina si el bebé llegó al estado S4.
