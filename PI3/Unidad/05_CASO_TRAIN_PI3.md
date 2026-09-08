# Caso TRAIN · ReservaLab, de PI2 al plan

**Ficción didáctica completa. No es el catálogo de AulaFlow.** Se conserva el significado de TRAIN-01…04 del caso PI2. Para este ensayo el cliente ficticio ya ha seleccionado inventario, reserva, cancelación e importación. Correo, exportación y estadísticas quedan OUT. No se negocia otra vez ni se puntúa alcance; no se convierten las UA de PI2 a horas.

## Encargo y datos de entrada

ReservaLab presta kits entre laboratorios. Necesita una consulta compartida, reservar sin conflictos, cancelar conservando historial e importar el pequeño inventario autorizado. El servicio común decide la reserva; el cliente consulta y presenta su resultado. Un rol de operador importa la muestra. No diseñes código, protocolo técnico completo ni base de datos.

Descarga la [entrada JSON](../Alumnado/Train/reservalab_entrada.json) y el [CSV de muestra](../Alumnado/Train/inventario.csv). El CSV tiene tres kits y dos filas defectuosas intencionadas: forman parte del criterio de importación. No hay personas reales. La planificación debe prever el contraste de filas válidas y defectuosas; no se exige programar un importador.

Calendario **ficticio**: 01–12/04/2030, diez jornadas laborables de lunes a viernes; D1=01/04, D5=05/04, D6=08/04, D10=12/04. No son fechas de AulaFlow ni de FE. La entrega sintética es al final de D10. Las horas son trabajo hipotético de ese proyecto; resolverlo como ejercicio se hace en los minutos ya reservados en la ruta PI3.

| Persona ficticia | Disponibilidad total | Reserva mínima | Capacidad comprometible | Capacidad de trabajo |
|---|---:|---:|---:|---|
| PERSONA-A | 20 h | 4 h | 16 h | Frontera y servicio |
| PERSONA-B | 14 h | 4 h | 10 h | Cliente, revisión e integración |
| PERSONA-C | 6 h | 2 h | 4 h | Datos e importación |

El JSON especifica además disponibilidad por día; una suma global correcta puede ocultar una sobrecarga diaria. La revisión ordinaria debe estimarse como trabajo; la reserva queda para contingencia y apoyo no comprometido. No cuentes las mismas horas dos veces. Un backup puede colaborar si tiene capacidad; no presupongas que conoce todo.

## Actividades que debes ordenar

La entrada contiene siete actividades TRAIN-A01…A07, estimaciones y dependencias. No contiene su calendario resuelto. Son trabajo de preparación/ejecución hipotético del proyecto; PI3 solo produce su plan. Cada una referencia uno o varios resultados contratados TRAIN-01…04. No aumenta el número de resultados al descomponerlos.

Entorno TRAIN-R01: hasta tres actividades a la vez, uso ficticio autorizado desde D2 por TRAIN-P01. Tablet TRAIN-R02: una actividad por jornada, necesaria para consulta de cliente y contraste integrado. Muestra CSV: autorización TRAIN-P02 disponible D4. Puede prepararse su criterio antes, pero no planificar su uso antes del permiso.

## Borrador defectuoso a auditar

El cliente recibe este borrador deliberadamente malo:

- TRAIN-A05 antes de TRAIN-A04: «la cancelación es más rápida».
- TRAIN-A03 y TRAIN-A07 usan a la vez la tablet en D5.
- TRAIN-A06 usa CSV en D3 y no tiene permiso en su ficha.
- Cliente y servicio deciden ambos qué reserva existe, sin autoridad de conflicto.
- Riesgo «fallo técnico» sin causa, trigger ni medios.
- TRAIN-A02 sale cuando «parezca acabado», sin muestra verificable.
- Solo PERSONA-A conoce la frontera; no hay backup ni tiempo para transferencia.
- La entrega se considera vinculada a una fecha de FE no confirmada.
- El plan estima usando «un AT equivale a una hora» y cambia el valor cuando se retrasa.

Son errores, no instrucciones. Localiza su efecto en P01–P12 y corrígelos sin ampliar el contrato.

## Construcción por capas y resultado esperado

En fases 2/4/5 prepara P01–P04 y dependencias; en 7/8 P05–P08; en 10 P09/P11; en 11 integra P10/P12 y comprueba coherencia. Usa las [plantillas](../Alumnado/02_PLANTILLAS_PAQUETE_PI3.md); las claves de actividades, recursos, decisiones y riesgos del caso empiezan por TRAIN-. PERSONA-A/B/C son códigos estables de personas ficticias.

El paquete terminado debe demostrar: grafo acíclico; secuencia compatible con precedencias y permisos; uso de la tablet sin colisión; horas diarias y globales defendibles; márgenes y revisión visibles; arquitectura con frontera de decisión; riesgos accionables; hito observable; versión antes/después de un ensayo de restricción. G1 del caso se registra como simulación, sin trasladarlo a tu G1 real.

Autocomprobación: localiza TRAIN-02, su actividad, predecesora, persona, ventana, permiso, salida, riesgo y evidencia. Si alguno contradice otro documento, aún no hay un único baseline. Puede haber varios planes válidos; se valora justificación y coherencia. Los ejemplos guiados ayudan, pero no son el oráculo de este caso.

---

[Índice de PI3](../README.md) · [Inicio del módulo](../../README.md)
