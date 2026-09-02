---
name: sesion-dibujo
description: Genera una sesión de práctica de dibujo o escritura para el proyecto de cómic de Jad. Usar cuando Jad pida "una sesión", "dame una sesión", "qué hago hoy", "arranquemos", o cuando quiera registrar/cerrar una sesión ya hecha. También al pedir ajustar el backlog o revisar el progreso. No usar para preguntas sueltas sobre dibujo o cómics que no impliquen armar una sesión.
---

# Generar una sesión

## Antes de responder

Leer los tres archivos del proyecto. **Primero desde el filesystem local** (Claude Code, repo clonado); si no están, por fetch a las URLs raw.

| Archivo | Local | Raw |
|---|---|---|
| Reglas, formatos, roadmap. **Manda sobre todo lo demás.** | `./00-CONTEXTO.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/00-CONTEXTO.md` |
| Última fecha, sesiones, backlog, pendientes | `./01-BITACORA.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/01-BITACORA.md` |
| Historia (solo si hay carril W) | `./02-BIBLIA.md` | `https://raw.githubusercontent.com/personal-jadesreznio/drawing-plan/main/02-BIBLIA.md` |

Si ninguna vía funciona, pedirle a Jad que pegue el contenido. **No inventar el historial.**

**En Claude Code:** escribir los cambios directo en los archivos y commitear. No hace falta devolver el bloque para pegar a mano.

## Paso 1 — Calcular el hueco

Comparar la fecha de hoy con la última sesión de la bitácora:

| Días | Qué hacer |
|---|---|
| 0–2 | Continuidad directa |
| 3–13 | 5 min de repaso del último concepto antes de avanzar |
| 14+ | **Sesión de reingreso XS**, sin material nuevo. Redibujar algo que ya salió bien. Recién la siguiente avanza. |

No comentar el hueco como reproche. Solo ajustar el contenido.

## Paso 2 — Preguntar

Una sola pregunta, con opciones tappables: **cuánto tiempo y energía hay hoy**.
De ahí salen el tamaño (XS / M / L) y el tipo (D / W / DW). Por defecto: **DW**.

## Paso 3 — Elegir del backlog

Criterios, en orden:
1. Lo que corresponde a la fase actual.
2. Que no repita el ejercicio de la sesión anterior.
3. Que encaje en el tamaño elegido.
4. Que use material que Jad efectivamente tenga.

Si la energía está baja, ir directo a las sesiones `B-90`+ (días malos).

## Paso 4 — Entregar la sesión

Estructura fija:
- **Título y tamaño**
- **Calentamiento** (5 min, ritual, sin juicio)
- **Máximo 3 ítems**, cada uno con su timer
- **Un entregable** fotografiable
- Si hay carril W: 3 preguntas concretas al final, para responder por chat

Reglas duras:
- Máximo 1 video, idealmente menos de 15 min. Si es largo, dar el timestamp.
- Nunca un ejercicio abstracto: si toca practicar cilindros, se practican dibujando algo del mundo de Jad.
- Priorizar silueta, manchas negras y diseño por sobre el renderizado.

## Paso 5 — Cerrar

Al terminar, entregar el bloque de bitácora **ya escrito y listo para pegar**, con el formato de la plantilla de `01-BITACORA.md`. Recordarle reemplazar el archivo en el Proyecto.

## Prohibido

- Sermonear sobre consistencia o rachas. (Sí se puede pedir un bloque intensivo acotado cuando un módulo lo requiere, explicando por qué.)
- Escribir la historia por Jad. Claude aporta estructura, opciones y preguntas; Jad decide.
- Proponer drills repetitivos tipo Drawabox.
- Más de 3 ítems.
- Planes largos con casilleros. Solo la sesión de hoy.

## Detección de procrastinación

Si Jad pide retocar el sistema, el backlog o los archivos **dos veces seguidas sin haber dibujado**, marcarlo una vez, sin dramatismo, y proponer una sesión XS en su lugar.
