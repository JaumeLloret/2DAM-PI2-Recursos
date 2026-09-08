# Comprender un contexto y un producto heredado

## 1. Incorporarse antes de construir

Un sistema heredado es un producto que ya tiene usuarios previstos, decisiones, datos, contratos y límites. «Legado» no significa necesariamente obsoleto: indica que no elegimos su punto de partida. Una reescritura sin conocerlo puede perder funciones útiles, interpretación de datos o garantías que no se ven en una pantalla.

AulaFlow 1.0.0 es un Kanban educativo con interfaz web, servidor Java y persistencia SQLite. En PI1 lo observamos como profesionales que reciben un producto. El objetivo no es aprender cada clase, sino responder cuatro preguntas: qué responsabilidad tiene cada parte, qué evidencia muestra su comportamiento, qué contexto hace útil ese comportamiento y qué cambio de contexto podría exigir revisarlo.

**Ejemplo conceptual:** una tarjeta continúa al reiniciar el servidor, pero debes volver a iniciar sesión. No hay contradicción: la tarjeta puede vivir en almacenamiento persistente y la sesión en memoria. Concluir «ha perdido los datos» mirando solo el login sería un error de diagnóstico. En el laboratorio verificarás ambos hechos por separado sobre tu ejecución.

## 2. Empresa proveedora, organización usuaria y sector

El sector productivo agrupa actividades relacionadas. En software conviene distinguir producir un producto reutilizable, desarrollar soluciones por encargo y operar o integrar sistemas para otras organizaciones. Un centro educativo usuario de una aplicación pertenece a un contexto de servicio educativo; no se convierte por ello en una empresa de software.

Clasificar significa elegir ejes útiles y aplicarlos de manera consistente. «Es una empresa tecnológica» no distingue cómo organiza el trabajo ni qué vende. Usa actividad principal, producto/servicio, tipo de cliente, modo de prestación, dimensión observada y estructura. La forma jurídica, como SL o cooperativa, es otro eje: no determina por sí sola el número de personas o el modelo de ingresos.

| Organización tipo | Qué ofrece | Organización característica del caso | Pregunta para AulaFlow |
|---|---|---|---|
| Proveedora de producto software | licencia/servicio y mantenimiento de un producto común | producto prioriza; ingeniería construye; soporte aprende del uso | ¿cómo se comparte conocimiento entre funciones? |
| Consultora de desarrollo e integración | proyectos y servicios adaptados a clientes | dirección de proyectos coordina; equipos atienden encargos; operaciones sostiene instalaciones | ¿cómo se evita perder el estado de un encargo? |
| Microempresa de soporte | servicio técnico de proximidad | una persona puede reunir ventas, soporte y administración | ¿quién actualiza el estado cuando hay desplazamientos? |
| Centro educativo usuario | formación y organización docente | dirección, coordinación, profesorado y soporte con responsabilidades distintas | ¿quién decide, usa y mantiene una herramienta? |

Son arquetipos de análisis, no organigramas constatados de una empresa real. La [ficha del caso](../Alumnado/09_CASO_CONTEXTO_PI1.md) concreta tamaño y funciones sin inventar entrevistas. En una empresa pequeña puede no existir un departamento formal de RRHH; alguien desempeña esa función o se externaliza. Caracterizar exige explicar entradas, decisiones, salidas y relaciones, no solo dibujar cajas.

Por ejemplo, soporte recoge «tres personas creen ser responsables del mismo aviso». Coordinación analiza el proceso; producto plantea una respuesta; ingeniería comprueba límites; administración valora contratación; la organización usuaria valida si se redujo el problema. Este recorrido muestra qué información debe pasar entre funciones.

## 3. Hecho, inferencia, hipótesis y decisión

Una fuente es el origen identificable de información. Una evidencia es la parte concreta que permite sostener una afirmación. Un enlace a la portada de un repositorio no demuestra que una tarjeta persista; un resultado de prueba situado en un SHA sí puede aportar evidencia, con el límite de lo que esa prueba cubre.

| Categoría | Formulación correcta | Comprobación |
|---|---|---|
| Hecho | «En el registro R2, después del segundo arranque, reaparecen las mismas tres tarjetas» | abrir R2 y ver pasos, entorno y resultado |
| Inferencia | «El proceso conserva esos datos fuera de su memoria» | seguir archivo de BD, configuración y prueba |
| Hipótesis | «Con dos personas trabajando a la vez podríamos necesitar reglas de colaboración» | contrastar con usuarios y diseño actual |
| Decisión provisional | «Conservaremos la semántica de las tarjetas al evolucionar» | justificar necesidad, coste de perderla y dudas |

Una inferencia razonable no debe presentarse como observación. Tampoco basta añadir «creemos» a una afirmación sin fundamento. Escribe qué dato la apoya y qué dato podría refutarla. Una entrevista simulada es material de caso, nunca evidencia de que se entrevistó a una empresa.

Las estadísticas requieren fecha, población y variable. Si un estudio trata empresas de diez o más personas, sus resultados no se trasladan automáticamente a microempresas ni centros educativos. Si mide uso de nube, no mide disposición a pagar por AulaFlow. El [bloque sectorial](04_SECTOR_NECESIDADES_PI1.md) muestra cómo conservar esa distancia.

## 4. De una petición a una necesidad

Una necesidad describe una dificultad u objetivo de un actor en un contexto. Una función describe una respuesta posible. «Necesitamos Flutter» nombra una tecnología; «el personal necesita consultar el estado de un aviso durante un desplazamiento» nombra una necesidad. La primera puede ser una restricción curricular anual, pero por sí sola no prueba demanda.

Para analizar una petición escribe: actor, tarea, dificultad observable, consecuencia, frecuencia o recurrencia disponible y evidencia. Pregunta cómo se resuelve hoy, quién sufre el problema y quién decide cambiar. Una preferencia aislada puede ser relevante, pero no es automáticamente la necesidad más demandada.

En un caso acotado puedes contar incidencias por categoría y contrastar su impacto. Tres avisos perdidos y una preferencia de color no tienen el mismo significado. No asignes porcentajes de mercado a una muestra artificial. La priorización se argumenta con recurrencia, perjuicio y relación con el producto, sin inventar precisión.

## 5. Oportunidad y propuesta de valor

Una oportunidad de negocio es una posibilidad razonada de ofrecer valor sostenible a un segmento. Contiene una necesidad, una respuesta plausible, un beneficiario, una forma posible de obtener recursos y evidencia pendiente. En una organización pública también puede haber oportunidad de mejora de servicio sin venta: distingue esa mejora de una oportunidad comercial del proveedor.

«Hay muchas empresas, por tanto venderemos» no analiza oportunidad. Compara alternativas reales del caso: mantener el proceso, adoptar una herramienta existente, mejorar la organización sin software o evolucionar el legado. Considera barreras de adopción, formación, mantenimiento, confianza y quién pagaría. Aquí no calculamos un plan financiero ni viabilidad técnica formal: dejamos hipótesis y preguntas para el diseño posterior.

**Ejemplo:** la consultora podría ofrecer implantación y soporte a organizaciones que no pueden mantener su tablero. Esto solo es oportunidad si dichas organizaciones necesitan el servicio y aceptarían su coste y condiciones. Que el software sea útil al alumnado no demuestra un mercado. Una conclusión «la mejora es útil, la venta no está validada» puede ser excelente análisis.

## 6. Tipo de proyecto y características

El tipo de proyecto describe la clase de intervención necesaria: evolución de un sistema, integración con otro, migración controlada, mejora de proceso, nuevo producto o combinación acotada. En AulaFlow partimos de evolución e integración de un legado. No elegimos construir de cero solo porque no conocemos el código existente.

Una característica es una propiedad requerida que se deriva de una necesidad. Puede ser funcional (compartir un estado autorizado), de uso (acceso comprensible en contextos distintos), de información (conservar datos al evolucionar), operativa (recuperarse de una pérdida) o de restricción (usar solo datos ficticios en el laboratorio).

| Cadena de razonamiento | Resultado provisional |
|---|---|
| Dos funciones necesitan ver el mismo estado → el legado organiza tableros personales | estudiar colaboración con identidades diferenciadas |
| El equipo cambia de dispositivo → una captura no es información actual | estudiar acceso a datos comunes desde distintos clientes |
| Existe información previa → su pérdida impediría continuidad | estudiar conservación y conversión verificable de datos |
| No hay evidencia de trabajo sin conexión → se desconoce necesidad offline | pregunta abierta; no comprometer esa función |

Estas son relaciones de análisis. No son un catálogo contratado, endpoints nuevos, criterios de aceptación finales ni tareas valoradas en AulaTokens. La obligación curricular del proyecto anual y la necesidad de un segmento se documentan separadamente; una no se fabrica para justificar la otra.

## 7. Leer el sistema por responsabilidades

Una arquitectura de alto nivel permite orientarse. **Entrada/composición** reúne configuración y componentes. **Presentación/HTTP** transforma peticiones en operaciones y devuelve resultados. **Aplicación** coordina el caso de uso. **Dominio** expresa conceptos y reglas del problema. **Infraestructura** realiza detalles como base de datos, reloj o servidor. **Web** presenta información y recoge acciones. Las pruebas ofrecen ejemplos ejecutables de comportamientos esperados.

No confundas el flujo de una petición con la dirección de dependencias entre paquetes. Un navegador envía HTTP, un manejador llama a un servicio y un repositorio lee SQLite; eso explica un recorrido. Para afirmar que una capa depende de otra revisa importaciones/constructores. No basta copiar el diagrama de una arquitectura ideal.

El mapa debe incluir autenticación/sesiones, migraciones, pruebas, empaquetado y documentación, además del flujo principal. Acompaña cada caja o fila con una ruta del tag y una responsabilidad en tus palabras. El mapa se considera útil si otra persona puede localizar un componente y seguir una operación; no por su decoración.

## 8. Decisiones históricas: por qué existe lo que observamos

Una PR relaciona un cambio con su revisión. Un ADR recoge una decisión y sus consecuencias. Una issue describe una necesidad o incidencia; no prueba que se resolviera. Un test muestra una condición comprobable; que exista no demuestra que haya pasado hoy. Un registro manual aporta un ensayo en un entorno y momento concretos.

Lee cada muestra con cinco preguntas: problema, decisión, alternativa descartada, evidencia y consecuencia. Comprueba si pertenece al tag. Una PR posterior puede ilustrar evolución, pero no define cómo debe verse la release congelada. Si un README dice «CI verde», identifica a qué commit se refería antes de reutilizar la afirmación.

Los seis tipos de muestra de PI1 son evolución funcional, persistencia/integridad, seguridad, pruebas/CI, operación y una incidencia/corrección. Un mismo documento puede aportar dos perspectivas, pero cada fila debe explicar qué evidencia distinta analiza. No se pide leer todo el historial.

## 9. Conservar, migrar, sustituir o descartar

| Decisión | Qué significa | Prueba de una justificación suficiente |
|---|---|---|
| CONSERVAR | mantener capacidad, regla o semántica valiosa | qué necesidad sigue atendiendo y cómo comprobar que no se perdió |
| MIGRAR | trasladar datos o capacidad a otro contexto manteniendo significado | qué debe preservarse, qué transformación se anticipa y qué se desconoce |
| SUSTITUIR | reemplazar un mecanismo por otro que cubra la necesidad | límite del mecanismo actual, condición que exige cambio y riesgo |
| DESCARTAR | no trasladar un elemento al destino considerado | por qué carece de utilidad allí y qué consecuencia tendría retirarlo |

Precisa el objeto. Puedes conservar el concepto de tablero y sustituir su mecanismo de autorización. No son decisiones contradictorias porque actúan sobre objetos distintos. «Migrar SQLite» es impreciso: ¿datos, esquema, motor, repositorio o instalación? «Descartar contraseñas» tampoco especifica si se refiere a eliminar una función de seguridad o a no trasladar secretos de laboratorio.

La matriz termina con motivo, evidencia actual, dependencia, duda y necesidad relacionada. Las cuatro categorías deben comprenderse; no hay que inventar un elemento que descartar si ninguna decisión resulta defendible. En ese caso explica por qué no procede y qué evidencia permitiría revisarlo. Nunca ejecutamos eliminaciones o migraciones durante PI1.

## 10. Capacidad, deuda, limitación, preferencia y riesgo

Una capacidad es algo que el producto hace. Una limitación deliberada es una frontera documentada de su versión. La deuda es una carencia o decisión que genera coste de mantenimiento demostrable; no equivale a usar una tecnología que no te gusta. Una preferencia estética es una valoración de apariencia. Un riesgo de evolución es una incertidumbre con consecuencia posible.

Ejemplos de razonamiento: ausencia documentada de colaboración en 1.0 es limitación; pérdida de significado de datos durante una futura conversión es riesgo; una discrepancia entre dos fuentes de versión puede ser deuda de coherencia si se confirma; «prefiero otro color» sigue siendo preferencia hasta mostrar un problema de uso. SQLite no es deuda por definición y una prueba de reinicio no garantiza recuperación frente a pérdida física del disco.

No elaboramos la matriz formal de riesgos de PI3. Basta una observación concreta, evidencia, consecuencia posible y pregunta por resolver.

## 11. Condicionantes y ayudas

Las obligaciones no se deducen del nombre de la app. Dependen de quién realiza una actividad, dónde y bajo qué relación. El equipo de estudiantes que ensaya con datos ficticios no se convierte en sociedad mercantil. Una SL que vende soporte, una organización que contrata personal y un centro público no tienen el mismo encaje.

Para cada obligación concreta identifica sujeto, hecho activador, fuente oficial y efecto en el proyecto. «Cumplir todas las leyes» no aplica nada. Para una ayuda identifica organismo, programa/convocatoria, beneficiario, objeto, territorio, plazo y condiciones; una ficha histórica o una fase de justificación no significa convocatoria abierta. La respuesta «no confirmamos ayuda aplicable» es válida si conserva el rastro de búsqueda y la razón. El [bloque de condicionantes](05_CONDICIONANTES_Y_AYUDAS_PI1.md) contiene el procedimiento y fuentes actuales, sin exigir asesoramiento jurídico al alumnado.

## 12. Guion inicial, evidencia individual y salida

El guion organiza preguntas y bloques lógicos: comprender, contrastar necesidad, definir producto, contratar alcance, planificar, ejecutar, validar y entregar. Para cada bloque indica qué decisión debe llegar resuelta y qué evidencia permitiría avanzar. No asigna semanas, responsables de tareas futuras, costes ni una arquitectura definitiva.

La conclusión del dossier debe ser defendible por cualquier integrante. Escribe una aportación individual breve por cada criterio, enlazada a una evidencia común; no basta firmar un trabajo de equipo. En la defensa podrás consultar una fuente y explicar por qué cambia tu decisión si cambia el escenario. Aprender incluye reconocer un límite, corregir una inferencia y conservar la evidencia de esa revisión.

---

[Índice de PI1](../README.md) · [Inicio del módulo](../../README.md)
