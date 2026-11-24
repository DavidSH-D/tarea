# Universidad Autónoma del Carmen
**Facultad de Ciencias de la Información**  
**Ingeniería en Sistemas Computacionales**  
*Ubicación:* Av. 10 de Julio, Benito Juárez  
*Lema:* "Educando con transparencia y responsabilidad social 2022-2026"

---

### **Datos de Identificación**
- **Materia:** Programación avanzada  
- **Semestre:** 8vo Semestre  
- **Alumno:** David del Jesús Solano Herrera  
- **Profesor:** Jesús Alejandro Flores Hernández  
- **Fecha:** 26-agosto-2026  

---

# Guión de Exposición: Sistemas Expertos

## Introducción General
> *"Emulando la inteligencia humana a través de reglas, conocimiento y lógica computacional"*

### **Guión Hablado**
> "Buenos días / tardes a todos. Mi nombre es David del Jesús Solano Herrera y el día de hoy les voy a presentar un tema fundamental dentro de la Historia y la Arquitectura de la Inteligencia Artificial: Los Sistemas Expertos.
> 
> Bajo el subtítulo 'Emulando la inteligencia humana a través de reglas, conocimiento y lógica computacional', analizaremos cómo los pioneros de la informática lograron capturar la experiencia de especialistas humanos e implementarla en programas capaces de tomar decisiones complejas y resolver problemas de alto nivel. A lo largo de esta presentación entenderemos su arquitectura interna, sus hitos históricos y su relevancia actual."

### **Objetivo General**
Definir formalmente el concepto de Sistema Experto (SE), sus áreas de aplicación y el cambio de paradigma clave: la separación entre conocimiento y procesamiento.

---

## Diapositiva 1: Definición y Fundamentos de los Sistemas Expertos

### **Objetivo de la Diapositiva**
Definir qué es un Sistema Experto, ilustrar su propósito y explicar el principio arquitectónico de separación entre conocimiento y motor de inferencia.

### **Guión Hablado**
> "Para comenzar, debemos preguntarnos: ¿qué es exactamente un Sistema Experto? Un Sistema Experto (abreviado SE) es un software diseñado específicamente para emular la capacidad de decisión y diagnóstico de un especialista humano en un área muy concreta.
> 
> Imaginen por un momento a un médico especialista con 20 años de experiencia o a un geólogo experto. Un SE busca codificar esa experiencia utilizando una base de conocimientos especializada y algoritmos de razonamiento formal.
> 
> Su objetivo principal es resolver problemas altamente complejos en dominios específicos como la medicina, las finanzas o la ingeniería. Pero lo verdaderamente revolucionario de estos sistemas es su arquitectura: separan de manera radical el conocimiento almacenado del mecanismo que lo procesa para llegar a conclusiones, lo que permite modificar el saber del sistema sin rehacer el programa desde cero."

---

## Diapositivas 2 y 3: El Conocimiento y la Base de Conocimiento

### **Objetivo de la Diapositiva**
Explicar la diferencia entre el conocimiento abstracto del experto y su estructuración digital dentro de la Base de Conocimiento mediante reglas condicionales.

### **Guión Hablado**
> "En la arquitectura de un Sistema Experto, el pilar central es el Conocimiento. Podemos definirlo como la 'materia prima'. Incluye datos, hechos probados, reglas empíricas, principios del dominio y, muy importante, la heurística, que son esas 'reglas generales o atajos mentales' que un experto usa para tomar decisiones ágiles y acertadas.
> 
> Ahora bien, ¿dónde se guarda este conocimiento? Se guarda en la Base de Conocimiento. Este es el repositorio digital donde la información se codifica y estructura formalmente. En el paradigma de la IA simbólica, se representa mediante hechos y reglas lógicas de producción, estructuradas casi siempre en condicionales del tipo SI [Condición] ENTONCES [Acción / Conclusión].
> 
> Por ejemplo: 'SI el paciente presenta fiebre Y sarpullido, ENTONCES evaluar probabilidad de sarampión'. La Base de Conocimiento mantiene estas reglas listas para ser consultadas."

---

## Diapositiva 4: El Motor de Inferencia: El Cerebro Lógico

### **Objetivo de la Diapositiva**
Detallar el funcionamiento del Motor de Inferencia como el componente ejecutor y comparar los dos modos de razonamiento: encadenamiento hacia adelante y hacia atrás.

### **Guión Hablado**
> "Si la Base de Conocimiento equivale a la memoria del sistema, el Motor de Inferencia es el cerebro activo, la capacidad de razonamiento. Es el componente algorítmico central que procesa la información.
> 
> Su función principal es tomar los hechos que introduce el usuario y combinarlos deductivamente con las reglas de la Base de Conocimiento para inferir nueva información o llegar a una conclusión final.
> 
> El Motor de Inferencia opera fundamentalmente mediante dos estrategias de razonamiento:
> 
> 1. **Encadenamiento hacia adelante (Forward Chaining):** Parte de los datos conocidos hacia la solución. Es decir, 'tengo estos síntomas, ¿qué enfermedad causa este patrón?'
> 2. **Encadenamiento hacia atrás (Backward Chaining):** Parte de una hipótesis o meta y busca los datos que la confirmen. Es decir, 'sospecho que es gripe, ¿se cumplen los síntomas requeridos para validarlo?'"

---

## Diapositiva 5: Evolución Histórica de los Sistemas Expertos

### **Objetivo de la Diapositiva**
Recorrer la cronología de los SE desde sus inicios en los años 60 hasta su convergencia actual con el Machine Learning y los Modelos de Lenguaje.

### **Guión Hablado**
> "Pasemos a revisar brevemente la trayectoria histórica que ha tenido esta tecnología a lo largo de seis décadas:
> 
> - **1965–1970 (DENDRAL):** Nace en Stanford el primer sistema experto de la historia, diseñado para identificar estructuras químicas orgánicas.
> - **1972–1976 (MYCIN):** Un gran hito médico. MYCIN introdujo las reglas de producción con factores de certeza para manejar la incertidumbre en infecciones sanguíneas.
> - **Década de 1980 (Auge Comercial):** Las empresas adoptan masivamente sistemas como XCON para configurar computadoras VAX, florecen las shells comerciales y las consultoras de IA.
> - **1987–1993 (El Invierno de la IA):** Tras altas expectativas no cumplidas y los elevados costos de mantenimiento de las bases de conocimiento, la inversión cayó drásticamente.
> - **1990s–2000s (Integración):** Los SE dejan de ser aplicaciones aisladas y se integran silenciosamente en los grandes sistemas empresariales (ERP, CRM, motores de reglas de negocio).
> - **Actualidad (Convergencia Moderna):** Hoy presenciamos un renacimiento: las reglas estructuradas se combinan con el Machine Learning y los Modelos de Lenguaje (LLMs) para dar explicabilidad y rigidez donde la IA probabilística falla."

---

## Diapositiva 6: Tipos de Sistemas Expertos y sus Aplicaciones

### **Objetivo de la Diapositiva**
Demostrar la diversidad funcional de los Sistemas Expertos según la tarea técnica que desempeñan en la industria y la ciencia.

### **Guión Hablado**
> "Los Sistemas Expertos no son una tecnología de propósito único; según el problema que abordan, podemos clasificarlos en nueve categorías principales:
> 
> 1. **Diagnóstico:** Identifican fallas o enfermedades a partir de síntomas (ej. diagnóstico médico o técnico).
> 2. **Interpretación:** Infieren el significado de señales o datos brutos (ej. análisis de sensores sísmicos o industriales).
> 3. **Predicción:** Estiman escenarios futuros a partir de condiciones actuales.
> 4. **Planificación:** Diseñan secuencias de pasos para lograr metas operativas.
> 5. **Diseño:** Configuran productos complejos respetando restricciones de ingeniería.
> 6. **Monitoreo:** Comparan continuamente datos en tiempo real para alertar sobre desviaciones.
> 7. **Reparación:** Recomiendan y aplican planes correctivos inmediatos.
> 8. **Instrucción:** Actúan como tutores inteligentes que evalúan el progreso del estudiante.
> 9. **Control:** Gobiernan el funcionamiento integral de un sistema en tiempo real."

---

## Diapositiva 7: Conclusión

### **Objetivo de la Diapositiva**
Cerrar la exposición sintetizando la contribución de los Sistemas Expertos, rindiendo mérito a sus creadores y ofreciendo respaldo bibliográfico.

### **Guión Hablado**
> "Para concluir nuestra presentación, es fundamental reconocer que los Sistemas Expertos demostraron al mundo que la tecnología podía emular el pensamiento humano mediante reglas bien estructuradas, convirtiéndose en la piedra angular de la lógica automatizada."
