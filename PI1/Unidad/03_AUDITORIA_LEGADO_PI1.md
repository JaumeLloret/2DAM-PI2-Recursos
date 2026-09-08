# Auditoría del legado · leer, ejecutar y explicar

## 1. Identificar el objeto

La referencia obligatoria es AulaFlow v1.0.0 (consulta el [acceso al legado](../../ACCESO_AULAFLOW_1_0.md)), commit `c727814aa6deed46c37141ff3f98585136b49593`. El tag anotado tiene su propio objeto Git, `da260d0b3c38781deeddf73ab61579bbd709dc3a`; el commit desreferenciado es el que identifica el código. No confundas los dos hashes ni sustituyas el tag por `main`.

El profesor proporciona acceso o una distribución autorizada del tag. Si falla el permiso, solicita acceso por el canal del curso. No uses copias de terceros. Para clonar utiliza la URL entregada por el profesor y tu método de autenticación ya configurado; no pegues tokens en comandos, capturas o documentos.

Sustituye `URL_FACILITADA_POR_EL_DOCENTE` por la URL autorizada recibida en AULES, conservando las comillas. El texto es un marcador, no una dirección que funcione. Si recibes un paquete descargable, sigue sus instrucciones de acceso. En una copia de trabajo limpia y dedicada al laboratorio:

```bash
git clone "URL_FACILITADA_POR_EL_DOCENTE" aulaflow-pi1
cd aulaflow-pi1
git status --short
git fetch --tags
git switch --detach v1.0.0
git rev-parse HEAD
git rev-parse 'v1.0.0^{commit}'
git describe --tags --exact-match
```

Si `git status --short` muestra cambios tuyos, detente antes de cambiar de revisión y conserva ese trabajo en otra copia; no uses reset ni opciones que lo borren. `detached HEAD` es normal al inspeccionar un tag: no vas a implementar cambios aquí. Ambos `rev-parse` deben dar el commit indicado y `describe` debe identificar `v1.0.0`.

En Windows usa Git Bash para esos comandos o las operaciones equivalentes de IntelliJ; no hace falta WSL. Para Maven en PowerShell usa `./mvnw.cmd`. No se exige instalar Bash a quien use las alternativas gráficas y Maven de Windows.

## 2. Comprobar el entorno

Desde la raíz del repositorio:

```bash
java --version
./mvnw --version
./mvnw clean verify
```

En PowerShell:

```powershell
java --version
./mvnw.cmd --version
./mvnw.cmd clean verify
```

Debe usarse **JDK 26** sin preview y Maven **3.9.16** mediante el wrapper. El `pom.xml` exige Java en `26,27)`. En IntelliJ comprueba Project SDK y el JRE de ejecución de Maven; que el editor reconozca Java no prueba qué JDK está usando Maven. Conserva versión observada, fecha, salida final y resumen de pruebas. El resultado satisfactorio de Maven es `BUILD SUCCESS`, sin ocultar fallos ni omitir tests. El artefacto esperado es `target/aulaflow-1.0.0.jar`; no compares el número de tests con el de una PR histórica.

Para este laboratorio no se pide explicar la sintaxis de Maven/JUnit ni desarrollar tests. Sí debes distinguir «no descargó dependencias», «falló una prueba» y «verificación correcta». Si tu entorno no puede ejecutar, registra `NO EJECUTADO` y la causa concreta. La G0 permanecerá pendiente hasta ejecutar/contrastar en un entorno autorizado.

## 3. Arrancar con datos ficticios y sin revelar credenciales

En IntelliJ IDEA Community abre la raíz, espera la sincronización Maven y crea una configuración **Application**:

| Campo | Valor o decisión |
|---|---|
| Main class | `es.aulaflow.AulaFlowApplication` |
| JRE | JDK 26 |
| Working directory | raíz de esta copia de `aulaflow-pi1` |
| `AULAFLOW_HTTP_HOST` | `127.0.0.1` |
| `AULAFLOW_HTTP_PORT` | `8080`, o `8081` si 8080 está ocupado |
| `AULAFLOW_DB_PATH` | `data/pi1-lab.db`, solo para esta copia de laboratorio |
| `AULAFLOW_ADMIN_USERNAME` | nombre local elegido, 3–64 caracteres ASCII minúsculos, números, punto, guion o guion bajo |
| `AULAFLOW_ADMIN_PASSWORD` | contraseña local elegida de 15–128 puntos de código; no se incluye en la entrega |

Las variables se escriben en **Environment variables**, no en Program arguments. No compartas la configuración del IDE ni actives guardar como archivo de proyecto para los secretos. `AULAFLOW_SESSION_COOKIE_SECURE` se omite en HTTP local (su valor predeterminado es `false`). La base predeterminada sin variable es `data/aulaflow.db`; aquí diferenciamos la base de ensayo. Las rutas relativas dependen del directorio de trabajo: cambiarlo puede crear otra base y aparentar pérdida de datos.

Alternativa Bash, desde la raíz y después de construir el JAR: leer las credenciales de forma interactiva evita escribir la contraseña en la línea de historial.

```bash
export AULAFLOW_HTTP_HOST=127.0.0.1
export AULAFLOW_HTTP_PORT=8080
export AULAFLOW_DB_PATH=data/pi1-lab.db
read -r -p 'Usuario local: ' AULAFLOW_ADMIN_USERNAME
read -r -s -p 'Contraseña local: ' AULAFLOW_ADMIN_PASSWORD
export AULAFLOW_ADMIN_USERNAME AULAFLOW_ADMIN_PASSWORD
java -jar target/aulaflow-1.0.0.jar
```

Si utilizas PowerShell, sigue la configuración de IntelliJ para introducir secretos; las variables configuradas en el IDE solo llegan al proceso arrancado desde esa configuración. No presupongas que un terminal externo las hereda.

Abre `http://127.0.0.1:8080/login` y `/boards` tras autenticarte. Cambia el puerto en todas las URLs si elegiste otro. Con Cartero crea una petición **GET**, URL `http://127.0.0.1:8080/api/v1/health`, sin autenticación ni cuerpo, y pulsa enviar. También puedes abrir esa URL en el navegador o ejecutar `curl -i http://127.0.0.1:8080/api/v1/health`. Espera HTTP 200 y `status: UP`. El campo de versión es una evidencia a contrastar con Git y Maven; una discrepancia se registra, no se corrige alterando el tag.

Una consola que sigue abierta tras arrancar el servidor es normal: el proceso está atendiendo peticiones. Verifica la URL antes de interpretar que está bloqueado.

## 4. Recorrido representativo reproducible

Dentro de los 25 minutos de recorrido de fase 4:

1. Inicia sesión y crea un tablero ficticio `PI1-Ensayo`.
2. Comprueba columnas y crea dos columnas si hacen falta. Registra sus nombres y orden.
3. Crea dos tarjetas ficticias, edita el título de una y muévela a otra columna; comprueba el nuevo orden. Usa formulario/botones si no puedes arrastrar.
4. Añade una etiqueta y una checklist de dos elementos; marca uno y observa el progreso.
5. Exporta ese tablero en CSV v1. Importa el archivo desde la interfaz: primero previsualización y después confirmación. Comprueba que crea otro tablero independiente. El CSV es un intercambio de tablero, no un backup completo; examina qué conserva y qué no.
6. Cierra sesión; comprueba que el acceso protegido solicita autenticación otra vez. Vuelve a entrar.

Anota **acción, resultado esperado, resultado observado y evidencia**. No registres cookies, contraseñas, cabeceras de autenticación o tokens CSRF. Los datos de contenido son exclusivamente ficticios.

## 5. Reinicio, identidad y persistencia

Detén con el botón Stop del IDE o Ctrl+C. Retira las dos variables iniciales de administrador de la configuración. En Bash, después de detener:

```bash
unset AULAFLOW_ADMIN_USERNAME AULAFLOW_ADMIN_PASSWORD
java -jar target/aulaflow-1.0.0.jar
```

Mantén exactamente **la misma base, ruta y directorio de trabajo**. Vuelve a iniciar sesión con las credenciales locales creadas antes: el administrador ya existe. Deben conservarse tablero, tarjetas, orden, etiqueta y checklist. Las sesiones en memoria se pierden al reiniciar, lo que no implica pérdida de los datos de negocio. Cambiar las variables iniciales no cambia la contraseña de un administrador ya persistido.

No borres la base para «arreglar» una discrepancia. Registra qué ruta resolvió la configuración y compara con el primer arranque. Termina deteniendo el proceso; conserva solo tu base local ficticia mientras necesites contrastarla. No la subas al repositorio ni a AULES.

## 6. Mapa y seis muestras históricas

Completa la plantilla de mapa con entrada, HTTP/presentación, web, aplicación/dominio, SQLite/migraciones, autenticación/sesiones, pruebas, empaquetado/operación y documentación. Escoge **un flujo** y enlaza al menos cuatro rutas reales de su recorrido. No basta enumerar carpetas.

Para cada familia dedica unos 3–4 minutos dentro de los 25 de historia a localizar problema, decisión y evidencia, utilizando este itinerario:

| Familia | Muestra acotada | Pregunta |
|---|---|---|
| Funcional | PR #20, resumen/contrato CSV v1 | ¿qué conserva la importación y qué queda fuera? |
| Persistencia | PR #14 y ADR-0012 | ¿cómo se comprueba un segundo ciclo independiente? |
| Seguridad | PR #27 y ADR-0017 | ¿qué amenaza trata la decisión y qué queda pendiente? |
| Pruebas/CI | `.github/workflows/ci.yml` y `VerticalSliceEndToEndTest` | ¿qué observa Maven y qué requiere otro entorno? |
| Operación | PR #22 y `docs/release/1.0.0.md` | ¿qué artefacto se ejecuta y dónde viven los datos? |
| Incidencia/corrección | `docs/incidents/INC-0005-containerignore-bloquea-jar-release.md` y PR #28 | ¿por qué compilar no garantizó construir la imagen? |

Todas las PR de esta tabla pertenecen al [repositorio heredado (consulta el [acceso al legado](../../ACCESO_AULAFLOW_1_0.md)), no al repositorio del curso. Usa el código del tag y conserva URL de PR y ruta del documento. El oráculo no es necesario para encontrar las evidencias.

## 7. Diagnóstico rápido

| Síntoma | Comprobar | Recuperación y estado honesto |
|---|---|---|
| No accedo a GitHub | cuenta y permiso del recurso autorizado | pedir acceso; no buscar un espejo; pendiente de acceso |
| Java incorrecto | `java --version` y JRE de Maven | seleccionar JDK 26; no cambiar `pom.xml` |
| Wrapper no ejecutable | permiso de `mvnw` en Linux/macOS | `chmod u+x mvnw` en la copia local; Windows usa `.cmd` |
| Descarga fallida | mensaje de red, proxy y repositorio de dependencias | registrar; equipo/caché autorizados; no desactivar TLS |
| Error de puerto | otro proceso usando 8080 | elegir 8081 en esta copia y sus URLs; no detener procesos ajenos |
| Base vacía sin administrador | variables y directorio de trabajo | aprovisionar solo la base ficticia de ensayo |
| Login no persiste | cookie Secure y si realmente se usa HTTPS | en HTTP local omitir Secure; volver a iniciar sesión |
| Tras reinicio no están los datos | base y working directory reales | abrir la misma base; no borrar ni recrear antes de investigar |
| Versión HTTP distinta | commit, pom y origen del valor | registrar hallazgo con fuentes; preservar baseline |

Podman/Compose y backup/restore completos son una extensión opcional con el runbook del legado, sin introducirlos como requisito de PI1. El paso obligatorio de operación es comprender el artefacto, la configuración, persistencia y parada del recorrido usado.

---

[Índice de PI1](../README.md) · [Inicio del módulo](../../README.md)
