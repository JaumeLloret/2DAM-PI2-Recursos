# AulaFlow · de una versión revisada a una entrega que alguien puede continuar

## 1. Recibir PI5 sin cambiar sus conclusiones

Una versión identifica un estado del producto. Una entrega pone ese estado a disposición de su destinatario. Una aceptación contractual requiere autoridad y evidencia suficientes. La evaluación académica es un juicio sobre RA/CE. Son decisiones relacionadas, con condiciones diferentes: entregar una carpeta no demuestra que el contrato esté aceptado.

Continuamos la historia de consulta de tarjetas de AulaFlow, pero recibimos **PI5-TRAIN-R2**, el corte del ejemplo vigente de PI5. Sus tarjetas son datos sintéticos de aprendizaje; no son resultados de vuestro equipo. TRAIN-C2 queda como antecedente de PI4, no como una nueva validación de PI5.

| Comprobación recibida de PI5 | Tarjeta sintética de R2 | Qué conserva PI6 |
|---|---|---|
| P1 · consulta autorizada | R2-E1 describe dos tarjetas correctamente consultadas. | Conforme en ese corte didáctico y con ese límite. |
| P2 · tablero vacío | R2-E2 describe el vacío comprensible. | Conforme en ese corte; no demuestra todos los estados. |
| P3 · perfil sin permiso, crítico | No hay ejecución de P3. | Pendiente; no convertirlo en rechazo comprobado ni en éxito. |
| P4 · sesión caducada, crítico | R2-E4 describe que las tarjetas restringidas ya no permanecen visibles. | Corrección y repetición descritas por PI5, no ejecución real del alumnado. |
| U1 · comprensión del mensaje | Guion preparado, sin observación posterior al cambio de texto. | Evaluación de uso pendiente; no convertirla en requisito contractual nuevo. |
| Aceptación contractual | PI5 propone mantener pendiente la aceptación global. | Sigue sin aceptación final confirmada. |

En PI6 no volvemos a diseñar estos indicadores ni a repetir PI5 completa. Añadimos lo necesario para que otra persona reciba esa versión, encuentre sus evidencias y continúe P3 y U1. En vuestro proyecto se conserva el estado real que exista, sea favorable, de retrabajo o pendiente.

**Actividad 1 · cinco minutos.** Corrige «Como PI5 está entregada, el contrato está aceptado». Debes explicar qué fuente y qué decisión faltan. Resultado esperado: una frase que separe entrega, propuesta y aceptación, sin inventar ninguna.

| Para resolverla | Indicación |
|---|---|
| Recurso | Frase sobre aceptación y estado_PI5.json del ejemplo. |
| Qué hacer | Escribe dos frases: qué demuestra la entrega y qué decisión falta. |
| Cómo comprobar | Tu respuesta conserva versión, evidencia y autoridad; no da por aceptado el conjunto. |
| Qué conservar | Una anotación en tus notas; después aplica la distinción a vuestro índice. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


En vuestro proyecto utilizad su estado auténtico. Si PI5 dejó una aceptación real delimitada, enlazad quién decidió, sobre qué versión y con qué condiciones. Si dejó retrabajo o una decisión pendiente, conservadlo.

## 2. Identificar exactamente qué se entrega

Un **artefacto** es el archivo o conjunto utilizable que entregáis: por ejemplo, el ejecutable ya generado en el módulo técnico, junto con las instrucciones. El **código fuente** permite conocer o reconstruir su origen; no siempre basta para usarlo. Una **dependencia** es una herramienta, servicio, biblioteca o dato necesario para ese uso. La ficha de entrega une esas referencias, sin imponer otra plataforma.


«La última versión de la rama» cambia con el trabajo. Identifica la revisión del código mediante su referencia exacta; identifica también el artefacto que recibe el destinatario y la documentación correspondiente. Si aún no existe artefacto ejecutable, registra esa ausencia: un archivo de documentación no lo sustituye.

Un índice útil permite encontrar versión, componentes, finalidad, ubicación, destinatario y límites. La etiqueta puede ayudar a leerlo; el commit exacto o una copia identificada evita confundir revisiones. Una huella de archivo permite comparar bytes: no demuestra calidad, autoría, funcionamiento o aceptación.

**Ejemplo rellenado:**

| Campo | Entrega didáctica |
|---|---|
| Identificador | PI6-TRAIN-ENTREGA-R1 |
| Base | Estado y tarjetas de PI5-TRAIN-R2 recibidos de PI5. |
| Contenido | Índice, instrucciones del ensayo documental, tarjetas sintéticas, registro de revisión y pendientes. |
| Destinatario | Persona que aprende a revisar una entrega. |
| Qué puede reproducir | Localizar archivos, cotejar condiciones y repetir el recorrido documental descrito. |
| Qué no incluye | Aplicación ejecutable, servicio desplegado, usuarios reales o comprobación del perfil sin permiso. |
| Decisión | Paquete de entrenamiento; sin aceptación contractual. |

Para el producto real, fija código, artefacto, manual, entorno y datos iniciales de la misma revisión. Una copia limpia de trabajo o una cuenta de prueba ayuda a detectar dependencias que solo existen en el ordenador del autor; no exige borrar instalaciones ni datos. Aplica las instrucciones del módulo técnico que ya usasteis. Si falta una herramienta, localiza la ayuda anterior y registra el bloqueo; no inventes un comando.

Si cambias instrucciones o código después de una revisión, crea una nueva revisión identificable y decide qué comprobaciones repetir. Conserva la anterior para explicar el cambio.

**Actividad 2 · ocho minutos.** En un ensayo ficticio de recepción de PI6-TRAIN-ENTREGA-R1, alguien sigue el paso 3 con tarjetas_otro_corte.json. Abre ese archivo y compáralo con tarjetas.json y con el resultado esperado de INSTRUCCIONES.md. Escribe archivo recibido, diferencia observada y paso que repetirías con la referencia correcta. No basta renombrar el archivo. Después aplica la misma revisión a un componente auténtico de vuestro índice.

| Para resolverla | Indicación |
|---|---|
| Recurso | ENTREGA.md, paso 3 de INSTRUCCIONES.md y los dos archivos de tarjetas de ejemplo. |
| Qué hacer | Relaciona referencia recibida, contenido y esperado; corrige la ubicación y repite el paso disponible. |
| Cómo comprobar | Detectas que DEMO-ANTERIOR pertenece a otra revisión; renombrarlo no cambia su contenido. |
| Qué conservar | Una fila de coherencia versión–archivo–evidencia, reutilizable en el índice. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


## 3. Escribir instrucciones que se puedan seguir

Un procedimiento explica quién lo usa, qué necesita, qué debe hacer, qué observar y cómo recuperar el estado o pedir ayuda. «Arranca el servidor» es insuficiente si el receptor no sabe qué componente, configuración o documentación corresponde.

En el proyecto real, enlaza y ajusta la documentación técnica ya existente: versiones necesarias, ubicación, preparación, configuración sin secretos, datos autorizados, comandos o acciones exactos, acceso, resultado y restablecimiento. PI6 comprueba su utilidad para entregar; no vuelve a enseñar el framework.

Para practicar sin inventar una aplicación, la descarga contiene **un paquete documental real con datos ficticios**, en la carpeta ejemplo. Este es su recorrido reproducible:

1. Abre ENTREGA.md e identifica PI6-TRAIN-ENTREGA-R1.
2. Abre estado_PI5.json. Localiza la condición P3 del perfil sin permiso y comprueba que conserva estado pendiente.
3. Abre tarjetas.json. Debe contener dos tarjetas con los identificadores DEMO-01 y DEMO-02. La descarga también contiene tarjetas_otro_corte.json con un dato distinto para practicar la detección de mezcla de versiones. Abrir el JSON no prueba que una API las sirva.
4. Abre INCIDENCIAS.md y localiza el siguiente ensayo propuesto para P3.
5. Vuelve a ENTREGA.md y localiza REVISION.md: distingue dificultad, corrección y repetición ficticias. Explica qué archivo respalda cada afirmación y qué sigue sin ejecutarse.

**Este recorrido comprueba documentos y datos de entrenamiento. No comprueba instalación, autenticación o integración de AulaFlow.** En vuestro trabajo la persona revisora seguirá el procedimiento real disponible. Si el entorno falta, quedará registrado y el docente acordará la oportunidad de contraste.

Puedes abrir los HTML equivalentes desde LEEME.html. Cuando transfieras el procedimiento al proyecto, anota qué componente y versión usas, qué preparación ya documentada necesitas y qué salida concreta compararás. Cambia «funciona» por una observación que otra persona pueda repetir.

## 4. Pedir una revisión y repetir el paso corregido

La persona revisora debe poder intentar el procedimiento sin que su autor vaya resolviendo oralmente todos los pasos. Puede ser alguien del equipo que no lo escribió. En un proyecto individual, se acuerda una persona revisora.

El caso de ejemplo incluye una revisión ficticia ya rellenada. Sirve para entender el registro; no es una sesión que haya ocurrido con alumnado real.

| Momento | Registro del ejemplo sintético |
|---|---|
| Paso original | «Carga las tarjetas de ejemplo». |
| Esperado | Encontrar los dos datos de entrenamiento. |
| Dificultad | No se indica archivo, ubicación ni resultado que comparar. |
| Corrección en r1 | «Abre ejemplo/tarjetas.json y comprueba DEMO-01 y DEMO-02». |
| Repetición descrita por el caso | La persona revisora localiza los dos identificadores. |
| Límite | Revisión documental didáctica; no ejecución de aplicación. |

En la revisión real registra fecha, versión, código de la persona revisora, pasos intentados, esperado, obtenido, ayuda recibida, corrección y repetición. Si no pudo repetirlo, la mejora continúa sin contrastar. No borres el fallo inicial: explica por qué cambió la instrucción.

**Actividad 3 · diez minutos.** Otra persona no sabe restablecer el estado. Redacta el paso que falta usando el entorno disponible y define cómo comprobarlo. En el paquete documental, basta volver a una copia intacta de los datos; en una aplicación con persistencia, habrá que usar su procedimiento autorizado, sin borrar datos reales.

| Para resolverla | Indicación |
|---|---|
| Recurso | INSTRUCCIONES.md y FICHA_REPRODUCIBILIDAD.md de la descarga. |
| Qué hacer | Redacta un paso de restablecimiento seguro y compáralo con el procedimiento disponible. |
| Cómo comprobar | Otra persona sabe qué estado recuperar, qué observar y cuándo pedir ayuda. Si no lo ejecuta, queda pendiente. |
| Qué conservar | El paso corregido y el estado de su repetición, en las instrucciones existentes. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


## 5. Mostrar resultados, errores y límites

Prepara un recorrido corto que tenga objetivo, versión, entrada, acción, resultado esperado y evidencia. Selecciona una condición representativa; añade un rechazo o fallo relevante y explica el restablecimiento cuando proceda.

| Parte | Qué dirías en el ejemplo |
|---|---|
| Identidad | «Este es PI6-TRAIN-ENTREGA-R1, un paquete documental de entrenamiento». |
| Resultado | «Puedo localizar las dos tarjetas y su correspondencia con las condiciones». |
| Límite | «Esto no demuestra que P3 se haya ejecutado». |
| Fallo | «Si el servicio no responde, no puedo afirmar disponibilidad en ese momento». |
| Continuidad | «La comprobación del perfil sin permiso sigue abierta y tiene un siguiente ensayo definido». |

En el producto real, la demostración usa los componentes disponibles y su evidencia auténtica. Un vídeo conserva una observación de una versión y momento concretos; no demuestra disponibilidad actual. Un doble o simulador permite ensayar una parte; identifica cuál. Un build no demuestra por sí solo instalación ni uso.

**Actividad 4 · diez minutos.** El servicio está caído durante la demostración. Clasifica qué puedes explicar con evidencia anterior, qué puedes ejecutar ahora y qué no puedes afirmar. Resultado esperado: tres afirmaciones delimitadas y una siguiente acción viable.

| Para resolverla | Indicación |
|---|---|
| Recurso | Guion de este capítulo; evidencia anterior y estado actual del entorno. |
| Qué hacer | Separa lo que puedes ejecutar ahora, explicar como histórico y no afirmar. |
| Cómo comprobar | Identificas versión/momento de la evidencia y una acción para el bloqueo. |
| Qué conservar | Tres frases para la demostración del proyecto. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


Antes de reutilizar una evidencia, comprueba tres cosas: a qué versión pertenece, qué parte ejercitó y si el cambio puede afectar a esa parte. Por ejemplo, corregir únicamente la ubicación de un archivo en el manual obliga a repetir ese paso con otra persona; no crea una nueva ejecución de P1 ni invalida automáticamente toda PI5. Si cambias un componente utilizado por la prueba, conserva el resultado anterior como histórico y contrasta el efecto antes de trasladar la conclusión.

**Actividad 5 · ocho minutos.** Variante adicional ficticia, no resultado ni cambio real de PI5: el servicio A entregaba la lista en el campo tarjetas; el servicio B la entrega en items y el cliente sigue leyendo tarjetas. Las tarjetas R2-E1, R2-E2 y R2-E4 describían el entorno A; no se ha ejecutado B. No hay un servicio oculto que debas instalar. Decide qué resultados requieren contraste, qué información te falta para acotar el efecto y qué estado conservan P3 y U1. Guarda el resultado anterior y el motivo; no declares un fallo ejecutado a partir de esta descripción.

| Para resolverla | Indicación |
|---|---|
| Recurso | Variante A/B de este enunciado y estado_PI5.json, que conserva las conclusiones originales. |
| Qué hacer | Escribe una fila: cambio, resultado potencialmente afectado, comprobación propuesta y estado real. |
| Cómo comprobar | Justificas lo que reutilizas y lo pendiente sin borrar el resultado anterior. |
| Qué conservar | Una nota enlazada con la incidencia y el mapa de PI5. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


## 6. Dejar mantenimiento que permita actuar

En el ejemplo, P3 no ejecutado es una falta de evidencia crítica, no una vulnerabilidad demostrada. Sigue impidiendo proponer aceptación global. U1 queda como observación de uso pendiente. Ambas líneas enlazan PI5; PI6 añade quién recibe el pendiente y qué necesita para retomarlo.


Una incidencia conocida describe un comportamiento o carencia observados. Una deuda técnica es trabajo aplazado que dificulta la continuidad. Un riesgo es una posibilidad futura. La prioridad debe justificarse por impacto y contexto; una etiqueta roja sin explicación no permite decidir.

| Elemento didáctico | Qué debe saber quien continúa |
|---|---|
| P3 del perfil sin permiso sin ejecutar | Versión afectada, condición no demostrada, entorno que falta, siguiente ensayo y criterio de cierre. |
| Instrucción incompleta | Paso, dificultad, corrección y estado de la repetición. |
| Posible pérdida del entorno | Señal de riesgo, qué conservar, a quién avisar y alternativa disponible. |

Una mitigación no es una solución definitiva. Tener una copia no demuestra que pueda restaurarse. Describe cómo y cuándo se contrastaría el retorno, quién decide y qué versión conservar; evita ejecutar operaciones destructivas sobre datos reales como ejercicio.

Los próximos pasos se mantienen en el tablero existente con acción, prioridad justificada, responsable o rol receptor, dependencia y condición de terminado. No prometas una persona, fecha de empresa o aprobación que no están confirmadas.

**Actividad 6 · diez minutos.** Ordena: una evidencia de permiso contradice el requisito; un icono tiene poco contraste; una comprobación de integración está pendiente. Justifica según el contexto y la evidencia. No existe un orden universal sin analizar impacto.

| Para resolverla | Indicación |
|---|---|
| Recurso | Tres situaciones del enunciado y pendiente I-P3 del ejemplo. |
| Qué hacer | Compara impacto y urgencia y señala qué dato necesitas para priorizar. |
| Cómo comprobar | Una comprobación no ejecutada no se llama fallo; una condición crítica no se compensa con estética. |
| Qué conservar | Prioridad, motivo y siguiente acción en el tablero existente. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


## 7. Explicar una aportación y una dependencia

Una contribución se reconoce por lo que permite localizar, explicar, justificar y adaptar. Puede ser una implementación, una revisión, una decisión o una comprobación pertinente. El número de commits no determina competencia.

Ejemplo de respuesta: «Revisé el procedimiento de carga del caso. El cambio está en estas instrucciones; aquí se ve la dificultad original y la repetición descrita. Depende de que el paquete incluya los datos correctos. Esto mejora la entrega documental, pero no resuelve la comprobación crítica pendiente».

En la comprobación personal puedes consultar las evidencias acordadas. Debes responder tú, sin agente durante el contraste. Una pregunta puede abordar una dependencia esencial del sistema, además de tu aportación.

**Actividad 7 · ocho minutos.** Ensaya con el error de la actividad 2: el paso recibido apunta a tarjetas_otro_corte.json, aunque el esperado describe DEMO-01 y DEMO-02. Conserva ese antes, corrige la referencia en una copia de trabajo identificada y repite el paso. Explica qué cambió y por qué esto no demuestra P3. Después localiza un ajuste equivalente de tu aportación real. Si no puedes repetirlo, registra el bloqueo.

| Para resolverla | Indicación |
|---|---|
| Recurso | Paso 3 de INSTRUCCIONES.md, archivos del ejemplo y referencia de tu aportación. |
| Qué hacer | Muestra antes/después de una referencia o instrucción y explica sus consecuencias. |
| Cómo comprobar | No declaras válido un contenido solo por cambiar su etiqueta; sabes qué contrastar. |
| Qué conservar | Una referencia breve para la tarea individual privada, dentro de sus 75 minutos de preparación. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |


## 8. Obtener una mejora del proceso a partir de hechos

Una retrospectiva breve parte de un hecho localizable, explica su efecto observado, propone un cambio y define cómo comprobarlo. Evita «trabajamos bien» o «hay que organizarse mejor», porque no indican una acción.

Dato adicional ficticio para practicar retrospectiva en PI6; no es un resultado de PI5: «En el registro de dos ciclos se seleccionó integración sin confirmar acceso. El cliente quedó bloqueado. Proponemos verificar acceso y formato antes de comprometer la tarea. En la siguiente oportunidad revisaremos si las tareas con dependencia externa entran con esa confirmación». No demuestra una causa universal ni un resultado futuro.

**Actividad 8 · ocho minutos.** Usa un hecho real de vuestro tablero y propón una mejora verificable. Si no hay datos para afirmar una causa, preséntala como hipótesis. La salida es un registro breve en vuestro espacio; no otra memoria del curso.

| Para resolverla | Indicación |
|---|---|
| Recurso | Un hecho de vuestro tablero o el registro sintético indicado en este capítulo. |
| Qué hacer | Escribe hecho, efecto, hipótesis, mejora pequeña y señal para contrastarla. |
| Cómo comprobar | Distingues datos de opinión y una mejora comprobable de un deseo general. |
| Qué conservar | Una entrada breve de retrospectiva; no otra memoria. |
| Entrega | No se envía como tarea separada. Se integra solo el resultado útil en el trabajo del proyecto. |




Ahora [aplica el procedimiento al proyecto](02_TRABAJA_EN_TU_PROYECTO.md). Si necesitas ver cómo rellenar un campo, abre [la ayuda editable con una fila resuelta](03_PLANTILLA.md).
