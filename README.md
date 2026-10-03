## Lector de código de barras

Este proyecto ayuda al registro de los contratos y facturas que paga el administrador, durante el mes en curso, permitiendo llevar un registro mensual, claro.
La intención principal del proyecto es ágilizar tiempo en esta tarea que es una de las mas desgastantes al finalizar el mes.

# Fase 0 — Escáner en vivo en la web

ID Requisito Criterio de aceptación
RF-01 Abrir la cámara trasera, pedir permiso y mostrar errores distintos para permiso denegado, sin cámara y contexto no seguro Cada caso muestra un mensaje propio
RF-02 Decodificar de forma continua Code 128/GS1-128 desde el video, sin tomar foto Se detecta sin pulsar nada
RF-03 Al detectar: vibrar/pitar, detener la lectura y mostrar proveedor, referencia y valor con botones Guardar / Descartar / Seguir El resultado aparece una sola vez por código (anti-rebote)
RF-04 Reutilizar el parser existente y devolver JSON Pasa todos los fixtures de shared/fixtures/gs1.json
RF-05 Avisar duplicados (mismo proveedor + referencia + valor) Aviso visible antes de guardar
RF-06 Modo lote: escanear varias facturas seguidas, listarlas y exportar TSV Exportación idéntica a la actual
RF-07 Linterna, cuando el dispositivo la soporte Botón visible solo si hay soporte
RF-08 Alternativa: seguir permitiendo cargar archivo Sin regresión respecto a la herramienta actual

# Cómo ejecutar

La idea del proyecto es poder captar con la cámara el código de barras, y que lea y genere los datos necesarios para llenar la base de datos, y además permita guardar en la base de datos.

· Aprendiendo a entender merge

Es una nueva linea para reforzar fast/foward
