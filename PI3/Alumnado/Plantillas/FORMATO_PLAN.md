# Contrato de datos del plan PI3 · versión 1.0

Plantilla abierta, UTF-8, JSON estándar. No permite comentarios ni comas finales. Markdown P01–P12 conserva el razonamiento; JSON permite comprobar relaciones. El validador docente acepta plantilla real pendiente o escenario TRAIN completo, y rechaza una aceptación real sin fuente cotejada.

| Campo | Tipo y regla | Significado |
|---|---|---|
| version / naturaleza | texto / REAL o TRAIN | Identidad del paquete |
| at_son_horas | booleano false | Prohibición de conversión inventada |
| contrato | objeto estado, baseline, huella_catalogo, tareas | REAL en producción: PENDIENTE_CATALOGO, huella null y tareas vacías |
| componentes | objeto con exactamente P01…P12 y ruta relativa | Documentos del mismo paquete |
| personas | lista id, capacidad_h, reserva_h, por_dia | PERSONA-A…D; horas no negativas y disponibilidad por día |
| actividades | lista de objetos descritos debajo | Trabajo de ejecución hipotético TRAIN; REAL vacío hasta catálogo |
| recursos | lista id, capacidad_simultanea | Capacidad material/entorno |
| permisos | lista id, disponible_dia, estado, evidencia | Preparación y prueba saneada, no secreto |
| riesgos | lista causa, impacto, probabilidad, prevencion, medios, trigger, contingencia, responsable, revision, estado | Identificadores TRAIN en ficción |
| decisiones | lista id, objeto, responsable, revision, evento_cierre, estado | Supuestos cerrables e historia en P11 |
| puertas | exactamente G2, G3, G4 y G5 | NO_ACTIVADA/PREPARADA/ACTIVA/BLOQUEADA_DEPENDENCIA/RECUPERADA, con competencia, criterio, evidencia, dependencia, condición, recuperación y decisión |
| g1 | estado, decision_docente, evidencia_individual, pendientes | No se concede automáticamente; caso TRAIN queda SIMULACION |

Una actividad TRAIN tiene: `id`, `descripcion`, `contrato` (lista de IDs TRAIN del contrato sintético), `depende` (IDs de actividades FS), `inicio_dia`, `fin_dia` (enteros 1…10), `esfuerzo_h`, `persona`, `backup`, `recursos` (IDs), `permisos` (IDs), `entrada`, `salida`, `hito`, `preparacion` y `evidencia`. Las horas se distribuyen uniformemente entre jornadas de la ventana para esta comprobación didáctica. Si tu plan usa reparto desigual, exprésalo en Markdown y pide contraste; no fuerces números falsos para encajar en el comprobador.

FS exige inicio posterior al fin de las predecesoras. La demostración automática usa FS; SS se puede justificar en Markdown con entrada parcial/control de salida y revisar manualmente, sin llamarlo PASS del grafo FS. No incluyas AT en una actividad: referenciar resultado contractual no crea alcance nuevo. La huella de catálogo auténtico no existe en la ficción.

Controles: claves únicas y conocidas, ausencia de ciclos, coherencia temporal, disponibilidad por persona/día y total neto, recurso compartido, permiso previo, trigger/medios, decisión de puerta y estado G1. El validador no observa una clase, no coteja un XLSX que no tiene y no evalúa comprensión.

---

[Índice de PI3](../../README.md) · [Inicio del módulo](../../../README.md)
