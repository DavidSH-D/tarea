# Resumen Ejecutivo: Ingeniería del Conocimiento

**Materia / Módulo:** SGMA. Ingeniería del Conocimiento — Capítulo 2 [cite: 3]  
**Basado en el texto de:** Vázquez (2009), Pech (1999), Rodríguez (2002) y Barco (2004) [cite: 3]  

---

## 1. Conceptos Fundamentales y Roles Principal

La **Ingeniería del Conocimiento (IC)** es una rama de la Inteligencia Artificial (IA) centrada en la adquisición, representación, validación, inferencia, explicación y mantenimiento del conocimiento para construir Sistemas Basados en el Conocimiento (SBC) y Sistemas Expertos (SE) [cite: 3]. Aborda dominios complejos donde la informática convencional falla debido a que el conocimiento suele ser no estructurado, incompleto, inconsistente o impreciso [cite: 3].

En este paradigma interactúan tres actores y conceptos clave:
* **Conocimiento:** Combinación de estructuras de datos y procedimientos interpretativos (hechos, reglas, abstracciones) que permiten un comportamiento inteligente [cite: 3]. Se divide en:
  * **Declarativo:** Hechos, atributos y relaciones entre objetos o conceptos abstractos [cite: 3].
  * **Procedural:** Conjunto de reglas operativas utilizadas para resolver problemas [cite: 3].
  * **Metaconocimiento:** Conocimiento sobre la operación del propio sistema y sus capacidades de razonamiento [cite: 3].
* **Ingeniero del Conocimiento (ICO):** Especialista en IA y software encargado de extraer el conocimiento de las fuentes (humanas o documentales) y plasmarlo de manera explícita e implementable en una Base de Conocimiento [cite: 3]. Requiere destrezas técnicas, de comunicación y nociones de psicología [cite: 3].
* **Experto Humano:** Persona de reconocido prestigio que aporta su experiencia explícita y heurística [cite: 3].
* **Usuario:** Destinatario final del sistema, cuyo nivel de conocimiento debe considerarse durante el desarrollo [cite: 3].

---

## 2. Procesos y Etapas de Desarrollo

La Ingeniería del Conocimiento comprende **cinco actividades principales** [cite: 3]:
1. **Adquisición:** Extracción del conocimiento desde las fuentes [cite: 3].
2. **Representación:** Organización formal y codificada dentro de la Base de Conocimiento [cite: 3].
3. **Validación:** Comprobación de que el sistema se comporta adecuadamente frente a problemas reales igual que el experto [cite: 3].
4. **Inferencia:** Diseño de los mecanismos de software que ejecutan deducciones lógicas [cite: 3].
5. **Explicación y Justificación:** Programación de la capacidad del sistema para justificar sus conclusiones ante el usuario [cite: 3].

### Etapas del Proceso de Adquisición del Conocimiento (AC)
El proceso iterativo de extracción se divide en 5 etapas secuenciales [cite: 3]:
1. **Identificación:** Reconocimiento y subdivisión del problema, identificación de actores y recursos [cite: 3].
2. **Entendimiento:** Determinación de conceptos clave, relaciones y la estrategia de extracción [cite: 3].
3. **Formalización:** Elección del esquema de representación (reglas, marcos, etc.) y estructuración del conocimiento extraído [cite: 3].
4. **Implementación:** Programación y desarrollo del prototipo del sistema experto en la computadora [cite: 3].
5. **Pruebas:** Evaluación de la validez del conocimiento con ejemplos reales e interacciones con el experto para refinar o depurar el sistema [cite: 3].

---

## 3. Esquemas de Representación del Conocimiento (KR)

La **Representación del Conocimiento** convierte la información en esquemas inteligibles [cite: 3]. Para ser óptimo, un esquema debe ser sencillo, transparente, fácil de modificar, independiente y relacional [cite: 3].

Los principales esquemas se clasifican en **declarativos** (hechos estáticos) y **procedimentales** (reglas dinámicas) [cite: 3]:

* **Reglas de Lógica Simbólica:**
  * **Lógica Proposicional:** Evaluación booleana de verdad/falsedad mediante fórmulas bien definidas ($P, Q$) y conectivos ($\wedge, vtee, \sim, 
ightarrow, \equiv$) [cite: 3]. Utiliza reglas como *Modus Ponens*, *Modus Tollens* y *Modus Tollendo Ponens* [cite: 3].
  * **Lógica de Predicados:** Lenguaje sintáctico con mayor capacidad expresiva constituido por constantes, variables, funciones, predicados y cuantificadores ($fforall, \exists$) [cite: 3].
* **Redes Semánticas:** Grafos formados por nodos (conceptos, objetos o atributos) y enlaces/arcos (relaciones como *ES-UN* o *ES-SUBCONJUNTO*) [cite: 3]. Su razonamiento opera por propagación de la activación [cite: 3].
* **Árboles de Decisiones:** Representación gráfica de espacios de búsqueda compuestos por nodos (metas) y ramas (decisiones o causas) [cite: 3].
* **Frames (Marcos) o Slots:** Estructuras jerárquicas de datos basadas en objetos divididas en *slots* (atributos) y *facets* (facetas) [cite: 3]. Permiten la herencia de propiedades y la asociación de conocimiento procedural [cite: 3].
* **Gráficos Conceptuales:** Diagramas causa-efecto que muestran relaciones secuenciales de precedencia y jerarquía [cite: 3].

---

## 4. Clasificación de Métodos y Técnicas de Adquisición

Los métodos para extraer información de **fuentes estáticas** (libros, artículos) o **dinámicas** (experto humano) se dividen en tres grandes grupos [cite: 3]:

### Métodos Manuales
El ICO interactúa directamente con el experto o documentos [cite: 3]:
* **Entrevistas:** Estructuradas (preguntas específicas y guiadas), Semiestructuradas (puntos abiertos a cubir) y No estructuradas (exploratorias e informales) [cite: 3].
* **Métodos de Búsqueda / Análisis de Protocolo:** Rastro formal del proceso de pensamiento del experto durante la resolución de un problema [cite: 3].
* **Otros:** Análisis de casos, Lluvia de ideas, Prototipos, Escalamiento multidimensional, Examen e Informes técnicos [cite: 3].

### Métodos Semiautomatizados
Herramientas asistidas por computadora para reducir costes y facilitar el trabajo [cite: 3]:
* **Soporte al Experto Humano:** Interfaces que le permiten al experto ingresar y refinar reglas directamente (ej. Análisis de Rejilla o *Repertory Grid Analysis* basado en la Teoría de Construcción Personal de Kelly) [cite: 3].
* **Soporte al ICO:** Editores, interfaces de captura, módulos de documentación y sistemas de explicación [cite: 3].

### Métodos Automatizados
Minimizan o eliminan la intervención directa del experto y del ICO mediante algoritmos [cite: 3]:
* **Reglas de Inducción Automatizadas:** Transforman matrices de datos en árboles de decisión o reglas a través de algoritmos como **ID3** (Interactive Dichotomizer 3) [cite: 3].
* **Aprendizaje Automatizado:** Programas heurísticos donde la máquina aprende autónomamente a partir de la experiencia y grandes volúmenes de datos [cite: 3].
