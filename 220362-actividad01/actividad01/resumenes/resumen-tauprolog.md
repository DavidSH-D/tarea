# Resumen: Introducción y Uso de Tau Prolog

## 1. ¿Qué es Tau Prolog?
Tau Prolog es un intérprete de Prolog de código abierto desarrollado íntegramente en JavaScript. Se ejecuta en el lado del cliente (navegador web) y cumple con el estándar ISO Prolog.

---

## 2. Instalación e Integración
* **Descarga:** Disponible gratuitamente en su sitio oficial ([tau-prolog.org](http://tau-prolog.org/)).
* **Inclusión:** Se descarga el archivo `tau-prolog.js` y se vincula en el documento HTML:
  ```html
  <script src="tau-prolog.js"></script>
  ```

---

## 3. Definición de la Base de Conocimiento (BC)
Las reglas y hechos de Prolog se incrustan directamente en el HTML utilizando una etiqueta `<script>` con el atributo `type="text/prolog"` y un identificador (`id`):

```html
<script id="habilidades.pl" type="text/prolog">
    programa(ana, c).
    programa(juan, java).
    programa(ana, html).
</script>
```

---

## 4. Flujo de Trabajo y Métodos Principales (Objeto `pl`)
Todas las funciones y utilidades de la librería se encuentran bajo el objeto global `pl`. El ciclo de ejecución consta de 4 pasos esenciales:

1. **Crear una sesión:**
   ```javascript
   var session = pl.create();
   ```
2. **Cargar la Base de Conocimiento:** Carga los hechos/reglas referenciando el `id` del script:
   ```javascript
   session.consult("habilidades.pl");
   ```
3. **Preparar la consulta:** Define la meta o pregunta a evaluar (no la ejecuta de inmediato):
   ```javascript
   session.query("programa(juan, java).");
   ```
4. **Ejecutar la consulta (`session.answer`):**
   * Es una función **asíncrona** que no bloquea la ejecución del navegador.
   * Recibe una **función callback** como parámetro, la cual se dispara automáticamente una vez obtenido el resultado.

---

## 5. Manejo de Respuestas y Callbacks
* El argumento devuelto a la función callback (`answer`) es un objeto de tipo `substitution`.
* Para convertir este objeto a una cadena de texto legible, se utiliza el método:
  ```javascript
  let r = pl.format_answer(answer);
  ```

---

## 6. Estructura Completa de Ejemplo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo Tau Prolog</title>
    <script src="tau-prolog.js"></script>
</head>
<body>
    <div id="respuesta"></div>

    <!-- Base de Conocimiento -->
    <script id="habilidades.pl" type="text/prolog">
        programa(ana, c).
        programa(juan, java).
        programa(ana, html).
    </script>

    <!-- Lógica de Consulta JS -->
    <script>
        var session = pl.create();
        session.consult("habilidades.pl");
        session.query("programa(juan, java).");

        session.answer(function(answer) {
            let r = pl.format_answer(answer);
            console.log("Respuesta: " + r);
            document.getElementById("respuesta").innerHTML = "La respuesta es: " + r;
        });
    </script>
</body>
</html>
```