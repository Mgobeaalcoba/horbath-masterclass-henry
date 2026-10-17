# AGENTS.md — Intelligent Request Automation (Horbath × Henry)

Guía para cualquier agente (Claude Code, Codex, Antigravity/Gemini, Copilot). Los puentes `CLAUDE.md`, `GEMINI.md` y `.github/copilot-instructions.md` apuntan a este archivo.

## Qué es

Automation de n8n que convierte solicitudes internas recibidas por email en registros estructurados: detecta emails nuevos, extrae y clasifica la solicitud con IA, valida confianza y campos obligatorios, pide información faltante, registra todo en Google Sheets y notifica por categoría en Slack. Material de masterclass para Henry (instructora: Mariano Gobea Alcoba). Repo público.

## Estructura

- `automation/` — `workflow.template.json` (workflow de n8n para importar) + README.
- `docs/` — `problem-and-solution.md`, `data-contract.md`, `configuration.md`, `safety.md`.
- `presentation/` — material de clase.
- `README.md` — guía general y cómo obtener la automation.

## Cómo trabajar acá

- Mantener `workflow.template.json` importable y sin credenciales (placeholders).
- Si cambia el flujo, sincronizar `data-contract.md` y `configuration.md`.
- Documentación en español; respetar la estructura de las docs existentes.

## Estado

Material publicado; última actividad registrada: julio de 2026.

## Memoria de sesiones

- `memory/STATE.md` (foto del estado) y `memory/LOG.md` (historial *append-only*).
- Al cerrar una sesión con cambios: actualizar STATE, agregar la entrada en LOG y commitear; `scripts/scan_secrets.py` corre como hook pre-commit.
