# PI5 · De la ejecución a una decisión de calidad

## 1. Qué pregunta responde la validación

Un equipo puede haber terminado su trabajo y seguir sin poder demostrar que cumple lo pedido. La validación relaciona una condición de uso o del pliego con evidencia suficiente de una versión concreta. El seguimiento de PI4 explica qué se hizo, qué cambió y por qué. PI5 usa esas salidas para decidir qué puede proponerse como conforme, qué necesita retrabajo y qué todavía no puede juzgarse. PI6 recibirá ese estado para la entrega y defensa final.

Verificar una salida técnica pregunta si cumple una especificación bajo condiciones definidas. Validar su adecuación pregunta si sirve al propósito previsto en el contexto pertinente. Una prueba automática puede ayudar a ambas preguntas, pero su mera existencia no decide la aceptación. Un formulario correcto puede ser incomprensible para quien lo usa; una opinión positiva no demuestra que la cancelación conserve historial. Combinar fuentes requiere delimitar su alcance, no promediar impresiones.

Una decisión defendible empieza con cinco elementos: condición, versión, evidencia, límite y autoridad. Si falta uno, se registra la carencia. «Funciona» no identifica ninguno. «En TRAIN-C1, el registro sintético TRAIN-EV-12 conserva la reserva tras cancelarla, pero no observa permisos de otro perfil» sí describe una afirmación delimitada. El registro es didáctico y no demuestra ejecución auténtica; aprender a reconocer esa frontera es parte del trabajo.

## 2. Congelar el objeto que se juzga

Una release candidate es una versión propuesta para validación. No significa publicada ni aceptada. Para reproducir su evaluación necesitas localizar código/documentación/artefacto, configuración no secreta, dependencia, instrucciones y datos autorizados. Una etiqueta legible ayuda; una referencia inmutable o huella evita que dos personas juzguen contenido diferente bajo el mismo nombre. Si cambia una dependencia, configuración o requisito, revisar qué evidencia continúa siendo válida.

El corte de evaluación debe señalar alcance incluido y excluido. No esconder como exclusión un requisito obligatorio fallido. Solo una decisión autorizada puede cambiar el compromiso, siguiendo el procedimiento de PI4. Si el catálogo auténtico no está disponible, no inventes una baseline contractual: puedes preparar el procedimiento y ensayar TRAIN, pero la aceptación nominal REAL permanece PENDIENTE_CATALOGO.

Conserva una tabla C1→C2: cambio observado, evidencia invalidada, comprobaciones conservables y retest. Un test de C1 puede conservar utilidad para una función sin cambios si justificas que sus dependencias siguen equivalentes; no se traslada automáticamente. La prueba final del candidato debe cubrir los riesgos introducidos. Borrar C1 dificulta explicar tanto el problema como su corrección.

## 3. Indicadores operativos

Un indicador es una medida ligada a una pregunta y una acción. Su ficha contiene nombre, propósito, unidad, universo, numerador, denominador cuando proceda, fuente, corte, frecuencia, umbral, responsable, limitaciones y respuesta. «Calidad 90 %» no es una ficha. «Condiciones del pliego con evidencia vigente suficiente / condiciones aplicables del corte» permite reconstruir un porcentaje, siempre que listes las condiciones y definas suficiente antes de observar el resultado.

No confundas ejecución con éxito. Si hay ocho comprobaciones previstas, seis ejecutadas y cinco conformes, cobertura de ejecución = 6/8 = 75 %, éxito entre ejecutadas = 5/6 ≈83,3 % y éxito sobre previstas = 5/8 =62,5 %. Las tres cifras responden a preguntas distintas. Ninguna autoriza ocultar las dos no ejecutadas. Con denominador cero el resultado es NO_MEDIDO; no es 100 %, 0 % ni una división arbitrariamente reparada.

Un conteo también es indicador: incidencias críticas abiertas por versión. No necesita porcentaje, pero sí definición de crítica, fuente y regla de deduplicación. Umbral cero críticas es distinto de 95 % de comprobaciones conformes. Los umbrales TRAIN son datos del ejercicio; no se imponen como pesos ni criterios contractuales de AulaFlow. Para REAL, el responsable autorizado acuerda umbrales vinculados al requisito antes de aceptar.

## 4. Comparar sin falsear

Una mejora solo es comparable si sabes qué cambió en la medida. Pasar de cinco éxitos entre seis pruebas a siete entre ocho modifica también el denominador. Explica la nueva cobertura y el efecto de las pruebas añadidas. Si cambias un umbral después de ver el fallo, el nuevo número no prueba que el producto mejoró. Mantén el valor original, la decisión y su vigencia.

La criticidad impide que un promedio oculte un incumplimiento esencial. Una importación puede rechazar 99 filas inválidas y aceptar una fila con una condición prohibida: si el criterio exige rechazo completo, ese caso sigue fallando. Un índice global sirve para seguimiento; la matriz de requisitos conserva la decisión por condición. No sumar porcentajes inconmensurables, como satisfacción, cobertura de tests y coste, para obtener una nota técnica inventada.

La medida puede inducir conductas no deseadas: contar incidencias cerradas incentiva cierres sin retest; contar encuestas incentiva respuestas superficiales. Añade control de suficiencia y revisa muestras. Describe incertidumbre y sesgos con lenguaje proporcional. Tres sesiones de conveniencia ayudan a encontrar problemas de comprensión, pero no estiman con precisión la aceptación de toda una población.

## 5. Matriz de cumplimiento

Cada fila de la matriz une requisito auténtico o TRAIN, condición observable, versión, evidencia exacta, resultado, limitación, incidencia/cambio y siguiente acción. Se puede usar texto, hoja o tablero; la estructura lógica permanece. Los resultados permitidos incluyen CONFORME_EN_CORTE, NO_CONFORME, NO_EJECUTADO y EVIDENCIA_INSUFICIENTE. Son juicios del cotejo, no estados contractuales de aceptación.

Empieza por una condición: «Al cancelar una reserva existente, desaparece de activas y sigue localizable en historial». Es distinta de «hay botón cancelar». Una evidencia suficiente necesita entrada, contexto, acción, esperado, obtenido y corte. Una captura aislada del botón observa interfaz; un registro de estados antes/después puede observar la transición; una prueba con almacenamiento simulado no observa persistencia del servicio real. Señala exactamente la parte acreditada.

Evita referencias vagas como «ver tests» o «PR aprobada». Localiza caso/archivo/run/fragmento y relación con la condición. En un expediente TRAIN, las referencias son tarjetas que puedes leer aquí; no crees URLs que simulen runs. En REAL, los enlaces y permisos se verifican con el rol previsto sin publicar contenido privado. Una referencia inaccesible al revisor es una carencia de evidencia, aunque la persona afirme haberla visto.

## 6. Participación de usuarios como procedimiento

RA4.f pide definir un procedimiento y elaborar documentos específicos. Su calidad no depende de conseguir muchas personas. Define objetivo, perfiles pertinentes, selección viable, condiciones de participación, tareas, guion neutral, registro, análisis, devolución y decisión sobre hallazgos. Si la participación real no es posible o no está autorizada, ensaya el procedimiento con datos sintéticos explícitos; no inventes personas ni consentimiento.

Una tarea neutral plantea un objetivo: «Necesitas liberar una reserva que ya no usarás y comprobar qué ocurrió». No indica «pulsa el botón azul de cancelar», porque eso oculta si la persona encuentra el camino. El moderador explica que se estudia el sistema, no la capacidad personal; permite detenerse y registra ayudas. Una ayuda puede ser apropiada por accesibilidad y debe describirse para interpretar el resultado, sin penalizar al participante.

Documentos mínimos: información/invitación didáctica, guion de sesión, ficha de observación y formulario de devolución. Recoge códigos de sesión, versión y hechos; no nombres, contacto o motivos privados si no son necesarios. No se graba por defecto. El centro determina condiciones de tratamiento/custodia y conservación antes de una recogida real. La ausencia de condiciones se resuelve dejando la sesión real pendiente, no con una casilla firmada por el propio equipo.

## 7. Del feedback a una decisión

Separa tres columnas: observación («dos personas vuelven atrás tras leer “Anular”»), interpretación («quizá no entienden el efecto») y propuesta («aclarar mensaje y repetir tarea»). La observación puede apoyar una hipótesis; no confirma por sí sola una causa. Una opinión como «me gusta» no acredita que alguien haya completado la tarea sin ayuda. Un fallo técnico no se descarta porque otra persona opine favorablemente.

Clasifica hallazgos por impacto sobre tarea/requisito y evidencia disponible. Si el problema contradice un requisito, se registra no conformidad y se solicita retrabajo. Si propone alcance nuevo, va al procedimiento de cambio de PI4 y no se introduce silenciosamente. Si refleja preferencia, puede ser mejora opcional con justificación. Toda devolución comunica qué se entendió, qué se hará o no y por qué, sin exponer a quien participó.

La triangulación compara fuentes distintas sobre la misma pregunta. Un test de cancelación conforme y dos sesiones con confusión no se anulan: la transición puede ser correcta y la comunicación insuficiente. Una prueba no ejecutada sigue pendiente aunque el ensayo de mesa sea convincente. La acción correctora debe incluir un retest que vuelva a observar el riesgo; renombrar un botón sin repetir la tarea no confirma la mejora.

## 8. Integrar evidencia técnica y preparar demo

PI5 consume resultados de módulos propietarios. Un informe de tests debe indicar alcance, versión, entorno y resultados. Un build demuestra que una combinación de fuentes/herramientas produce un artefacto; no prueba instalación, interacción, accesibilidad ni funcionamiento en hardware. Un despliegue verificado requiere entorno, configuración segura, pasos, comprobación de servicio y resultado observado. Si no existe esa capacidad, preparar un procedimiento y marcar PENDIENTE_DESPLIEGUE; no simular que se ha observado.

La demo reproducible se ensaya con datos sintéticos o autorizados, estado inicial conocido y acciones acotadas. Incluye un camino válido, un rechazo significativo y recuperación/restablecimiento. Define qué vería el observador para confirmar cada condición y qué evidencia se conservará. El plan alternativo puede ser un recorrido documental TRAIN cuando falte infraestructura, siempre identificado como tal. No sustituye una instalación real exigida por una puerta activada.

Un plan de retorno o rollback limita el impacto de una versión candidata: cómo identificar la anterior, qué condiciones obligan a detenerse, quién decide y qué datos/configuración deben preservarse. No ejecutar operaciones destructivas ni restauraciones reales como ejercicio de PI5 sin entorno/autoridad adecuados. Aquí se evalúa la coordinación y evidencia del procedimiento, no la sintaxis técnica de contenedores o bases de datos.

## 9. Puertas y aceptación

Las puertas son condiciones del proyecto, no insignias concedidas por tener un documento. G0/G1/G6/G7 están activas desde el inicio según evaluación vigente, pero su satisfacción requiere evidencia. G2–G5 solo se vuelven no compensables con activación expresa, criterios observables, justificación curricular, capacidad/oportunidad y recuperación. La ficha de revisión conserva esas cinco condiciones y el resultado. Un campo sin fuente queda TBD.

La propuesta de aceptación cita contrato/pliego vigente, corte, evidencia por condición, no conformidades, límites, riesgos, autoridad y siguiente decisión. Se puede proponer aceptar cuando existe base suficiente y autorizada; proponer retrabajo cuando una corrección concreta permitiría volver a juzgar; o rechazar justificadamente una entrega que no satisface el compromiso. La falta de catálogo/evidencia no obliga a inventar un rechazo contractual: impide tomar una decisión final y se marca pendiente.

Solo el estado contractual ACEPTADA con catálogo/contrato y evidencia auténticos valida AT. Un oráculo TRAIN o una validación automática del formato no concede ese estado real. «Aceptación condicionada» no se usa para otorgar AT antes de cumplir las condiciones. Las decisiones docentes globales de evaluación permanecen fuera del expediente didáctico.

## 10. Desviaciones, retrabajo y retest

Una no conformidad debe poder abrirse, priorizarse, asignarse y verificarse. PI4 conserva el procedimiento de incidencia/cambio. PI5 aporta la relación con la condición de aceptación y el plan de retest: caso que falló, regresiones pertinentes, corte de corrección y responsable de revisión. Si una limitación exige cambiar el alcance, usar solicitud→impacto→propuesta→aprobación→rebaseline; no editar el requisito para que el resultado parezca conforme.

Tras el retest, conservar C1 y añadir C2. Una incidencia puede quedar corregida técnicamente y seguir pendiente de observación del usuario o del entorno real. Usa estados que lo expliquen. No es un fracaso del dossier: es información necesaria para que PI6 no presente como final lo que todavía está pendiente. El riesgo residual incluye condición, consecuencia, responsable y siguiente contraste, sin prometer fechas desconocidas.

## 11. Handoff, autenticidad y evaluación

V09 entrega a PI6 inventario de versiones, matriz actual, decisiones, incidentes/cambios, límites de release/demo, necesidades de mantenimiento y contribución individual. No vuelve a hacer la retrospectiva final ni asigna CE de PI6. Permite que otra persona reconstruya por qué un resultado sigue pendiente y cómo comprobarlo.

Para acreditar autoría no basta con figurar en el equipo. Debes localizar una ficha, reconstruir un cálculo, justificar una exclusión, corregir una traza ante evidencia nueva y defender una decisión del sistema esencial. La asistencia declarada puede ayudar a preparar; no sustituye la revisión propia ni el I3 sin agente. El docente triangula proceso, producto y verificación individual.

PI II mantiene RA1 15 %, RA2 25 %, RA3 30 % y RA4 30 %, todos ≥5, caso profesional presencial obligatorio ≥5, evidencia individual suficiente y puertas activadas satisfechas o recuperadas. La contribución agregada objetivo del caso global es 20 %, distribuida por los RA/CE que observe. No añadimos aquí una nota paralela de demo ni de indicadores. La nota final es min(nota curricular, techo AT) cuando hay base auténtica; sin catálogo no se inventa ese techo.

## Glosario operativo y autocontrol

**Corte:** conjunto identificable de contenido/configuración juzgado. **Indicador:** medida ligada a decisión. **Universo:** conjunto al que se refiere la medida. **Retest:** nueva comprobación del riesgo después de corregir. **Candidate:** propuesta de versión. **No conformidad:** discrepancia con una condición aplicable. **Trazabilidad:** relación localizable entre condición, evidencia y decisión. **Pendiente:** juicio que aún no puede completarse, con causa y condición de resolución.

Antes de cerrar, responde: ¿qué afirmas?, ¿de qué versión?, ¿a partir de qué fuente?, ¿qué no observa?, ¿quién decide?, ¿qué harás si cambia? Si una respuesta falta, el siguiente paso es obtenerla o registrar la limitación, no redactar una conclusión más contundente.
