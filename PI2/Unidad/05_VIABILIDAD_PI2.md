# Viabilidad técnica: decidir con evidencia
## Qué responde el estudio
«La tecnología existe» y «podemos comprometernos a este resultado» son afirmaciones distintas. El estudio responde si el alcance puede lograrse bajo condiciones conocidas, qué falta demostrar y qué consecuencia contractual se deriva. No es arquitectura global, tutorial o promesa de aprender cualquier cosa.

Dependencia: algo que debe estar disponible. Supuesto: afirmación aún no comprobada. Condición: comprobación pendiente con consecuencia explícita. «Habrá un entorno compatible» es supuesto; «comprobar acceso autorizado antes de confirmar esta prestación; si falta, elevar incompatibilidad conservando obligación» es condición.

| Dictamen | Fundamento | Consecuencia |
|---|---|---|
| VIABLE | Evidencia pertinente suficiente para condiciones declaradas | Puede proponerse confirmación; no acredita implementación |
| VIABLE_CON_CONDICION | Camino razonable con comprobación pendiente explícita | Condicionar la confirmación al hecho concreto |
| NO_DEMOSTRADO | Información insuficiente | Recabar evidencia; no afirmar certeza ni imposibilidad |
| NO_VIABLE | Incompatibilidad concreta demostrada | Rechazar alternativa o cambiar condiciones mediante decisión autorizada |

El dictamen pertenece a una prestación y contexto, no a una tecnología «buena/mala». Compatibilidad documental no acredita acceso local.

## Método reproducible
1. Pregunta acotada: «¿puede conservarse esta información del legado?» frente a «¿es viable la app?».
2. Hechos: fuente, revisión/fecha, observación y límite; recuperar G0 y decisiones C/M/S/D.
3. Dependencias: destino, acceso, autenticación común, formato, servicio o competencia pertinente. Sin inventario detallado de recursos/personas.
4. Alternativas dentro del alcance: variar una opción/condición, sin eliminar unilateralmente cliente o backend obligatorio.
5. Dictamen: unir evidencia → limitación → decisión y qué observación lo cambiaría.
6. Propagación: alcance, aceptación, financiación, ficha de diseño y calidad. CR si afecta baseline confirmada.

## Suficiencia de fuentes
| Pregunta | Evidencia | Lo que no demuestra |
|---|---|---|
| Destino compatible | Documentación oficial versionada | Acceso o capacidad local |
| Fallo del legado | G0 localizado/repetible | Que ya está arreglado |
| Formato importable | Muestra autorizada y campos | Que todo el histórico cumple |
| Servicio utilizable | Acceso/condiciones para uso previsto | Gratuidad futura o ausencia de límites |
| Competencia disponible | Evidencia de formación/experiencia | Entrega garantizada de otro módulo |

Registrar título, URL/ruta, versión, consulta, afirmación y límite. Una captura sin contexto no acredita versión o reproducibilidad. Una respuesta de IA no sustituye documentación primaria.

## Ejemplo actual de compatibilidad
Una propuesta presupone .NET MAUI dirigido exclusivamente a Linux de escritorio. La lista oficial de plataformas estándar consultada no incluye Linux como destino .NET MAUI soportado; **inferencia acotada:** no está demostrada esa combinación como destino estándar con soporte oficial. Esto no afirma que todo desarrollo desde Linux sea imposible. [Plataformas .NET MAUI](https://learn.microsoft.com/en-us/dotnet/maui/supported-platforms?view=net-maui-10.0), consulta 05/09/2026.

Microsoft también documenta en `maui-labs` un backend **Linux GTK4 experimental**. La propia documentación indica que estos backends experimentales pueden cambiar entre versiones y **no tienen soporte oficial de Microsoft**. Por tanto, su existencia no convierte Linux desktop en un destino estándar soportado; sí puede registrarse como alternativa experimental que exige valorar madurez, dependencia y condiciones antes de comprometerla. [Backends experimentales .NET MAUI](https://learn.microsoft.com/en-us/dotnet/maui/developer-tools/platform-backends/?view=net-maui-10.0), consulta 05/09/2026.

Mantener el requisito MAUI; aclarar destino permitido y comprobar acceso autorizado a entorno compatible antes de confirmar. Si no se resuelve, elevar incompatibilidad; no sustituir unilateralmente el cliente. La distribución detallada de equipos/trabajo es de PI3.

La documentación de Flutter distingue soporte y comprobaciones de integración; eso no demuestra acceso local. La preparación para distribución iOS requiere macOS y Xcode. [Soporte Flutter](https://docs.flutter.dev/reference/supported-platforms), [preparación iOS](https://docs.flutter.dev/deployment/ios), consulta 05/09/2026. No se cambian por esa lectura las versiones autorizadas del curso.

## Estudio real E07
Estudia cinco aspectos pertinentes: continuidad del legado, cliente obligatorio, backend común, información a conservar/migrar y una opción/dependencia relevante. No son cinco VIABLE predeterminados.

Por aspecto: pregunta, hechos, fuente, supuesto, dictamen, condición/fallback y efecto. Seis a diez líneas razonadas pueden bastar. Rechazar una alternativa con evidencia también aporta aprendizaje.

Migración aquí significa compatibilidad y resultado de conservación; no ETL detallado. Integración significa comportamiento compartido esperado, no OpenAPI completo. Identificar falta de competencia no convierte a otro profesor en puerta de aprobación ni garantiza la disponibilidad.

## Autocorrección
- «Viable porque lo hará AD»: precisar condición real y fuente.
- «Será gratis»: comprobar cobertura/condiciones; mientras, NO_DEMOSTRADO.
- «Si falla, quitamos un obligatorio»: elevar incompatibilidad; no borrar obligación.
- «No sabemos, imposible»: separar carencia actual y contradicción demostrada.
- «Riesgo medio»: describir supuesto y consecuencia, sin matriz formal de riesgos.

Practica primero con ReservaLab; transfiere el método con honestidad sobre lo desconocido.

---

[Índice de PI2](../README.md) · [Inicio del módulo](../../README.md)
