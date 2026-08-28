# Resumen: Conclusión sobre Sistemas Expertos

Este documento sintetiza de forma clara y estructurada los conceptos fundamentales presentados en la presentación sobre **Sistemas Expertos (SE)**.

---

## 1. Clasificación de los Sistemas Expertos

Los sistemas expertos se dividen principalmente en dos grandes ramas según su enfoque de razonamiento:

```
                      Sistemas Expertos
                       /            \
             Deterministas         Estocásticos
                  |                 /        \
           Basados en reglas  Incertidumbre  Probabilidad
                  |                 |             |
         Programación lógica   Lógica difusa   Redes probabilísticas
```

* **Deterministas:** Basados en reglas y hechos concretos que utilizan inferencias lógicas precisas (programación lógica).
* **Estocásticos:** Modelan entornos con incertidumbre o probabilidad:
  * **Incertidumbre:** Abordada mediante *Lógica Difusa*.
  * **Probabilidad:** Abordada mediante *Redes Probabilísticas*.

---

## 2. Representación de la Base de Conocimiento (BC)

La información se extrae típicamente de documentos (por ejemplo, mediante expresiones regulares) y se estructura en la Base de Conocimiento en tres formatos principales:

1. **Árbol Conceptual:** Estructura jerárquica de conceptos interconectados por relaciones causales o descriptivas (ejemplo: determinación de las estaciones del año a partir de la inclinación del eje terrestre y la luz solar).
2. **Redes Probabilísticas:** Estructuras probabilísticas para razonamiento bajo incertidumbre.
3. **Reglas y Hechos:** Representación formal en lógica de predicados.

---

## 3. Redes Probabilísticas (Enfoque Estocástico)

* **Redes Bayesianas (Thomas Bayes, 1702–1761):**
  * Basadas en el **Teorema de Bayes**, que calcula la probabilidad condicional de un suceso $A_i$ dado un evento $B$:
    $$P(A_i|B) = \frac{P(A_i)P(B|A_i)}{\sum_{i=1}^{n} P(A_i)P(B|A_i)}$$
* **Cadenas de Markov (Andréi Márkov, 1856–1922):**
  * Sucesión de eventos en la cual la probabilidad de cada resultado depende exclusivamente del estado inmediatamente precedente y no de la historia previa (propiedad sin memoria).

---

## 4. Sistemas Expertos Deterministas

Fundamentados en la lógica proposicional y de predicados:

* **Inferencias Lógicas:**
  * Implicación ($A \Rightarrow B$)
  * Bicondicional ($A \Leftrightarrow B$)
* **Conceptos Clave:**
  * **Tautología:** Proposición que resulta verdadera para cualquier combinación de valores de verdad.
  * **Contradicción:** Proposición falsa para cualquier combinación.
  * **Falacia:** Inferencia inválida o falsa formulada a partir de premisas.

---

## 5. Implementación de Base de Conocimiento con Prolog

Para la programación lógica determinista se emplea **Prolog** (ej. *SWI-Prolog*).

### Elementos Básicos de Prolog
* **Hechos:** Expresan relaciones entre objetos. Los predicados y argumentos se escriben en minúsculas:
  ```prolog
  aprobo(juan, programacion1).
  reprobo(maria, estructuradedatos).
  ```
* **Reglas:** Tienen la estructura `consecuente :- antecedente.` (se lee: *el consecuente es verdad si el antecedente es verdad*). Las variables inician con letra mayúscula:
  ```prolog
  programa(P) :- aprobo(P, programacion1).
  programaoo(P) :- aprobo(P, programacionoo).
  ```
* **Consultas:** Preguntas dirigidas al motor de inferencia:
  * Consultar valor de variable: `?- reprobo(maria, X).` $\rightarrow$ `X = estructuradedatos.`
  * Verificación booleana: `?- programaoo(juan).` $\rightarrow$ `false.`
  * Predicado `call`: `?- call(aprobo, juan, programacion1).` $\rightarrow$ `true.`

### Flujo de Trabajo en SWI-Prolog
1. Cambiar al directorio de trabajo: `?- cd('c:/trabajo').`
2. Crear o editar el archivo `.pl` (vía editor externo o menú `File > New` en SWI-Prolog).
3. Cargar las cláusulas: `?- consult('programadores.pl').` o mediante `Compile > Compile buffer`.
4. Ejecutar consultas interactivas.