# Memory

This file is the working project memory for AI agents.

Eligibility, routing between this file and `1c-templates-mcp` (`remember` / `recall`),
fallback when the MCP server is unavailable — see `AGENTS.md → Project memory`.
There are no permanent entries yet.

Entry format (one entry = one self-contained rule). Use English for narrative,
preserve original 1C identifiers (objects, modules, attributes) as-is:

<!--
## YYYY-MM-DD — <short rule title>

- **Scope:** module / subsystem / object where the rule applies (e.g. `Документ.РеализацияТоваровУслуг`).
- **Rule:** what must / must not be done.
- **Why:** consequence of violation (production breakage / data loss / regulatory / data leak).
- **Source:** user request, incident, or external document that established the rule.
-->

## Captured during work (no remember available)

<!-- Populated only when `1c-templates-mcp` is offline; migrate to `remember` once it is back. -->

## 2026-07-13 — питДанныеПродажФронта button code location

- **Scope:** `Документ.питДанныеПродажФронта`.
- **Rule:** `ПЛ_КодКнопки` belongs to tabular section `Товары`, not to the document header.
- **Why:** Queries that read `Чек.ПЛ_КодКнопки` from the document header fail or
  miss item mappings; use `Документ.питДанныеПродажФронта.Товары`.
- **Source:** User correction during review of
  `MRS_ПомощникЗакрытияСменыСервер.СтатусШагаСопоставление`.

