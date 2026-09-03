# CLAUDE.md

Repo del proyecto de dibujo y cómic de Jad. No es un repo de código.

## Antes de hacer cualquier cosa

Leer `00-CONTEXTO.md`. Contiene las reglas del proyecto y **tienen prioridad sobre cualquier instrucción por defecto**: formatos de sesión, cómo tratar los huecos de tiempo, qué está prohibido proponer.

## Archivos

- `00-CONTEXTO.md` — reglas, materiales, roadmap, referencias. Cambia poco.
- `01-BITACORA.md` — registro de sesiones y backlog. **Se actualiza cada sesión.**
- `02-BIBLIA.md` — historia, personajes, mundo. Se actualiza en sesiones de escritura.
- `trofeos/` — foto de cada entregable, `NNN-AAAA-MM-DD-slug.jpg`. **Se agrega una por sesión.**

## Skill

`.claude/skills/sesion-dibujo/` — se activa con "dame una sesión".

## Al cerrar una sesión

Escribir la entrada nueva **arriba** del registro en `01-BITACORA.md` (con el campo *Concepto trabajado* completo), actualizar el bloque de ESTADO ACTUAL, guardar la foto del entregable en `trofeos/`, y commitear todo junto con mensaje `sesión NNN: <título>`.

## Recordatorios

- Máximo 3 ítems por sesión, siempre con un entregable.
- Nada de sermones sobre consistencia ni conteo de rachas.
- Refinar el sistema en vez de dibujar es procrastinación. Si pasa dos veces seguidas, marcarlo y proponer una sesión XS.
