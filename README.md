# Sistema de Materiales de Rony — Planificador con kardex (ET505 · Semana 9)

## Propósito
Ampliación de mi Planificador de materiales de la semana 7 (taller «Maqueta del Sistema Solar», 5.º grado, presupuesto S/ 200.00) con un pequeño **kardex**: materiales ficticios con código estable, búsqueda por nombre o código, cambio de nombre por id, entradas y salidas enteras, existencia = entradas − salidas, inactivación/eliminación, persistencia en localStorage y exportación de movimientos a CSV. Se conservan el cálculo, el presupuesto y la validación del pedido.

## Archivos
- `index.html`: pantalla del planificador (S7) y sección `#kardex` integrada (ids `k-*`); carga `app.js` y `kardex.js`.
- `styles.css`: estilos de S7 más las reglas de `personalizacion.css` (etiqueta y paleta verde rgb(22,101,52)).
- `app.js`: lógica del planificador (objeto `limites`, `calcularTotal`, `validarPedido`, acciones de pantalla). Presupuesto en céntimos.
- `kardex.js`: operaciones del kardex (`saldoDe`, `agregarMovimiento`, `siguienteCodigo`, `exportarCSV`) y comportamiento de la sección.
- `README.md`: este documento.

## Ejecutar y usar
Local: mantener juntos los cinco archivos en la misma carpeta y abrir `index.html` en Chrome o Edge. Sitio publicado: abrir la URL de GitHub Pages indicada abajo.
1. Planificador: escribir material, cantidad (1–30) y precio (S/ 0.01–50); Comprobar o Confirmar.
2. Kardex: crear material → seleccionarlo → registrar ENTRADA/SALIDA → ver existencia y tabla de movimientos.
3. Cambiar nombre, eliminar (sin movimientos, con confirmación) o inactivar (con movimientos, el historial se conserva).
4. Exportar CSV (`movimientos-materiales.csv`, separador `;`, abre en Excel).

## Publicación
Repositorio: [PEGAR AQUÍ la URL del repositorio]
Sitio GitHub Pages: [PEGAR AQUÍ la URL que GitHub muestre]

## Aportes y ayuda recibida
Autor: Rony Chumpik Casenta (estudiante). Ayuda: asistente de IA Claude (Anthropic), 05/11/2026, para integrar los fragmentos del recurso S9, adaptar `kardex.js` (código corto MAT-001 y limpieza de mensajes), añadir `novalidate` al formulario de movimientos y preparar pruebas e informe. El detalle de consultas, adaptaciones y comprobaciones está en el PDF entregado en MAXEDRA.

## Límites
- localStorage pertenece sólo al navegador y al origen (sitio) donde se usa: no hay base de datos compartida ni sincronización entre equipos o usuarios.
- El CSV es una copia de los movimientos, no una sincronización con Excel.
- La existencia del kardex son unidades físicas y es independiente del dinero del presupuesto del planificador.
- Sólo datos ficticios; no se guardan datos personales ni claves.
