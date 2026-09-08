# ReservaLab Ejecución · caso TRAIN de PI4

**Caso ficticio.** Continúa el dominio de ReservaLab conocido en PI3, con un corte de ejecución nuevo y simplificado suministrado aquí. No se afirma que un equipo real ejecutara PI3 ni que estos datos procedan de GitHub. Las referencias TRAIN-01…04 mantienen consulta, reserva, cancelación e importación como contexto; las tarjetas TRAIN-X* son actividades de este ensayo y no catálogo ni tareas de AulaFlow. No se asignan AT.

## Entrada completa

El servicio de préstamo necesita comprobar que consulta y reserva comparten la misma decisión, que la cancelación conserva historial y que la importación rechaza filas inválidas. El equipo ficticio tiene PERSONA-A/B/C. La baseline TRAIN-B1 y sus condiciones se encuentran en [entrada.json](../Alumnado/Train/entrada.json). D1–D10 son jornadas ordinales ficticias sin fecha de curso o FE. No reutilices fechas de PI3 como si se hubiese observado una ejecución.

| Tarjeta | Salida contratada de ejemplo | Actividad de seguimiento | Estimación inicial | Dependencia |
|---|---|---|---:|---|
| TRAIN-X1 | TRAIN-01 | Preparar procedimiento de revisión de consulta | A 4 h | ninguna |
| TRAIN-X2 | TRAIN-02 | Ensayar y revisar frontera de reserva | A 8 h | X1 |
| TRAIN-X3 | TRAIN-03 | Documentar/revisar cancelación e historial | B 8 h | X2 |
| TRAIN-X4 | TRAIN-04 | Coordinar verificación de muestra importada | C 6 h | permiso TRAIN-P1 desde D3 |

TRAIN-X2 incluye, dentro de su estimación, un ensayo comparativo opcional de interfaz que no forma parte del criterio nuclear de reserva. En el corte D5 quedan 3 h de A para ese ensayo; posponerlo requiere 1 h de B para separar su documentación. Esta es la alternativa V5: se conserva la salida nuclear TRAIN-02 y se cambia trabajo futuro de apoyo, sin inventar un entregable contractual.

Las 26 h-persona del proyecto hipotético no son minutos de clase. A tiene tarifa de ejercicio 18 €/h, B 15 €/h y C 12 €/h; recurso único 30 €; reserva inicial 10 % del directo. Revisión se considera dentro de las estimaciones por tarjeta; si propones una revisión adicional debes presupuestarla. No hay AT ni tarifas de AulaFlow.

## Secuencia de eventos a procesar

| Evento | Momento ficticio | Dato de entrada | Qué debes decidir/documentar |
|---|---|---|---|
| TRAIN-V1 | D2 | X1 tiene documento pero no comprobación de rechazo; la autora pide DONE_TECH | Revisión y devolución justificadas; E02/E04 |
| TRAIN-V2 | D3 | Permiso P1 disponible para muestra sintética; no hay permiso sobre datos personales | Actualizar disponibilidad, mantener frontera de privacidad |
| TRAIN-V3 | D4 | El servicio compartido no responde; el ensayo con respuesta simulada sí funciona | Impacto, mitigación y condición de prueba real; no cerrar integración |
| TRAIN-V4 | D5 | Corte de consumo A=14 h, B=7 h, C=5 h; recurso pagado. Restante A=4 h, B=3 h, C=2 h | Recalcular previsión, justificar causa y comparar alternativa |
| TRAIN-V5 | D5 | El coordinador ficticio propone retirar trabajo opcional: ahorro A=3 h, preparación extra B=1 h | Redactar CR pendiente; no asumir aprobación; E06 |
| TRAIN-V6 | D6 | La autoridad ficticia aporta decisión TRAIN-DEC-01: se aprueba posponer esa salida opcional desde D7, sin tocar núcleo ni atribución previa | Generar TRAIN-B2 prospectiva y vincular decisión |
| TRAIN-V7 | D7 | C no tiene disponibilidad restante; B puede asumir una revisión de 1 h si otra actividad se desplaza | Recalcular capacidad y contingencia, sin inventar motivo personal |
| TRAIN-V8 | D8 | Servicio disponible, pero evidencia aportada solo corresponde al ensayo simulado D4 | Mantener verificación real pendiente; solicitar salida del nuevo corte |
| TRAIN-V9 | D9 | Se aporta registro sintético de cotejo TRAIN-EV-09: criterios de frontera coinciden en esa muestra; no incluye uso en hardware | Revisar alcance exacto y limitación del resultado |
| TRAIN-V10 | D10 | Retrospectiva: dos devoluciones por criterios incompletos y tres por falta de revisión disponible | Mejora de proceso y handoff a PI5; no aceptación final automática |

TRAIN-DEC-01 y TRAIN-EV-09 son tarjetas de un caso, no decisiones ni pruebas auténticas del docente. Una solución del caso puede registrar SIMULADO, pero nunca OBSERVADA_REAL. Los eventos con datos incompletos deben seguir incompletos; se evalúa si identificas la información necesaria.

## Trabajo por iteraciones

En A03 congela E01 y tablero inicial. En A06 procesa V1–V3. En A07/A08 resuelve V4 y procedimiento de verificación; en A09 prepara E03–E05. En A10/A11 procesa V5–V6; en A12 conserva versiones. En A14/A15 procesa V7–V8. En A17 procesa V9 solo como evidencia sintética, identificando qué no observa. En A16/A18 trabaja V10 y E10. No se exige programar ReservaLab.

## Producto esperado sin oráculo

Un dossier E01–E10 coherente y un tablero con transiciones explicadas. Debe poder reconstruirse por qué no se aceptó una salida, qué se ensayó con fake, cuándo se cambió la baseline y qué parte económica seguía desviada. El registro individual debe sostener al menos una decisión y una revisión. Puede haber alternativas válidas si respetan las entradas, recursos y autoridad.
