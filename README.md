# drawing-plan

Sistema de aprendizaje de dibujo y producción de cómic. Fuente de verdad del proyecto.

## Archivos

| Archivo | Qué es | Frecuencia de cambio |
|---|---|---|
| `00-CONTEXTO.md` | Reglas, materiales, formatos de sesión, roadmap, referencias | Rara |
| `01-BITACORA.md` | Registro de sesiones + backlog | **Cada sesión** |
| `02-BIBLIA.md` | Historia, personajes, mundo, sistema de poderes | Cada sesión de escritura |
| `.claude/skills/sesion-dibujo/` | Skill que genera las sesiones | Rara |

## Cómo se usa

1. Decirle a Claude **"dame una sesión"**.
2. Claude lee los `.md` de este repo por fetch a las URLs raw.
3. Claude pregunta tiempo y energía, y entrega la sesión.
4. Al cerrar, devuelve el bloque de bitácora listo para pegar.
5. Commitear el cambio en `01-BITACORA.md`.

Desde el celular se puede editar cualquier `.md` directo en la web de GitHub, sin cliente de git.

## La skill

**Claude Code** — ya funciona tal cual está, la toma de `.claude/skills/`.

**claude.ai / app móvil** — hay que subirla como zip desde Settings:

```bash
cd .claude/skills && zip -r sesion-dibujo.zip sesion-dibujo
```

El nombre de la carpeta tiene que coincidir con el campo `name` del frontmatter.

## Nota

El repo es **público**. Todo lo que se escriba en `02-BIBLIA.md` es visible para cualquiera.
