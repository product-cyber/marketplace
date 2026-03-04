# product-cyber Marketplace

Claude Code Marketplace fuer das zipmend Hackathon-Team.

## Quick Start

```bash
# Marketplace hinzufuegen
/plugin marketplace add product-cyber/marketplace

# Alle Plugins anzeigen
/plugin

# Plugin installieren
/plugin install clemens@product-cyber
```

## Plugins

| Plugin | Autor | Inhalt |
|--------|-------|--------|
| `clemens` | Clemens | 16 Agents, 8 Commands, 9 Templates |

---

## Eigenes Plugin hinzufuegen

### 1. Ordner anlegen

```
plugins/dein-name/
├── .claude-plugin/
│   └── plugin.json
├── agents/
│   └── dein-agent.md
├── commands/
│   └── dein-command.md
└── templates/
    └── dein-template.md
```

### 2. plugin.json erstellen

```json
{
  "name": "dein-name",
  "description": "Beschreibung deines Plugins",
  "version": "1.0.0",
  "author": {
    "name": "Dein Name",
    "email": "deine@email.com"
  }
}
```

### 3. In marketplace.json registrieren

Fuege unter `"plugins"` einen neuen Eintrag hinzu:

```json
{
  "name": "dein-name",
  "source": "./plugins/dein-name",
  "description": "Beschreibung",
  "version": "1.0.0",
  "author": {
    "name": "Dein Name"
  }
}
```

### 4. Push und Update

```bash
git add . && git commit -m "Add plugin: dein-name" && git push
```

Die anderen Teilnehmer updaten mit:
```bash
/plugin marketplace update product-cyber
```

---

## Plugin: clemens

### Workflow

```
Discovery --> Wireframes --> Architecture --> Planning --> Implementation --> Testing
    |              |               |              |              |              |
  Gate 0        Gate 0          Gate 1        Gate 2/3     Code Review     QA Manual
```

### Agents (16)

| Agent | Phase | Beschreibung |
|-------|-------|--------------|
| `discovery` | Discovery | Feature-Konzeption mit Diverge/Converge Pattern |
| `wireframe` | Discovery | ASCII-Wireframes aus Discovery-Docs |
| `discovery-wireframe-compliance` | Discovery | Gate 0: Bidirektionale Validierung |
| `ux-expert-review-de` | Discovery | Senior UX Expert Review (DE) |
| `architecture` | Architecture | Technische Architektur-Konzeption |
| `architecture-compliance` | Architecture | Gate 1: Architecture-Validierung |
| `slice-writer` | Planning | Slice-Spezifikationen schreiben |
| `slice-compliance` | Planning | Gate 2: Slice-Validierung |
| `integration-map` | Planning | Gate 3: E2E-Integration |
| `slice-implementer` | Implementation | Fokussierte Slice-Implementierung |
| `code-reviewer` | Implementation | Adversarial Code Review |
| `debugger` | Implementation | Systematische Fehlersuche |
| `test-writer` | Testing | Tests gegen Acceptance Criteria |
| `test-validator` | Testing | Test-Pipeline mit Auto-Detection |
| `qa-manual` | Testing | Gefuehrtes manuelles Testing |
| `roadmap` | Strategy | Strategische Produkt-Orientierung |

### Commands (8)

| Command | Beschreibung |
|---------|--------------|
| `/discovery` | Feature-Konzeption starten |
| `/wireframe` | Wireframes + UX Review + Gate 0 |
| `/pm-ux-review-de` | Manueller UX Expert Review |
| `/architecture` | Architecture + Gate 1 Compliance |
| `/planner` | Slice-Planning + Gate 2/3 |
| `/orchestrate` | Feature-Implementation (6-Step Pipeline) |
| `/qa-manual` | Manuelles QA-Testing |
| `/roadmap` | Strategische Roadmap |

### Templates (9)

| Template | Zweck |
|----------|-------|
| `discovery-feature.md` | Feature-Discovery Dokument |
| `wireframe-template.md` | ASCII-Wireframe Spezifikation |
| `architecture-feature.md` | Technische Architektur-Spec |
| `plan-spec.md` | Slice-Spezifikation |
| `checkpoint-example.md` | Progress-Tracking |
| `ui-implementation-checklist.md` | UI-Implementation Checkliste |
| `roadmap.md` | Roadmap-Definition |
| `project.md` | Projekt-Dokumentation |
| `summary.md` | Session-Summary |
