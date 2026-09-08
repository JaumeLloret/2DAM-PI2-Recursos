# Entrenamiento graduado · PI3

Estas 14 actividades usan tiempos incluidos en la ruta. A01 comparte sus 12 min con la lectura de entrada; no añade otros 12. Trabaja en el cuaderno. Las pistas siguientes permiten revisar sin publicar la solución completa del caso.

## A01 · Distinguir capas

**Fase 1 · 12 min · RA2.c, RA2.e.**

Entrada: Cuatro frases: «usuario cancela reserva», «preparación», «muestra aceptada», «revisar frontera».

Tarea: Clasifica requisito, fase, hito y actividad; añade a cada una la pregunta que responde.

Salida esperada: Cuatro filas y una duda PI2.

Autocomprobación: Un hito describe estado observable; no añadas tareas al contrato.

## A02 · Orden mínimo

**Fase 2 · 8 min · RA3.a.**

Entrada: TRAIN-X1 preparar muestra; X2 acordar frontera tras X1; X3 cliente tras X2; X4 contraste tras X3. Todos con prefijo TRAIN-.

Tarea: Dibuja precedencias y justifica dos flechas.

Salida esperada: Orden y grafo de cuatro nodos.

Autocomprobación: No hay ciclos; cada flecha explica una entrada necesaria.

## A03 · Hito observable

**Fase 2 · 7 min · RA2.c.**

Entrada: «TRAIN-H: acabar todo el viernes».

Tarea: Reescribe propósito, muestra de salida y ventana condicionada por una autorización.

Salida esperada: Hito con señal de preparación y cierre.

Autocomprobación: Otra persona puede decidir si se cumplió sin preguntar qué significa todo.

## A04 · Margen explícito

**Fase 2 · 10 min · RA2.c, RA3.f.**

Entrada: Cadena TRAIN-X1/X2/X3 de 1, 2 y 1 días; plazo día 4; autorización puede tardar 1 día más.

Tarea: Compara consumir margen inexistente, adelantar preparación autorizada o renegociar fecha.

Salida esperada: Dos alternativas, decisión y supuesto.

Autocomprobación: No prometas simultáneamente el plazo y una entrada todavía incierta.

## A05 · Frontera clara

**Fase 4 · 10 min · RA2.e, RA3.a.**

Entrada: Dos clientes de TRAIN escriben reservas independientes y el dibujo no tiene autoridad de conflicto.

Tarea: Asigna responsabilidad de decisión, entradas/salidas y muestra de integración sin código.

Salida esperada: Tabla de una frontera y efecto sobre dos actividades.

Autocomprobación: No exige implementar un backend para explicar la dependencia.

## A06 · Disponibilidad no equivale a adquisición

**Fase 4 · 10 min · RA3.a, RA3.c.**

Entrada: Capacidad móvil prevista el 10/11; no hay evidencia del equipo; se quiere integrar el 11/11.

Tarea: Separa fecha prevista, condición, evidencia, bloqueo y alternativa.

Salida esperada: Fila P10 y decisión P11.

Autocomprobación: El calendario no activa la puerta.

## A07 · Backlog bloqueado

**Fase 5 · 10 min · RA3.a.**

Entrada: En ReservaLab TRAIN-03 depende de TRAIN-02; el borrador pone cancelación antes de reserva.

Tarea: Corrige el orden y relaciona actividades, entrada y salida con los IDs sintéticos del caso.

Salida esperada: Fragmento P04 corregido.

Autocomprobación: El número de tareas contratadas no aumenta por descomponer actividades.

## A08 · Recurso y logística

**Fase 7 · 10 min · RA2.f, RA3.b.**

Entrada: Dos actividades TRAIN necesitan la única tablet de demo el mismo día; solo una franja de 2 h.

Tarea: Registra previsión general y reserva por actividad; propón alternativa que respete capacidad.

Salida esperada: P05 con disponibilidad, ubicación y plan B.

Autocomprobación: Cambiar de persona no crea otra tablet.

## A09 · Permiso ausente

**Fase 7 · 10 min · RA3.c.**

Entrada: Se quiere cargar un CSV con personas reales en un servicio externo. No hay autorización.

Tarea: Localiza solicitante/autorizador/plazo/evidencia; prepara alternativa con datos sintéticos.

Salida esperada: P06 y entrada bloqueada de la actividad.

Autocomprobación: No incluyas el CSV real ni credenciales en el paquete; NO_APLICA necesita motivo.

## A10 · Procedimiento accionable

**Fase 8 · 12 min · RA3.d.**

Entrada: Borrador: «programar, subir y poner done».

Tarea: Añade entrada, responsable, revisión, evidencia, aceptación y escalado cuando falle un control.

Salida esperada: Procedimiento P07 de seis pasos como máximo más regla de fallo.

Autocomprobación: Una PR fusionada no concede aceptación ni AT.

## A11 · Reasignar capacidad

**Fase 8 · 13 min · RA3.f.**

Entrada: PERSONA-A tiene 10 h netas y 12 h asignadas; PERSONA-B tiene 6 h netas y 4 h asignadas; revisión transferible de 2 h.

Tarea: Reasigna con condición de capacidad técnica y mantén precedente de integración; considera ausencia del backup.

Salida esperada: P08 antes/después y decisión.

Autocomprobación: Comprueba tanto suma como disponibilidad antes del hito.

## A12 · Riesgo con medios

**Fase 10 · 15 min · RA3.e.**

Entrada: Riesgo de único especialista; otro de permiso que podría retrasarse. No hay trigger ni medios.

Tarea: Razona prioridad, prevención, medios incluidos, trigger, contingencia viable y responsable.

Salida esperada: Dos filas P09 y referencia P08/P06.

Autocomprobación: La contingencia puede ejecutarse con los recursos del plan.

## A13 · Detectar falsa precisión

**Fase 5 · 10 min · RA3.a, RA3.f.**

Entrada: Un borrador afirma que 5 AT obligan a 5 horas, ajusta AT al retrasarse y convierte FE hipotética en fecha confirmada.

Tarea: Refuta las tres decisiones y registra alternativas prospectivas.

Salida esperada: Tres correcciones con motivo.

Autocomprobación: Ningún dato contractual se deriva de la estimación; FE sigue condicionada.

## A14 · Integrar y revisar

**Fase 11 · 15 min · RA2.c, RA2.e, RA2.f, RA3.a, RA3.b, RA3.c, RA3.d, RA3.e, RA3.f.**

Entrada: Capas TRAIN elaboradas durante las fases anteriores.

Tarea: Recorre un ID sintético desde P01 a P12 y detecta tres incoherencias cruzadas; integra la versión.

Salida esperada: Mini-baseline con referencias y registro de cambios.

Autocomprobación: No crear doce entregas: una misma decisión debe concordar en todos los componentes.

## Ensayo de fase 12 · 35 min antes de T4

Usa tu TRAIN integrado. Supón que una persona reduce 2 horas de disponibilidad, sin especificar cuál hasta que tú la elijas: 5 min localizar, 15 replanificar, 10 comparar y registrar, 5 preparar tu evidencia. Es un ensayo libre; I3 utilizará otra variante no publicada y otra condición. Conserva el antes y después. Los 15 min restantes de fase 12 se reservan para feedback y entrega después de T4.

---

[Índice de PI3](../README.md) · [Inicio del módulo](../../README.md)
