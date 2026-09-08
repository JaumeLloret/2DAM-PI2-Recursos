# Ejemplos y entrenamiento integrados

Estos ejercicios se resuelven dentro de los tiempos de las fases 2–5 y 7–8. Sus resultados alimentan las tablas del dossier; no constituyen tareas adicionales ni nueve entregas nuevas.

## Ejemplo 1 · convertir una petición en análisis

**Mini caso inventado para modelar, diferente de la evidencia evaluable:** una biblioteca vecinal entrega material con una hoja que solo consulta una persona. Dos voluntarios dicen que no saben si un préstamo está devuelto.

1. Petición: «queremos una app móvil».
2. Necesidad reformulada: «quien atiende el servicio necesita conocer el estado actual de un préstamo cuando la otra persona no está».
3. Evidencia disponible: dos testimonios simulados del mini caso, sin observación real ni dato de frecuencia.
4. Inferencia: el acceso a un estado común podría reducir incertidumbre.
5. Alternativa: corregir el proceso de registro y consultar una fuente compartida ya existente.
6. Oportunidad provisional: servicio de implantación/mantenimiento si la organización lo necesita y puede sostenerlo.
7. Pregunta pendiente: ¿los voluntarios registran siempre el cambio o el problema es de hábito de trabajo?

**Resultado esperado:** una cadena que no confunde tecnología, necesidad ni promesa de negocio. No hay evidencia suficiente para cerrar funcionalidades o ventas.

## Ejemplo 2 · una lectura reproducible de identidad

Abre el repositorio autorizado en el tag. Ejecuta `git rev-parse HEAD`, localiza versión en `pom.xml` y abre `docs/release/1.0.0.md`. Escribe dónde está cada evidencia. Ahora formula una regla: una captura visual de `main` no identifica una release congelada.

**Resultado esperado:** un registro con tres referencias compatibles a la versión seleccionada. Si aparece una discrepancia, anota fuente, valor y pregunta; no sustituyas el dato observado por lo que «debería» decir. Esta actividad pertenece a los 10 min de baseline de fase 4.

## Ejemplo 3 · transferencia de una decisión

Mini caso inventado: un archivo guarda solicitudes cerradas de un grupo que desaparece. El nuevo servicio necesita el historial, pero no las cuentas de prueba.

Puede **conservarse** la semántica de solicitud cerrada, **migrarse** información necesaria del historial, **sustituirse** el mecanismo de acceso si cambia el contexto y **descartarse** la cuenta ficticia en el destino sin borrar el histórico. Son objetos distintos. Debe comprobarse qué significa cada dato y con qué autorización se conserva; la tabla no ejecuta esas acciones.

**Resultado esperado:** cuatro decisiones que especifican objeto y razón, no cuatro etiquetas intercambiables. En AulaFlow deberás justificar tus propias decisiones con el legado real.

## Gimnasio graduado

### T1 · distinguir y clasificar · fase 2

Lee: «una consultora adapta software para clientes» y «un centro usa ese software para organizarse». Aplica los mismos ejes de actividad, servicio, prestación y función. Después añade la microempresa del caso. Incorpora las filas a E05.

Pista: comprador/usuario/proveedor pueden ser sujetos diferentes. Autocomprobación: si todas las filas dicen «empresa TIC que programa», revisa la actividad principal. No deduzcas una estructura empresarial completa a partir de una forma jurídica.

### T2 · seguir una función · fase 2

Toma el aviso C02 del caso: identifica quién lo recibe, quién decide, quién actúa y quién comprueba el resultado. Explica qué información pierde el proceso si dos funciones no comparten estado. Incorpora esa relación al organigrama/tablas, no al backlog.

Pista: función no significa necesariamente departamento independiente. Criterio de salida: puedes contar el recorrido sin usar «todos hacen todo».

### T3 · graduar una afirmación · 10 min de entrenamiento de fase 3

Clasifica y reescribe: a) «como muchas empresas usan nube, comprarán nuestra app»; b) «C01 y C03 contienen un problema de estado compartido»; c) «el móvil resolverá toda la coordinación»; d) «si cambia la persona responsable, hay que comprobar qué datos necesita consultar».

Comprueba: a) inferencia comercial no sustentada; b) afirmación contrastable dentro del caso; c) hipótesis excesiva; d) pregunta razonada de análisis. Escribe una refutación posible de tu hipótesis más importante y úsala en E06. No obtienes puntos por marcar letras: importa la corrección razonada.

### T4 · observar sin programar · fase 4

Sigue [la guía de G0](03_AUDITORIA_LEGADO_PI1.md). Antes de reiniciar escribe qué esperas que permanezca y qué podría perderse. Después contrasta el resultado con rutas de almacenamiento/sesiones. Tu predicción inicial no se borra; se corrige si procede.

Pista: registra base y directorio, no solo puerto. Criterio de salida: no confundes reinicio, sesión, persistencia ni backup. Si no pudiste ejecutar, marca la evidencia pendiente.

### T5 · leer una prueba · fase 5, tramo de mapa/historia

Localiza `RestartRecoveryIntegrationTest`. Busca el método que compara el segundo ciclo con el primero. Describe en tres frases: preparación, acción y afirmación. Indica una cosa que esa prueba **no** demuestra, como recuperación ante pérdida del soporte físico.

Pista: busca `@Test`, `verifySecondCycle` y las aserciones. No traduzcas línea a línea. Criterio de salida: explicas un comportamiento y el límite del ensayo, sin afirmar que pasó en tu equipo si solo lo leíste.

### T6 · historia y decisión · fase 5

Completa las seis familias de la tabla de la guía. Escribe una razón por la que CI de un commit anterior no certifica tu revisión. Después clasifica seis objetos del legado C/M/S/D. Para una fila cambia la necesidad del escenario y decide si mantendrías la clasificación.

Pista: un mecanismo y la semántica que implementa pueden recibir decisiones diferentes. Criterio de salida: cada fila tiene una ruta/evidencia y una necesidad, no solo preferencia de stack.

### T7 · aplicar una fuente · fase 7

Abre una ficha de obligación y compara SL con personal, primera contratación y equipo académico sin actividad comercial. Abre DIGITALIZA y localiza solicitud, ejecución y justificación. ¿Qué fecha responde a «puedo solicitarla ahora»?

Pista: una página accesible puede describir un plazo terminado. Criterio de salida: sujeto y condición explícitos, sin cuantías inventadas ni confundir candidatura con concesión.

### T8 · cerrar sin contratar · fase 8

Convierte «semana 3, persona X, 12 horas, implementar endpoint Y» en una pregunta y validación de alto nivel para el guion inicial. Revisa que tu transición conserve significado de datos y declare incertidumbre.

Autocomprobación: si tu documento ya compromete tareas, AT, arquitectura o fechas de sprints, has adelantado decisiones de PI2/PI3. Recupera el nivel de pregunta/bloque lógico y mantén la evidencia disponible.

---

[Índice de PI1](../README.md) · [Inicio del módulo](../../README.md)
