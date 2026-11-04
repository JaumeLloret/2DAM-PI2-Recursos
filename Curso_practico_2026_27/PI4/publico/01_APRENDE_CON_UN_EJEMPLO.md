# PI4 · Del sprint al incremento: ejemplo explicado

Seguimos la historia de PI3: «Como persona con acceso a un tablero, quiero consultar sus tarjetas para conocer el trabajo pendiente». Sus criterios observan dos tarjetas autorizadas, un tablero vacío comprensible y la protección de información ante un perfil sin permiso. El ejemplo es completamente didáctico: sus versiones TRAIN-C1 y TRAIN-C2, incidencias y cantidades no son ejecución ni aceptación real del proyecto. Las referencias locales no crean IDs contractuales ni AulaTokens.

Puedes practicar todos los ejercicios leyendo los datos y escribiendo una nota: no necesitas instalar una aplicación de entrenamiento. Los resultados de las tablas son datos proporcionados del caso, no pruebas que tú hayas ejecutado. En el proyecto real sí obtendréis las evidencias con vuestras capacidades disponibles.

## 1 · Ejecutar y comprobar antes de terminar

Una historia expresa un resultado útil; una tarea organiza trabajo para conseguirlo. El criterio de aceptación describe un comportamiento observable. La definición de terminado añade reglas comunes del equipo: comprobar, revisar, identificar versión y guardar evidencia. Una tarea técnica cerrada no demuestra por sí sola la historia completa.

El sprint ya tiene objetivo y trabajo elegido. Al empezar el día, el equipo mira qué resultado persigue, quién realiza el siguiente paso y qué dependencia está disponible. Si el sprint anterior terminó, revisa su resultado y prepara el siguiente según su propia duración; no crea un sprint porque haya taller.

### Datos comunes del caso

El equipo didáctico usa el tablero TRAIN-T1. Sus tarjetas sintéticas son TRAIN-A «Preparar demo» y TRAIN-B «Revisar instrucciones». TRAIN-LECTOR identifica un perfil permitido, no unas credenciales. Ana ejecuta, Bruno contrasta y Carmen mantiene las instrucciones; los papeles pueden rotar y no imponen el reparto de vuestro equipo. La condición de protección incluye no dejar información restringida visible cuando la sesión deja de ser válida. Se comprobarán por separado ese caso y los permisos entre componentes: una prueba no demuestra automáticamente la otra.

Tarjeta de tarea resuelta: «Comprobar consulta y vacío en TRAIN-C1». Regla del equipo: Ana registra criterio, versión, estado inicial, acción, esperado y observado; Bruno revisa antes de cerrar. Si falta prueba, queda En revisión. Si hay fallo, se registra una incidencia y se deja visible lo pendiente. La tarea acotada puede terminar aunque la historia siga parcial.

En el ejemplo, la versión TRAIN-C1 presenta dos tarjetas de prueba desde la consulta disponible. El caso vacío también se ha repetido. La comprobación de permisos entre componentes aún no está realizada.

| Criterio de la historia | Resultado observado en TRAIN-C1 | Qué podemos afirmar |
|---|---|---|
| Persona autorizada consulta dos tarjetas | Ambas aparecen y se identifica el entorno de prueba | Comprobado en esa versión y entorno |
| Tablero autorizado vacío | Aparece un mensaje de lista vacía; no se confunde con error | Comprobado |
| Perfil sin permiso | No hay repetición del caso sobre esta versión | Pendiente; la historia completa no está aceptada |

Antes de mover una tarea a Terminada: localiza criterio y versión, realiza la comprobación, registra esperado/obtenido y evidencia, solicita una revisión proporcional y conserva el resultado. Una captura sin estado inicial puede no demostrar lo que afirmas. Una PR puede mostrar el cambio, pero no garantiza que el comportamiento se haya repetido.

**Ejercicio 1 · 5 minutos.** Una tarjeta dice «pantalla terminada» y solo adjunta una captura de dos tarjetas. Decide qué parte podría estar hecha, qué criterios no demuestra y cuál es la siguiente comprobación. **Autocomprobación:** tu respuesta distingue tarea, historia y evidencia; no da por probado el vacío ni el permiso por una captura de otro caso.

## 2 · Mostrar un incremento real y sus límites

Un incremento es una parte utilizable y comprobable del producto. No es la suma de «he trabajado mucho» de sus miembros. Una respuesta simulada sirve para entrenar una interfaz, pero no prueba una consulta al servicio real. El avance se explica sin esconder sus límites.

Demostración resuelta de TRAIN-C1: fijar versión y entorno; restablecer dos tarjetas sintéticas autorizadas; abrir la consulta con un perfil permitido; comprobar que aparecen ambas; mostrar el caso vacío; señalar que el permiso negativo sigue pendiente. Quedan enlazados pasos, resultados y evidencia. La consulta probada es un avance; la historia no se declara completa hasta comprobar todos sus criterios.

Para revisar usa cuatro estados comprensibles: comprobado, parcial, pendiente y bloqueado. Añade qué criterio se observa y dónde. Si algo depende de un módulo o acceso, indica responsable y siguiente revisión. No cambies el requisito para convertir un fallo en éxito.

### Guion con los datos preparados

1. Identifica TRAIN-C1, TRAIN-T1 y el perfil permitido; indica que estás analizando resultados proporcionados del caso.
2. Estado inicial: TRAIN-A y TRAIN-B, sesión válida. Acción: abrir consulta. Esperado y observado proporcionado: aparecen ambas tarjetas.
3. Estado inicial: tablero autorizado sin tarjetas. Acción: abrir consulta. Esperado y observado: mensaje de lista vacía.
4. Límite: falta contrastar sesión no válida y permisos entre componentes; no se ha demostrado toda la historia ni el producto anual.
5. Siguiente acción: Ana prepara la comprobación de sesión; Bruno revisa su resultado antes de cerrar la historia.

Comprobado significa conforme en un caso y versión identificados; parcial, que solo se cumplen algunas condiciones; pendiente, que falta contraste; bloqueado, que una dependencia impide seguir y requiere ayuda y revisión. Una condición puede estar pendiente por un bloqueo: explica ambos. No midas el avance contando tarjetas cerradas: una tarea pequeña y una integración crítica no aportan el mismo resultado.

**Ejercicio 2 · 5 minutos.** Prepara el guion de una demostración de TRAIN-C1 con estado inicial, acción, esperado, observado y límite. **Autocomprobación:** otra persona puede repetirla y entiende qué no se ha demostrado. No necesitas grabar un vídeo ni construir una función nueva para este ejercicio.

## 3 · Revisar el sprint y mejorar cómo trabajamos

La revisión del sprint compara objetivo y resultado: qué incremento existe, qué criterios se comprobaron, qué quedó pendiente y qué decisión viene después. La retrospectiva examina el modo de trabajar: qué ayudó, qué dificultó y qué mejora concreta probaremos. No exige dos memorias ni reuniones extensas; puede quedar una nota breve en la revisión del tablero.

En el ejemplo se habían repartido tareas, pero las pruebas se dejaron para el último día. Dos tarjetas llegaron a revisión sin versión. El equipo acuerda una mejora: «Durante el próximo ciclo, toda tarea que pase a Revisión llevará criterio, versión y evidencia». Al cerrar ese ciclo revisará las tarjetas que pasaron por Revisión y anotará si la mejora se cumplió y si ayudó. El dato sirve para decidir, no para conceder nota por contar tarjetas.

Una nota útil puede decir: «Objetivo: consulta autorizada. Resultado: dos criterios comprobados y uno pendiente. Problema de trabajo: pruebas acumuladas al final. Mejora: revisar criterio/versión/evidencia antes de mover. Responsable del seguimiento: quien revise cada tarea. Próxima comprobación: cierre del siguiente ciclo».

Resultado posterior proporcionado: en el siguiente ciclo tres tarjetas llegaron con criterio, versión y evidencia; una llegó sin versión, volvió a revisión y se completó. El equipo conserva la mejora porque permitió corregir esa carencia antes de cerrar. Esta observación completa la mejora: no basta anunciarla. La previsión siguiente se corrige con disponibilidad, dependencias y trabajo pendiente; no se reescribe el objetivo anterior como si siempre hubiera sido menor.

**Ejercicio 3 · 5 minutos.** De las propuestas «comunicarnos mejor», «hacer más reuniones» y «avisar del bloqueo en la tarjeta el día que aparece, indicando ayuda necesaria y próxima revisión», escoge o redacta una mejora comprobable. **Autocomprobación:** explicas qué cambia, cuándo se probará y cómo sabréis si se aplicó. No se repite la retrospectiva final de PI6.

## 4 · Registrar, diagnosticar y resolver una incidencia

Una incidencia es un problema que impide o contradice lo esperado durante la ejecución. Puede ser un fallo del producto o un problema del proceso o entorno. Registrar permite que otra persona lo entienda; evaluar permite decidir su impacto, prioridad y seguimiento. Prioridad no equivale a dificultad de programación.

La gravedad describe daño y alcance; la prioridad decide cuándo actuar considerando también urgencia y alternativas. Regla didáctica del equipo: información restringida visible o pérdida de datos se atiende primero y se avisa a su responsable; un bloqueo del objetivo sin alternativa va después; un detalle visual con alternativa puede esperar. En el proyecto acordad una regla proporcional, sin prometer guardias ni probar con datos reales.

Caso TRAIN-INC-1, en TRAIN-C1: abrir una consulta autorizada, caducar la sesión de prueba y volver a la vista. Esperado: no exponer información restringida fuera de la sesión válida. Obtenido: permanece información anterior. El ejemplo usa datos sintéticos y un escenario de prueba autorizado. Impacto alto en el ejercicio por información visible fuera de la condición prevista; se asigna responsable y próxima revisión. No se ensaya con cuentas ajenas ni datos reales.

El procedimiento del equipo responde quién registra, qué datos mínimos usa, quién revisa la prioridad, cuándo se vuelve a mirar y quién confirma el cierre. Para resolver: reproducir; delimitar versiones, condiciones y alcance; proponer hipótesis; buscar evidencia que las apoye o descarte; aplicar la acción técnica con herramientas ya disponibles; repetir el caso fallido y las regresiones relevantes; pedir revisión; registrar resultado y versión.

Ejemplo de diagnóstico: «Podría mantenerse un resultado antiguo en la vista» es una hipótesis. Se compara qué ocurre al caducar la sesión y al volver a abrir la vista en el entorno autorizado. Esa comparación ayuda a localizar el problema; no autoriza a afirmar una causa que no se ha contrastado ni sustituye su solución técnica en el módulo correspondiente.

En TRAIN-C2 el caso original se repite y deja de mostrar la información; se vuelven a comprobar consulta autorizada y vacío. Quien revisa puede cerrar con esas evidencias. Si solo existe una propuesta de corrección, el estado es corrección propuesta o pendiente de comprobación. Si reaparece, se reabre y se enlaza la nueva evidencia. No hace falta terminar una corrección compleja en 45 minutos para dejar un diagnóstico y una acción útiles.

### Registro y comprobaciones resueltos

| Campo | Registro proporcionado |
|---|---|
| Identificación y reproducción | TRAIN-INC-1, TRAIN-C1, TRAIN-T1 con TRAIN-A y TRAIN-B; consultar con sesión válida, darla por caducada en el caso y volver a la vista |
| Esperado / obtenido | No dejar información restringida visible / siguen visibles las dos tarjetas; observación didáctica OBS-3 |
| Impacto, prioridad y seguimiento | Alto por información fuera de la condición prevista; atender antes de ampliar funciones. Ana investiga; Bruno contrasta antes del cierre de la historia |
| Hipótesis y contraste | H1: la vista conserva resultados anteriores. Dato del caso: al volver a la vista abierta conserva tarjetas; en una vista limpia sin sesión válida no aparecen. Orienta hacia el estado previo, sin demostrar todos los controles de acceso |
| Acción y versión | Acción técnica proporcionada: invalidar la información mostrada al perder la sesión y aplicar el tratamiento de acceso previsto; identificada como TRAIN-C2. Su implementación corresponde al módulo técnico |
| Cierre | Bruno revisa los tres resultados siguientes y cierra TRAIN-INC-1 con referencia a TRAIN-C2. Si reaparece, conserva el cierre anterior, reabre y enlaza nueva evidencia |

| Comprobación proporcionada en TRAIN-C2 | Resultado y límite |
|---|---|
| Repetir el caso de sesión caducada | Ya no quedan tarjetas visibles: retest conforme de ese caso |
| Repetir consulta autorizada con dos tarjetas | Aparecen TRAIN-A y TRAIN-B: regresión conforme |
| Repetir tablero autorizado vacío | Mensaje de lista vacía: regresión conforme |

**Retest** es repetir el caso que falló; **regresión** es comprobar que siguen funcionando casos relacionados. Este contraste no es una auditoría de seguridad completa ni demuestra permisos entre todos los componentes. En vuestro proyecto los resultados deben ser reales; si solo existe propuesta o no puede repetirse, se deja pendiente, con responsable y siguiente acción.

**Ejercicio 4 · 7 minutos.** El registro dice «falla el login; arreglado; cerrar» y enlaza una PR sin versión probada. Complétalo para que otra persona pueda investigar y decidir el cierre. **Autocomprobación:** aparecen pasos, esperado/obtenido, impacto/prioridad razonados, responsable, hipótesis contrastable, prueba nueva y condición de cierre. No inventes una ejecución que no está en los datos.

## 5 · Gestionar un cambio y conservar la decisión anterior

Un cambio solicita modificar alcance, recurso, tarea o condición del plan. Corregir el comportamiento que ya estaba acordado es una incidencia; añadir otro comportamiento es un cambio. Una incidencia puede originar un cambio, pero no permite eliminar el requisito incumplido.

Solicitud TRAIN-CR-1: el entorno externo estará indisponible durante el próximo ciclo. El equipo compara continuar tareas independientes, solicitar otro entorno de prueba autorizado o desplazar trabajo de integración dentro del calendario. Para cada opción considera resultado, tareas, recursos, tiempo, coste y riesgos. No se presupone que otra cuenta, servicio o pago esté autorizado.

| Decisión | Quién puede tomarla |
|---|---|
| Orden y reparto de tareas dentro del acuerdo y capacidad | El equipo, dejando motivo y plan actualizado |
| Cambio de funciones comprometidas, hito docente o condiciones del acuerdo | La autoridad del acuerdo/docente; el equipo presenta propuesta y espera decisión |
| Acceso o uso de un recurso compartido | Su responsable; el equipo no se concede permiso |

Resultado didáctico: se propone continuar tareas independientes y solicitar una franja en un entorno autorizado. El registro conserva «pendiente de autorización» mientras no exista respuesta. El plan P1 se conserva; P2 indica qué se ha reorganizado, qué decisión ya puede tomar el equipo y qué parte sigue pendiente. Si cambia el acuerdo, se enlaza el anexo aprobado; no se vuelve a copiar todo el contrato.

### Comparación con datos suficientes para decidir

Para el siguiente ciclo se habían previsto dos horas de contraste. Se pierde esa franja, pero hay otra posible antes del mismo hito. Tarifa didáctica de comparación: 15 €/h. Son **estimaciones del plan siguiente**; no se suman al tramo cerrado del paso 6.

| Opción | Impacto adicional sobre P1 | Dependencia y riesgo |
|---|---|---|
| A · Reordenar trabajo y pedir otra franja | Mantiene las 2 h previstas y añade 1 h de coordinación: +15 € de esfuerzo; desembolso adicional 0 € | El equipo reordena; el responsable confirma la franja; riesgo de no conseguirla |
| B · Otro alojamiento de prueba | Mantiene las 2 h y añade 2 h de preparación: +30 € de esfuerzo y 12 € supuestos de recurso; total +42 € | Requiere autorización de recurso, acceso y eventual pago; puede no reproducir el entorno previsto |

Historial resuelto: P1 conserva franja, objetivo y responsables originales. TRAIN-CR-1 propone A. P2 provisional avanza instrucciones y pruebas independientes y mantiene pendiente el contraste; +1 h es previsión. Más tarde, una respuesta proporcionada del responsable confirma la nueva franja antes del mismo hito: se incorpora su referencia y fecha y P2 pasa a autorizado para ese recurso. No cambia el contrato ni la fecha docente. En el proyecto solo se registra esa aprobación cuando existe una respuesta real localizable; mientras no llegue, continúa pendiente. Suprimir el contraste comprometido no sería una decisión unilateral válida.

**Ejercicio 5 · 7 minutos.** Compara A y B con los datos anteriores: indica impacto valorado, desembolso, ventajas, dependencias y autoridad. Explica qué puede avanzar el equipo mientras espera y si podría marcar B como aplicada solo porque la prefiere. **Autocomprobación:** comparas el mismo trabajo base y sumas solo extras; separas propuesta, aprobación y aplicación; mantienes fecha y plan anterior. No se pide contratar servicios.

## 6 · Valorar esfuerzo, recursos y desviaciones

La estimación anticipa trabajo; el registro observado dice lo realmente dedicado. Las horas-persona se suman entre integrantes: 4 h + 5 h + 5 h = 14 h de trabajo, aunque parte haya sido simultánea. No son 14 horas de calendario ni un reparto obligatorio. El equipo usa la unidad que pueda explicar; no mezcla puntos de estimación con horas.

Ejemplo resuelto del mismo tramo de consulta ya terminado. Previsión: 12 horas-persona a una tarifa didáctica de 15 €/h, más un recurso de pruebas de 8 € para el período. La tarifa es un supuesto del ejercicio, no salario ni precio de mercado. Se compara el mismo alcance y período; una ejecución parcial no se presenta como coste final.

| Concepto | Cálculo previsto | Cálculo observado | Desviación |
|---|---:|---:|---:|
| Esfuerzo | 12 h × 15 €/h = 180 € | 14 h × 15 €/h = 210 € | +30 € |
| Recurso de pruebas del período | 1 período × 8 € = 8 € | 1 período × 8 € = 8 € | 0 € |
| Total valorado | 188 € | 218 € | +30 € |

Paso 1: sumar horas observadas del equipo sin duplicarlas. Paso 2: multiplicar por la tarifa explícita. Paso 3: añadir recursos del mismo período. Paso 4: calcular observado menos previsto: 218 − 188 = +30 €. Paso 5: dividir 30 entre 188 y multiplicar por 100: aproximadamente 16 %. Paso 6: explicar la causa con evidencia: dos horas adicionales de diagnóstico y repetición de pruebas, registradas en la incidencia del ejemplo.

Fuente de las 14 horas del caso: registro didáctico del tramo, Ana 4 h, Bruno 5 h y Carmen 5 h, incluyendo las comprobaciones. El porcentaje sin redondear es 15,96 %. Son supuestos de aprendizaje, no salarios actuales ni presupuesto completo de una empresa.

### Ejemplo cuando todavía queda trabajo

Escenario alternativo, sin sumarlo al anterior: previsión inicial de 12 h; ya observadas 10 h; quedan 4 h estimadas para el mismo alcance. Previsión al terminar: 10 + 4 = 14 h; a 15 €/h y con recurso de 8 €, total previsto al terminar 218 €. Solo se han observado 150 € de esfuerzo; los 60 € de esfuerzo restante son previsión. No escribas «coste final 218 €» hasta cerrar el alcance ni sumes otra vez las 12 h iniciales. Si no conoces lo restante, indícalo y explica cómo lo estimarás.

Bajo el supuesto de que no se pagan remuneraciones ni hay otras compras, el desembolso es 8 €; el esfuerzo valorado es 210 €. Un equipo escolar no tiene que pagar ese esfuerzo ni contratar recursos para demostrar el CE. Un coste desconocido se declara desconocido, no cero. En el proyecto registra concepto, cantidad/unidad, coste unitario, fuente y fecha o supuesto, período y alcance, previsto, observado, pendiente estimado y causa de desviación. Si el tramo no ha terminado, separa gasto/esfuerzo observado y previsión restante; no los confundas con el resultado final.

| Magnitud | Significado y límite |
|---|---|
| Estimación de tarea | Previsión de esfuerzo para decidir qué cabe; se revisa |
| Horas observadas | Trabajo registrado, con fuente y período |
| Euros | Valoración de trabajo/recursos o pago; hay que indicar cuál |
| AulaTokens | Alcance y aceptación conforme a catálogo y acuerdo auténticos; no son horas ni euros |

No se convierten AT en horas, euros o nota por tarea propia. La valoración de PI2 sirve como entrada; ahora se explica la ejecución y su desviación, sin rehacer el contrato.

**Ejercicio 6 · 7 minutos.** Para el mismo alcance completo se observan 16 horas y un recurso de 10 €. Calcula esfuerzo valorado, total, desviación frente a 188 € y desembolso bajo los mismos supuestos. **Autocomprobación:** las unidades acompañan los cálculos, el porcentaje usa la previsión inicial y explicas una causa que necesitaría evidencia. No usas AT para obtener horas.

## 7 · Mantener instrucciones que otra persona pueda seguir

Documentar para ejecutar significa permitir que alguien localice una versión, prepare el estado autorizado, realice el paso y entienda el resultado. Usa el README, una tarjeta o instrucciones existentes. Enlaza la explicación técnica del módulo propietario; no vuelvas a enseñar el lenguaje o la instalación completa si ya tiene una guía vigente.

### Procedimiento completo para ensayar sin aplicación

1. Abre los pasos 1 y 4 y crea una nota «Ensayo documental de consulta · TRAIN-C2». No la presentes como ejecución real del proyecto.
2. Copia el estado inicial: TRAIN-T1 con TRAIN-A y TRAIN-B, perfil permitido y sesión válida. Escribe las tres condiciones: consulta con datos, vacío y protección al caducar la sesión.
3. Prepara tres filas, una por condición. En cada una anota estado inicial, acción y esperado. Los datos de los pasos 1, 2 y 4 permiten completarlas sin pedir otra explicación.
4. Localiza los tres resultados proporcionados de TRAIN-C2 al final del paso 4. Cópialos como «observado del caso»; compara cada uno con su esperado.
5. Explica qué permite cerrar TRAIN-INC-1, qué regresiones se han contrastado y qué permisos/integración no se han demostrado. Señala el registro que respalda cada afirmación.
6. Otra persona sigue tu nota sin que le dictes pasos. Si estás solo, repítela desde el principio y marca «autocotejo»; el contraste personal que requiera observación se acuerda con el docente dentro de la alternativa, sin inventarlo.
7. Para reiniciar, vuelve a los datos iniciales del paso 1; no hay base de datos que borrar. Si falta información, señala campo/paso y pide ayuda indicando versión, esperado y obtenido.

Esto permite aprender el procedimiento con los materiales incluidos. Para el producto real añade los pasos y enlaces técnicos que existan y que se hayan probado. No hace falta instalar una aplicación ficticia para entender el ejemplo.

En el proyecto deben aparecer los enlaces o pasos reales que sustituyan esas referencias didácticas, datos iniciales, versiones de componentes relevantes, resultado esperado y recuperación del estado cuando proceda. No inventes comandos o direcciones que no existen. Otra persona sigue las instrucciones sin que el autor le dicte lo que falta; se registra dónde se pierde y se corrige.

Ejemplo de mejora tras usar una guía: Bruno se pierde en «prueba el vacío»; Carmen lo concreta: «parte del tablero autorizado sin tarjetas; abre la consulta; espera un mensaje de lista vacía». Se conserva qué se corrigió y en qué versión. No incluyas secretos ni datos personales en un README público.

**Ejercicio 7 · 5 minutos.** Revisa «abre el proyecto, ejecútalo y comprueba que funciona». Indica qué falta y redacta una instrucción aplicable al ejemplo. **Autocomprobación:** permite encontrar versión, preparación, acción, resultado y ayuda; no se basa en adivinar lo que sabe el autor.

## 8 · Preparar una versión para PI5

PI4 deja un corte identificable: commit, etiqueta o exportación estable, fecha, componentes incluidos, requisitos y criterios con evidencia, incidencias/cambios, instrucciones y pendientes con responsables. Puede seguir habiendo trabajo pendiente; se declara para decidir cómo validar. No se afirma aceptación final.

Índice resuelto de TRAIN-C2: versión identificada; consulta y vacío comprobados; repetición de sesión caducada y revisión enlazadas; consulta entre ambos clientes pendiente si aún no se ha contrastado; solicitud de entorno con decisión localizable; coste del tramo y supuestos; instrucciones verificadas. El mismo estado pasa a PI5, donde se trabajarán indicadores, participación de usuarios y contraste de cumplimiento. No hace falta fabricar esos resultados en PI4.

### Cómo quedaría localizado el corte

| Entrada | Referencia del caso y significado |
|---|---|
| Producto y criterios | TRAIN-C2, consulta de TRAIN-T1; registros de datos/vacío y sesión del paso 4 |
| Trabajo y mejora | Nota del paso 3 y resultado posterior de la mejora; no solo anuncio de reunión |
| Incidencia | TRAIN-INC-1: OBS-3 en C1, acción y tres comprobaciones en C2, revisión de Bruno |
| Cambio | TRAIN-CR-1 con P1 conservado, P2 y confirmación proporcionada del recurso |
| Economía | Tramo cerrado: 188 € previstos, 218 € observados, +30 € y fuente/supuestos del paso 6 |
| Instrucciones | Ensayo documental del paso 7; en el producto será una guía técnica real contrastada |
| Pendiente | Permisos/consulta entre componentes no demostrados; en el proyecto se asignan responsable y próxima comprobación |

Una rama o «última versión» puede cambiar. Usa un commit fijo, identificador de publicación o exportación recuperable; si usas etiqueta, conserva también el identificador al que apunta. En el proyecto cada entrada del índice enlaza a lo existente en el espacio habitual; una copia autorizada debe corresponder al mismo estado y omitir secretos. Preparado para validar significa que se sabe qué comprobar y qué falta, no que el producto ya esté aceptado.

**Ejercicio 8 · 5 minutos.** Se entrega una captura y el enlace «última versión», que cambia cada día. Decide qué añadir para poder validar y repetir las comprobaciones. **Autocomprobación:** indicas versión estable, alcance, pasos, evidencias y pendientes; no das por válida una función solo por su aspecto.

La IA puede ayudar a proponer hipótesis, revisar instrucciones o señalar contradicciones. Es opcional y no requiere cuenta ni herramienta de pago. Registra brevemente qué ayuda usaste y qué contrastaste. Una prueba sugerida no equivale a una prueba ejecutada. Las decisiones, revisión del alcance y explicación de lo esencial siguen siendo del equipo.
