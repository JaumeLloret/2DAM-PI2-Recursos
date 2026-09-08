# Trasladar el plan a GitHub Projects

Tiempo: los 20 min de lectura de fase 5 se comparten con teoría; el traslado TRAIN se hace dentro de sus 30 min. Resultado: una vista del mismo plan con referencias estables, o una tabla manual equivalente si no tienes permiso de Projects.

## Preparar el espacio

En el perfil personal u organización autorizada, entra en Projects, crea un proyecto desde Table o Board y dale un nombre que indique TRAIN. Escribe propósito y enlace al baseline en su descripción. En el proyecto real utiliza la visibilidad y accesos decididos por el docente. No hagas público un contrato privado. [Documentación de creación, consultada 07/09/2026](https://docs.github.com/en/issues/planning-and-tracking-with-projects/creating-projects/creating-a-project).

Los siguientes campos son una convención PI3: título, ID de actividad, referencia contractual, preparación, hito, depende de, responsable, ventana, evidencia y TBD. Usa texto/selección/fecha cuando la interfaz lo permita; si faltan permisos para campos, escribe los mismos rótulos en el cuerpo de la issue. No necesitas automatizaciones, gráficos de pago ni integración API.

## Cargar y contrastar

1. Crea manualmente una issue ficticia con la [plantilla](Plantillas/ISSUE_PLANIFICACION.md) en el repositorio de ejercicio autorizado, o usa un borrador del Project. Mantén TRAIN en título y referencias. Los borradores viven en el proyecto; una issue vive en el repositorio.
2. Añade la issue al Project pegando su URL en Add item o desde su campo Projects. Esto representa trabajo planificado, no envía una solicitud a otra persona. No asignes cuentas ajenas sin acuerdo. [Añadir elementos](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-items-in-your-project/adding-items-to-your-project), consulta 07/09/2026.
3. Usa labels descriptivas como `planificacion`, `bloqueo` y `train`; milestone para un hito observable, con fecha solo si está confirmada. En el cuerpo escribe predecesoras y condición FS; el orden de tarjetas por sí solo no explica dependencia.
4. Agrupa la vista Board por preparación: POR_ACLARAR, BLOQUEADA_DEPENDENCIA, PREPARADA. Conserva el orden de ejecución y los hitos en tabla. No añadas ACEPTADA ni DONE para fingir ejecución; la aceptación real será una decisión con evidencia.
5. Contrasta dos entradas al azar con P04/P08: misma referencia, dependencia, persona y ventana. Corrige el baseline y vista de forma conjunta, dejando fecha/versión.

## Exportar y volver a importar de forma controlada

GitHub documenta exportación de una vista como **TSV** mediante View → Export view data. Guarda la vista con los campos relevantes y su filtro anotado; una vista filtrada puede omitir tareas. [Exportar datos](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-your-project/exporting-your-projects-data), consulta 07/09/2026.

No se promete importación CSV nativa. La importación propuesta es **manual**: lee cada fila del JSON/tabla abierto, crea/actualiza la entrada por su clave estable, coteja cantidad de filas y referencias, revisa duplicados y exporta otra vez para contrastar. No alteres IDs/AT del contrato auténtico. No pegues TRAIN en el backlog real. Si aparece el catálogo, primero debe cotejarlo el docente por el procedimiento del laboratorio.

Alternativa sin Projects: usa P04 en Markdown y el JSON del plan bajo Git, con columnas de preparación. Reordenar filas y guardar diff ofrece el mismo ejercicio de secuenciación. El control manual comprueba las mismas invariantes; la interfaz no es un CE y su indisponibilidad se registra como PENDIENTE_ENTORNO. La prueba de cuentas, permisos y exportación real queda en prepublicación.

---

[Índice de PI3](../README.md) · [Inicio del módulo](../../README.md)
