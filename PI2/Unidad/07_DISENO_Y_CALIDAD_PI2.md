# Documentación elaborada y calidad prevista
## Definir y elaborar
RA2.h contiene dos acciones. Definir: decidir qué documentación hace falta y para qué. Elaborar: producir contenido que permita comprender la propuesta. Un índice de documentos futuros no cumple ambas.

El paquete contiene briefing/fuentes, objetivos/alcance, contrato/anexo, aceptación, estudio, financiación, mapa y fichas, controles, decisiones y evidencia individual. Una revisión común y enlaces evitan copiar el mismo texto en doce sitios.

El diseño inicial de PI2 describe decisiones funcionales interpretables; no arquitectura global, API completa o implementación técnica de otros módulos.

## Mapa documental y ficha
Para cada documento: pregunta que resuelve, destinatario funcional, contenido mínimo, revisión/enlace y decisión que sostiene. Sin asignar autores, personas, horas o fechas de producción.

Elabora al menos **dos fichas funcionales distintas**:
1. Objetivo/escenario.
2. Actor funcional y precondiciones.
3. Información de entrada/salida.
4. Recorrido principal numerado.
5. Excepción y respuesta esperada.
6. Aceptación observable.
7. Decisión, fuente/supuesto y límite.
8. Control de calidad y referencia auténtica cuando exista catálogo.

No hace falta diagrama. Si lo usas, que explique un comportamiento y tenga texto equivalente, sin arquitectura global encubierta.

## Ejemplo elaborado: devolución de Archivo de barrio
Objetivo: cerrar préstamo conservando trazabilidad. Actor: personal autorizado. Precondición: préstamo abierto localizable. Entrada: referencia y confirmación de recepción. Salida: cierre, disponibilidad y registro autorizado.

Recorrido: 1) localizar préstamo; 2) mostrar qué se cerrará; 3) confirmar; 4) observar estado e historial. Excepción: ya cerrado; informar sin duplicar devolución ni borrar historial.

Aceptación: tras una devolución se observa cierre/disponibilidad; repetir no crea otro cierre y conserva el historial previo. Decisión: proteger trazabilidad frente a repetición, según necesidad ficticia. Control: muestra saneada antes/después y repetición cuando exista el flujo.

Describe comportamiento, sin imponer tablas, endpoints o librerías. En tu paquete desarrolla otra ficha distinta, no dos copias de esta.

## Aceptación frente a calidad
Aceptación: resultado observable que permite aceptar una prestación. Calidad prevista: aspectos que deben controlarse para confiar en el resultado. Relacionarlos no crea AT extra.

| Aspecto | Débil | Utilizable |
|---|---|---|
| Coherencia | «Va bien» | Observaciones compatibles de un cambio autorizado desde dos clientes |
| Autorización | «Seguro» | Perfil sin permiso no obtiene acción/contenido restringido |
| Conservación | «No perder datos» | Muestra conserva atributos definidos y explica excepciones |
| Trazabilidad | «Guardar logs» | Relacionar decisión, requisito y evidencia sin secretos |
| Acceso/usabilidad | «Intuitivo» | Acción crítica etiquetada y feedback sin depender solo del color |
| Error | «Sin fallos» | Entrada inválida informa causa sin confirmar resultado inexistente |

No declarar ejecutadas las pruebas por redactar controles. Su estado puede ser previsto y su exigibilidad depende de disponibilidad/activación.

## Especificación de un control
Aspecto → objetivo/ficha → escenario → resultado → evidencia suficiente → exigible cuando… → estado actual. La condición puede ser «cuando exista el flujo integrado»; no sprint, fecha o reparto de personas.

E10 tendrá seis controles pertinentes. Distinguir:
- documental revisable ahora: coherencia IN/OUT, fuentes, ausencia de doble conteo, catálogo auténtico;
- producto previsto: comportamiento compartido, autorización, conservación, acceso y error;
- puerta de madurez: según activación canónica, sin AT por puerta.

G0/G1/G6/G7 activas desde inicio en sus términos. G2–G5 requieren activación expresa, criterios observables, justificación curricular, competencia disponible y recuperación. PI2 no las declara todas superadas.

## Controles que se concretarán según disponibilidad
Sin impartir su implementación, considerar también:
| Aspecto | Qué controlar | Evidencia prevista y condición |
|---|---|---|
| Pruebas/análisis/build/CI | Que los controles acordados del producto sean reproducibles y coherentes con aceptación | Resultado localizable y revisión identificada cuando exista competencia y G3 esté activada |
| Configuración/secretos | Que la evidencia y configuración compartida no expongan credenciales | Revisión saneada conforme a criterios G5 cuando se active y pueda recuperarse |
| Documentación/demo | Que el comportamiento mostrado corresponda a la revisión y alcance declarados | Documentos/demostración identificados según exigibilidad G6, sin fingir release en PI2 |
| Incidencias/cambios | Que motivo, decisión, impacto y revisión sean trazables | Registro y CR prospectivo cuando corresponda, ligado a G7 |

Seleccionar controles pertinentes según disponibilidad/activación. No exige ejecutar pruebas, montar infraestructura ni entregar documentación operativa adicional durante PI2.

## Revisión previa a negociar
Recorre necesidad → objetivo → IN → tarea auténtica o pendiente → aceptación → ficha → control → evidencia. Si falta catálogo, conserva la unión pendiente; no inventes un ID.

Otra persona encuentra una contradicción con efecto: OUT niega objetivo; aceptación exige una opción excluida; condición omitida; coste desconocido tratado como cero; ficha solo con títulos. La persona autora decide, corrige y registra razón. Revisión entre iguales no sustituye confirmación docente o autenticidad individual.

---

[Índice de PI2](../README.md) · [Inicio del módulo](../../README.md)
