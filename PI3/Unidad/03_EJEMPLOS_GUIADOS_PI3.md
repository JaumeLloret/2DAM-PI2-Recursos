# Ejemplos guiados · PI3

Todos los datos y claves de estos ejemplos son sintéticos `TRAIN-*`. Son ejemplos resueltos cortos, distintos de la solución completa de ReservaLab. Se leen dentro de las fases indicadas.

## 1. De una lista a un hito · fase 2

Entrada: un archivo debe ser autorizado, después leído y por último presentado al solicitante. Lista débil: «martes datos, miércoles interfaz, viernes terminado». La salida del viernes no se puede verificar y la autorización no está planificada.

Procedimiento:

1. Identifica resultado: el solicitante ve los tres registros de muestra autorizados.
2. Define `TRAIN-E1A` autorización de la muestra (1 día), `TRAIN-E1B` lectura contrastada (2 días), `TRAIN-E1C` presentación y revisión (1 día).
3. Explica FS A→B por disponibilidad legal/operativa de la entrada; FS B→C por coherencia del resultado.
4. Programa días ficticios 1, 2–3, 4; reserva día 5 para contingencia. Hito: tres registros coinciden y la persona revisora conserva evidencia de contraste.

Resultado: una cadena de cuatro días y un día de margen. Si A tarda dos días, B pasa a 3–4 y C a 5; el margen se consume. Si A tarda tres, hay que revisar el compromiso. Comprobación: ¿por qué no sirve dejar C en día 4? Su entrada ya no estaría disponible. No has cambiado el alcance ni creado otra tarea contractual.

## 2. Frontera arquitectónica · fase 4

Entrada: «dos clientes guardarán reservas; ya sincronizaremos». Faltan fuente de verdad, regla de conflicto y dependencia de integración.

Modelo corregido: cliente solicita una reserva al servicio común; el servicio decide si el intervalo está libre y devuelve confirmación o conflicto; el cliente muestra la decisión. El dataset es sintético. Contrato lógico: kit, intervalo y referencia de solicitante ficticia de entrada; referencia de reserva o motivo de conflicto de salida. No se define una API técnica ni algoritmo de bloqueo.

P03 registra servicio responsable de la decisión, clientes consumidores, información que cruza y muestra de dos solicitudes incompatibles. P10 registra disponibilidad del servicio y evidencia que habilita integrar. P11 mantiene `ASUMIDO` hasta contrastar la frontera. Resultado esperado: ninguna responsabilidad duplicada y una prueba observable prevista. No marques la frontera `CONFIRMADO` solo porque ambos dibujaron la misma flecha.

## 3. Capacidad frente a deseo · fase 8

Entrada: PERSONA-A declara 12 h, PERSONA-B 8 h. Reservan 2 h cada una. Trabajo previsto: preparar 4 h, revisar 2 h, integrar 6 h, documentar decisión 2 h y verificar salida 2 h: 16 h. Capacidad comprometible: 10+6=16 h.

Asignación razonada: A prepara 4, integra 6; B revisa 2, documenta 2, verifica 2. Hay equilibrio respecto a disponibilidad, aunque no tengan las mismas horas. Antes de integrar, B debe haber revisado: FS revisión→integración. Las reservas no son más tareas. Si la revisión ocupa también 1 h de A, el plan sube a 17 h y hay déficit de 1: hay que ajustar entrada, ventana o asignación; no esconder ese tiempo.

Resultado esperado: las sumas cierran y las dependencias permiten el orden. El ejemplo no autoriza convertir AT a horas. Revisa el supuesto de que B puede verificar la salida, y prevé apoyo si no tiene esa capacidad.

## 4. Riesgo y cambio prospectivo · fase 10

Entrada: entorno externo previsto para día 8, sin confirmación. Riesgo débil: «puede fallar el servidor; solución arreglarlo».

Versión útil: causa, acceso depende de autorización ajena; probabilidad media porque no hay confirmación; impacto alto sobre integración; prevención, solicitar y contrastar acceso antes de día 6; medios, responsable y ventana de comprobación incluidas; trigger, día 6 sin confirmación; contingencia, ensayo local con datos sintéticos y nueva ventana de integración real; responsable, PERSONA-B; estado abierto; revisión día 6.

Al llegar el trigger en una simulación, se guarda baseline 1, se compara mover la integración o cambiar entorno, se elige con motivo y se registra baseline 2. El ensayo local no acredita integración real ni despliegue. Si cambiar entorno altera alcance, el CR se decide antes de rebaselinar el contrato. Si solo cambia la ventana de una actividad, conserva los IDs/AT y registra revisión del plan. Seguimiento real sostenido: PI4.

---

[Índice de PI3](../README.md) · [Inicio del módulo](../../README.md)
