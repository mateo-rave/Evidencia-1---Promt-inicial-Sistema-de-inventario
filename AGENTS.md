# Sistema de Inventario

Aplicación web para administrar productos y controlar las existencias de un pequeño negocio.

## Stack y estructura
- HTML, CSS y JavaScript puros, sin frameworks ni librerías.
- Tres archivos: index.html, styles.css y app.js.
- Ejecución local mediante index.html.

## Convenciones
- Comentarios e interfaz en español; nombres de variables en inglés.
- Funciones cortas, con una sola responsabilidad.
- Validar los datos antes de guardarlos.

## Datos
- Cada producto tiene identificador, nombre, categoría, precio y cantidad.
- El precio debe ser mayor que 0.
- La cantidad debe ser un entero igual o mayor que 0.
- Guardar los productos en localStorage con la clave "products".
- Las fechas se calculan con la hora local del equipo, nunca con UTC.
- Las existencias se calculan sumando entradas y restando salidas, en orden cronológico.

## Inventario
- Registrar entradas y salidas de unidades.
- Nunca permitir que las existencias sean negativas.
- Mostrar una alerta cuando haya 5 unidades o menos.
- Solicitar confirmación antes de eliminar un producto.

## Límites
- Explicar qué archivos se modifican y por qué.
- Preguntar antes de instalar dependencias o cambiar la estructura de archivos.
- No borrar los datos del usuario sin confirmación.
- No incorporar servicios externos.

## Verificación
- Probar el registro, la edición y la eliminación de productos.
- Probar entradas y salidas válidas e inválidas.
- Comprobar las alertas de existencias bajas.
- Recargar la página y verificar que los datos persistan.
