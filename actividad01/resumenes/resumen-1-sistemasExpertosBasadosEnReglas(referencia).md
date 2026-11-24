# Resumen Ejecutivo: Sistemas Expertos Basados en Reglas

**Materia / Módulo:** Sistemas Basados en Reglas (2010/2011)  
**Autor del documento original:** Luis Valencia Cabrera (Universidad de Sevilla, Departamento de Ciencias de la Computación e Inteligencia Artificial)  

---

## 1. Introducción y Conceptos Fundamentales

Los **sistemas basados en reglas** constituyen una de las metodologías más eficientes, clásicas y deterministas dentro del ámbito de los Sistemas Expertos [cite: 1]. Resultan idóneos para abordar situaciones complejas que se rigen por un conjunto claro de condiciones lógicas y deterministas, tales como el control de tráfico ferroviario, las transacciones en cajeros automáticos, la seguridad informática y los sistemas de control de procesos [cite: 1, 1].

En la arquitectura general de un sistema experto basado en reglas intervienen dos pilares fundamentales:
1. **Memoria de Trabajo (Base de Hechos):** Almacena la información declarativa y dinámica sobre el estado o situación particular en un instante determinado [cite: 1, 1]. Su naturaleza es temporal y cambia continuamente a medida que transcurre la consulta o la ejecución del sistema [cite: 1, 1].
2. **Base de Conocimiento:** Contiene la información estática y permanente del dominio del problema en forma de reglas [cite: 1, 1]. Estas reglas representan las relaciones lógicas y generales entre los distintos objetos del sistema [cite: 1].

---

## 2. Estructura y Definición de las Reglas

Una **regla** es una afirmación lógica que vincula dos o más objetos y adopta la estructura condicional estándar:  
$$\text{Si } \langle \text{Premisa} \rangle \text{ entonces } \langle \text{Conclusión} \rangle$$ [cite: 1]

* **Premisa (Antecedente):** Es una expresión lógica ubicada tras la palabra clave *Si*. Consta de una o más afirmaciones objeto-valor unidas por operadores lógicos (*y*, *o*, *no*) [cite: 1].
* **Conclusión (Consecuente):** Es la expresión lógica situada tras la palabra clave *entonces* que determina los nuevos hechos a deducir o las acciones a ejecutar [cite: 1].

Si la regla contiene únicamente afirmaciones objeto-valor simples, se le conoce como **regla simple**; si incluye combinaciones lógicas compuestas, se clasifica como **regla compuesta** [cite: 1].

### Restricciones y Sustitución de Reglas
Para optimizar el rendimiento computacional y facilitar la codificación en programas informáticos, muchos motores de inferencia imponen restricciones formales (por ejemplo, prohibir el operador *o* en las premisas o exigir formas normales) [cite: 1]. La **sustitución de reglas** permite transformar un conjunto de reglas complejas en un conjunto equivalente de reglas simples mediante equivalencias de la lógica proposicional (como las leyes de De Morgan), sin perder generalidad ni capacidad expresiva [cite: 1].

---

## 3. El Motor de Inferencia y sus Estrategias

El **motor de inferencia** es el componente central encargador de procesar los hechos de la memoria de trabajo junto con las reglas de la base de conocimiento para deducir nuevas conclusiones [cite: 1]. Su ciclo básico de funcionamiento opera en tres fases [cite: 1]:
1. **Reconocimiento de patrones:** Compara los hechos vigentes en la memoria de trabajo con los antecedentes de las reglas para determinar cuáles se satisfacen (las cuales se añaden a la *Agenda*) [cite: 1].
2. **Resolución de conflictos:** Selecciona una regla específica dentro de la agenda activa aplicando criterios de control [cite: 1].
3. **Ejecución:** Evalúa el consecuente de la regla seleccionada, modificando, añadiendo o eliminando hechos en la memoria de trabajo [cite: 1].

### Reglas de Inferencia Lógica
* **Modus Ponens:** Inferencia orientada hacia adelante (*premisa* $\rightarrow$ *conclusión*). Si la premisa de la regla "Si $A$, entonces $B$" es cierta y se conoce el hecho de que $A$ es cierto, se deduce con certeza que $B$ es cierto [cite: 1].
* **Modus Tollens:** Inferencia orientada hacia atrás (*conclusión* $\rightarrow$ *premisa*). Dada la regla "Si $A$, entonces $B$" y conociendo que $B$ es falso, se concluye deductivamente que $A$ es falso [cite: 1]. La combinación de ambas permite ampliar significativamente la capacidad reflexiva del sistema [cite: 1].
* **Mecanismo de Resolución:** Transforma las reglas en cláusulas equivalentes y las combina dinámicamente para derivar conclusiones compuestas a partir de múltiples reglas interrelacionadas [cite: 1].

### Estrategias de Encadenamiento
* **Encadenamiento de Reglas (Hacia Adelante / Forward Chaining):** Partiendo de un conjunto de hechos iniciales conocidos, el motor activa sucesivamente las reglas cuyas premisas se cumplen, generando nuevos hechos hasta que no sea posible realizar más deducciones [cite: 1].
* **Encadenamiento Orientado a Objetivo (Hacia Atrás / Backward Chaining):** El usuario define un objeto o variable *objetivo* [cite: 1]. El algoritmo busca recursivamente las reglas que concluyen sobre dicho objetivo y, si faltan datos en los antecedentes, pregunta de manera dirigida al usuario por la información estrictamente necesaria [cite: 1].
* **Compilación de Reglas:** Cuando tanto las variables de entrada como las metas están predeterminadas, las reglas se sustituyen analíticamente por *ecuaciones objetivo*, acelerando de forma sustancial la velocidad de procesamiento [cite: 1].

---

## 4. Subsistemas Clave: Coherencia y Explicación

### Subsistema de Control de Coherencia
Garantiza la validez lógica de la base de conocimiento y de los datos suministrados durante la interacción [cite: 1]. Se divide en dos vertientes:
1. **Coherencia de Reglas:** Evita que se introduzcan reglas contradictorias (por ejemplo, aquellas que con las mismas premisas deriven consecuentes opuestos) [cite: 1]. Se define que un conjunto de reglas es coherente si existe al menos un conjunto de valores que no produzca contradicciones [cite: 1]. Detecta y elimina **valores no factibles** para las variables [cite: 1].
2. **Coherencia de Hechos:** Verifica que los datos introducidos por el usuario o los hechos intermedios no contradigan las reglas existentes [cite: 1]. Se logra ofreciendo únicamente listas de opciones válidas/factibles y actualizando de forma continua e inmediata la base de hechos tras cada adquisición [cite: 1].

### Subsistema de Explicación
A diferencia de otros modelos opacos, los sistemas basados en reglas poseen la capacidad nativa de justificar su razonamiento [cite: 1]. Al mantener la traza de las reglas ejecutadas en la memoria de trabajo, el sistema puede desplegar paso a paso la cadena lógica empleada para alcanzar una conclusión determinada, respondiendo a las preguntas de *¿por qué?* y *¿cómo?* formuladas por el usuario [cite: 1].

---

## 5. Casos de Aplicación y Limitaciones

### Ejemplos Prácticos
El documento ilustra la eficacia de estos sistemas mediante varios escenarios concretos:
* **Cajero Automático:** Definición estricta de condiciones (tarjeta verificada, NIP correcto, balance suficiente, límites no excedidos) para autorizar o denegar giros monetarios [cite: 1, 1].
* **Agentes Secretos:** Resolución de problemas combinatorios y asignación de ubicaciones geográficas a partir de telegramas contradictorios y reglas de veracidad/falsedad [cite: 1, 1].
* **Control de Tráfico Ferroviario:** Sistema de gestión de senales ($U_1 \dots U_8$, $L_1 \dots L_6$) y ocupación de vías ($S_1 \dots S_5$) para evitar colisiones entre trenes que circulan en direcciones opuestas [cite: 1].

### Limitaciones e Introducción de Incertidumbre
Aunque la lógica determinista clásica es sumamente sólida y transparente, presenta limitaciones severas en dominios reales donde existe información incompleta, ruidosa o imprecisa (como en el diagnóstico médico) [cite: 1]. Para superar este obstáculo, el marco determinista se extiende mediante **sistemas expertos basados en probabilidad** y redes probabilísticas, introduciendo grados de certeza y razonamiento bajo incertidumbre [cite: 1].
