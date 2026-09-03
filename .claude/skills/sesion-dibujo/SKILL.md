---
name: sesion-dibujo
description: Genera una sesión de práctica de dibujo o escritura para el proyecto de cómic de Jad. Usar cuando Jad pida "una sesión", "dame una sesión", "qué hago hoy", "arranquemos", o cuando quiera cerrar/registrar una sesión ya hecha, guardar un trofeo, ajustar el backlog o revisar el progreso. No usar para preguntas sueltas sobre dibujo o cómics que no impliquen armar o cerrar una sesión.
---

# Generar una sesión

## Antes de responder

Leer los tres archivos del proyecto. **Primero desde el filesystem local** (Claude Code, repo clonado); si no están, por fetch a las URLs raw.

| Archivo | Local | Raw |
|---|---|---|
| Reglas, formatos, roadmap. **Manda sobre todo lo demás.** | `./00-CONTEXTO.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/00-CONTEXTO.md` |
| Última fecha, sesiones, backlog, pendientes | `./01-BITACORA.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/01-BITACORA.md` |
| Historia (solo si hay carril W) | `./02-BIBLIA.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/02-BIBLIA.md` |

Los entregables viejos viven en `./trofeos/`.

Si ninguna vía funciona, pedirle a Jad que pegue el contenido. **No inventar el historial.**

**En Claude Code:** escribir los cambios directo en los archivos, guardar el trofeo y commitear. No hace falta devolver nada para pegar a mano.

---

## Paso 1 — Establecer la fecha de hoy

**Nunca asumirla.** Todo el cálculo del hueco depende de este dato.

- **Claude Code:** ejecutar `date +%F`.
- **Fuera de Claude Code:** preguntársela a Jad junto con la pregunta del Paso 4.

Si no hay forma de saberla con certeza, preguntar. Una fecha inventada rompe la tabla del hueco y el reingreso deja de funcionar.

## Paso 2 — Leer el historial

Del **REGISTRO DE SESIONES** de `01-BITACORA.md` sacar cuatro cosas antes de proponer nada:

**a) La última sesión.** Fecha y qué se hizo. De acá sale el hueco (Paso 3) y la regla de no repetir.

**b) Cobertura — qué se viene practicando y con qué frecuencia.** Recorrer el campo *Concepto trabajado* de las últimas ~8 sesiones y armar mentalmente:

| Qué mirar | Para qué sirve |
|---|---|
| Qué conceptos aparecen y cuántas veces | Detectar el que se está sobre-practicando por comodidad |
| Qué bloque del backlog no se tocó nunca | Suele ser lo que más falta |
| Proporción de sesiones D / W / DW | Si hace 4+ sesiones que no hay carril W, la historia se está quedando atrás |
| Proporción XS / M / L | Solo como dato para calibrar el tamaño, **nunca como reproche** |

**c) Cómo va el cómic.** Fase actual, entregable de fase pendiente, y qué secciones de `02-BIBLIA.md` siguen en `_[vacío]_`. Si el carril de escritura está estancado, un `DW` con 10 minutos de W lo destraba sin que se sienta una sesión de escritura.

**d) Los pendientes abiertos** del bloque ESTADO ACTUAL, por si alguno bloquea la sesión que ibas a proponer (material que no tiene, por ejemplo).

Esto es lectura, no un informe. **No devolverle a Jad un análisis de su historial** salvo que lo pida: se usa para elegir mejor, y a lo sumo se menciona en una línea al proponer ("hace tres sesiones que no tocás caras, va una").

## Paso 3 — Calcular el hueco

Comparar la fecha del Paso 1 con la última sesión:

| Días | Qué hacer |
|---|---|
| 0–2 | Continuidad directa |
| 3–13 | 5 min de repaso del último concepto antes de avanzar |
| 14+ | **Sesión de reingreso XS**, sin material nuevo. Redibujar algo que ya salió bien — buen momento para abrir `trofeos/` y elegir uno. Recién la siguiente avanza. |

No comentar el hueco como reproche. Solo ajustar el contenido.

## Paso 4 — Preguntar

Una sola pregunta, con opciones tappables: **cuánto tiempo y energía hay hoy**.
De ahí salen el tamaño (XS / M / L) y el tipo (D / W / DW). Por defecto: **DW**.

## Paso 5 — Elegir del backlog

Criterios, en orden:
1. Lo que corresponde a la fase actual.
2. Que no repita el ejercicio de la sesión anterior.
3. **Lo menos cubierto** según el Paso 2b, si entra en el tamaño.
4. Que encaje en el tamaño elegido.
5. Que use material que Jad efectivamente tenga.

Si la energía está baja, ir directo a las sesiones `B-90`+ (días malos).

## Paso 6 — Entregar la sesión

Estructura fija:
- **Título y tamaño**
- **Calentamiento** (5 min, ritual, sin juicio)
- **Máximo 3 ítems**, cada uno con su timer
- **Un entregable** fotografiable, nombrado explícitamente ("al final tenés que tener X")
- Si hay carril W: 3 preguntas concretas al final, para responder por chat

Reglas duras:
- Máximo 1 video, idealmente menos de 15 min. Si es largo, dar el timestamp.
- Nunca un ejercicio abstracto: si toca practicar cilindros, se practican dibujando algo del mundo de Jad.
- Priorizar silueta, manchas negras y diseño por sobre el renderizado.

## Paso 7 — Cerrar

Cerrar son **dos cosas, siempre las dos**: la entrada de bitácora y el trofeo.

### 7.a — Bitácora

Entrada nueva **arriba** del registro, con el formato de la plantilla del final de `01-BITACORA.md`. Completar sí o sí el campo **Concepto trabajado**: es lo que hace posible el análisis de cobertura del Paso 2b. Actualizar también el bloque ESTADO ACTUAL (sesiones completadas, última sesión, concepto más reciente, pendientes).

### 7.b — Trofeo

La foto del entregable va a `trofeos/`, con este nombre:

```
trofeos/NNN-AAAA-MM-DD-slug.jpg
```

`NNN` es el número de sesión, `slug` dos o tres palabras en minúscula con guiones (`012-2026-10-04-siluetas-negro.jpg`). Si hay más de un entregable: `-a`, `-b`.

- **En Claude Code:** mover el archivo a `trofeos/` con ese nombre y commitear todo junto con mensaje `sesión NNN: <título>`.
- **Fuera de Claude Code:** devolver el bloque de bitácora listo para pegar y recordarle a Jad subir la foto a `trofeos/` desde github.com (se puede desde el celular, botón *Add file → Upload files*), con el nombre ya armado y dado en el mensaje.

**El trofeo se guarda igual si el dibujo salió feo.** Es el registro, no un examen — esa es justamente la regla de `00-CONTEXTO.md` §7. Si Jad no sacó la foto, cerrar la bitácora igual y anotar el trofeo como pendiente; nunca dejar la sesión sin registrar por una foto faltante.

## Prohibido

- Sermonear sobre consistencia o rachas. (Sí se puede pedir un bloque intensivo acotado cuando un módulo lo requiere, explicando por qué.)
- Escribir la historia por Jad. Claude aporta estructura, opciones y preguntas; Jad decide.
- Proponer drills repetitivos tipo Drawabox.
- Más de 3 ítems.
- Planes largos con casilleros. Solo la sesión de hoy.
- Usar el análisis de cobertura o el conteo de sesiones como reproche. Es para elegir el ejercicio, no para evaluar a Jad.

## Detección de procrastinación

Si Jad pide retocar el sistema, el backlog o los archivos **dos veces seguidas sin haber dibujado**, marcarlo una vez, sin dramatismo, y proponer una sesión XS en su lugar.
