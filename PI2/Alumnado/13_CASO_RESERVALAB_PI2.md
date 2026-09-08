# ReservaLab · caso de entrenamiento
**Ficticio, sin AT reales.** IDs TRAIN-* y UA_TRAIN solo pertenecen a este ejercicio. [JSON del caso](13_CASO_RESERVALAB_PI2.json). Nunca copiar al anexo AulaFlow.

## Encargo e información cerrada
Un laboratorio comunitario presta kits de electrónica y usa copias distintas de una hoja.
| Fuente ficticia | Hecho | Límite |
|---|---|---|
| C01 recepción | Duplicidades cuando reservan el mismo kit/franja | No cuantifica frecuencia anual |
| C02 muestra | CSV autorizado de inventario: referencia, nombre y disponibilidad, cabeceras conocidas | Sin reservas/historial |
| C03 coordinación | Necesita consultar reservas/cancelaciones para aclarar discrepancias | No autoriza publicar datos personales |
| C04 entorno | Acceso autorizado a entorno web de prueba y dispositivo cedido | No acredita correo externo |
| C05 propuesta | Avisos de correo serían cómodos | No obligación ni acceso confirmado |
| C06 consulta | Necesita descargar reservas CSV para consulta autorizada | Dos botones equivalentes no son dos resultados |
| C07 patrocinador | Núcleo obligatorio; límite 18 UA_TRAIN | No obliga a agotarlo |
| C08 estética | Sugiere panel estadístico | Sin necesidad prioritaria acreditada |

Actores: recepción/coordinación autorizadas. No repartir personas del equipo de desarrollo.

## Catálogo ficticio cerrado
| ID | Entregable | UA_TRAIN | Tipo/dependencia |
|---|---|---:|---|
| TRAIN-01 | Inventario compartido consultable | 4 | Obligatoria; sin dependencia |
| TRAIN-02 | Reserva sin conflicto de kit disponible | 5 | Obligatoria; TRAIN-01 |
| TRAIN-03 | Cancelación con historial | 2 | Obligatoria; TRAIN-02 |
| TRAIN-04 | Importación del inventario CSV disponible | 3 | Opcional; TRAIN-01 |
| TRAIN-05 | Aviso por correo mediante servicio externo | 3 | Opcional; TRAIN-02; Acceso y financiación por confirmar |
| TRAIN-06 | Exportación CSV de reservas autorizada | 2 | Opcional; TRAIN-02; excluyente con la otra salida CSV |
| TRAIN-07 | Descarga equivalente del mismo CSV | 2 | Opcional; TRAIN-02; excluyente con la otra salida CSV |
| TRAIN-08 | Panel estadístico agregado | 4 | Opcional; TRAIN-02 |

TRAIN-08 es ampliación avanzada sin prioridad acreditada. No cambiar valores, añadir filas o contar 06+07 a la vez. En el catálogo real ALT necesita autorización explícita.

## Economía cerrada
Datos ficticios, euros con impuestos incluidos; tres meses de observación económica, sin sprints. Alta única 12, alojamiento 8/mes, copia 2/mes, reserva hipotética 10, caja confirmada 20. Dispositivo cedido sin pago adicional en el supuesto. Correo opcional 18/mes, acceso no confirmado. Sin ayuda concedida.

## Trabajo progresivo
Fase 2: núcleo/dependencias/duplicado. Fase 3: objetivos, IN/OUT, selección ≤18 y dos aceptaciones fuertes. Fase 5: entorno/importación/correo con dictamen y condición. Fase 7: necesidad y déficit base/con correo. Talleres: selección, condición y concesión. El aprendizaje se transfiere a las fichas reales sin entregar otro paquete TRAIN completo.

Autocomprobación: ¿núcleo íntegro?, ¿duplicado?, ¿comodidad desplaza necesidad?, ¿correo probado?, ¿cobertura confirmada?, ¿cancelación repetida verificable? Justifica antes de feedback.

---

[Índice de PI2](../README.md) · [Inicio del módulo](../../README.md)
