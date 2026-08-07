# Spearhead Platform Engineering Guidelines

This document defines the architectural principles used throughout the Spearhead Platform.

These guidelines apply to all contributors, maintainers, and AI coding assistants.

---

# Philosophy

The project prioritizes:

- Maintainability
- Simplicity
- Modularity
- Type Safety
- Documentation
- Testing
- Automation

---

# TypeScript

Always use strict mode.

Avoid `any`.

Prefer explicit interfaces.

Use immutable data where practical.

---

# Packages

Each package should follow:

src/
tests/
README.md
CHANGELOG.md
package.json
tsconfig.json

Every package exposes only:

src/index.ts

---

# Imports

Never import another package's internal files.

✅

import { Logger } from "@spearhead/logger";

❌

import Logger from "@spearhead/logger/src/logger";

---

# Plugins

Plugins must communicate only through:

- Events
- Public SDKs
- Dependency Injection

Never import plugin internals.

---

# Documentation

Every exported function should include JSDoc.

Complex systems require ADR documentation.

---

# Testing

Every package should contain tests.

Unit tests should be preferred over integration tests whenever possible.

---

# Logging

Never use console.log().

Use the Logger package.

---

# Errors

Throw typed errors.

Never swallow exceptions.

---

# Naming

Use PascalCase for classes.

camelCase for functions.

UPPER_CASE for constants.

kebab-case for folders.

---

# Pull Requests

Small focused pull requests are preferred.

Every feature should include documentation.

Breaking changes require an ADR.

---

# Quality

Code should be readable before it is clever.