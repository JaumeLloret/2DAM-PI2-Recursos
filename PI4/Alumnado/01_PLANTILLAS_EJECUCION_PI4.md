# Plantillas E01–E10 · un sistema de ejecución

Copia en un espacio autorizado. Encabeza cada registro con modo TRAIN/REAL, versión, fecha, fuente y autoría por código. Si desconoces un dato, usa TBD y añade responsable/evento de contraste. Las tablas vacías no son evidencia completada. Se admiten documentos separados o uno con estos diez encabezados; se evalúa coherencia, no formato.

## E01 · Recepción y baseline

| Entrada PI3 | Versión/fuente exacta | Confirmado/cambio/TBD | Consecuencia para ejecución | Responsable y próximo contraste |
|---|---|---|---|---|
| P01–P04: fases, dependencias, arquitectura, backlog | TBD | TBD | TBD | TBD |
| P05–P08: recursos, permisos, procedimiento, capacidad | TBD | TBD | TBD | TBD |
| P09–P12: riesgos, puertas, decisiones, G1 | TBD | TBD | TBD | TBD |

Contrato: PENDIENTE_CATALOGO hasta cotejo auténtico; referencia/huella/versiones TBD; tareas e IDs reales vacíos. Baseline de ejecución actual: TBD. Diferencia entre acuerdo y previsión: justificar. No conceder G1 por recibir el paquete.

## E02 · Procedimiento, tablero y revisión

| Transición | Entrada necesaria | Actor autorizado | Acción | Salida/evidencia | Control | Si falla |
|---|---|---|---|---|---|---|
| READY → ACTIVE | TBD | TBD | TBD | TBD | Capacidad/entrada suficientes | No iniciar; registrar causa |
| ACTIVE → REVIEW | TBD | TBD | TBD | TBD | Criterio y corte identificados | Completar salida |
| REVIEW → DONE_TECH | TBD | TBD | TBD | TBD | Revisión efectuada | Devolver y conservar comentario |
| Cualquier estado → BLOCKED | TBD | TBD | TBD | TBD | Impacto/condición de desbloqueo | Escalar al rol acordado |

Periodicidad del seguimiento: TBD. Variables/fuentes/umbral/acción: TBD. Límite WIP y tratamiento de bloqueadas: TBD. Regla para revisar una versión posterior: TBD. DONE_TECH no equivale a ACEPTADA; Projects es soporte, no autoridad de aceptación.

## E03 · Valoración económica

| Concepto | Unidad | Cantidad prevista | Tarifa/fuente/supuesto | Incurrido | Restante estimado | Reserva restante | Explicación de desvío |
|---|---|---|---|---|---|---|---|
| Trabajo por persona/actividad | horas-persona | TBD | TBD | TBD | TBD | TBD | TBD |
| Recurso único/compartido | unidad/período | TBD | TBD | TBD | TBD | TBD | Evitar doble imputación |

Baseline directa + reserva = total aprobado: TBD. Previsión = incurrido + restante + reserva restante: TBD. Diferencia comparable: TBD. Alternativas y autoridad de decisión: TBD. No convertir AT a horas ni tarifas TRAIN a precios reales; sin fuente auténtica, supuesto identificado.

## E04 · Registro y triage de incidencia

ID local: TBD; modo: TBD; registrada en: TBD; versión afectada: TBD. Fuente/entrada/pasos: TBD. Resultado esperado: TBD. Resultado obtenido: TBD. Impacto: TBD; urgencia: TBD; prioridad razonada: TBD. Causa confirmada o hipótesis: TBD. Relación con riesgo/incidencia previa: TBD. Responsable: TBD; siguiente control: TBD. Datos saneados y permiso: TBD.

## E05 · Solución y verificación

Incidencia: TBD. Opciones: corregir / mitigar / posponer justificadamente. Acción elegida y motivo: TBD. Responsable/autoridad: TBD. Resultado esperado antes de ejecutar: TBD. Evidencia posterior y corte: TBD. Revisor y decisión: TBD. Estado final: ABIERTO / MITIGADO / PENDIENTE_VERIFICACION / CERRADO_VERIFICADO. Limitación y condición de reapertura: TBD. Documentos afectados: TBD. Una mitigación con fake no demuestra integración real.

## E06 · Solicitud y análisis de cambio

ID y fecha: TBD; solicitante por código: TBD; motivo: TBD. Actividades/referencias contractuales auténticas afectadas: TBD. Si no hay catálogo, mantener referencias contractuales vacías. En TRAIN usar TRAIN-CR*. No alterar el namespace contractual.

| Alternativa | Alcance antes/después | Horas/capacidad | Coste restante | Hitos/dependencias | Riesgos/puertas | Atribución | Ventajas/limitaciones |
|---|---|---|---|---|---|---|---|
| A | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| B | TBD | TBD | TBD | TBD | TBD | TBD | TBD |

AT antes/después: TBD hasta fuente auténtica; valores del catálogo congelados. Decisión PENDIENTE / APROBADO / RECHAZADO. Autoridad, fecha y evidencia de decisión: TBD. Propuesta preferida y motivo: TBD. No aplicar al contrato mientras falte aprobación.

## E07 · Rebaseline

| Versión anterior y fuente | Cambio/decisión | Nueva versión | Fecha de decisión | Vigencia desde | Qué permanece congelado | Qué se actualiza |
|---|---|---|---|---|---|---|
| TBD | TBD | propuesta TBD | TBD | TBD | Aceptación y atribución anteriores válidas | Trabajo futuro autorizado |

Lista de documentos/tablero afectados: TBD. Revisión de consistencia: TBD. La vigencia no precede a la aprobación; el registro anterior se conserva. Una corrección factual fechada hoy no se presenta como decisión histórica.

## E08 · Riesgos y contingencia de ejecución

| Causa-evento-consecuencia | Disparador observable | Responsable | Prevención | Contingencia | Capacidad/recurso necesario | Incidencia relacionada | Próxima revisión |
|---|---|---|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |

No incorporar datos de salud/familia o secretos. Una pérdida de disponibilidad se expresa como capacidad y efecto; el motivo privado queda fuera.

## E09 · Capacidad y contribución individual

| Código | Disponibilidad restante | Reserva | Compromiso/revisión | Actividad/evidencia exacta | Responsabilidad | Colaboración/revisión | Qué puede explicar/modificar |
|---|---|---|---|---|---|---|---|
| PERSONA-A | TBD | TBD | TBD | TBD | TBD | TBD | TBD |

Cada evidencia requiere contenido, no solo conteo. Horas-persona de una colaboración se contabilizan por persona. Congela atribución de trabajo ya aceptado; no redistribuyas historia al cambiar de equipo. Una discrepancia se contrasta individualmente.

## E10 · Retrospectiva y traspaso a PI5

| Hecho/fuente | Interpretación y límite | Decisión/mejora | Responsable/evento | Señal para contrastarla |
|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD |

| Evidencia a PI5 | Corte/ubicación autorizada | Capacidad realmente disponible | Estado y limitación | Pendiente/acción/rol |
|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD |

Registra G0/G1/G6/G7 sin concederlas; G2–G5 solo con activación expresa y oportunidad. No incluir aceptación final, AT validados o release real si no existen. Checklist final: documentos coherentes, enlaces accesibles al rol, versiones exactas, TRAIN separado, ausencia de datos sensibles y explicación individual.
