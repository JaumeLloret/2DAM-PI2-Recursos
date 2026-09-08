# PI6 · Entregar, explicar y permitir continuidad

## 1. Tres cierres que conviene distinguir

Cerrar un dossier de aprendizaje significa que sus evidencias están reunidas y su estado explicado. Cerrar una entrega de proyecto exige identificar qué recibe alguien, en qué versión y con qué límites. Cerrar una evaluación requiere juicio docente por RA/CE y condiciones del módulo. Ninguno ocurre automáticamente porque los otros dos tengan una carpeta llamada «final».

PI5 conserva la decisión de aceptación basada en pliego/evidencia. PI6 recibe esa decisión o su ausencia y prepara entrega, defensa y continuidad. Si un requisito no estaba acreditado, sigue pendiente hasta nueva evidencia pertinente; no se vuelve conforme al escribir notas de versión. Puedes entregar profesionalmente un paquete candidato con pendientes claros cuando ese es su estado auténtico. Lo que no puedes es presentarlo como release aceptada.

PI6 no introduce CE exclusivos. F01–F10 integra evidencias de criterios ya existentes: documentación, procedimientos, riesgos, seguimiento, cambios, calidad y cumplimiento. Su valor depende de lo que observes, no de la etiqueta del documento. Una defensa clara puede confirmar que comprendes la evidencia; no sustituye un procedimiento ausente ni crea una nota de comunicación paralela.

## 2. Inventario que otro pueda verificar

Un inventario útil contiene identificador local, nombre, propósito, versión, ubicación, relación con requisito/evidencia, rol destinatario, permiso, estado y límite. No es solo una lista de archivos. «manual.pdf» no dice si corresponde al candidato. «Manual de operación C2, revisión 3, para operador autorizado; instalación real pendiente» permite saber para qué sirve y qué no afirmar.

Un manifiesto representa el contenido esperado de un paquete. Al comprobarlo, busca archivos ausentes, repetidos, sobrantes sensibles y rutas que escapen del paquete. Una huella criptográfica permite contrastar si unos bytes coinciden con los descritos; no prueba calidad, autoría, aceptación o ausencia de código malicioso. Si una huella cambia al corregir documentación, actualiza el manifiesto del nuevo corte y conserva el anterior. No inventar hashes de artefactos que no existen.

En el TRAIN se entregan archivos reales de contenido ficticio. Sus huellas se pueden calcular de verdad; eso solo acredita integridad de esos archivos didácticos. No acredita una aplicación ReservaLab desplegada. Distinguir ambos niveles evita que una comprobación técnica legítima termine convertida en una afirmación falsa sobre el proyecto real.

## 3. Mapa final de requisitos y estados

F02 parte de V03/V09 de PI5. Conserva requisito, condición, corte, evidencia, decisión y limitación. Añade ubicación final y responsable del pendiente. No cambia el contrato ni borra el resultado anterior. Si una condición se corrigió, referencia la nueva evidencia y la decisión auténtica que permite actualizar el estado. Si no, explica la condición de retest.

No confundas AUSENTE con NO_APLICA. AUSENTE significa que se esperaba evidencia y falta. NO_APLICA necesita razón válida y autoridad cuando afecta al compromiso. PENDIENTE no es un eufemismo para conforme: debe tener causa, efecto, rol y evento de contraste. ACEPTADA es un estado contractual que exige base auténtica; en TRAIN solo se practican propuestas. Sin catálogo, REAL permanece PENDIENTE_CATALOGO y no se calcula alcance nominal.

Evita una tabla tan resumida que pierda el criterio observado. Una fila «pruebas: verde» oculta versión y límite. Una fila «modelo local C2 conforme en ocho casos; integración con servicio pendiente» conserva la frontera. PI6 puede mejorar la claridad del mapa sin reenseñar testing técnico ni recalificarlo como contenido propio.

## 4. Paquete final, candidate y notas de versión

Un paquete preparado para entrega contiene instrucciones de entrada, inventario, versión exacta, documentación de uso/operación, evidencia de verificación, límites y canal/rol de continuidad. Si procede una aplicación o servicio, se referencia el artefacto auténtico ya producido por su módulo/rol propietario. No se programa un sistema nuevo para simular cierre.

Las notas de versión responden: qué cambia, qué permanece, qué necesita el receptor, qué incompatibilidad o migración hay, qué se comprobó y qué queda pendiente. Un texto «mejoras y correcciones» no permite decidir si actualizar. Relaciona un cambio con su motivo y evidencia sin exponer datos sensibles. Si no hay despliegue autorizado, estado «paquete candidato preparado», no «publicado en producción».

La numeración ayuda a comunicar, pero una etiqueta por sí sola no inmoviliza el contenido. Usar referencia exacta y manifiesto permite reconstruir el corte. Si se modifica después, crear nueva revisión y repetir las comprobaciones afectadas; no mantener una afirmación de validación del HEAD anterior como si correspondiera al nuevo. Esta regla aplica también a documentación y a la campaña del curso.

## 5. Uso, operación y transferencia

La guía de uso se dirige a quien realiza tareas: propósito, condiciones, pasos, resultados y recuperación comprensible. La guía de operación se dirige a quien mantiene el servicio o paquete: prerrequisitos, configuración sin secretos, verificación, copia/retorno cuando proceda, escalado y límites. No son el mismo documento con título distinto.

Un procedimiento de transferencia define emisor/receptor por rol, contenido, acceso permitido, estado inicial, pasos de comprobación, resultados esperados, incidencias y registro de recepción. Antes de decir «entregado», comprobar que el receptor autorizado puede localizarlo. Una URL accesible por su creador puede no serlo por quien recibe. Ajustar el permiso necesario es preferible a publicar información reservada.

El ensayo de mesa recorre el procedimiento con documentos/datos sintéticos. Sirve para detectar falta de pasos, contradicciones y dependencias, pero no demuestra que el servicio arranque ni que un receptor real lo haya usado. Si no existe entorno, dejar PENDIENTE_ENTORNO y describir la comprobación futura. El rol del centro confirma cuándo y cómo se puede hacer; PI6 no inventa una instalación real.

## 6. Known issues, deuda y riesgo

Un problema conocido es un comportamiento o carencia ya identificado: versión, condición de aparición, impacto, evidencia, estado, mitigación y condición de cierre. La deuda expresa trabajo pendiente que dificulta continuidad o mejora; debe describir consecuencia y criterio para abordarlo. Un riesgo es una posibilidad futura con causa-evento-consecuencia, disparador, prevención, contingencia y responsable.

No confundir mitigación con solución definitiva. Si un doble permite ensayar mientras falta servicio, la integración sigue pendiente. Si un manual sugiere evitar una función, registrar qué compromiso queda afectado. «No se detectaron errores» solo describe el alcance de unas pruebas; no prueba ausencia universal de fallos.

La transferencia necesita prioridades justificadas. Un error que compromete integridad de datos puede requerir parada antes que una mejora visual; la prioridad depende del contexto y evidencia, no solo de una etiqueta. PI4 mantiene el procedimiento de incidencia/cambio y PI5 la condición de retest/aceptación. PI6 los reúne para que quien continúa sepa qué hacer sin reconstruir todo desde conversaciones dispersas.

## 7. G6 y G7 como revisión con evidencia

G6 reúne documentación, release, demo y defensa individual. Tener un índice no acredita que todos esos componentes estén disponibles y hayan sido observados. Registrar por componente fuente, corte, alcance y pendiente. Una demo de mesa y un ensayo de defensa son preparación; si el contrato exige observación real, esa parte no está satisfecha hasta que exista evidencia auténtica.

G7 se centra en trazabilidad de incidencias, cambios y decisiones. La cadena permite reconstruir entrada→análisis→decisión→acción→verificación, con autoría, versión y vigencia. No toda fila debe estar cerrada: una incidencia pendiente bien descrita puede mostrar trazabilidad. Lo insuficiente es hacerla desaparecer o asignarle una aprobación retroactiva inexistente.

Las puertas G0/G1/G6/G7 están activas según marco, no satisfechas por defecto. G2–G5 mantienen las cinco condiciones de activación y oportunidad curricular. PI6 no activa tecnologías que el alumnado nunca pudo usar ni transforma una decisión de calendario pendiente en incumplimiento automático. Cada puerta aplicable conserva su mecanismo de recuperación.

## 8. Defensa individual del sistema y del proceso

Una defensa profesional es un contraste de comprensión y responsabilidad. Puede pedir localizar una evidencia, explicar su relación con una necesidad, justificar una decisión, mostrar una limitación y modificar una parte ante una nueva entrada. No se reduce a recitar diapositivas ni a hablar solo de la feature propia. La pregunta puede abordar cualquier parte esencial del sistema/proceso.

Prepara un guion breve: contexto y alcance; recorrido de una condición a su evidencia; decisión difícil y alternativas; estado actual y riesgo; contribución/revisión propia. Para cada afirmación, ten una ubicación concreta. Si no sabes un dato, localiza la fuente o explica qué falta; improvisar una certeza es peor que delimitar conocimiento.

La modificación individual permite comprobar transferencia. Si cambia un corte, indicador, requisito o disponibilidad, debes explicar qué documento se afecta y qué afirmación deja de ser válida. Durante la observación no hay agente. En preparación puedes usar asistencia declarada, pero debes revisar y sostener el resultado. El docente registra el comportamiento observado y el CE existente que informa, sin una calificación nueva por estilo escénico.

## 9. Contribución y responsabilidad sin contadores

Un registro de contribución enlaza persona/código con tarea o decisión, evidencia exacta, responsabilidad, colaboración, revisión y capacidad de explicación/modificación. El conteo de commits o líneas no describe complejidad, calidad, ayuda recibida o aprendizaje. Una revisión que detectó una condición crítica puede aportar evidencia importante aunque no produzca muchas líneas.

La defensa global evita que el reparto de tareas impida comprender lo esencial. No exige saber cada detalle técnico ajeno, pero sí las decisiones, interfaces, riesgos y flujo de evidencia pertinentes al proyecto. Si alguien no puede explicar una evidencia atribuida, el docente pide contraste y nueva evidencia; no inventa un porcentaje de colaboración para repartir nota.

Si cambió el equipo, mantener aceptación/atribución ya válidas, documentar capacidad restante y rebaseline prospectiva según el procedimiento. No redistribuir retrospectivamente contribuciones para obtener AT. Los datos privados que expliquen disponibilidad no pertenecen al dossier público; basta el efecto de capacidad permitido.

## 10. Retrospectiva con hechos y experimento

Una retrospectiva útil empieza por hechos localizables, no por «trabajamos bien». «Hubo dos devoluciones por criterio incompleto y tres por falta de revisión» permite investigar un patrón. La interpretación propone una explicación y reconoce otras posibles. La decisión de mejora define un cambio pequeño, responsable, coste/capacidad, señal y evento de revisión.

No afirmar causalidad con una comparación pequeña que cambia varios factores. Si después de introducir checklist bajan devoluciones de 5 a 2, también pudo variar tamaño de tareas o disponibilidad. Conserva denominador y contexto. Puedes proponer probar entrada de revisión con criterio explícito y reserva de tiempo, medir devoluciones por causa y contrastar en la siguiente oportunidad confirmada, sin inventar fecha de retorno.

No esconder fallos para producir una retrospectiva positiva. Documentar un experimento que no mejoró y explicar el siguiente ajuste es evidencia de control. La retrospectiva final integra lo aprendido, pero no vuelve a ejecutar el seguimiento de PI4 ni concede aceptación de PI5.

## 11. Refuerzo de RA/CE existentes

El refuerzo se diseña desde una carencia concreta: CE original, evidencia anterior, qué no acreditaba, tarea nueva, producto, instrumento y autenticidad. Si faltaba un procedimiento de participación, una portada más bonita no lo recupera. Si faltaba explicar una decisión, puede hacer falta un cambio individual nuevo, no repetir el mismo discurso.

La tabla de refuerzo mantiene propietarios PI2/PI3/PI4/PI5 y literales exactos. No exige trabajar todos; sirve para seleccionar lo pertinente. Otras carencias se toman de la matriz original. Las evidencias de empresa solo se incorporan cuando corresponden al plan formativo individual y con permisos; no se convierten automáticamente en nota ni se exige relatar datos confidenciales.

La evaluación global conserva RA1 15 %, RA2 25 %, RA3 30 %, RA4 30 %, todos ≥5, caso presencial obligatorio ≥5, evidencia individual y puertas activadas satisfechas/recuperadas. La contribución agregada objetivo del caso profesional es 20 % distribuida por RA/CE. El techo AT limita alcance con base auténtica, nunca eleva nota curricular. PI6 no añade un porcentaje de defensa o mantenimiento.

## 12. Registrar un cierre honesto

F10 enumera qué se entrega/prepara, qué se verificó realmente, qué observación queda pendiente y qué evento permitirá completarla. PENDIENTE_CALENDARIO_RETORNO sigue vigente hasta fechas confirmadas; PENDIENTE_DEFENSA hasta observación; PENDIENTE_CATALOGO hasta fuente auténtica. Estos estados no se sustituyen por una fecha ficticia para que la tabla parezca terminada.

El estado curricular, la aceptación contractual, la integridad del paquete y la disponibilidad del entorno se registran por separado. La persona receptora solo confirma lo que haya revisado realmente. Una firma o un test no tienen significado ilimitado. Entregar con límites precisos permite continuar el trabajo y tomar decisiones; ocultarlos impide ambas cosas.

**Autocontrol final:** otra persona puede localizar versión y requisitos, distinguir candidato de release aceptada, repetir el cotejo documental, saber qué hacer ante un problema, reconstruir una decisión y identificar qué observación sigue pendiente. Tú puedes explicar y modificar una evidencia esencial. Si falta alguno, registra y resuelve la carencia pertinente antes de afirmar más.
