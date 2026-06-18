# HCAM-AKU™ Spiritual Corpus Ontology

| Attribute | Value |
|------------|------------|
| File | `docs/ontology.md` |
| Corpus ID | `HCAM-SPIRIT-HANUMAN-CHALISA-V1` |
| Ontology Version | 1.0 |
| Source Work | Hanuman Chalisa |

---

# 1. Purpose

This document defines the ontology used by the HCAM-AKU™ Spiritual Corpus.

The ontology is not a Schema.org ontology.

The ontology is a domain-specific HCAM-AKU™ Knowledge Ontology designed for:

- Knowledge Graph Construction
- Retrieval-Augmented Generation (RAG)
- Fine-Tuning Datasets
- AI Training Systems
- Educational Systems
- Spiritual Knowledge Architecture
- Multilingual Cognitive Retrieval

The ontology models spiritual knowledge as reusable Atomic Knowledge Units (AKUs).

---

# 2. Ontology Design Philosophy

Traditional spiritual texts are written for human interpretation.

AI systems require:

- explicit concepts
- explicit relationships
- explicit boundaries
- explicit contexts
- explicit retrieval signals

The HCAM-AKU™ Ontology transforms narrative scripture into structured knowledge objects.

The ontology follows:

```text
Source Text
→ Evidence
→ Concept
→ Knowledge Unit
→ Context
→ Relationship
→ Retrieval
→ Practice
→ Application
```

---

# 3. Core Ontology Layers

The ontology contains eight primary layers.

- Evidence Layer
- AKU Layer
- Concept Layer
- Context Layer
- Life Situation Layer
- Practice Layer
- Relationship Layer
- Retrieval Layer

These layers collectively create an AI-trainable spiritual knowledge graph.

---

# 4. Evidence Layer

## Entity Type

```text
EvidenceUnit
```

Represents original source evidence.

## Purpose

Preserves source traceability.

## Example

```json
{
  "evidence_id":"HC-EVIDENCE-CH-001",
  "source_work":"Hanuman Chalisa",
  "chaupai_number":"1"
}
```

## Relationships

```text
EvidenceUnit
SUPPORTS
AKU
```

---

# 5. AKU Layer

## Entity Type

```text
AtomicKnowledgeUnit
```

Represents a complete reusable spiritual concept.

## Purpose

Creates the smallest complete machine-readable knowledge object.

## Example

```json
{
  "aku_id":"HCAM-SPIRIT-HC-0001",
  "aku_name":"Wisdom And Virtue As Foundational Excellence"
}
```

## Relationships

```text
AKU
SUPPORTED_BY
EvidenceUnit
```

```text
AKU
HAS
Concepts
```

```text
AKU
MAPPED_TO
Life Situations
```

```text
AKU
MAPPED_TO
Practices
```

---

# 6. Concept Layer

## Entity Type

```text
Concept
```

Represents extracted knowledge concepts.

## Concept Categories

- Core Concept
- Supporting Concept
- Hidden Concept
- Practical Concept

## Example

```json
{
  "concept_id":"HC-CONCEPT-0001",
  "name":"Wisdom",
  "concept_type":"Core Concept"
}
```

## Relationship

```text
Concept
BELONGS_TO
AKU
```

---

# 7. Context Layer

## Entity Type

```text
ContextDomain
```

Represents practical application domains.

## Allowed Context Domains

- Personal Growth
- Career
- Leadership
- Education
- Relationships
- Decision Making
- Emotional Wellbeing
- Spiritual Practice

## Relationship

```text
AKU
APPLIES_TO
ContextDomain
```

---

# 8. Life Situation Layer

## Entity Type

```text
LifeSituation
```

Represents human situations that can trigger retrieval.

## Examples

- Fear
- Anxiety
- Self-Doubt
- Career Confusion
- Leadership Pressure
- Relationship Challenges
- Purpose Seeking
- Decision Making
- Failure Recovery
- Stress
- Overthinking
- Lack Of Confidence

## Relationship

```text
LifeSituation
TRIGGERS
AKU Retrieval
```

---

# 9. Practice Layer

## Entity Type

```text
Practice
```

Represents actions connected to AKUs.

## Core Practices

- Recitation
- Reflection
- Meditation
- Japa
- Seva
- Discipline
- Breath Awareness

## Applied Practices

- Wisdom Reflection
- Goal Visualization
- Humility Practice
- Values Alignment Review
- Mission Reflection
- Decision Review
- Resilience Practice

## Relationship

```text
Practice
REINFORCES
AKU
```

---

# 10. Retrieval Layer

## Entity Type

```text
RetrievalIntent
```

Represents discoverability pathways.

## Retrieval Types

- User Question
- Search Query
- Conversational Query
- Voice Query

## Examples

- How can I build courage?
- How can I overcome fear?
- What does Hanuman teach about service?
- Prayer for confidence.

## Relationship

```text
RetrievalIntent
POINTS_TO
AKU
```

---

# 11. Relationship Layer

## Entity Type

```text
ConceptRelationship
```

Represents conceptual graph links.

## Relationship Categories

- Related Concept
- Supporting Concept
- Dependent Concept
- Opposing Concept

## Example

```text
Wisdom
→ Clarity

Wisdom
→ Discernment

Wisdom
→ Humility

Wisdom
↔ Ignorance
(opposing)
```

---

# 12. Anchor Layer

## Entity Type

```text
MemoryAnchor
```

Represents cognitive recall structures.

## Anchor Types

- Hindi Memory Anchor
- Hinglish Recall Anchor
- Story Anchor

## Example

```text
ज्ञान का सागर, भ्रम से बाहर।

Wisdom gives direction.

Hanuman is praised for wisdom before strength.
```

## Relationship

```text
Anchor
STRENGTHENS
AKU Recall
```

---

# 13. Delivery Layer

## Entity Type

```text
DeliveryObject
```

Represents human-readable outputs.

## Delivery Types

- English Summary
- Hindi Summary
- Hinglish Summary
- Voice Explanation

## Relationship

```text
DeliveryObject
EXPLAINS
AKU
```

---

# 14. Packaging Layer

## Entity Type

```text
PackagingObject
```

Represents AI-ready training formats.

## Packaging Types

- RAG Chunk
- Training Pair
- Fine-Tuning Pair
- Question Answer Pair

## Relationship

```text
PackagingObject
TRAINS
AI Systems
```

---

# 15. Ontology Relationship Vocabulary

The corpus uses a controlled relationship vocabulary.

## Primary Relationships

```text
SUPPORTED_BY

HAS_CONCEPT

APPLIES_TO

MAPPED_TO

REINFORCES

POINTS_TO

RELATED_TO

SUPPORTS

DEPENDS_ON

OPPOSES

STRENGTHENS

EXPLAINS
```

Only approved relationships should be used in future corpus expansion.

---

# 16. Ontology Graph Model

The complete ontology graph is:

```text
Evidence
   ↓
AKU
   ↓
Concept
   ↓
Life Situation
   ↓
Practice
   ↓
Retrieval Intent
   ↓
Anchor
   ↓
Delivery
   ↓
Packaging
```

## Expanded Graph

```text
Evidence
    ↓
AKU
 ├── Concepts
 ├── Life Situations
 ├── Practices
 ├── Retrieval Queries
 ├── Anchors
 ├── Delivery Objects
 └── Packaging Objects
```

---

# 17. Hanuman Chalisa Corpus Statistics

Current corpus:

| Entity | Count |
|----------|----------|
| Evidence Units | 40 |
| Primary AKUs | 40 |
| Concepts | 160 |
| Life Situations | 200+ |
| Practices | 70 |
| Retrieval Units | 40 |
| Relationship Units | 40 |
| Anchor Units | 40 |

---

# 18. Future Ontology Expansion

The ontology supports future expansion to:

- Ramayana Corpus
- Bhagavad Gita Corpus
- Upanishad Corpus
- Vedic Knowledge Corpus
- B30Bharat Educational Corpus
- Corporate Leadership Corpus
- HCAM-AKU Universal Knowledge Graph

## Future Versions May Introduce

- Shared AKUs
- Cross-Corpus AKUs
- AKU Hierarchies
- AKU Clusters
- AKU Families
- AKU Inheritance

---

# 19. Ontology Governance Rules

Every future AKU must:

- Be supported by evidence.
- Have a unique AKU ID.
- Contain concepts.
- Contain retrieval mappings.
- Contain life-situation mappings.
- Contain practice mappings.
- Contain relationship mappings.
- Contain anchor mappings.

**No AKU may exist without source evidence.**

---

# 20. Canonical Ontology Statement

HCAM-AKU™ Spiritual Corpus Ontology is a domain-specific knowledge ontology that transforms spiritual literature into reusable, machine-readable, retrieval-ready Atomic Knowledge Units.

The ontology enables spiritual concepts to function as governed knowledge graph entities capable of supporting retrieval, reasoning, learning, AI training, and multilingual cognition while maintaining traceability to the original source evidence.

---

# Status

| Attribute | Value |
|------------|------------|
| Ontology Version | 1.0 |
| Corpus | HCAM-SPIRIT-HANUMAN-CHALISA-V1 |
| Status | Locked |
| Framework | HCAM-AKU™ Spiritual Corpus Ontology |

---
