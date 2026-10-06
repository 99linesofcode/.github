# ARCHITECTURE.md

The architecture document for this repository, following the
[architecture.md](https://architecture.md) schema — built so an agent (or a
new colleague) can comprehend the codebase from this file alone, and so this
repository's own architectural principles are visible in how it actually
works. Fill every section; delete nothing. Update it in the same change that
alters the architecture it describes.

## 1. Project Structure

High-level overview of the directory and file structure — module-first,
following the language's dominant convention. State where the logic lives:
which concerns sit in actions, which in pure calculations, which in domain
services — and why.

```
[Project Root]/
├── src/                  # [the module layout — one folder per bounded concept]
├── tests/                # [mirrors src/]
├── docs/                 # [developer manual — flows as sequence diagrams]
└── ...
```

## 2. High-Level System Diagram

A simple block diagram (C4 Level 1: System Context, or a basic component
diagram) or a clear text description: the major components, their
interactions, how data flows, where the architectural boundaries are.

```
[User] <--> [System] <--> [External Service]
```

## 3. Core Components

The main components — for each: name, primary responsibility, key
technologies, deployment target.

### Ports & adapters

List each port the core owns: the core NEED it serves (never the tool's
API it wraps), and the adapter(s) implementing it. If a component's logic
reaches around a port, that is a defect — document it as debt or fix it.

## 4. Data Stores

The databases and persistent storage — for each: name, type, purpose, key
schemas/collections (names only).

## 5. External Integrations / APIs

Third-party services and external APIs — for each: name, purpose,
integration method (REST, SDK, webhook). Note which port each integration
sits behind.

## 6. Deployment & Infrastructure

Cloud provider, key services, CI/CD pipeline, monitoring and logging.

## 7. Security Considerations

Authentication, authorization, encryption in transit/at rest, security
tooling and practices.

## 8. Development & Testing Environment

Local setup (link CONTRIBUTING.md or brief steps), testing frameworks, code
quality tools — including the mechanical gates (boundary enforcement,
invariance tests) and what each gate makes impossible.

## 9. Future Considerations / Roadmap

Known architectural debt, planned major changes — and the **deliberate
non-goals**: what the lean guardrail excluded, and why. A non-goal recorded
here is a decision; one that isn't recorded gets re-proposed every quarter.

## 10. Project Identification

Project Name: [name]

Repository URL: [url]

Primary Contact/Team: [owner]

Date of Last Update: [YYYY-MM-DD]

## 11. Glossary / Acronyms

Project-specific terms and acronyms, defined.

## 12. Conventions & Boundaries

The house standards this repository adheres to — stated here in full; this
section records what is enforced HERE, and by which gate.

- **Folder structure**: module-first, following the language's dominant
  convention (PSR-4 in PHP; lowercase module folders in TypeScript). The
  path locates the module; the name locates the role.
- **File naming**: the language's convention for classes vs pure functions
  (PascalCase classes with role suffixes, camelCase function files in
  TypeScript).
- **Entry point**: at the conventional root (`src/main.ts` for apps,
  `src/index.ts` for libraries) — above the modules, never inside one.
- **Dependency matrix**: which modules may import which, enforced
  mechanically (eslint-plugin-boundaries, deptrac, or the language's
  equivalent boundary gate) — a naming standard without a gate erodes one
  change at a time.
- **Provider neutrality**: provider names appear only in provider modules
  and the composition root; shared and cross-cutting vocabulary is neutral.
- **Canonical DTOs**: one canonical shape per domain concept, owned by the
  core; diff/merge logic operates on canonical fields only. A DTO mimicking
  a provider's structure is a provider shape, whatever its file name.
- **Documentation surfaces**: WHY comments at the change site; the
  developer manual (`docs/developer-manual.md`) updated when a flow
  changes; the behavioral contract amended only by the owner.
