# Ejemplos reproducibles · PI5

Todos los datos de estos ejemplos son sintéticos; no son resultados de AulaFlow ni de usuarios reales. Reproduce las operaciones a mano o con calculadora antes de leer la explicación.

## 1. Tres porcentajes que no se pueden intercambiar

Entrada: ocho comprobaciones previstas, seis ejecutadas, cinco conformes y una fallida. Primero enumera P1–P8; marca P1–P5 conforme, P6 fallida y P7–P8 no ejecutadas. Calcula cobertura: 6÷8×100=75 %. Calcula conformidad entre ejecutadas: 5÷6×100≈83,3 %. Calcula conformidad respecto del plan: 5÷8×100=62,5 %. La segunda cifra no informa de P7/P8 y por tanto no demuestra que el plan se haya completado.

Salida: ficha con los tres universos explícitos y acción «ejecutar P7/P8 y resolver P6». Si P6 es crítico, no concluir aceptación aunque otro indicador supere el umbral. Comprobación propia: si no hay pruebas planificadas, los tres cocientes carecen de base y se informa NO_MEDIDO, no 100 %.

## 2. Una traza que sí permite revisar

Entrada: condición TRAIN-R «cancelar conserva historial»; evidencia «captura de botón», corte TRAIN-C1. Paso 1: preguntar qué observaría cumplimiento. Paso 2: localizar reserva antes, estado activa después y entrada de historial. Paso 3: marcar EVIDENCIA_INSUFICIENTE porque la captura solo muestra una posibilidad de interacción. Paso 4: pedir registro antes/después en el mismo corte y perfil, con dato sintético.

Segunda entrada didáctica: una tarjeta describe activa antes, ausente después e historial presente, pero usa almacenamiento simulado. La traza puede afirmar conformidad del modelo en ese ensayo; no afirma persistencia del servicio compartido. Salida: dos límites separados. Prueba de transferencia: si cambia el código que decide el estado, la tarjeta anterior no certifica por sí sola el candidato nuevo.

## 3. Feedback sin inducir la respuesta

Objetivo: comprobar comprensión de cancelación. Guion inicial «pulsa cancelar y confirma» enseña el camino; sustitúyelo por «ya no necesitas esta reserva; deja constancia y comprueba qué sucedió». Registrar tarea, corte, ayuda y conducta observable. Tarjeta sintética: S1 termina sin ayuda; S2 vuelve atrás y pide explicación; S3 termina tras una pista. Completadas sin ayuda: 1/3, no 3/3. Completadas con o sin ayuda: 2/3 (S1 y S3). Completadas tras recibir ayuda: 1/3 (S3); cada tasa responde a una pregunta distinta y debe conservar su etiqueta.

No concluir que S2 «no sabe usar aplicaciones». Hipótesis de interfaz: la consecuencia del diálogo resulta ambigua. Propuesta: aclarar texto y repetir tarea con versión nueva y guion neutral. La plantilla se evalúa sin publicar identidades. La tarjeta no autoriza afirmar que se ha entrevistado a tres personas.

## 4. CI y candidato distintos

Entrada: informe técnico de TRAIN-C7 PASS; candidato entregado TRAIN-C8; cambio entre ambos en validación de reserva. Abrir fila de diferencia y localizar condiciones dependientes de esa validación. Conservar C7 como histórico. Solicitar retest de consulta/reserva del corte C8 y regresiones justificadas. Un build de C8 sin pruebas demuestra empaquetado, no que las pruebas de C7 hayan corrido de nuevo.

Salida de V06: corte C8, build descrito por tarjeta sintética, retest pendiente, demo solo de mesa. No fabricar hash o URL para completar el documento. En un proyecto real se anotaría la referencia auténtica disponible y sus permisos. PI5 no prescribe cómo programar el test: pide evidencia al módulo/rol responsable.

## 5. Puerta activada, todavía no satisfecha

Entrada: G3 dispone de decisión de activación, criterio y oportunidad curricular; hay informe de pruebas, pero ninguna recuperación definida. No están documentadas las cinco condiciones de puerta técnica no compensable. Solicitar el mecanismo de recuperación y mantener estado de revisión pendiente. No confundir ese defecto de activación con un suspenso automático de la persona.

Segunda entrada: la activación está completa, pero el informe es de una versión anterior al cambio. La puerta puede estar activada y su satisfacción pendiente de retest. Salida: dos campos diferentes, activación y resultado, con fuentes. Este ejemplo no activa G3 en un contrato real.

## 6. Proponer retrabajo sin borrar el contrato

Entrada: cuatro requisitos; tres tienen evidencia suficiente y uno falla; el equipo pide retirar el cuarto para entregar. Paso 1: conservar matriz y fallo. Paso 2: estudiar corrección y retest. Paso 3: si se plantea cambio de alcance, iniciar el proceso de PI4 con impacto y autoridad; no editar la condición unilateralmente. Paso 4: proponer RETRABAJO y condición concreta de nueva revisión.

Una plantilla de acta contiene objeto, corte, fuentes, resultados, pendientes, propuesta, autoridad y próxima revisión. En TRAIN la autoridad es un rol ficticio y la salida PROPUESTA_TRAIN, nunca ACEPTADA real. En REAL sin catálogo la salida es PENDIENTE_CATALOGO y no se calculan AT. Saber no concluir es evidencia de criterio profesional cuando faltan entradas.
