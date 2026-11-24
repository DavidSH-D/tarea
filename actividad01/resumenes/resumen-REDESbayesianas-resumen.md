# Resumen: Redes Bayesianas y Teorema de Bayes

**Autor del documento original:** Jesús Alejandro Flores Hernández

## 1. Introducción al Problema
El documento presenta la aplicación práctica de las **Redes Bayesianas** y el **Teorema de Bayes** para resolver un problema de probabilidad condicional. Específicamente, busca identificar las causas o factores demográficos que influyen en el fracaso o deserción escolar de un grupo de alumnas, basándose en estadísticas históricas.

## 2. Conceptos Clave
*   **Teorema de Bayes:** Desarrollado por el matemático inglés Thomas Bayes, es una herramienta fundamental para calcular las probabilidades de sucesos condicionados.
*   **Redes Bayesianas:** Son estructuras gráficas que permiten realizar inferencias probabilísticas, deduciendo el valor de variables desconocidas a partir de variables que ya se conocen (evidencia).

## 3. Caso Práctico (Ejemplo de Análisis)
Se analiza una población de mujeres estudiantes de la FCI. La población se divide en tres categorías demográficas, cada una con un porcentaje de presencia y una tasa específica de deserción (fracaso) y éxito:

| Clase (Estado Civil) | Población Total (%) | Tasa de Fracaso / Deserción (D) | Tasa de Éxito (N) |
| :--- | :---: | :---: | :---: |
| **(A) Solteras** | 45% (0.45) | 3% (0.03) | 97% (0.97) |
| **(B) Casadas** | 30% (0.30) | 4% (0.04) | 96% (0.96) |
| **(C) Madres Solteras** | 25% (0.25) | 5% (0.05) | 95% (0.95) |

## 4. Desarrollo y Cálculo Bayesiano
El problema central plantea la siguiente pregunta analítica: **Si se selecciona al azar a una alumna y se sabe que pertenece al grupo que desertó, ¿cuál es la probabilidad de que sea una mujer casada?**

Para resolver esto, se aplica el Teorema de Bayes buscando la probabilidad de "ser casada" (B) dado "que desertó" (D), es decir, $P(B|D)$:

*   **Fórmula Aplicada:** $P(B|D) = \frac{P(B) * P(D|B)}{P(A)*P(D|A) + P(B)*P(D|B) + P(C)*P(D|C)}$
*   **Sustitución de Valores:** $P(B|D) = \frac{0.30 * 0.04}{(0.45 * 0.03) + (0.30 * 0.04) + (0.25 * 0.05)}$
*   **Resultado:** $0.316$

## 5. Conclusión
El análisis probabilístico concluye que **existe un 31.6% (o aproximadamente 31%) de probabilidad** de que, si encontramos a una mujer que abandona la carrera, esta sea una mujer casada.
