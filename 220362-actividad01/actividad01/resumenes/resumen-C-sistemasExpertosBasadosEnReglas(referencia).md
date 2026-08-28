# Resumen: Sistemas Expertos Basados en Reglas

Este documento presenta una síntesis clara y precisa sobre los fundamentos y el funcionamiento de los sistemas expertos basados en reglas deterministas [cite: 1].

## 1. Introducción y Conceptos Básicos
Los sistemas basados en reglas son herramientas eficientes para abordar situaciones complejas gobernadas por reglas deterministas (como sistemas de tráfico o transacciones bancarias) y representan la metodología más sencilla dentro de los sistemas expertos [cite: 1]. 
Se componen fundamentalmente de dos partes:
*   **Base de conocimiento:** Define el problema mediante un conjunto estático de reglas [cite: 1].
*   **Motor de inferencia:** Deduce y saca conclusiones aplicando la lógica clásica sobre dichas reglas [cite: 1].

## 2. Elementos de la Base de Conocimiento
La base de conocimiento opera con dos elementos clave:
*   **Hechos:** Son los datos dinámicos conocidos en una situación particular [cite: 1]. No son permanentes y se almacenan en la **memoria de trabajo** [cite: 1].
*   **Reglas:** Son relaciones lógicas permanentes y estáticas que vinculan objetos [cite: 1]. Se componen de:
    *   **Premisa (antecedente):** Expresión lógica (con un "Si...") que puede tener una o varias afirmaciones conectadas con operadores lógicos (y, o, no) [cite: 1].
    *   **Conclusión (consecuente):** Resultado lógico (tras un "Entonces...") [cite: 1].
*   *Restricciones y Sustitución:* Frecuentemente, las reglas complejas se sustituyen por un conjunto de reglas más simples equivalentes para facilitar su procesamiento computacional [cite: 1].

## 3. El Motor de Inferencia
Es el mecanismo que interpreta las reglas mediante tres pasos: reconocimiento de patrones, resolución de conflictos y ejecución [cite: 1]. Para obtener conclusiones, utiliza diferentes reglas y estrategias lógicas:
*   **Modus Ponens:** Razonamiento hacia adelante. Deduce conclusiones simples partiendo de premisas verdaderas (Si A es cierto -> B es cierto) [cite: 1].
*   **Modus Tollens:** Razonamiento hacia atrás. Si la conclusión es falsa, deduce que la premisa también lo es (Si B es falso -> A es falso) [cite: 1]. Su uso complementa al Modus Ponens para obtener más conocimiento [cite: 1].
*   **Mecanismo de Resolución:** Combina expresiones lógicas de dos o más reglas para obtener conclusiones compuestas [cite: 1].

### Estrategias de Inferencia (Encadenamiento)
*   **Encadenamiento de reglas (hacia adelante):** Se utiliza cuando los hechos iniciales coinciden con las premisas de las reglas. Las conclusiones generadas pasan a ser nuevos hechos, repitiendo el ciclo hasta que no se puedan obtener más conclusiones [cite: 1].
*   **Encadenamiento orientado a un objetivo (hacia atrás):** El sistema parte de un objetivo o meta. Navega por las reglas buscando los hechos que lo validen; si falta información, le pregunta directamente al usuario [cite: 1].

## 4. Control de la Coherencia
Es vital para evitar que el sistema experto tenga un comportamiento no satisfactorio o arroje conclusiones absurdas [cite: 1]. 
*   **Coherencia de Reglas:** Un conjunto de reglas es coherente si existe al menos una combinación de valores que produzca conclusiones no contradictorias [cite: 1]. El sistema debe rechazar o corregir reglas inconsistentes [cite: 1].
*   **Coherencia de Hechos:** El sistema no debe aceptar datos del usuario que contradigan el conocimiento existente [cite: 1]. Elimina automáticamente los "valores no factibles" para asegurar la coherencia continua durante la sesión [cite: 1].

## 5. Explicación de Conclusiones e Incertidumbre
*   **Subsistema de explicación:** Los usuarios esperan entender por qué el sistema tomó cierta decisión. Puesto que el motor de inferencia conoce la trazabilidad lógica, puede enumerar al usuario la lista de hechos y las reglas exactas utilizadas para llegar a una conclusión [cite: 1].
*   **Transición a la Incertidumbre:** Aunque estos sistemas son útiles en escenarios deterministas, existen problemas (como los diagnósticos médicos) donde los síntomas no implican certezas absolutas. Para estos casos, los sistemas basados en reglas deben evolucionar hacia **sistemas probabilísticos** para manejar la incertidumbre [cite: 1].
