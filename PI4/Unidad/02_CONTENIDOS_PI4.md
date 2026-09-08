# Gobernar la ejecución: teoría autosuficiente

## 1. Del plan a una intervención que deja rastro

Un plan describe lo que se pretende hacer. La ejecución incorpora hechos: una entrada llegó tarde, una revisión rechazó la salida o una persona no dispuso del recurso. Seguimiento es comparar esos hechos con la previsión y decidir. Control es aplicar la decisión y verificar su efecto. Un tablero sin criterios de transición muestra etiquetas, pero no permite distinguir progreso de una declaración optimista.

En PI3 preparaste P01–P12. PI4 no los vuelve a escribir: congela una versión de entrada y añade documentación de ejecución E01–E10. P04 aporta actividades; E02 define cómo se autorizan y revisan. P08 aporta capacidad; E03 y E09 muestran su consumo y previsión. P09 aporta riesgos; E08 registra qué disparadores aparecieron. P11 conserva supuestos; E06/E07 distingue una propuesta de cambio de su aprobación. Mantener estas relaciones evita dos planes incompatibles.

**Baseline** es una versión acordada que sirve para comparar. No significa que nunca se cambie. Una nueva baseline debe indicar de qué decisión procede y desde cuándo se aplica. Congela el estado anterior mediante versión o SHA. Si el contrato no está disponible, registra la limitación; no inventes un baseline contractual a partir de lo que recuerdas.

Actividad, tarea contractual y evidencia son cosas distintas. Una tarea contractual identifica un entregable aceptable y sus AT en el catálogo auténtico. Una actividad organiza el trabajo para producirlo o revisarlo. Una evidencia permite examinar qué ocurrió. Dividir una actividad en tres no crea tres tareas contractuales ni nuevos AT. En TRAIN hay referencias sintéticas y horas hipotéticas; no hay valores de AulaTokens.

## 2. Un procedimiento utilizable

Un procedimiento responde a seis preguntas: qué entra, quién actúa, qué hace, qué sale, qué control permite avanzar y qué se hace si falla. «Hacer review» no es suficiente: no indica objeto, responsable ni condición. «La persona revisora abre el diff contra el criterio TRAIN-RESERVA, ejecuta la comprobación provista y registra coincidencia o discrepancia; si falta evidencia devuelve a ACTIVE y describe lo que falta» sí puede ejecutarse.

La documentación debe ser proporcional. Un registro de incidencia puede ocupar media página si permite reproducir el problema, valorar impacto, tomar decisión y verificar. Diez capturas sin secuencia no son mejores. Diseña un índice estable para que una persona ausente pueda recuperar la decisión sin preguntarla en un chat privado. No escribas en un documento público quién tiene un problema personal: basta disponibilidad restante y canal del acuerdo.

Una **Definition of Ready** local comprueba entrada suficiente, criterio, responsable, dependencia y capacidad. No es una ley de XP ni una puerta curricular nueva; es una ayuda del equipo. Una **Definition of Done técnico** exige salida identificable, revisión realizada, comprobaciones pertinentes y documentación actualizada. La aceptación contractual exige además criterio del anexo y autoridad competente. En consecuencia, DONE_TECH no equivale a ACEPTADA.

## 3. Tablero, estados y límites de trabajo en curso

Un flujo útil es READY → ACTIVE → REVIEW → DONE_TECH. BLOCKED conserva la razón y la condición de desbloqueo, no sirve para esconder tarjetas. Si una revisión encuentra un defecto vuelve a ACTIVE manteniendo el comentario. Una tarea sin entrada suficiente permanece en preparación; no llenes ACTIVE para aparentar actividad.

Define quién puede cambiar cada estado y la evidencia requerida. Por ejemplo, una persona autora puede pasar a REVIEW al aportar salida y prueba; la revisora confirma o devuelve. Mantén una referencia al contrato auténtico cuando exista y otra a la actividad local. El tablero facilita localizar el trabajo; el registro enlazado conserva la decisión. El sistema manual sigue las mismas reglas si Projects no está accesible.

El **WIP** cuenta elementos iniciados aún no terminados. Limitarlo obliga a ayudar a terminar en vez de abrir más frentes. Si dos personas tienen una revisión pendiente y ambas abren otra tarea, quizá el cuello de botella sea la revisión. Un límite didáctico de dos elementos ACTIVE para un equipo de tres es una hipótesis a contrastar, no una medida de aprendizaje. Si lo cambias, registra motivo y efecto esperado. La tarjeta bloqueada continúa ocupando atención; acuerda si se cuenta dentro del límite y no cambies la definición durante el cálculo.

El tablero real requiere permisos reales. Puedes ensayar con una tabla exportada. No generes una historia falsa de issues, fechas o reviews para rellenar huecos. Si se perdió trazabilidad, redacta una reconstrucción fechada hoy a partir de fuentes existentes e identifica qué no puede recuperarse. Esa reconstrucción no se convierte en un registro contemporáneo.

## 4. XP adaptado a semipresencial

XP propone ciclos breves de feedback y prácticas que se refuerzan. En esta unidad se usa un compromiso pequeño de iteración, revisión frecuente, trabajo compartido, diseño simple y retrospectiva. El objetivo es detectar pronto una decisión equivocada, no llenar ceremonias. La duración de un ciclo debe encajar con la disponibilidad del equipo; los talleres son puntos de contraste, no sprints idénticos impuestos.

Al iniciar una iteración, contrasta prioridades, entradas y capacidad; selecciona lo que cabe con revisión y margen. Durante la ejecución cada persona deja un estado asíncrono breve: salida conseguida, próximo paso, bloqueo con evidencia. Una reunión no genera capacidad adicional. Al terminar, demuestra el resultado, revisa lo que no quedó verificado y decide una mejora concreta.

En un ensayo por parejas, una persona ejecuta el procedimiento y otra observa inconsistencias; intercambian roles. Ambas deben poder explicar la decisión. Propiedad compartida no significa autoría indiferenciada: E09 indica responsabilidad, colaboración y revisión con referencias. Si alguien no puede explicar un cambio, se necesita acompañamiento o contraste; un gran número de commits no resuelve esa incertidumbre.

TDD, analyzer o integración continua pueden proporcionar outputs técnicos desde los módulos que los enseñan. PI4 examina por qué esa salida sirve para permitir o bloquear un avance, sin reimpartir sus comandos. Antes de que PM6 esté disponible se puede definir qué evidencia de calidad hará falta, pero no exigir la competencia como aprendida. Los agentes se pueden usar bajo la política vigente para apoyar documentación o análisis; el flujo técnico completo SDD de Flutter se formaliza en PM7. Un documento generado debe ser comprendido y revisado.

## 5. Seguimiento con datos interpretables

Define un procedimiento periódico: responsable, momento, variables, fuente, umbral de intervención y acción. Por ejemplo, en cada revisión de iteración se cotejan capacidad restante, elementos en REVIEW, bloqueos sin responsable y desviación de previsión. «Seguimos el proyecto semanalmente» no especifica qué obliga a actuar. RA4.a exige definir cómo se evalúan las actividades, no diseñar ya la aceptación final de PI5.

Una variable de seguimiento solo sirve si se puede interpretar. **Trabajo terminado** necesita una definición estable de terminado. **Tiempo de ciclo** debe fijar entrada y salida: por ejemplo, desde ACTIVE hasta DONE_TECH, incluyendo espera de revisión. **Antigüedad del bloqueo** mide tiempo desde su registro hasta el corte; no concluye automáticamente quién tiene la culpa. No compares ciclos calculados con definiciones diferentes.

En TRAIN se iniciaron tres elementos en D2, D3 y D4; se terminaron dos en D4 y D6, y el tercero seguía bloqueado en D6. No calcules la media como si el tercero hubiese durado cero. Informa los dos tiempos completos y el elemento censurado con su edad. Tres observaciones no permiten prometer una velocidad estable. Lo relevante es la decisión: revisar entrada o capacidad antes de asumir un nuevo compromiso.

Una tendencia no es una causa. Más tiempo en REVIEW puede proceder de una salida incompleta, una revisora sin disponibilidad o una dependencia externa. Busca evidencia y evita convertir un indicador en castigo. PI5 definirá indicadores de calidad/aceptación del producto; aquí las variables ayudan a gobernar las actividades y registrar decisiones.

## 6. Registrar y evaluar una incidencia

Una **incidencia** es un hecho que afecta a la ejecución. Un **riesgo** es un evento posible; cuando ocurre se registra como incidencia y se conserva el enlace al riesgo. Un **cambio** altera recursos, tareas o condiciones acordadas. El mismo hecho puede abrir una incidencia y motivar un cambio, pero son registros con funciones diferentes.

Escribe síntoma observable, contexto/versión, pasos o fuente, resultado esperado, resultado obtenido, alcance del impacto, prioridad justificada, responsable y próximo control. La causa inicialmente es una hipótesis. «La API está mal» culpa sin evidencia. «Con la muestra TRAIN, la respuesta del servicio declara disponible un kit ya reservado; no se ha confirmado la causa; bloquea el ensayo de reserva» permite decidir.

El triage valora impacto y urgencia por separado. Una errata visible en una página secundaria puede ser frecuente y poco grave; una pérdida de datos poco frecuente puede impedir seguir. No se requiere una matriz numérica complicada: explica a quién afecta, qué actividad impide y qué riesgo de daño existe. Una incidencia que implica datos reales sensibles se retira del material público y se escala por canal autorizado.

Evita duplicados: enlaza registros relacionados sin borrar su origen. A cada incidencia asigna responsable de investigación y de decisión, que pueden ser personas distintas. El estado ABIERTO no se cambia por tiempo transcurrido. Una fecha objetivo es una previsión; el próximo control se define incluso si la solución técnica depende de otro módulo.

## 7. Resolver y verificar

Resolver incluye elegir una acción, ejecutarla o coordinarla, comprobar el resultado y actualizar los documentos afectados. Puede ser corregir, aplicar una mitigación temporal o posponer con riesgo explícito. Mitigar no equivale a eliminar la causa. Si se usa una respuesta simulada mientras no llega el servicio real, puede desbloquear un ensayo de interfaz, pero la integración continúa pendiente.

Antes de actuar define el resultado esperado de la comprobación. Después guarda evidencia y versión. La persona revisora confirma qué se observó y qué limitación queda. Solo entonces se propone cierre. Si reaparece el síntoma, reabre o crea una incidencia vinculada explicando la relación. Mantén la primera decisión; no reescribas el historial para que parezca correcta desde el principio.

Un procedimiento de recuperación también debe ser seguro. No borres datos o despliegues externos como parte del ejercicio sin un entorno autorizado y plan de vuelta. PI4 registra quién puede realizarlo y qué evidencia necesita; el módulo técnico aporta el mecanismo. El caso sintético permite ensayar el razonamiento sin tocar producción.

## 8. Cambios y rebaseline prospectivo

La solicitud de cambio registra motivo y alternativa. Su análisis abarca alcance contractual, actividades, horas/capacidad, coste, hitos, dependencias, riesgos, personas y puertas. «Nos llevará más» es insuficiente. Indica qué se mantiene, qué se retrasa, qué sale o entra y qué evidencia seguirá siendo exigible.

Compara al menos dos alternativas viables. Dividir una actividad puede permitir entregar una parte coherente si el contrato la admite, pero no autoriza aceptar una tarea incompleta. Posponer una ampliación puede proteger un núcleo obligatorio; retirar parte del núcleo requiere una decisión sustantiva que el equipo no toma unilateralmente. Los AT congelados del catálogo no se renegocian porque una tarea resultó difícil.

El flujo es solicitud → impacto → decisión docente cuando afecta contrato → actualización del anexo → nueva baseline. La aprobación lleva fecha y entrada en vigor. El cambio se aplica al trabajo futuro; lo ya aceptado y su atribución se conservan salvo evidencia inválida. Una propuesta PENDIENTE no permite anunciar un contrato cambiado. Un cambio de recurso interno sin cambio contractual puede decidirlo el rol previsto, conservando capacidad y trazabilidad; si compromete alcance o puerta se escala.

Cuando cambia el tamaño del equipo, congela aceptación/atribución existente y recalcula la capacidad pendiente. No repartas de nuevo la historia ni escales valores de las tareas. La fórmula AT se aplicará desde la base auténtica cuando proceda; en este material el campo permanece TBD. La ausencia del catálogo es limitación de entrada, no falta académica del estudiante.

## 9. Valoración económica de ejecución

RA3.g requiere valorar económicamente las condiciones de ejecución. Las horas de trabajo, coste monetario y AulaTokens son unidades distintas. Un precio supuesto del caso no es un precio de mercado. Una estimación sin fuente se marca como supuesto, con responsable y evento para contrastarlo. No hace falta comprar servicios para aprender el cálculo.

Coste de trabajo = suma de horas-persona por tarifa correspondiente. Coste directo = trabajo + recursos imputables. Una reserva explícita cubre incertidumbre identificada y no es trabajo ya consumido. No multipliques las horas-persona otra vez por el tamaño del equipo. No cuentes una suscripción mensual completa en cada actividad si se paga una vez.

Ejemplo TRAIN: A 12 h a 18 €/h, B 8 h a 15 €/h, C 6 h a 12 €/h y recurso único de 30 €. Trabajo 216 + 120 + 72 = 408 €; directo 438 €; reserva didáctica 10 % del directo = 43,80 €; baseline aprobada ficticia = 481,80 €. El 10 % no es norma del curso ni recomendación financiera: es dato del caso.

En el corte: consumo A 14 h, B 7 h, C 5 h, recurso pagado 30 €. Coste incurrido = 252 + 105 + 60 + 30 = 447 €. Trabajo restante estimado: A 4 h, B 3 h, C 2 h; ETC = 72 + 45 + 24 = 141 €. Previsión base al terminar = 447 + 141 = 588 €. Reserva restante del caso = 10 % de ETC = 14,10 €; previsión total = 602,10 €. Diferencia frente a baseline total 481,80 € = +120,30 €. No vuelvas a sumar el recurso ya pagado ni toda la reserva inicial.

El desvío no determina automáticamente una nota ni obliga a cambiar AT. Pregunta qué condición explica el aumento, qué alternativa reduce trabajo restante, qué coste de cambio introduce y quién decide. Mantén baseline, incurrido, restante y reserva en columnas separadas. Si no sabes el restante, el total es TBD, no cero. Si hay financiación real, documenta el límite y fuente autorizada; no inventes ingresos ni participantes.

## 10. Riesgos, contingencias y continuidad

Un riesgo accionable incluye causa, evento, consecuencia, disparador, responsable, prevención y contingencia. «Puede fallar internet» no decide nada. «Si el servicio compartido no está disponible en la revisión acordada, el equipo ensaya con contrato de ejemplo identificado y mantiene integración real pendiente; responsable de coordinación solicita nueva ventana» conecta el riesgo con una acción verificable.

La contingencia consume capacidad: debe quedar visible en E09 y, si altera compromisos, motivar E06. Una mitigación temporal lleva fecha/condición de revisión para no transformarse por olvido en la solución definitiva. Registra deuda o limitación en E10 para que PI5 no acepte sin conocerla.

## 11. Integración progresiva y puertas

Integrar significa comprobar una frontera compartida con entradas y resultados compatibles. PI4 prepara y sigue ese trabajo; no evalúa como suyos los CE de Flutter, API o despliegue. La evidencia puede ser un resultado de test o demo aportado por un módulo, con versión y alcance. Un fake prueba una suposición controlada, no el servicio real. Una APK construida no demuestra uso en dispositivo.

La disponibilidad por calendario es una previsión. G2–G5 solo se activan expresamente con criterio observable, oportunidad de aprendizaje, evidencia y recuperación. PM6 termina su segundo taller después de PI4 el 12/01; no se exige su resultado a las 18:35 de ese día. Lo mismo ocurre con PM7 el 26/01. PM8 el 02/02 analiza motor; no entrega RA5. PM9 comienza tras PI4 el 09/02. Además, el juego no forma parte obligatoria de AulaFlow.

G0/G1/G6/G7 figuran como puertas globales, pero activación no es satisfacción. El registro identifica qué está pendiente y quién puede valorar. Ninguna puerta se concede por producir esta unidad, por una fecha o por merge. PI5 recibirá las evidencias para aceptación; PI6 conservará el cierre y defensa global.

## 12. Retrospectiva y evidencia individual

Una retrospectiva útil parte de hechos: dos devoluciones por falta de criterio, una dependencia no prevista o una decisión que evitó retrabajo. Explica la hipótesis causal y propone un experimento pequeño con señal de resultado. «Comunicarnos mejor» no se puede comprobar; «antes de REVIEW incluir criterio y evidencia; observar si disminuyen devoluciones por ausencia de entrada durante el siguiente ciclo» sí.

No deduzcas contribución de actividad digital. Una revisión que descubre una contradicción puede ser más relevante que muchos commits. Cada persona señala responsabilidad, evidencia concreta y decisión que puede explicar o modificar. La triangulación combina dossier, observación y cambio individual; no usa detectores de IA. Si falta evidencia, se abre una oportunidad nueva y suficiente, no se inventa historial.

Al cerrar PI4, E10 informa a PI5 de fuentes, versiones, pendientes, riesgos, capacidades disponibles y decisiones aún no tomadas. No declara aceptación final, release real ni AT. Un traspaso profesional reduce incertidumbre aunque deba decir PENDIENTE_CATALOGO.
