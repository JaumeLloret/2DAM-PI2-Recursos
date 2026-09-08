# Plantillas del paquete integrado PI3

Copia esta carpeta a tu espacio autorizado. Conserva una versión del paquete con fecha, fuente de contrato y registro de decisiones. Los P01–P12 son componentes de **una entrega**, sin doce notas. Puedes mantenerlos separados para revisar diffs o agruparlos con los mismos encabezados.

| Componente | Uso y CE | Plantilla |
|---|---|---|
| P01 | ROADMAP FASES Y HITOS · RA2.c | [Abrir P01](Plantillas/P01_ROADMAP_FASES_Y_HITOS.md) |
| P02 | MAPA ACTIVIDADES Y DEPENDENCIAS · RA2.e, RA3.a | [Abrir P02](Plantillas/P02_MAPA_ACTIVIDADES_Y_DEPENDENCIAS.md) |
| P03 | ARQUITECTURA GLOBAL · RA2.e, RA3.a | [Abrir P03](Plantillas/P03_ARQUITECTURA_GLOBAL.md) |
| P04 | BACKLOG SECUENCIADO · RA3.a | [Abrir P04](Plantillas/P04_BACKLOG_SECUENCIADO.md) |
| P05 | MATRIZ RECURSOS Y LOGISTICA · RA2.f, RA3.b | [Abrir P05](Plantillas/P05_MATRIZ_RECURSOS_Y_LOGISTICA.md) |
| P06 | PERMISOS Y AUTORIZACIONES · RA3.c | [Abrir P06](Plantillas/P06_PERMISOS_Y_AUTORIZACIONES.md) |
| P07 | PROCEDIMIENTOS DE EJECUCION · RA3.d | [Abrir P07](Plantillas/P07_PROCEDIMIENTOS_DE_EJECUCION.md) |
| P08 | ASIGNACION CAPACIDAD PERSONAS TIEMPOS · RA3.f | [Abrir P08](Plantillas/P08_ASIGNACION_CAPACIDAD_PERSONAS_TIEMPOS.md) |
| P09 | RIESGOS PREVENCION CONTINGENCIA · RA3.e | [Abrir P09](Plantillas/P09_RIESGOS_PREVENCION_CONTINGENCIA.md) |
| P10 | DEPENDENCIAS INTERMODULARES Y PUERTAS · RA3.a, RA3.b, RA3.c, RA3.e | [Abrir P10](Plantillas/P10_DEPENDENCIAS_INTERMODULARES_Y_PUERTAS.md) |
| P11 | DECISIONES SUPUESTOS TBD · RA2.c, RA3.a, RA3.e | [Abrir P11](Plantillas/P11_DECISIONES_SUPUESTOS_TBD.md) |
| P12 | EVIDENCIA G1 Y CHECKPOINT INDIVIDUAL · RA2.c, RA2.e, RA2.f, RA3.a, RA3.b, RA3.c, RA3.d, RA3.e, RA3.f | [Abrir P12](Plantillas/P12_EVIDENCIA_G1_Y_CHECKPOINT_INDIVIDUAL.md) |

## Datos abiertos y edición

[plan_real.json](Plantillas/plan_real.json) es una plantilla sin catálogo ni tareas reales. Sus componentes apuntan a los doce documentos. `null` significa dato desconocido; `[]` es una colección aún sin entradas. No escribas 0 como estimación si no sabes el valor. Mantén `PENDIENTE_CATALOGO` hasta recibir y cotejar el anexo. Las tareas contractuales y de ejecución se relacionan; no son listas intercambiables.

[Contrato de datos](Plantillas/FORMATO_PLAN.md) describe los campos y controles. El equipo puede usar solo Markdown; el docente dispone de validación del JSON equivalente. Rellena la tabla y el dato de forma coherente; un parseo correcto no evalúa por sí mismo tu planificación.

Ejemplo mínimo de clave sintética: TRAIN-E1A pertenece a una copia TRAIN y apunta a una referencia TRAIN del caso de ejemplo. Ejemplo de dato real desconocido: anexo `PENDIENTE_CATALOGO`, tareas `[]`, huella `null`. Nunca cambies ese vacío por una fila con un ID parecido al catálogo.

## Importación posterior del contrato auténtico

El docente distribuye el XLSX y anexo de equipo por canal autorizado; registra procedencia/versión/huella y coteja las 264/572/96/150, IDs y AT congelados con la fuente. No se promete reconstrucción ni importación automática de hojas desconocidas. El equipo traslada **literalmente** las filas seleccionadas a su anexo privado y referencias P04; contrasta recuento, unicidad, núcleo y dependencias con el docente. Hasta completar ese control no cambia a COTEJADO.

Añade actividades de ejecución locales debajo de las referencias auténticas, sin generar nuevos AT. Cuando el orden/horas cambie conserva la versión anterior. Si cambia alcance, espera el CR prospectivo aprobado y referencia su nueva vigencia. No conviertas la huella o una casilla COTEJADO en sustituto del cotejo humano.

---

[Índice de PI3](../README.md) · [Inicio del módulo](../../README.md)
