# Ejemplos guiados · PI4

Todos los identificadores y hechos de esta página son TRAIN. Son modelos didácticos resueltos, no historia de AulaFlow ni aprobación real. No incluyen AT. Realiza los ejemplos dentro de los bloques de la ruta, no como tiempo añadido.

## Ejemplo 1 · Una tarjeta que todavía no puede salir

**Entrada:** TRAIN-EJ-01 prepara un procedimiento de reserva. PERSONA-A lo marca DONE_TECH porque subió un documento. El criterio indica que otra persona debe poder ejecutar los cinco pasos y reconocer un rechazo. La evidencia adjunta contiene solo una captura de título.

**Paso 1.** Separa salida de evidencia: el documento puede existir, pero no se ha demostrado su usabilidad. **Paso 2.** Revisa la condición de transición: necesita revisión contra criterio. **Paso 3.** Devuelve a ACTIVE manteniendo el comentario: «Falta ejecutar el recorrido con entrada válida y rechazo, e indicar versión». **Paso 4.** La autora añade dos registros; PERSONA-B los revisa y registra coincidencia. **Paso 5.** Pasa a DONE_TECH con esa referencia.

**Resultado esperado:** el historial contiene la primera declaración, la devolución y la comprobación posterior. El estado contractual continúa fuera de este ejemplo. **Comprueba:** si se modifica el documento después, ¿la revisión anterior cubre la nueva versión? No; debe identificarse el corte nuevo y repetirse lo afectado.

## Ejemplo 2 · Incidencia, mitigación y reapertura

**Entrada:** TRAIN-EJ-02 bloquea una demo porque falta el servicio de prueba. No hay datos reales. El criterio de integración exige una respuesta del servicio compartido.

Registro: síntoma «no se puede obtener respuesta», corte «paquete TRAIN-v1», impacto «no puede comprobarse frontera compartida», causa «TBD», responsable de coordinación PERSONA-C. La alternativa de ensayar con respuesta simulada permite revisar la navegación, pero no cumplir el criterio de integración. La decisión ficticia conserva dos estados: ensayo local COMPLETADO_TRAIN, integración PENDIENTE_ENTORNO.

Cuando vuelve el servicio, se ejecuta el recorrido acordado y se guarda respuesta saneada con versión. Si el resultado difiere del contrato de ejemplo, la incidencia sigue abierta y se coordina el defecto; no basta con que haya respuesta. El cierre incluye responsable, resultado observado y limitaciones. No se presenta una ejecución de este ejemplo como una prueba de red real.

## Ejemplo 3 · Capacidad que no cuenta dos veces

**Entrada:** tres personas declaran 6, 4 y 3 h disponibles para un ciclo hipotético. Se reservan respectivamente 1, 1 y 0,5 h para contingencia. La capacidad comprometible es 5 + 3 + 2,5 = 10,5 h-persona. Dos actividades requieren 5 y 4 h y la revisión compartida 2 h. Total 11 h: no cabe.

Una propuesta es comprometer solo la primera actividad y una parte coherente de la segunda, con criterio de salida específico y revisión incluida. Otra es retrasar la segunda entera. No se «arregla» la cuenta multiplicando 10,5 por tres ni quitando revisión. Si ambas personas dedican una hora a una revisión, consume dos horas-persona aunque transcurra una hora de reloj. El cambio de capacidad se documenta sin exponer su motivo privado.

## Ejemplo 4 · Coste y decisión de cambio

**Entrada:** usa los datos de economía de la teoría: baseline total 481,80 €, incurrido 447 €, restante 141 €, reserva restante 14,10 €, previsión 602,10 €. Son cifras didácticas.

Se detecta que una actividad opcional pendiente consume 3 h de A a 18 €/h. Posponerla ahorra 54 € de trabajo futuro, pero requiere 1 h de B a 15 €/h para separar el entregable. Ahorro neto directo = 39 €. Nuevo ETC = 102 €; nueva reserva, según la regla del caso, 10,20 €; previsión = 447 + 102 + 10,20 = 559,20 €. Sigue por encima de 481,80 € en 77,40 €.

**Decisión:** no afirmar que la alternativa devuelve el proyecto al presupuesto. Presenta ambas previsiones y solicita decisión del rol autorizado. La actividad opcional solo se retira del contrato real con CR aprobado. El coste incurrido no desaparece por posponer trabajo. La revisión económica aporta RA3.g; no modifica valores de AT.

## Ejemplo 5 · Dos versiones sin reescribir la historia

**Entrada:** TRAIN-B1 compromete una salida en D6. En D4 se descubre una dependencia; el análisis propone D8. Una decisión ficticia TRAIN-DEC-02 en D5 aprueba la nueva vigencia desde D6.

Conserva TRAIN-B1 y el desvío observado D4. Crea TRAIN-B2 con referencia al cambio, decisión D5 y vigencia D6. No cambies el documento inicial para que parezca que siempre decía D8. Lo completado antes de D6 se contrasta contra B1; lo posterior, contra B2 cuando le afecte. Si la aprobación real no existe, B2 permanece propuesta. Una fecha escrita por el equipo no es aprobación docente.

## Transferencia

Antes del laboratorio, escoge un ejemplo y explica qué parte cambia al pasar a REAL: fuente contractual, referencias de tareas, actores autorizados y evidencia observada. El procedimiento puede reutilizarse; los hechos sintéticos no. Conserva dudas en E01/E10 en vez de rellenarlas por semejanza.
