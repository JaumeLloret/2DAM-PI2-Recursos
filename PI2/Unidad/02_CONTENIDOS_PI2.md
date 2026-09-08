# Teoría de PI2 · Del análisis al compromiso
## 1. Qué cambia respecto de PI1
PI1 describe contexto, necesidad y legado. PI2 decide qué resultados se pueden comprometer y cómo reconocerlos. No se empieza de cero: una observación G0, una necesidad del contexto y una clasificación C/M/S/D deben tener consecuencias en el nuevo alcance.

Ejemplo: «El equipo observó una discrepancia de versión en la revisión del legado» es un hecho si existe evidencia localizable. «La evolución deberá hacer identificable su versión» es una propuesta. «El criterio exige una referencia de versión comprobable en la evidencia futura» es una condición de aceptación. Ninguna de esas frases prueba que el cambio ya se haya implementado.

El merge de una unidad docente certifica integración de materiales; no certifica G0 de cada estudiante. Se conserva la duda o recuperación cuando falte evidencia.

## 2. Cadena de decisión
**Necesidad → objetivo → alcance → especificación → tarea auténtica → aceptación → evidencia.**
La viabilidad explica bajo qué condiciones puede cumplirse; financiación identifica pagos/coberturas necesarios; documentación permite interpretar la propuesta; calidad señala qué controlar.

| Concepto | Pregunta | Error frecuente |
|---|---|---|
| Necesidad | ¿Qué problema importa y a quién? | Una preferencia estética sin evidencia |
| Objetivo | ¿Qué mejora observable se busca? | Nombre de tecnología |
| Especificación | ¿Qué comportamiento se describe? | Suponer que cada frase suma AT |
| Tarea contractual | ¿Qué entregable del catálogo se selecciona? | Inventar ID/valor |
| Aceptación | ¿Qué resultado demostraría cumplimiento? | «Funciona bien» |
| Evidencia | ¿Qué permite comprobarlo y con qué límites? | Captura sin contexto |
| Control de calidad | ¿Qué aspecto debemos vigilar? | Afirmar que ya se probó |

Una especificación puede agrupar varias tareas; una tarea puede apoyar varios objetivos sin contarse varias veces. Los códigos E01–E12 son evidencias documentales locales, no tareas ni AT.

## 3. Recopilar información con límites
Anota título/ruta/URL, versión, consulta, afirmación apoyada y límite. Distingue fuente primaria, observación propia y supuesto. Un dato técnico necesita documentación oficial pertinente; disponibilidad local necesita comprobación del entorno autorizado.

Una respuesta de IA puede sugerir dónde buscar, pero no sustituye el documento. Abre la fuente, contrasta y corrige antes de usarla. Cuando dos fuentes contradicen, aplica jerarquía: fuente canónica vigente prevalece sobre borrador histórico; registra qué decisión cambia. En este curso prevalece baseline contractual v1.0, que adopta artefactos v0.4 sin reabrir IDs/AT.

## 4. Contrato como acuerdo verificable
El contrato académico hace explícitos objeto, alcance, condiciones, aceptación y cambios. No es solo una lista de funcionalidades: permite a equipo/docente decidir qué compromiso existe y qué falta demostrar. Tiene dos capas: contrato corto y anexo auténtico de tareas.

Una propuesta se puede revisar antes de confirmar. Después de confirmar baseline, un cambio requiere CR prospectivo: motivo, impacto, propuesta, aprobación y revisión efectiva. No cambiar silenciosamente el pasado. La aprobación docente de un documento no acepta por adelantado una implementación.

El XLSX contractual auténtico ha sido recuperado y cotejado por el docente; se distribuye por el canal autorizado del curso. Si aún no lo has recibido, no puedes reconstruir filas desde descripciones funcionales. E05 conserva PENDIENTE_CATALOGO, filas vacías y totales desconocidos. Continúa el resto de la propuesta; la unión con tareas/AT se verifica al distribuir el libro.

## 5. AulaTokens: alcance aceptado
El baseline v1.0 declara 264 tareas / 572 AT de oferta / 96 tareas obligatorias / 150 AT obligatorios. IDs/AT congelados. Solo ACEPTADA valida AT. La cantidad contratada, realizada o con PR verde no sustituye aceptación.

La media de equipo y la contribución personal son distintas: AT_equipo = aceptados equipo / tamaño real; AT_efectivo = 0,40·AT_equipo + 0,60·AT_personal. El techo limita la nota curricular; no la aumenta. El detalle y ejemplos están en [baseline/AT](03_BASELINE_Y_AULATOKENS_PI2.md).

Una tarea no entrega su valor completo a cada colaborador. Se preserva atribución y aceptación histórica; el reparto operativo prospectivo se concreta en PI3. Las puertas valen 0 AT y tienen criterios propios.

## 6. Objetivos y alcance
Un objetivo expresa beneficiario, mejora y resultado observable. «Usar una base de datos moderna» no dice qué mejora; «permitir que el personal autorizado localice el préstamo vigente sin contradicciones» sí.

IN declara resultados incluidos. OUT declara exclusiones con razón. OUT no puede borrar una obligación. Un supuesto relevante se convierte en condición explícita, no se oculta en letra pequeña. La selección de opciones se justifica por necesidad y viabilidad; no se persigue simplemente consumir todos los AT ofrecidos.

El alcance contractual no es planificación. Personas/horas, recursos detallados, secuencia por sprints, riesgos formales y arquitectura global permanecen PENDIENTE_PI3.

## 7. Viabilidad
Viabilidad no significa «la tecnología existe». Pregunta si este alcance puede comprometerse en las condiciones conocidas. Estados: VIABLE, VIABLE_CON_CONDICION, NO_DEMOSTRADO, NO_VIABLE. La ausencia de prueba no demuestra imposibilidad.

Método: pregunta acotada → hechos → dependencia/supuesto → alternativa → dictamen → condición y efecto contractual. Ejemplo: una API documentada sin acceso local confirmado no permite garantizar una integración. El estudio identifica qué observación resolvería la duda y qué opción se mantendría fuera o condicionada.

No transformar el estudio en curso de arquitectura global o tutorial de otro módulo. La disponibilidad de una competencia se comprueba; no se presupone que otro profesor entregará a tiempo una funcionalidad.

## 8. Financiación
Necesidad, coste, caja y cobertura son conceptos distintos. Un medio cedido puede evitar compra adicional, pero requiere confirmación de disponibilidad. Un pago recurrente se multiplica por un periodo económico explícito; ese periodo no es una planificación de sprints.

Con importes comparables: financiación adicional = max(0, necesidad de caja − cobertura confirmada). Si falta un importe imprescindible, solo hay subtotal conocido, no total definitivo. Una ayuda solicitada no equivale a concedida. No convertir AT en euros/horas ni repetir el análisis fiscal de PI1.

Ejemplo ficticio: alta 15 + alojamiento 5×2 + reserva 5 = 30; cobertura confirmada 12; déficit 18. Una promesa no confirmada de 10 no lo reduce. No son precios actuales de mercado.

## 9. Diseñar documentación útil
RA2.h exige definir y elaborar. Un mapa de futuros documentos no basta: el paquete debe contener dos fichas funcionales desarrolladas. Cada ficha explica objetivo, actor funcional, precondición, entrada/salida, recorrido, excepción, aceptación, fundamento y control.

No hace falta imponer tablas, endpoints o widgets. El diseño inicial debe permitir entender el comportamiento sin invadir arquitectura global. La revisión documental enlaza fuentes, alcance y aceptación; no reparte personas/tiempos.

## 10. Calidad y aceptación
Aceptación pregunta qué resultado permite aceptar una prestación. Calidad prevista pregunta qué aspectos debemos controlar y con qué evidencia. «Seguro», «rápido» o «usable» son etiquetas; se convierten en escenario, observación y límite.

Ejemplo: ante una acción no autorizada, el sistema no confirma un cambio ni expone el contenido restringido; cuando exista ese flujo, se conservará una muestra saneada de permitido/denegado. Es un control previsto, no una prueba ya ejecutada. Las puertas técnicas requieren activación y condiciones canónicas.

## 11. Negociar sin borrar el compromiso
Una objeción puede revelar una necesidad, una condición o una preferencia. Antes de conceder, pregunta qué cambia en objetivo, IN/OUT, viabilidad, financiación, aceptación y documentación. Mantén núcleo e IDs/AT. Si la baseline ya está confirmada, tramita CR antes de cambiarla.

El acta conserva propuesta, objeción, concesión, razón, efectos y decisión pendiente/confirmada. No disimula una incompatibilidad con «lo veremos en un sprint».

## 12. Defender y transferir
Cada persona debe localizar una decisión, explicar su fuente, reconocer su límite y modificarla sin agente. Una buena defensa no recita todo el paquete: responde al hecho nuevo y propaga sus efectos. Se observa con E12, microcambio y explicación focalizada; el historial o la declaración de ayuda no bastan solos.

Primarios PI2: RA2.a,b,d,g,h,i. RA2 completo sigue pendiente de c,e,f en PI3. G1 puede tener componente contractual establecido tras confirmación real, pero permanece EN_PROGRESO hasta planificación. **Contrato/alcance no equivalen a planificación detallada.**

---

[Índice de PI2](../README.md) · [Inicio del módulo](../../README.md)
