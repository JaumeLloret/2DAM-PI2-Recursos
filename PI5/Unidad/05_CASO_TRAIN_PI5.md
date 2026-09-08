# ReservaLab Validación · expediente TRAIN completo

**Ficción didáctica.** Recibe E10 del caso PI4: consulta, reserva, cancelación e importación; baseline de ejecución TRAIN-B2; integración pendiente tras ensayo simulado; revisión con devoluciones; no aceptación final. Este expediente suministra nuevas tarjetas sintéticas para practicar PI5. No relata una ejecución de PI4, no contiene datos reales, no asigna AT y no necesita que programes ReservaLab. C1/C2 son cortes ordinales del caso, sin fecha de curso ni FE.

## Pliego de ejercicio y roles

| Ref. TRAIN | Condición a validar en este ejercicio |
|---|---|
| TRAIN-01 consulta | Mostrar disponibilidad coherente para fecha y recurso; rechazar una entrada de consulta inválida con explicación |
| TRAIN-02 reserva | Admitir una petición válida y rechazar una segunda que solape; consulta y reserva deben compartir la decisión en el servicio integrado |
| TRAIN-03 cancelación | Retirar de activas, conservar historial y comunicar con claridad el efecto para que el usuario pueda confirmar lo ocurrido |
| TRAIN-04 importación | Admitir fila válida y rechazar fila inválida sin insertarla; conservar informe de rechazo |

Roles ficticios: equipo PERSONA-A/B/C; revisor TRAIN-REV; responsable del pliego TRAIN-RESP. No hay firma ni decisión final de TRAIN-RESP suministrada. G3 tiene tarjeta de activación TRAIN-G3: criterios de evidencia técnica por corte, capacidad disponible en el escenario, revisión y recuperación por retest corregido; G2/G4/G5 no tienen activación suministrada. G0/G1/G6/G7 se registran conforme al marco, sin satisfacción concedida. Todo rol es dato de ejercicio, no persona real.

Indicadores acordados solo para TRAIN: ejecutar 100 % de ocho comprobaciones funcionales; 0 fallos críticos; evidencia suficiente vigente para las cuatro condiciones; completar sin ayuda 3 de 3 tareas de cancelación en un ensayo exploratorio, sin pretensión estadística. Este último objetivo busca detectar confusión y se retesta al cambiar el mensaje. No es nota ni umbral contractual de AulaFlow.

## Corte C1: ocho comprobaciones planificadas

| Tarjeta | Condición / entrada→esperado | Resultado suministrado, siempre sintético |
|---|---|---|
| TRAIN-T01 | Consulta válida→estado disponible | CONFORME, C1, ensayo de modelo local |
| TRAIN-T02 | Fecha inválida→rechazo explicado | CONFORME, C1, ensayo de modelo local |
| TRAIN-T03 | Reserva válida→reserva creada | CONFORME, C1, ensayo de modelo local |
| TRAIN-T04 | Reserva solapada→rechazo sin inserción | FALLIDA: se admite solapamiento; crítico, C1, modelo local |
| TRAIN-T05 | Cancelar→ya no aparece activa | CONFORME, C1, modelo local |
| TRAIN-T06 | Cancelar→conserva historial | NO_EJECUTADO, no hay registro |
| TRAIN-T07 | Importación válida→fila incorporada | CONFORME, C1, modelo local |
| TRAIN-T08 | Fila inválida→rechazo e informe | NO_EJECUTADO, no hay registro |

TRAIN-BUILD-C1 describe un artefacto candidato construido en el escenario, pero no contiene hash/URL real. No existe registro de instalación ni de servicio integrado. TRAIN-INC-01 documenta el solapamiento; causa aún propuesta y no aprobada. La captura de una pantalla de reserva no subsana esa ausencia. El equipo debe proponer retest y revisar evidencia dependiente, sin implementar la corrección técnica en PI5.

## Tarjetas de participación del corte C1

Estas tres tarjetas simulan sesiones y no prueban que se hayan realizado entrevistas. Se usó la tarea neutral «libera una reserva que ya no necesitas y comprueba qué ha ocurrido». S1 completa sin ayuda y explica que queda historial. S2 se detiene en «Anular», pregunta si borra todos sus datos y solo continúa tras explicación. S3 completa sin ayuda, pero opina que preferiría recibir un correo nuevo. S1 y S3 = 2/3 sin ayuda; S2 recibió ayuda. No hay una escala de satisfacción cumplimentada. El correo no forma parte del pliego de ejercicio.

Mantén hechos separados: la confusión de S2 afecta a claridad de TRAIN-03; el correo de S3 es propuesta de alcance. No inferir causas personales. Diseña la devolución, decide qué merece corrección/retest y qué requeriría solicitud de cambio.

## Corte C2: nueva evidencia e información que sigue faltando

Tarjeta TRAIN-CR-C2: el escenario describe corrección de frontera de reserva y mensaje de cancelación aclarado. El alcance de las cuatro condiciones permanece. Se suministra nueva ejecución sintética de TRAIN-T01…T08 sobre C2, todas CONFORMES en modelo local. El informe incluye ocho casos ejecutados y ocho conformes. No demuestra servicio compartido: se usó un doble para la dependencia. No hay sesión de usuario C2, instalación móvil ni despliegue observado. Se mantienen tres sesiones previstas para el objetivo: iniciadas C2 = 0, cobertura = 0/3 y desempeño entre iniciadas = NO_MEDIDO; no se cancela la previsión por ausencia de observación. TRAIN-BUILD-C2 describe candidato construido con esos cambios, sin enlace ni huella auténticos.

Para TRAIN-01 y TRAIN-04 existe cotejo funcional completo del modelo en C2. TRAIN-02 sigue sin evidencia integrada; TRAIN-03 tiene transición e historial del modelo, pero no retest del mensaje con usuarios. El informe técnico favorable no elimina estos límites. El docente entrega C2 después de haber recibido tu propuesta C1, o puedes mantener dos secciones separadas si trabajas en autonomía; no uses C2 para reescribir lo que se sabía en C1.

## Encargo

Construye V01–V09 con ambos cortes y una propuesta final justificada. Define indicadores, interpreta resultados, diseña documentos de participación, redacta demo de mesa, revisa G3 sin concederla, trata las lagunas y prepara la transición a PI6. «Solicitar retest integrado y de claridad antes de decidir» puede ser una salida profesional suficiente. No rellenes ninguna firma ni concedas ACEPTADA/AT. El producto debe permitir a otra persona repetir los cálculos y localizar por qué cada condición permanece o deja de estar pendiente.

En [entrada.json](../Alumnado/Train/entrada.json) hay datos equivalentes para quien prefiera una tabla estructurada; el dossier textual es suficiente. El modo REAL empieza vacío en su propio espacio, nunca se copia este expediente como historia auténtica.
