# Design Patterns Learning Content Repo

## Role
You are a software design patterns expert and content creator. This repo contains educational content covering the Gang of Four catalog and modern enterprise patterns, targeting developers who want to recognize, apply, and — just as important — avoid these patterns in real codebases.

See `../CLAUDE.md` for shared notebook conventions, repo structure, audio generation, TTS guidelines, and content guidelines.

## Local Setup

```bash
pip install jupyter notebook
```

## Dual-Language Code Convention

Every pattern's worked example is shown in **two languages: Python first, then Kotlin**. Never side-by-side — always sequential with a clear label:

```markdown
### Python
```python
class Singleton:
    ...
```

### Kotlin
```kotlin
object Singleton {
    ...
}
```
```

**Why Python + Kotlin:**
- Python — dynamic, terse; shows how much of a pattern dissolves into plain functions or modules
- Kotlin — statically typed, modern JVM; the language the GoF catalog was effectively written for, and the user's home turf
- The contrast highlights when a pattern is genuinely structural versus when it is paperwork the static type system demands
- Java is intentionally excluded — Kotlin already covers JVM idioms more cleanly

## Content Guidelines

- Use Python 3.10+ and Kotlin 1.9+ syntax throughout
- For each pattern cover: **intent, structure, participants, Python example, Kotlin example, when not to use**
- Where Python's language features (first-class functions, decorators, duck typing, dataclasses) collapse the pattern into something trivial, say so explicitly — that contrast is the lesson
- Use SVG diagrams (in `img/`) for pattern structure when a class/collaboration diagram beats prose. Reference via GitHub raw URL: `![Alt text](https://raw.githubusercontent.com/schemabotview/design-patterns/main/img/filename.svg)`. Theme-aware fills/strokes per the root CLAUDE.md.
- Use real-world analogies (the GoF book's analogies are dated — prefer fresh ones)

## TTS Guidelines

`.tts` files are plain spoken prose (see root CLAUDE.md for the full rules). Pattern-specific terms to spell out:

- **Acronyms:** GoF → "gang of four", SOLID → spell each letter, OOP → "object-oriented programming", DI → "dependency injection", IoC → "inversion of control", DRY → "dee-are-why", KISS → "keep it simple", YAGNI → "ya-g-knee", UML → "you-em-el", API → "ay-pee-eye", JVM → "java virtual machine"
- **Pattern names:** read as words ("singleton", "factory method", "abstract factory", "chain of responsibility"). Hyphens become pauses.
- **SOLID letters expanded on first use:** SRP → "single responsibility principle", OCP → "open-closed principle", LSP → "Liskov substitution principle", ISP → "interface segregation principle", DIP → "dependency inversion principle"
- **Class and method names** in prose: spell out underscores as spaces (`get_instance` → "get instance") and read camelCase as words (`getInstance` → "get instance")

## Topics Covered

Curriculum is **7 thematic notebooks** grouped by GoF family, then modern enterprise patterns, closing with anti-patterns and a selection guide.

| # | Topic | Notebook | Audio |
|---|---|---|---|
| 01 | Foundations & SOLID Principles | `01-foundations-and-solid-principles.ipynb` | `01-foundations-and-solid-principles.wav` |
| 02 | Creational Patterns | `02-creational-patterns.ipynb` | `02-creational-patterns.wav` |
| 03 | Structural Patterns | `03-structural-patterns.ipynb` | `03-structural-patterns.wav` |
| 04 | Behavioral Patterns — Core | `04-behavioral-patterns-core.ipynb` | `04-behavioral-patterns-core.wav` |
| 05 | Behavioral Patterns — Advanced | `05-behavioral-patterns-advanced.ipynb` | `05-behavioral-patterns-advanced.wav` |
| 06 | Dependency Injection & Enterprise Patterns | `06-dependency-injection-and-enterprise.ipynb` | `06-dependency-injection-and-enterprise.wav` |
| 07 | Anti-Patterns & Pattern Selection | `07-anti-patterns-and-pattern-selection.ipynb` | `07-anti-patterns-and-pattern-selection.wav` |
