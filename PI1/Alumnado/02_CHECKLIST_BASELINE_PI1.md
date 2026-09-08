# E01 · Baseline, ejecución e incidencias

## Identidad

- Repositorio/distribución autorizada: [completar].
- Tag esperado: `v1.0.0`.
- Commit esperado: `c727814aa6deed46c37141ff3f98585136b49593`.
- Commit observado con `git rev-parse HEAD`: [completar].
- Tag desreferenciado con `git rev-parse 'v1.0.0^{commit}'`: [completar].
- ¿Copia limpia y dedicada? [sí/no y actuación, sin borrar trabajo].
- Fecha, sistema, JDK observado y Maven Wrapper observado: [completar].

## Ensayo

Sigue [la guía](../Unidad/03_AUDITORIA_LEGADO_PI1.md); marca `OK`, `FALLO` o `NO EJECUTADO`. «Esperado» no es «observado».

| Paso | Comando/acción | Resultado esperado | Resultado real y estado | Evidencia saneada |
|---|---|---|---|---|
| Toolchain | versión Java/Wrapper | JDK 26 / Maven 3.9.16 | [completar] | |
| Verificación | clean verify | BUILD SUCCESS; artefacto 1.0.0 | [completar resumen de tests] | |
| Arranque | IDE/JAR, base ficticia | servidor local operativo | [completar] | |
| Salud | GET /api/v1/health | HTTP 200 / UP; contrastar versión | [completar] | |
| Login | credenciales locales | acceso protegido | [completar, nunca credenciales] | |
| Kanban | crear/editar/mover | estado y orden actualizados | [completar] | |
| Etiqueta/checklist | añadir/marcar | vínculo y progreso visibles | [completar] | |
| CSV | exportar/previsualizar/confirmar | tablero independiente, límites contrastados | [completar] | |
| Logout | cerrar y volver a entrar | exige nueva autenticación | [completar] | |
| Reinicio | misma BD sin variables iniciales | datos conservados; nuevo login | [completar] | |
| Parada | Stop / Ctrl+C | proceso detenido, datos locales conservados | [completar] | |

Ruta de base ficticia y working directory utilizados: [solo lo necesario, sin ruta personal en material público]. Qué predije antes del reinicio y qué corregí después: [completar].

## Incidencia reproducible si procede

Objetivo y fase: [completar]. Fecha/entorno/SHA: [completar]. Pasos mínimos: [completar]. Esperado: [completar]. Observado: [completar]. Evidencia sin secretos: [completar]. Hipótesis y comprobación: [completar]. Próximo paso/acceso de contingencia: [completar]. Lo que sigue **sin ejecutar**: [completar].

- [ ] No he copiado cookies, tokens, contraseñas ni bases.
- [ ] No he cambiado el tag ni las versiones para evitar un fallo.
- [ ] El resultado de una PR histórica no aparece como prueba de mi equipo.
- [ ] Si falta ejecución, G0 permanece pendiente y hay una acción concreta.

---

[Índice de PI1](../README.md) · [Inicio del módulo](../../README.md)
