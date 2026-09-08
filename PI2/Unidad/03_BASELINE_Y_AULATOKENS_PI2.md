# Baseline contractual v1.0 y AulaTokens
## Autoridad y congelación
Prevalece AulaFlow 2.0 v1.0: **264 tareas / 572 AT de oferta / 96 tareas obligatorias / 150 AT obligatorios**. Núcleo por ámbito: PI II 25, AD 70, PMDM 25, DI 30 AT. La suma es 150; no son pesos de nota ni reparto entre personas.

La baseline adopta vertical mínimo, contrato corto y CR v0.4. Su nombre histórico no los devuelve a borrador. El nombre del libro adoptado es Presupuesto_AulaFlow_2_0_auditado_v0.4.xlsx; la distribución se identifica como baseline v1.0. No confundirlo con la matriz curricular XLSX.

IDs y AT están congelados. Las referencias anuales de presupuesto —1001 horas-persona de oferta y 320 del núcleo— no equivalen a las 900 min de PI2 ni establecen 1 AT = 1 hora. PI2 no hace distribución detallada de esfuerzo.

## Leer el catálogo cuando se suministre
Jerarquía contractual: **módulo/ámbito → especificación/funcionalidad → tarea/entregable → aceptación/evidencia**. El ámbito sitúa propiedad; la especificación agrupa comportamiento; la tarea es la unidad de selección y cómputo.

Identifica tarea/entregable, ID, tipo, AT, dependencias y alternativas declaradas. El núcleo obligatorio se incluye íntegro; una opcional no lo sustituye. Una opcional/avanzada seleccionada se convierte en compromiso. ALT solo opera cuando la fuente lo permite explícitamente.

Especificación no equivale a fila de tarea. El mismo resultado no suma por aparecer en contrato, issue, PR y demo. No contar una puerta como tarea ni asignar el valor completo a cada colaborador.

El XLSX contractual auténtico ha sido recuperado y cotejado por el docente. Se distribuye por el canal autorizado del curso; no se reconstruye desde esta biblioteca. E05 continúa vacío PENDIENTE_CATALOGO, con totales null/desconocidos, hasta que tu equipo recibe la fuente y coteja su selección. Antes de contratar se comprueba el acceso desde vista estudiante; recuperar el catálogo no firma ni acepta el contrato de un equipo.

## Contratado, realizado y aceptado
Solo **ACEPTADA** valida AT. Estar seleccionado, terminado, entregado o con PR verde no basta. Hace falta evidencia aplicable y aceptación humana conforme al acuerdo. No se aceptan futuras implementaciones por entregar PI2.

AT_equipo = AT validados del equipo / tamaño real del equipo.
AT_efectivo = 0,40 × AT_equipo + 0,60 × AT_personal.

| AT efectivos, sin redondear al tramo superior | Techo |
|---|---:|
| Menos de 50 | Contrato insuficiente para aprobar |
| 50 ≤ AT < 60 | 5 |
| 60 ≤ AT < 70 | 6 |
| 70 ≤ AT < 80 | 7 |
| 80 ≤ AT < 90 | 8 |
| 90 ≤ AT < 100 | 9 |
| AT ≥ 100 | 10 |

59,9 sigue en techo 5. No se transforma un decimal en el tramo siguiente. Nota final PI = min(nota curricular, techo AT). Se mantienen todos los RA ≥5, presencial ≥5, evidencia individual y puertas exigibles. Muchos AT no compensan un RA insuficiente.

Ejemplo agregado ficticio: 240 contratados; solo 180 aceptados; tres personas con contribuciones validadas dadas 40, 60 y 80. Media 60; efectivos 48, 60 y 72: insuficiente, 6 y 7. No asignar esa distribución a un equipo real ni aceptar 240 por prometerlos.

## Tamaño de equipo y núcleo
Esta tabla es una referencia matemática de alcance total **aceptado con contribuciones equilibradas**, no una asignación operativa:

| Tamaño | Suelo 5 | Techo 6 | 7 | 8 | 9 | 10 |
|---|---:|---:|---:|---:|---:|---:|
| 2 | 100 | 120 | 140 | 160 | 180 | 200 |
| 3 | 150 | 180 | 210 | 240 | 270 | 300 |
| 4 | 200 | 240 | 280 | 320 | 360 | 400 |

El núcleo obligatorio continúa siendo 150: dos personas no pueden recortarlo a 100. Para cuatro, solo núcleo equilibrado da 37,5 efectivos, insuficiente. No asumir equilibrio personal ni confundir selección con aceptación.

## Vertical, puertas y PI3
Se conserva H0 legado; H1 contrato y posterior planificación/base; H2 backend y clientes con autenticación; H3 Kanban compartido Flutter/MAUI y migración; H4 calidad; H5 release/runbook/demo/retrospectiva/defensa. Son referencias del producto, no filas/AT nuevos ni un plan de fechas.

G0, G1, G6 y G7 activas desde inicio. G2–G5 requieren activación expresa, aceptación observable, justificación curricular, disponibilidad de competencia/tecnología y recuperación. Puertas 0 AT.

G1 incluye contrato, backlog, planificación y repositorio profesional. PI2 prepara su componente contractual; solo puede establecerse tras G0, catálogo y confirmación real. G1 EN_PROGRESO hasta completar PI3. Campos de responsables/personas/horas/sprints/recursos/hitos/riesgos formales/arquitectura global: PENDIENTE_PI3.

## Cambio prospectivo
Antes de confirmar: revisión de propuesta. Después: solicitud → motivo → impacto → propuesta → aprobación → revisión efectiva del contrato. Un CR pendiente no modifica la baseline. Mantener IDs/AT, histórico aceptado y atribución; un cambio de catálogo necesita decisión/versionado competente.

Cambio de equipo: congelar lo aceptado y atribución, reconocer nuevo tamaño real y revisar prospectivamente el alcance restante. PI2 explica el efecto contractual; no reparte personas/tiempos. Impactos operativos no definidos: PENDIENTE_PI3, no cero.

---

[Índice de PI2](../README.md) · [Inicio del módulo](../../README.md)
