# ARCHITECTURE.md

The architecture document for this repository, following the
[architecture.md](https://architecture.md) schema — built so an agent (or a
new colleague) can comprehend the codebase from this file alone. Fill every
section; delete nothing. Update it in the same change that alters the
architecture it describes. The conventions section (§12) is the join with
our house standards: the structure it describes is enforced by gates, not
agreement.

## 1. Project Structure

High-level overview of the directory and file structure, categorised by
architectural layer or major functional area — enough to navigate and locate
responsibilities quickly.

```
[Project Root]/
├── src/                  # [describe the module layout — module-first, lowercase]
├── tests/                # [mirrors src/]
├── docs/                 # [developer manual, flows]
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

The main components of the system — for each: name, primary responsibility,
key technologies, deployment target.

### 3.1. [Component Name]

Description: [purpose and how users or systems interact with it]

Technologies: [language, framework, key libraries]

Deployment: [where it runs]

## 4. Data Stores

The databases and persistent storage — for each: name, type, purpose, key
schemas/collections (names only).

## 5. External Integrations / APIs

Third-party services and external APIs — for each: name, purpose,
integration method (REST, SDK, webhook).

## 6. Deployment & Infrastructure

Cloud provider, key services, CI/CD pipeline, monitoring and logging.

## 7. Security Considerations

Authentication, authorization, encryption in transit/at rest, security
tooling and practices.

## 8. Development & Testing Environment

Local setup (link CONTRIBUTING.md or brief steps), testing frameworks, code
quality tools.

## 9. Future Considerations / Roadmap

Known architectural debt, planned major changes, significant future features
that impact the architecture.

## 10. Project Identification

Project Name: [name]

Repository URL: [url]

Primary Contact/Team: [owner]

Date of Last Update: [YYYY-MM-DD]

## 11. Glossary / Acronyms

Project-specific terms and acronyms, defined.

## 12. Conventions & Boundaries

The house standards this repository adheres to — the full contract lives in
the `software-architecture` skill; this section records what is enforced
HERE.

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
- **Documentation surfaces**: WHY comments at the change site; the
  developer manual (`docs/developer-manual.md`) updated when a flow
  changes; the behavioral contract (`scenarios.md`) amended only by the
  owner.
