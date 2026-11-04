# PI3 · convertir un acuerdo en un plan útil

Sigue un mismo ejemplo desde la necesidad de una persona usuaria hasta las tareas y el primer sprint. Primero distinguirás los conceptos; después redactarás historias con criterios, revisarás una propuesta de IA y comprobarás capacidad, dependencias y riesgos. Al terminar podrás trasladar el procedimiento a vuestro acuerdo de PI2. La práctica principal y los talleres están en «Prepara vuestro tablero y primer sprint».

## Qué significa planificar aquí

El acuerdo dice qué resultado se quiere y con qué condiciones. El plan dice en qué orden trabajaremos, con qué personas y medios, qué debe estar disponible y cómo sabremos que podemos continuar. No predice cada hora del curso: detalla lo próximo y deja una previsión revisable de lo lejano.

Un **requisito** expresa una capacidad o condición del producto. Una **tarea** es trabajo que alguien puede realizar para conseguirla. Un **hito** es un resultado con fecha de revisión. El **backlog** es el trabajo ordenado que queda por hacer. El **sprint** es un ciclo corto con objetivo, capacidad disponible y revisión final. Una tarea terminada no equivale necesariamente a un requisito aceptado.

## Historias de usuario: ordenar el trabajo por necesidades

Una **historia de usuario** expresa una necesidad desde la perspectiva de quien usa el producto y el valor que obtiene. Una forma de empezar es: **«Como [persona o perfil], quiero [capacidad], para [beneficio]»**. La frase abre una conversación: debe acompañarse de condiciones que permitan comprobarla.

Ejemplo: **«Como persona con acceso a un tablero, quiero consultar sus tarjetas para saber qué trabajo queda pendiente»**. «Crear una pantalla con una lista» es una posible tarea técnica; no explica por sí sola la necesidad. «Como desarrollador quiero crear una tabla» suele describir trabajo técnico: puede ser necesario, pero conviene vincularlo a la historia que ayuda a resolver.

El **backlog de historias** ordena necesidades y resultados por valor, obligación contractual, riesgo y dependencias. Para cada historia guarda título, necesidad, referencia al alcance auténtico, prioridad y motivo, criterios de aceptación y dudas. El **trabajo del sprint** concreta qué historias o partes coherentes abordaremos y qué tareas requieren. Puedes mantener ambas vistas en el mismo tablero: una tarjeta de historia con tareas enlazadas o una tabla con relación historia–tarea. No hace falta duplicar archivos.

Una historia pequeña permite demostrar un resultado útil. «Gestionar toda la aplicación» es demasiado grande. Se puede comenzar por consultar tarjetas, después realizar un cambio permitido y después comprobar su persistencia entre clientes, según prioridades y dependencias. Dividir no elimina las funciones obligatorias del contrato ni permite declarar una historia completa cuando solo está hecha su interfaz.

### Criterios de aceptación de una historia

Describen comportamiento observable y límites. El formato **«Dado…, cuando…, entonces…»** ayuda a concretarlos, aunque también sirve una lista de condiciones verificables. Para el ejemplo didáctico:

- Dado un tablero de prueba autorizado con dos tarjetas, cuando la persona autorizada lo consulta, entonces puede identificar ambas tarjetas.
- Dado un tablero autorizado sin tarjetas, cuando lo consulta, entonces entiende que no hay tarjetas; no se presenta el vacío como fallo de conexión.
- Dado un perfil que no tiene permiso, cuando intenta consultar, entonces no se expone la información restringida.

Son condiciones del ejemplo para aprender: en el proyecto se cotejan con el catálogo y acuerdo auténticos. No se inventa un permiso o se cambia el alcance sin autoridad. Los criterios de aceptación se refieren a la historia; la **definición de terminado** añade reglas comunes del equipo, como revisión, comprobación y evidencia enlazada.

### De la historia a una especificación y a las tareas con SDD

**SDD significa desarrollo dirigido por especificaciones (Spec-Driven Development).** La historia explica quién necesita qué y para qué. Una especificación concreta comportamiento, criterios de aceptación, límites, datos necesarios y dudas. El plan trata dependencias y decisiones; las tareas organizan el trabajo ejecutable. La cadena que usamos es: **acuerdo → historia → especificación aclarada → tareas → comprobación**. No exige crear cinco documentos para una función: puede vivir en la tarjeta y sus enlaces.

Las plantillas oficiales de GitHub Spec Kit utilizan historias priorizadas con escenarios de aceptación y organizan las tareas por historia. Es un ejemplo de SDD, no una regla universal de todas las herramientas ni una instalación obligatoria de esta unidad.

Un agente de IA puede proponer historias, preguntar por ambigüedades o sugerir tareas. **El equipo revisa esas propuestas y conserva la decisión.** Una historia bien redactada no garantiza una implementación correcta: hay que aclarar, contrastar el trabajo y comprobar los criterios. Si el agente cambia el alcance, inventa una capacidad o declara una prueba que nadie ha realizado, se corrige la propuesta.

Ejemplo de petición para aprender el procedimiento: «A partir de esta historia y de estas condiciones del acuerdo, señala las dudas, propone criterios observables y divide el trabajo en tareas pequeñas. Separa lo confirmado de lo pendiente. No inventes tecnologías, accesos, endpoints ni funciones. No implementes todavía». Se puede hacer el mismo ejercicio leyendo la propuesta didáctica inferior, sin cuenta de IA ni herramienta de pago.

### Ejercicio de revisión de una propuesta de IA

Propuesta didáctica: «Como usuario quiero una aplicación rápida y moderna. Tareas: hacer todo el frontend, crear una base de datos nueva y añadir notificaciones. Aceptación: todo funciona. Duración: un día». El acuerdo solo contempla en este punto consultar las tarjetas del servicio existente.

Identifica necesidad/beneficio imprecisos, criterio no comprobable, tareas demasiado grandes, capacidades añadidas y una duración sin disponibilidad ni dependencias. Reescribe una historia de consulta y tres criterios observables; conserva las dudas que no puedes resolver. Después propón tareas relacionadas con esos criterios. La pauta de comprobación es el ejemplo de consulta de este recurso: hay varias redacciones válidas, pero deben respetar el alcance y permitir observar un resultado.

Este ejercicio sustituye la clasificación básica del entrenamiento final: no es otra entrega ni aumenta las 15 horas.

## Ejemplo continuo · consulta de tarjetas en AulaFlow

Es un fragmento didáctico sin IDs ni AT contractuales. Tras comprenderlo, usa el resultado y referencias auténticos del equipo. No copies su selección de tareas como lista obligatoria.

**Resultado propuesto:** una persona autorizada puede consultar sus tarjetas desde el cliente previsto. **Comprobación prevista:** con dos tarjetas de prueba autorizadas, aparecen ambas; con un perfil sin permiso no se expone su información. El contrato anual conserva además los demás resultados obligatorios.

### 1. Ver el conjunto antes de repartir

| Componente | Responsabilidad | Información que intercambia | Estado a contrastar |
|---|---|---|---|
| Cliente móvil | Pedir y presentar las tarjetas; comunicar errores | Petición/respuesta del servicio | Capacidad real del equipo y versión disponible |
| Cliente de escritorio | Consultar el mismo tablero y respetar permisos | Mismo significado de datos | Capacidad real y contrato de integración |
| Servicio común | Autenticar, autorizar y responder | Identidad, tarjetas, estados y errores | Acceso y comportamiento comprobables |
| Persistencia | Conservar los datos autorizados | Estado consistente tras una nueva consulta | Responsable técnico y evidencia de disponibilidad |

La tabla ayuda a descubrir dependencias; no obliga a usar una tecnología nueva. Una flecha de un diagrama tampoco prueba que la integración funciona.

### 2. Dividir un resultado en tareas comprobables

| Tarea didáctica | Depende de | Medio/recurso | Se termina cuando |
|---|---|---|---|
| Confirmar consulta, formato y errores disponibles | Acceso al servicio | Documentación o consulta autorizada | Hay ejemplo de respuesta y límite conocido |
| Preparar dos tarjetas de prueba | Permiso de usar un entorno de prueba | Datos sintéticos y responsable del entorno | Se conoce su estado inicial y cómo restablecerlo |
| Realizar una consulta desde el cliente | Consulta y acceso disponibles | Cliente y entorno que ya domina el equipo | Hay respuesta identificada o error reproducible |
| Presentar las tarjetas y el estado de error | Respuesta conocida | Pantalla y datos autorizados | Se observa la lista y un fallo comprensible |
| Contrastar resultado y permiso | Versión de cliente y servicio accesibles | Caso de prueba definido | Queda evidencia de lo que cumple y lo que falta |

«Hacer frontend» es demasiado grande y no permite comprobar avance. «Mostrar las dos tarjetas de la respuesta autorizada y el estado vacío» permite explicarlo. Una tarea propia referencia su requisito auténtico; no crea un nuevo código o valor AT.

### 3. Ajustar trabajo a capacidad

Dos personas declaran 150 minutos cada una para un sprint didáctico: 300 minutos de capacidad conjunta. Las tareas propuestas estiman 60, 40, 80, 100 y 60: 340. Se reservan además 40 para revisión/contingencia, por lo que el trabajo planificable es 260. No cabe el conjunto.

El equipo acuerda empezar por confirmar consulta (60), datos (40), consulta desde cliente (80) y una primera presentación acotada (80). Suman 260. El contraste de permisos y el resto de interfaz se preparan para después. **Este recorte sirve para planificar, no para declarar aceptado el requisito completo.** Si solo hay una persona con acceso y está ausente al principio, se cambia el orden o se pide resolver acceso; 300 minutos totales no eliminan esa dependencia.

Las cifras son del ejercicio, no horas obligatorias ni AT del catálogo. En tu proyecto usa disponibilidad y estimaciones propias, ajustadas a la carga de la ruta.

### 4. Preparar permiso, procedimiento y riesgo

**Permiso:** usar el entorno de pruebas; lo confirma su responsable. Hasta confirmación se usan respuestas sintéticas para aprender el formato; la integración real queda pendiente. No usar credenciales de otra persona.

**Procedimiento de una tarea:** leer requisito y criterio; aclarar duda; trabajar en una rama si se modifica código; comprobar resultado; pedir revisión proporcional; registrar versión/evidencia y mover el estado. Es la secuencia especificación–aclaración–plan–tarea–comprobación, sin redactar un documento distinto para cada paso. Una tarea documental puede revisarse con un diff y una explicación en vez de compilar nada.

**Riesgo:** el acceso podría llegar después de la revisión. Se previene comprobándolo antes; la señal es no tener acceso confirmado al comienzo del sprint; la respuesta es practicar formato con datos sintéticos y reasignar una tarea independiente. El docente/responsable resuelve el acceso y el equipo deja fecha de nueva comprobación. La simulación no satisface una integración real exigida por el contrato.

Prevé también pérdida accidental de trabajo, permisos sobre datos, carga excesiva o un puesto de trabajo inadecuado: identifica efecto, prevención y medios disponibles sin redactar un catálogo de peligros ajenos al proyecto. «Riesgo alto» sin actuación no ayuda a ejecutar.

### 5. Fijar hitos y preparar el primer sprint

El 30/11 se revisa la planificación: no se exige aplicación terminada. El equipo prepara objetivo, duración elegida, tareas priorizadas, responsables, capacidad, dependencias y prueba del resultado. Conserva una previsión de ejecución hasta PI4, validación PI5 y cierre PI6. Las tareas futuras pueden tener menos detalle; no se oculta una dependencia crítica con «ya se hará».

En la revisión se muestra qué ha cambiado respecto al plan y por qué. Con un dato nuevo se actualiza la previsión y se conserva la anterior. Replanificar no significa cambiar unilateralmente el contrato o la entrega docente.

## Practica antes de trasladarlo

1. Básico: revisa la propuesta de IA anterior, redacta la historia y relaciona sus criterios con tareas concretas. Distingue historia, tarea e hito usando el mismo ejemplo.
2. Intermedio: vuelve al presupuesto de 300 minutos. Propón otra selección que quepa en 260 y diga qué resultado parcial puede observarse y qué no.
3. Aplicación: el acceso llega dos días tarde. Propón una tarea que sí puede avanzar, una que permanece bloqueada y una pregunta al responsable. Revisa orden, recursos, permisos y riesgo.

Comprueba tu razonamiento: no debería aparecer un requisito aceptado sin toda su evidencia ni una persona asignada a dos tareas simultáneas que ocupan toda su disponibilidad. El docente contrasta la solución; no hay una única descomposición válida.

## Referencias para ampliar

- [Plantilla oficial de especificaciones de GitHub Spec Kit](https://github.com/github/spec-kit/blob/main/templates/spec-template.md).
- [Plantilla oficial de tareas agrupadas por historia](https://github.com/github/spec-kit/blob/main/templates/tasks-template.md).
- [Recorrido oficial de SDD con Spec Kit](https://github.github.com/spec-kit/quickstart.html).

Son consulta opcional. El procedimiento necesario para esta unidad está explicado aquí; no se requiere instalar Spec Kit ni utilizar un agente de pago.
