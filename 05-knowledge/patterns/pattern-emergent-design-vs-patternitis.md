---
type: "pattern-analysis"
pattern: "emergent-design-vs-patternitis"
created: "2026-08-15"
domains: ["professional", "software-architecture"]
frequency: "high"
tags: ["#pattern", "#analysis", "#software-design", "#antipatterns", "#clean-code"]
---

# Pattern: Diseño Emergente vs. Patternitis

## Pattern Description
La tensión sistemática entre la introducción prematura de patrones de diseño orientados a objetos (denominada coloquialmente *Patternitis* o *Golden Hammer*) y la evolución pragmática del código mediante refactorización dirigida por necesidad comprobada (*Diseño Emergente*).

**Frequency:** Observada como principio rector fundamental en el análisis de patrones GoF.

**Domains:** Professional / Software Architecture / Technical Leadership

**Significance:** Es la principal causa de sobrecomplejidad accidental en bases de código empresariales. Comprender este patrón permite a los equipos mantener alta velocidad de entrega sin acumular deuda técnica por abstracciones vacías.

---

## Occurrences

### 2026-08-15 - [[03-professional/braindumps/braindump-2026-08-15-2257-catalogo-patrones-gof|braindump-2026-08-15-2257-catalogo-patrones-gof]]
**Context:** Definición y análisis riguroso de los 23 patrones GoF y la necesidad crítica de definir cuándo *NO* utilizarlos.

**Manifestation:** La necesidad recurrente de advertir contra el uso preventivo de patrones como Singleton, Visitor, Flyweight, Abstract Factory y Bridge sin una justificación matemática o funcional de peso.

**Outcome:** Creación de un filtro arquitectónico explícito de 3 pasos para justificar la introducción de cualquier patrón.

---

## Analysis

**What Triggers This Pattern:**
- Lectura de catálogos teóricos de patrones sin contexto de trade-offs.
- Miedo al cambio futuro (*Speculative Generality* / "por si acaso lo necesitamos").
- Falta de confianza en la capacidad de refactorizar de forma segura gracias a tests automatizados.

**What Follows This Pattern (Consecuencias de la Patternitis):**
- Proliferación de interfaces con una sola implementación.
- Dificultad para rastrear el flujo de ejecución (indirección innecesaria).
- Curva de aprendizaje empinada para nuevos desarrolladores.

**Cross-Domain Implications:**
- Aplica igualmente al diseño de microservicios, arquitecturas cloud-native y selección de stacks tecnológicos.

**Potential Actions:**
- **Promover:** Refactorizar hacia el patrón sólo cuando el dolor de la duplicación o la rigidez sea evidente.
- **Mitigar:** Preguntar siempre en code reviews: *"¿Qué problema concreto resuelve esta abstracción hoy?"*.

---

## Evolution Over Time
El diseño orientado a objetos tradicional tendía a crear jerarquías rígidas. En el ecosistema moderno (tipos inmutables, programación funcional, frameworks reactivos e inyección de dependencias), los 23 patrones GoF han evolucionado hacia composiciones mucho más ligeras y funcionales.

---

*Pattern identified through consolidation of 1 source document*
