# PI5 · De una versión a una decisión con evidencia

Continuamos la historia de PI4: «Como persona con acceso a un tablero, quiero consultar sus tarjetas para conocer el trabajo pendiente». Sus criterios observan dos tarjetas autorizadas, un tablero vacío comprensible y la protección de información ante un perfil sin permiso.

El corte didáctico de PI4 se llamaba TRAIN-C2. Sus referencias a consulta, vacío, sesión caducada y pendientes se conservan como historial. Aquí no cambiamos sus resultados ni los atribuimos a equipos reales. Para aprender a evaluar incorporamos **tarjetas nuevas, completamente sintéticas**, llamadas PI5-TRAIN-R1 y PI5-TRAIN-R2. No son software descargable, ejecuciones reales, IDs del catálogo ni AulaTokens. Puedes resolver todo el ejemplo leyendo sus datos.

## 1 · Fijar qué versión vamos a juzgar

Verificar significa contrastar una condición especificada; validar significa examinar si el resultado sirve para su uso previsto. Una comprobación técnica y una observación de uso aportan respuestas diferentes. Aceptar es una decisión sobre un compromiso y requiere la autoridad correspondiente.

Una versión candidata es la que proponemos evaluar. Para identificarla necesitamos una referencia estable, componentes incluidos, entorno, datos iniciales e instrucciones. «Última versión» puede cambiar mientras revisamos. En el proyecto sirve un commit concreto con el artefacto correspondiente o una exportación identificada; una etiqueta legible debe permitir encontrar esos mismos bytes. No es obligatorio inventar una numeración comercial.

Puedes escribir «exportación del proyecto del 14/02, guardada sin sobrescribir» si todavía no utilizáis etiquetas. Un commit identifica un estado del repositorio; un artefacto es el archivo o aplicación que se generó a partir de él. Un build es el proceso de generar ese artefacto. Relacionar ambos evita juzgar un archivo distinto del código revisado. Reutiliza las instrucciones técnicas de PI4 para abrirlo; aquí aprendemos a decidir qué demuestra el resultado.

En el ejemplo, el corte de PI4 queda como antecedente. PI5-TRAIN-R1 representa una nueva comprobación en un escenario didáctico descrito expresamente: consulta de tarjetas, perfiles sintéticos y sesión de prueba. Sus resultados nuevos no sustituyen los antiguos. Una evidencia de TRAIN-C2 no demuestra automáticamente el comportamiento de R1: compara versión, componente, configuración, entorno y dato afectado antes de reutilizarla.

En tu proyecto anota: «Evaluamos [referencia estable], con [componentes], en [entorno], siguiendo [instrucciones]. Reutilizamos [evidencia anterior] para [condición] porque [equivalencia comprobada]. Falta [dato/acceso]». Si no puedes justificar la equivalencia, el resultado queda pendiente de comprobación.

**Ejercicio 1 · 5 min.** Recibes una captura y un enlace a la rama principal que cambia a diario. ¿Qué necesitas añadir para que otra persona evalúe el mismo producto? **Autocomprobación:** identificas versión estable, artefacto/componentes, entorno, pasos y límites. No declaras inválido todo el trabajo: precisas qué evidencia falta.

## 2 · Pasar de una historia a comprobaciones observables

El criterio describe qué comportamiento se espera; la comprobación concreta cómo observarlo. Una evidencia útil relaciona estado inicial, acción, esperado, obtenido, versión y fuente. Una captura de dos tarjetas no demuestra el caso vacío ni que un perfil sin permiso quede bloqueado. Un build demuestra generación del artefacto en unas condiciones; no demuestra uso, instalación o permisos.

Esta es la entrada íntegra del ejercicio R1. Las cuatro filas son **comprobaciones**, no cuatro historias ni cuatro requisitos contractuales nuevos. Las dos últimas examinan situaciones distintas de la protección de información. La criticidad alta del permiso es una condición explícita del ejercicio.

| Caso y relación con la historia | Estado inicial y acción | Esperado | Tarjeta sintética R1: obtenido | Estado |
|---|---|---|---|---|
| P1 · consulta autorizada | Perfil permitido, tablero con dos tarjetas; abrir consulta | Aparecen ambas tarjetas | R1-E1 describe ambas y el perfil usado | Conforme en ese corte |
| P2 · tablero vacío | Perfil permitido, tablero sin tarjetas; abrir consulta | Se entiende que no hay tarjetas | R1-E2 describe el mensaje de lista vacía | Conforme en ese corte |
| P3 · perfil sin permiso, crítico | Perfil no autorizado; intentar consultar | No se exponen tarjetas | No existe ejecución de este caso en R1 | No ejecutado |
| P4 · sesión caducada, crítico | Consultar con permiso, caducar sesión de prueba y volver | No permanece información restringida visible | R1-E4 describe que siguen visibles las tarjetas anteriores | No conforme |

El fallo de P4 es un dato nuevo y sintético de R1. No reescribe el resultado descrito en PI4 para TRAIN-C2. En un proyecto real una diferencia entre cortes obliga a investigar condiciones y versiones; no autoriza a inventar una causa ni una ejecución.

Mantén cuatro estados: **conforme**, **no conforme**, **no ejecutado** y **evidencia insuficiente**. Este último corresponde, por ejemplo, a «lo probamos» sin versión ni resultado localizable. No ejecutado dice que falta la ejecución; insuficiente dice que lo aportado no permite juzgar. Ninguno equivale a conforme.

**Ejercicio 2 · 7 min.** La evidencia de P3 pasa a ser una captura de la pantalla inicial, sin perfil ni acción. ¿Se puede marcar conforme? **Autocomprobación:** explicas qué observa la captura y qué no; propones obtener perfil autorizado para la prueba, pasos y resultado. No conviertes ausencia de evidencia en éxito ni en un fallo técnico demostrado.

## 3 · Medir para decidir

Un indicador debe responder una pregunta y llevar a una acción. Define nombre, propósito, unidad, universo, cálculo, fuente, corte, frecuencia, umbral y origen, responsable y límite. Un umbral es una regla para actuar: se acuerda antes de juzgar, a partir de la condición pertinente. Cambiarlo después del fallo no mejora el producto.

Con R1 hay cuatro comprobaciones previstas, tres ejecutadas y dos conformes. Calculamos:

| Pregunta | Cálculo con R1 | Lectura y acción |
|---|---|---|
| ¿Cuánto hemos ejecutado? | 3 / 4 × 100 = 75 % | P3 necesita ejecución; localizar acceso y responsable |
| ¿Qué parte de lo ejecutado es conforme? | 2 / 3 × 100 = 66,7 % | P4 necesita corrección y nueva comprobación |
| ¿Qué parte de lo previsto tiene resultado conforme? | 2 / 4 × 100 = 50 % | Mantener visibles tanto P3 pendiente como P4 fallido |

El universo son estos cuatro casos aplicables de R1, no todo AulaFlow. No llamamos a estas cifras «porcentaje del contrato aceptado». Además registramos **una comprobación crítica fallida y una crítica sin ejecutar**. El promedio no las compensa. El objetivo del ejercicio exige evidencia suficiente en todas sus condiciones críticas antes de proponer aceptación del conjunto.

Ficha resuelta: «Ejecución de comprobaciones; pregunta: ¿qué falta observar?; unidad: %; universo: P1–P4; numerador: casos ejecutados; denominador: casos previstos aplicables; fuente: matriz R1; frecuencia: cada corte evaluado; responsable: persona revisora; acción: planificar los no ejecutados; límite: ejecución no implica conformidad». Una condición excluida sin autorización sigue en el universo que le corresponde.

Cuando el denominador es cero, escribe **no medido**, explica por qué y define el siguiente paso. No muestres 100 % ni conviertas un cero técnico de una fórmula en una conclusión sobre calidad. Un conteo, como «incumplimientos críticos pendientes», también puede ser útil sin porcentaje.

Para vuestro proyecto empezad por pocas preguntas: cobertura de comprobaciones, impedimentos críticos y uso de una tarea. Justificad cuáles os ayudan. Número de commits, líneas de código o documentos producidos no demuestran aceptación. Tampoco se suman satisfacción, pruebas y coste para fabricar una supuesta nota de calidad.

**Ejercicio 3 · 8 min.** En otro corte didáctico hay 10 casos previstos, 8 ejecutados y 6 conformes. Calcula las tres medidas y explica qué harías si aún no hay casos previstos. **Autocomprobación:** obtienes 80 %, 75 % y 60 %, con denominadores explícitos; para 0 previstos indicas no medido y una acción. No confundes estas medidas con aceptación.

## 4 · Preparar una sesión de evaluación con usuarios

Observar uso ayuda a descubrir dificultades que una comprobación técnica no describe. Elegimos una tarea y un perfil pertinentes, explicamos qué pedimos, preparamos datos y entorno, moderamos sin dar la solución, registramos hechos y devolvemos una respuesta. No hace falta alcanzar una cantidad arbitraria de participantes. Una muestra pequeña descubre problemas, pero no representa automáticamente a toda la población.

En este ensayo el objetivo adicional es examinar si se entiende cómo consultar y qué hacer cuando no se puede acceder. Es un objetivo de evaluación de uso; no se convierte por sí solo en un nuevo requisito contractual. Para exigirlo como condición de aceptación habrá que localizar la condición auténtica o tramitar la propuesta correspondiente.

Los cuatro documentos se pueden reunir en una sola sección:

| Documento | Ejemplo didáctico listo para ensayar |
|---|---|
| Información/invitación | «Queremos revisar si se entiende la consulta. Observamos el producto, no te examinamos. Puedes parar o pedir ayuda. Registraremos solo acciones y dificultades necesarias, sin grabar por defecto». Antes de una sesión real se confirma la vía del centro. |
| Guion | Preparar tablero y perfil de prueba. Plantear: «Quieres conocer las tareas pendientes de tu tablero. Consulta la información y, si no puedes acceder, explica qué harías». Observar sin indicar botones. Preguntar al final «¿qué esperabas?» y «¿qué te resultó difícil?». |
| Observación | Código de sesión, versión, tarea, acciones observables, resultado, ayuda ofrecida y limitación. Registrar ayudas permite interpretar el resultado. |
| Devolución | Resumir lo observado, qué se propone hacer o no y por qué, quién lo revisa y cómo se comprobará después. |

Ensayo de mesa R1-U1, totalmente sintético: la tarjeta dice «lee “Error 401”, vuelve atrás y pregunta cómo continuar; quien modera le indica que vuelva a iniciar sesión». Eso no es una sesión real. Un compañero puede representar el guion para ensayar su claridad, identificándolo como ensayo; tampoco demuestra comportamiento de usuarios externos.

### Ensayo resuelto que puedes hacer desde casa

Reserva 10 minutos del bloque de ensayo, dentro del tiempo ya previsto. Si trabajas solo, lee la tarjeta R1-U1; si hay compañero, puede representar el guion sin fingir que es una sesión con usuarios externos.

| Minutos | Qué preparas o dices | Qué guardas |
|---|---|---|
| 0–2 | Señala R1, el objetivo de consulta y la modalidad de ensayo. Lee la información inicial y explica que se puede pedir ayuda. | Versión, objetivo y modalidad |
| 2–5 | Plantea la tarea neutral del guion. En el ensayo de mesa toma las acciones de R1-U1; no inventes otras. | «Lee Error 401, vuelve atrás y pide ayuda» |
| 5–7 | Anota la ayuda: «quien modera indica volver a iniciar sesión». Separa lo observado de su posible causa. | Ayuda registrada; comprensión sin ayuda no demostrada |
| 7–10 | Redacta devolución: «Proponemos aclarar la acción del mensaje y repetir la tarea. Aún no sabemos si el texto nuevo se entiende sin ayuda». | Propuesta, responsable de revisión y comprobación posterior |

La ficha cumplimentada dice: «Código R1-U1; versión R1; modalidad: tarjeta sintética; tarea: consultar y explicar qué hacer al perder acceso; hecho: vuelve atrás y pide ayuda; ayuda: indicación de iniciar sesión; interpretación: el mensaje podría ser poco claro; límite: no hay usuario real ni causa confirmada; devolución: proponer aclaración y repetir». Los cuatro documentos pueden convivir en esta misma sección: no son cuatro entregas.

Usa datos de prueba y códigos. No publiques nombres, contactos, credenciales, firmas ni observaciones personales en el repositorio. La recogida real utiliza las condiciones y canal que confirme el centro. Si no están disponibles, deja pendiente esa participación y practica con las tarjetas. El procedimiento y los documentos pueden evaluarse sin inventar una sesión.

**Ejercicio 4 · 8 min.** Reescribe «Pulsa el botón de arriba, entra y dime que lo has entendido» como tarea neutral, y añade dos preguntas abiertas de cierre. **Autocomprobación:** planteas un objetivo sin enseñar el recorrido; tus preguntas permiten descubrir expectativas y dificultades sin pedir una respuesta favorable.

## 5 · Convertir observaciones en hallazgos útiles

Una observación cuenta qué ocurrió. Una interpretación propone qué podría significar. Una acción responde qué haremos para contrastar o mejorar. Mantenerlas separadas evita dar por probada una causa y ayuda a conservar opiniones discrepantes.

| Hecho y fuente | Interpretación con límite | Propuesta |
|---|---|---|
| R1-U1: tras «Error 401», vuelve atrás y pide ayuda | El mensaje podría no explicar la siguiente acción; una tarjeta no demuestra la causa ni frecuencia general | Proponer texto con acción comprensible y repetir la tarea después |
| R1-E4: quedan visibles tarjetas al caducar sesión | Incumple la condición de protección del ejercicio; la causa técnica no está diagnosticada | Enlazar la incidencia del procedimiento de PI4, investigar y comprobar la corrección |
| R1-U2: solicita avisos nuevos por correo | Es una petición nueva si no figura en el alcance vigente | Enviar al procedimiento de cambios de PI4; no introducirla silenciosamente |

Para medir uso, otras tres tarjetas sintéticas dicen: una persona completa sin ayuda, otra con ayuda y otra abandona. Finalización sin ayuda = 1/3; finalización con o sin ayuda = 2/3; finalización con ayuda = 1/3. No hay un dato de satisfacción: no se preguntó. Mantén recuentos, tarea, versión y límite de la muestra, evitando presentar estos datos como una encuesta real.

Clasifica cada hallazgo según condición afectada, impacto en la tarea y evidencia. Un incumplimiento de permiso tiene consecuencias distintas de una preferencia de color. El equipo prepara una respuesta: corregir, contrastar más, proponer cambio o no actuar con motivo. Si ya existe incidencia, amplíala y enlaza la comprobación; no dupliques el registro de PI4.

**Ejercicio 5 · 7 min.** Se afirma «Los usuarios están satisfechos: dos de tres terminaron». Corrige esa conclusión y clasifica la petición de avisos nuevos. **Autocomprobación:** distingues finalización, ayuda y satisfacción no medida; localizas el alcance antes de decidir si una petición es fallo o cambio.

## 6 · Corregir, repetir y comprobar efectos secundarios

Repetir el caso fallido comprueba si se corrigió ese problema. Las pruebas de regresión revisan comportamientos que el cambio podría haber alterado. Elegirlas exige explicar la relación entre cambio y riesgo; no basta repetir lo cómodo ni aceptar «todo verde» de otra versión.

Continuamos el ejercicio: la tarjeta R2-C indica una corrección didáctica en la limpieza de datos de la vista al perder la sesión y un texto que explica cómo volver a acceder. Es una descripción sintética de un cambio; la enseñanza técnica de su implementación corresponde al módulo propietario.

| Qué volver a observar en R2 | Por qué | Nueva tarjeta didáctica disponible |
|---|---|---|
| P4: caducar sesión y volver a la vista | Es el caso que falló | R2-E4 indica que no quedan tarjetas restringidas visibles |
| P1: consultar dos tarjetas con permiso | La limpieza de vista podría impedir la consulta válida | R2-E1 describe consulta correcta |
| P2: abrir tablero vacío | El mismo estado de vista podría confundir vacío y error | R2-E2 describe el vacío comprensible |
| P3: intentar acceso con perfil sin permiso | Sigue siendo un caso obligatorio sin observar | No hay ejecución: permanece pendiente |
| U1: comprender qué hacer al perder acceso | Cambiar el texto no demuestra comprensión | El guion está preparado, pero no hay nueva observación |

En el ámbito de las cuatro comprobaciones P1–P4, R2 tiene 3/4 ejecutadas, 3/3 conformes entre ejecutadas y 3/4 conformes sobre previstas. El 100 % entre ejecutadas **no permite aceptar el conjunto**: P3 sigue pendiente. U1 se registra aparte como evaluación de uso; no se añade al denominador de esos cuatro casos.

Registro resuelto del antes y después: «P4, condición de protección de información. Antes: R1-E4, las tarjetas quedan visibles; estado no conforme. Acción descrita: R2-C, limpieza de la vista al perder sesión. Repetición: R2-E4 indica que ya no quedan visibles. Regresiones: R2-E1 y R2-E2, para no romper consulta válida ni vacío. Resultado de P4 en R2: conforme según la tarjeta. Límite: P3 continúa sin ejecutar y U1 sin observación posterior». En el proyecto sustituye esas referencias por tus resultados reales y la incidencia existente; no copies la conclusión si no has realizado la comprobación.

Para el proyecto, registra versión anterior, cambio, incidencia enlazada, casos afectados, responsable, esperado, obtenido y evidencia nueva. Si solo preparaste la repetición, marca «planificada». Si una dependencia impide ejecutar, registra bloqueo y próxima revisión. Una solución técnica puede estar aplicada y seguir pendiente su comprobación o su contraste de uso.

**Ejercicio 6 · 8 min.** Una PR cambia el almacenamiento y solo adjunta las pruebas anteriores. Prepara el plan de comprobación: caso fallido, regresiones pertinentes, nueva versión y evidencias que pedirías. **Autocomprobación:** justificas cada elección por el cambio y su riesgo, conservas el historial y no inventas resultados.

## 7 · Proponer aceptación, corrección o decisión pendiente

La matriz de cumplimiento mantiene, para cada condición aplicable, la comprobación prevista, evidencia exacta, versión, estado, límite y siguiente acción. Este sistema permite revisar el compromiso sin reescribirlo para que encaje con el resultado. Un promedio resume; la decisión se justifica por condiciones.

Con R1 proponemos **corregir y volver a comprobar**: P4 falla y P3 no está ejecutado. Con R2 podemos declarar que P4 dispone de nueva evidencia didáctica favorable y sus regresiones descritas son conformes. Proponemos **mantener pendiente la aceptación del conjunto** hasta ejecutar P3 y resolver los requisitos de uso que realmente sean exigibles. No se borra R1 ni se presenta el cambio de texto como comprensión observada.

Una propuesta favorable debe delimitar contrato/pliego y versión, evidencias suficientes, condiciones cumplidas, límites, pendientes compatibles con el acuerdo y autoridad. Solo la persona o función autorizada confirma la aceptación contractual. El equipo no se concede permiso ni AulaTokens. Aceptar una parte exige que esa parte sea separable y que el acuerdo lo permita; no convierte el resto en aceptado.

Si un incumplimiento impide satisfacer el compromiso, explica el retrabajo necesario o la propuesta de rechazo motivada. Si falta evidencia, no fabriques un rechazo por comportamiento que no observaste: mantén pendiente el juicio y concreta cómo resolverlo. Los riesgos o mejoras opcionales no autorizan a ocultar incumplimientos obligatorios bajo «aceptado con pendientes».

Acta breve resuelta: «PI5-TRAIN-R2; P1, P2 y P4 conformes según sus tarjetas; P3 crítico no ejecutado. Se propone mantener pendiente la aceptación global. Siguiente acción: ejecutar P3 en entorno autorizado y registrar resultado; responsable: persona revisora del ensayo. U1 necesita repetir observación si se quiere afirmar mejora de comprensión. Autoridad del acuerdo: pendiente de decisión. Este ejercicio no valida AT reales».

**Ejercicio 7 · 7 min.** Hay 99 comprobaciones conformes y una condición crítica obligatoria fallida. El equipo propone aceptar porque alcanza el 99 %. Responde con condición, evidencia, decisión y siguiente acción. **Autocomprobación:** no compensas el fallo con el promedio; conservas el requisito y distingues propuesta del equipo y autoridad de aceptación.

## 8 · Dejar un estado que otra persona pueda continuar

PI6 recibe una versión y una explicación localizable de qué se sabe y qué falta. Reutiliza el índice, matriz, incidencias y documentos de uso. No redactes una memoria que repita todo el curso ni anticipes una aceptación favorable.

Salida resuelta del ejercicio: «Referencia R2; matriz P1–P4 y tarjetas R1/R2 conservadas; P3 pendiente, U1 sin observación posterior; propuesta de aceptación pendiente; siguientes pasos y responsables indicados; instrucciones y entorno referenciados». Se puede encontrar cada afirmación sin llamar al autor.

Cada persona debe poder reconstruir una medida, explicar qué demuestra una evidencia y ajustar una decisión si cambian los datos. Si se retira por inválida una prueba, revisa estado y cálculo, conserva la decisión anterior y explica el efecto. No basta aparecer como integrante del equipo.

**Ejercicio 8 · 5 min.** Escribe cinco líneas para que otra persona continúe desde R2. **Autocomprobación:** localizas versión, evidencia, decisión, pendientes y responsables. No afirmas que PI4 o PI5 estén aceptadas por terminar el plazo.

Puedes usar IA para comprender, revisar cálculos o proponer comprobaciones cuando la actividad lo permita. Contrasta la respuesta y registra brevemente qué ayuda utilizaste y qué comprobaste. Una prueba sugerida no es una prueba ejecutada. La comprobación individual observada se realiza sin agente, en la modalidad comunicada.

Ahora [aplica estos pasos al proyecto](02_TRABAJA_EN_TU_PROYECTO.md). Si necesitas localizar un campo, consulta la [ayuda editable con un ejemplo cumplimentado](03_PLANTILLA.md).
