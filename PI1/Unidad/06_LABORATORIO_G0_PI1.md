# Laboratorio integrado · Dossier de incorporación y contexto

## Encargo

Llevant Suport Digital, SL, estudia la continuidad de un gestor de trabajo heredado para un contexto con varias funciones y organizaciones usuarias. Antes de comprometer alcance, necesita saber qué ofrece AulaFlow 1.0.0, qué necesidades están justificadas y qué decisiones merecen investigarse. Vuestro equipo elaborará un **dossier único** y cada integrante defenderá su comprensión.

El contexto empresarial es simulado y sus datos están en la ficha del caso. El software, tag, historial y pruebas a auditar son **reales**. No simules una ejecución que no hayas hecho. No implementes AulaFlow 2.0, no cambies el tag, no solicites ayudas y no firmes un contrato de tareas/AT.

## Material de entrada

- [Caso de contexto](../Alumnado/09_CASO_CONTEXTO_PI1.md).
- [Plantilla de dossier](../Alumnado/01_PLANTILLA_DOSSIER_PI1.md) y sus anexos de trabajo.
- [Procedimiento reproducible de G0](03_AUDITORIA_LEGADO_PI1.md).
- [Fuentes oficiales y revisión](10_REFERENCIAS_Y_ACTUALIZACION_PI1.md).

El laboratorio es la actividad integradora de las fases 1–9 de la guía. No tiene horas adicionales a los **540 min**. Se trabaja progresivamente: cada tabla que elaboras se incorpora al dossier, sin redactar después una segunda memoria.

## Evidencias de equipo e individuales

| ID | Evidencia | Suficiencia orientativa |
|---|---|---|
| E01 | Baseline y ejecución | tag/commit, entorno, comandos, resultado real de Maven, arranque, recorrido y reinicio; incidencias delimitadas |
| E02 | Mapa y flujo | responsabilidades del sistema con rutas del tag y un recorrido de cuatro componentes o más |
| E03 | Historia | seis filas: funcional, persistencia, seguridad, pruebas/CI, operación e incidencia; decisión y evidencia diferentes |
| E04 | Capacidades y transición | seis decisiones sobre objetos concretos con evidencia, motivo, necesidad, dependencia y duda; comprensión de las cuatro categorías |
| E05 | Sector y organizaciones | tres tipos con ejes comparables; dos empresas caracterizadas por sus funciones y relaciones |
| E06 | Necesidades y oportunidades | tres necesidades priorizadas, dos oportunidades, evidencia y límites; una petición no priorizada |
| E07 | Proyecto y características | tipo de intervención y tres cadenas necesidad–característica–legado–pregunta |
| E08 | Condicionantes y ayudas | seis filas de obligaciones aplicadas y dos candidatas investigadas con fuente, fecha y conclusión |
| E09 | Guion inicial | 6–8 bloques lógicos, preguntas, decisiones y validaciones; sin estimaciones/contrato |
| E10 | Síntesis individual | una conclusión breve propia por CE y enlaces; atribución de contribución y revisión; I3 sin agente |

Las cantidades evitan un trabajo superficial, pero el número de filas no prueba dominio. Una misma evidencia puede apoyar varios CE si la relación se explica. Para C/M/S/D, si no procede descartar ningún objeto, una justificación explícita y un contraejemplo defendible sustituyen a forzar una decisión falsa.

## Desarrollo y puntos de control

1. **Antes del taller 1:** E05–E06 borrador y E01–E04 iniciadas. Ejecutar sobre base ficticia; leer muestras acotadas. Llevar un bloqueo reproducible o una observación contrastable, no solo una captura.
2. **Taller 1:** demostrar un recorrido, localizar un componente que pregunte el profesor y corregir el mapa. Registrar G0 `SUFICIENTE`, `PENDIENTE_ENTORNO` o `PENDIENTE_EVIDENCIA` con razón. La suficiencia final requiere verificación individual.
3. **Entre talleres:** volver a las necesidades a la luz de lo observado; completar E07–E09 y fuente/fecha/aplicabilidad. Conectar al menos tres decisiones C/M/S/D con necesidades del caso. Añadir preguntas que podrían cambiar la transición.
4. **Taller 2:** contraste de fuentes y una microvariación individual. Revisar la conclusión y la entrega dentro de los minutos reservados.

## Primer corte hipotético y límite

La transición inicial describe una experiencia funcional de alto nivel que tendría sentido investigar, qué semántica/datos del legado habría que preservar y qué incógnita de colaboración, identidad o cliente impide comprometerla hoy. No diseña API, esquemas nuevos, backlog, arquitectura ni criterios de aceptación finales. Debe quedar identificada como **HIPÓTESIS PARA PI2**.

## Entrega

En AULES, una tarea de equipo recoge dossier Markdown o PDF accesible, evidencias saneadas y enlaces a revisión autorizada. Si hay repositorio de equipo, entregar también SHA/enlace de la revisión; no basta una rama que seguirá cambiando. Cada integrante incluye su sección E10 en el mismo dossier; el docente conserva el acta individual I3 de forma reservada.

No adjuntar código completo del legado, bases de datos, archivos `.env`, credenciales, cookies, tokens, logs brutos o configuraciones del IDE. Se aceptan registros textuales legibles en lugar de vídeo. Las capturas muestran datos ficticios y llevan pie que explica qué prueban. Usa títulos jerárquicos y tablas con cabecera; no dependas solo de color.

## Puerta de salida

El equipo debe poder explicar qué producto recibió y por qué contexto/necesidad justifican sus decisiones; cualquier integrante debe localizar una parte no preparada. Un bloqueo de entorno bien documentado permite valorar el razonamiento disponible y reprogramar la ejecución, pero **no acredita G0 sin ejecución real**. No compensa una G0 pendiente con páginas de teoría ni con puntuación de contexto.

---

[Índice de PI1](../README.md) · [Inicio del módulo](../../README.md)
