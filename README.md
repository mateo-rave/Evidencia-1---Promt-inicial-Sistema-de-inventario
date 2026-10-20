# Sistema de Inventario  - Mateo Rave Giraldo

Adaptación del taller "Diario de Estudio · Módulo 01". Este repositorio contiene la **planificación y el diseño** del proyecto. La aplicación todavía no ha sido construida ni probada.

## Objetivo
Aplicación web sencilla para registrar productos, controlar existencias y consultar movimientos de un pequeño negocio, usando HTML, CSS y JavaScript puros y `localStorage`.

## Contenido
- `AGENTS.md`: reglas permanentes que debe respetar el agente (Estación 2).
- `README.md`: este documento (Estaciones 1, 3 y 4).

## Estación 1. Prompt inicial

**Rol:** desarrollador web senior que enseña a principiantes; código claro, organizado y comentado.

**Contexto:** primera versión de un Sistema de Inventario para uso local.

**Tarea**
- Formulario de productos: nombre, categoría, precio y cantidad.
- Validaciones: nombre y categoría no vacíos; precio > 0; cantidad entera >= 0.
- Lista de productos con nombre, categoría, precio y unidades.
- Editar y eliminar (con confirmación).
- Entradas y salidas de unidades; no se permiten salidas mayores a las existencias.
- Alerta visual con 5 unidades o menos.
- Persistencia en `localStorage`.

**Restricciones**
- Solo HTML, CSS y JS puros; sin librerías externas.
- Tres archivos: `index.html`, `styles.css`, `app.js`.
- Funciona abriendo `index.html` sin servidor.
- Sin credenciales ni servicios externos.
- Comentarios e interfaz en español; funciones cortas y nombres descriptivos.
- Sin cantidades negativas ni existencias inválidas.
- Reglas de fecha y cálculo: cada movimiento se fecha con la hora local del equipo (no UTC) y las existencias se calculan sumando entradas y restando salidas en orden cronológico.

**Formato de salida:** plan de 3 a 5 líneas antes del código; cada archivo completo en su bloque; responsabilidad de cada archivo; decisiones propias; lista de pruebas.

## Estación 2. AGENTS.md
Ver [AGENTS.md](AGENTS.md).

## Estación 3. Petición de plan (historial de movimientos)

**Objetivo:** añadir un historial para consultar las entradas y salidas de cada producto.

**Petición al agente** (sin escribir código hasta recibir aprobación):
1. Cómo registrar cada movimiento (producto, tipo, cantidad y fecha local) y cómo se calcularía el saldo de existencias a partir del historial.
2. Qué archivos se modificarían y qué cambiaría en cada uno.
3. Cómo guardar y recuperar el historial con `localStorage`.
4. Casos límite: salidas superiores a las existencias, cantidades <= 0, productos eliminados con movimientos y movimientos duplicados por error del usuario.
5. Dudas a decidir antes de desarrollar (por ejemplo, si se podrá consultar el historial de productos eliminados).
6. Reglas nuevas para `AGENTS.md`.

**Instrucción final:** no escribir código todavía; esperar aprobación.

## Estación 4. Revisión crítica de un plan con errores

| Propuesta del agente | Problema | Corrección |
|---|---|---|
| Guardar movimientos solo en una variable de JS | Pérdida de información al recargar | Persistir en `localStorage` |
| Permitir existencias negativas | Existencias inválidas | Validar la salida antes de modificar el inventario |
| Instalar una librería para la tabla | Dependencia no autorizada; contradice las restricciones | Usar JS puro; pedir autorización previa si fuera necesario |
| Borrar todos los movimientos al eliminar un producto | Pérdida del historial | Definir y decidir la política antes de programar |
| Mostrar movimientos en orden de almacenamiento | Orden incorrecto | Ordenar por fecha, del más reciente al más antiguo |
| Plan sin archivos, casos límite ni reglas | Plan incompleto | Especificar archivos, casos límite y cambios en `AGENTS.md` |

## Resultado esperado
Un prompt inicial adaptado al inventario, un `AGENTS.md` con las reglas del proyecto, una solicitud de planificación para una nueva funcionalidad y una revisión crítica de una propuesta con errores.
