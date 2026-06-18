# HCAM-SKG™ AKU Governance

| Attribute | Value |
|------------|------------|
| File | `docs/aku-governance.md` |
| Framework | HCAM™ Spiritual Knowledge Graph (HCAM-SKG™) |
| Parent Framework | HCAM™ Atomic Knowledge Unit (HCAM-AKU™) |
| Corpus | `HCAM-SPIRIT-HANUMAN-CHALISA-V1` |
| Version | 1.0 |

---

# 1. Purpose

This document defines governance rules for creating, validating, maintaining, updating, merging, deprecating, and reusing HCAM™ Atomic Knowledge Units inside the HCAM™ Spiritual Knowledge Graph.

The purpose is to ensure that every AKU remains:

- evidence-grounded
- conceptually clear
- reusable
- machine-readable
- retrieval-ready
- context-aware
- boundary-controlled
- scalable across future corpora

AKU governance prevents the corpus from becoming a loose collection of interpretations.

It ensures that every knowledge unit functions as a structured, governed, AI-trainable object.

---

# 2. Core Governance Principle

An HCAM-AKU™ is not a commentary.

An HCAM-AKU™ is a governed knowledge object.

Each AKU must represent one complete concept with:

- Evidence
- Definition
- Concepts
- Context
- Boundaries
- Relationships
- Reasoning
- Evaluation
- Retrieval Signals
- Practice Mapping
- Anchors
- Packaging Assets

The AKU must be understandable by humans and usable by machines.

---

# 3. AKU Definition

An HCAM™ Atomic Knowledge Unit is a structured, self-contained knowledge object designed to represent a single concept in a machine-readable, retrievable, explainable, and reusable format.

Inside HCAM-SKG™, an AKU converts spiritual knowledge into a concept-level unit that can support:

- AI retrieval
- RAG systems
- knowledge graph construction
- multilingual cognition
- learning systems
- fine-tuning datasets
- conversational AI grounding
- spiritual education workflows

---

# 4. AKU Creation Rule

An AKU should be created only when there is enough evidence to support a distinct concept.

Do not create an AKU merely because a verse, chaupai, or passage exists.

The correct structure is:

```text
Evidence
    ↓
AKU
```

not:

```text
Every verse must permanently become a separate AKU
```

In the Hanuman Chalisa evaluation corpus, 40 chaupais have been mapped to 40 primary AKUs for proof-of-concept clarity.

However, in future corpora, multiple evidence units may support the same AKU.

---

# 5. AKU Reuse Principle

The same AKU may be supported by multiple evidence units across multiple scriptures.

### Example

```text
Courage
```

may be supported by:

- Hanuman Chalisa
- Bhagavad Gita
- Ramayana
- Mahabharata
- Upanishads

In future versions, shared AKUs may become cross-corpus knowledge objects.

This means:

```text
One AKU
can have
many evidence sources
```

---

# 6. AKU ID Policy

## Current Hanuman Chalisa Pattern

```text
HCAM-SPIRIT-HC-XXXX
```

### Example

```text
HCAM-SPIRIT-HC-0001
```

## Future Corpus Patterns

```text
HCAM-SPIRIT-BG-0001
HCAM-SPIRIT-SK-0001
HCAM-SPIRIT-RM-0001
HCAM-SPIRIT-MB-0001
HCAM-SPIRIT-UP-0001
```

## Cross-Corpus Canonical AKU Pattern

For future shared AKUs across scriptures:

```text
HCAM-SKG-AKU-XXXX
```

### Example

```text
HCAM-SKG-AKU-0001
```

This may be used when one concept becomes a reusable master AKU across multiple spiritual corpora.

---

# 7. AKU Lifecycle

Each AKU should move through a defined lifecycle.

---

## 7.1 Draft

The AKU has been created but not reviewed.

### Status

```text
Draft
```

### Allowed Use

- internal development
- early testing
- structure review

### Not Recommended For

- public citation
- production deployment
- commercial use

---

## 7.2 Reviewed

The AKU has been structurally reviewed.

### Status

```text
Reviewed
```

### Review Checks Include

- evidence linkage
- definition clarity
- concept extraction
- retrieval relevance
- boundary clarity
- relationship consistency

---

## 7.3 Validated

The AKU has passed governance review.

### Status

```text
Validated
```

### Validation Checks Include

- correct ID
- correct evidence link
- non-generic definition
- clear boundaries
- usable retrieval queries
- relevant life-situation mapping
- accurate practice mapping
- no unsupported claims

---

## 7.4 Published

The AKU is part of a public corpus release.

### Status

```text
Published
```

### Published AKUs May Be Used For

- public repository display
- educational reference
- research evaluation
- RAG testing
- corpus demonstration
- knowledge graph traversal

---

## 7.5 Deprecated

The AKU is no longer recommended for active use.

### Status

```text
Deprecated
```

### Reasons May Include

- duplicate concept
- weak evidence support
- better replacement available
- naming improvement
- scope mismatch

Deprecated AKUs should not be deleted immediately.

They should remain traceable.

---

## 7.6 Merged

The AKU has been merged into another AKU.

### Status

```text
Merged
```

### Example

```text
HCAM-SPIRIT-HC-0003
merged_into
HCAM-SKG-AKU-0007
```

Used when multiple AKUs represent the same concept.

---

## 7.7 Archived

The AKU is preserved for historical record but removed from active corpus use.

### Status

```text
Archived
```

Archived AKUs should not be used for new retrieval, training, or graph expansion unless explicitly reactivated.

---

# 8. Required AKU Fields

Each AKU should include:

```json
{
  "aku_id": "",
  "aku_name": "",
  "domain": "",
  "definition": "",
  "supported_by": []
}
```

### Recommended Extended Fields

```json
{
  "status": "",
  "version": "",
  "concepts": [],
  "life_situations": [],
  "practices": [],
  "retrieval_units": [],
  "relationships": [],
  "anchors": [],
  "boundary_layer": {},
  "reasoning_layer": {},
  "evaluation_layer": {},
  "packaging_layer": {}
}
```

---

# 9. AKU Definition Rules

A definition must be:

- clear
- concept-specific
- non-preachy
- non-sectarian
- evidence-aligned
- reusable
- machine-readable

### Avoid

```text
This chaupai teaches us that...
```

### Prefer

```text
[Concept Name] is the principle that...
```

### Example

> Wisdom And Virtue As Foundational Excellence is the principle that true greatness begins with deep understanding, noble qualities, ethical clarity, and character-based influence.

---

# 10. Evidence Grounding Rule

Every AKU must be supported by at least one evidence unit.

### Required

```json
"supported_by": ["HC-EVIDENCE-CH-001"]
```

An AKU without evidence should not be published.

For future corpora, one AKU may have multiple evidence links:

```json
"supported_by": [
  "HC-EVIDENCE-CH-001",
  "BG-EVIDENCE-CH-002-047",
  "RM-EVIDENCE-AYODHYA-012"
]
```

---

# 11. Concept Extraction Rule

Each AKU should identify:

### Core Concept

Wisdom

### Supporting Concept

Virtue

### Hidden Concept

Divine Recognition

### Practical Concept

Leadership

This ensures that each AKU supports both philosophical retrieval and practical retrieval.

---

# 12. Life-Situation Mapping Rule

An AKU may map to real-life human situations.

### Allowed Examples

- Fear
- Anxiety
- Self-Doubt
- Leadership Pressure
- Career Confusion
- Decision Making
- Purpose Seeking
- Relationship Challenges
- Emotional Recovery
- Discipline Failure
- Service Responsibility
- Purpose Confusion

Life-situation mapping should be practical but not therapeutic diagnosis.

Do not imply medical, clinical, legal, or psychological treatment unless the corpus has a validated domain-specific layer.

---

# 13. Practice Mapping Rule

An AKU may map to relevant practices.

### Allowed Examples

- Recitation
- Reflection
- Meditation
- Seva
- Japa
- Discipline
- Breath Awareness
- Self-Observation
- Value Review
- Gratitude Practice
- Mentor Reflection

Practice mapping should remain educational and reflective.

It should not claim guaranteed outcomes.

---

# 14. Retrieval Governance Rule

Each AKU should support multiple retrieval surfaces.

### Recommended Retrieval Categories

- User Questions
- Search Queries
- Conversational Queries
- Voice Queries

### Example

- How can I gain wisdom?
- Hanuman teaching on knowledge
- Prayer for clarity
- What does Hanuman Chalisa say about courage?

Retrieval queries should reflect how real users ask questions.

---

# 15. Boundary Governance Rule

Every AKU should define what it includes and excludes.

### Example

#### Includes

- Discernment
- Ethical clarity
- Applied knowledge

#### Excludes

- Blind memorization
- Intellectual arrogance
- Information overload

Boundary layers reduce hallucination and prevent overextended interpretations.

---

# 16. Reasoning Governance Rule

Each AKU may include IF → THEN logic.

### Example

```text
IF wisdom increases
THEN confusion decreases
```

Reasoning rules must be simple, non-dogmatic, and application-oriented.

They should not claim supernatural guarantees.

---

# 17. Evaluation Governance Rule

Each AKU should support assessment.

Evaluation may include:

- Assessment Questions
- Common Misunderstandings
- Error Patterns

### Example

#### Question

```text
Does wisdom mean memorization?
```

#### Common Misunderstanding

```text
Confusing information with wisdom.
```

#### Error Pattern

```text
Using knowledge without ethical clarity.
```

---

# 18. Relationship Governance Rule

Each AKU should connect to other objects using approved relationship vocabulary.

### Required Or Recommended Relationships

```text
SUPPORTED_BY
HAS_CONCEPT
MAPS_TO_LIFE_SITUATION
MAPS_TO_PRACTICE
HAS_RETRIEVAL_UNIT
HAS_ANCHOR
IS_PART_OF_CORPUS
```

### Optional Relationships

```text
RELATED_TO
OPPOSES
INCLUDES
EXCLUDES
DEPENDS_ON
HAS_REASONING_RULE
HAS_EVALUATION_CRITERIA
HAS_RAG_CHUNK
HAS_TRAINING_PAIR
CROSS_CORPUS_RELATED_TO
```

---

# 19. Anchor Governance Rule

Each AKU should include HCAM-style anchors where relevant.

### Anchor Types

- Hindi Memory Anchor
- Hinglish Recall Anchor
- Story Anchor

### Example

#### Hindi Memory Anchor

```text
ज्ञान का सागर, भ्रम से बाहर।
```

#### Hinglish Recall Anchor

```text
Information yaad reh sakti hai, wisdom direction deta hai.
```

#### Story Anchor

```text
Hanuman is praised first for wisdom before strength.
```

Anchors should support recall, not replace the AKU definition.

---

# 20. Packaging Governance Rule

Each AKU may include packaging assets for AI systems.

### Packaging Assets Include

- RAG Chunk
- Training Pair
- Fine-Tuning Pair
- Q&A Pair

These make the AKU usable for:

- RAG pipelines
- supervised fine-tuning
- AI assistants
- educational bots
- retrieval testing

---

# 21. Naming Governance Rule

AKU names should be:

- concise
- concept-driven
- reusable
- non-generic
- non-commentarial

### Good

```text
Wisdom And Virtue As Foundational Excellence
```

### Weak

```text
Meaning of Chaupai 1
```

### Good

```text
Obstacle Transformation Through Support And Grace
```

### Weak

```text
Hanuman Helps Devotees
```

---

# 22. Cross-Corpus Governance

When future corpora are added, AKUs should be reviewed for reuse.

### Examples

- Courage
- Service
- Wisdom
- Discipline
- Humility
- Devotion
- Purpose
- Protection
- Surrender
- Leadership

If the same concept appears in multiple corpora, the project may create a higher-level shared AKU.

### Example

```text
HCAM-SKG-AKU-COURAGE-0001
```

or

```text
HCAM-SKG-AKU-0007
```

This shared AKU may be supported by multiple evidence units.

---

# 23. Versioning Rule

Each AKU should support version tracking.

### Recommended Version Fields

```json
{
  "version": "1.0",
  "created_for_corpus": "HCAM-SPIRIT-HANUMAN-CHALISA-V1",
  "status": "Published",
  "last_reviewed": "",
  "revision_notes": []
}
```

### Version Changes Should Be Made When

- definition changes
- evidence support changes
- concept mappings change
- boundary layer changes
- relationship mapping changes
- lifecycle status changes

---

# 24. Review Checklist

Before publication, each AKU should pass the following checklist:

- AKU ID is unique
- AKU name is concept-based
- Definition is clear
- Evidence support exists
- Concepts are extracted
- Life situations are relevant
- Practices are relevant
- Retrieval queries are usable
- Relationships are valid
- Boundaries are clear
- Anchors are useful
- No unsupported claim exists
- No sectarian commentary is inserted
- No generic filler is used

---

# 25. Anti-Patterns

Avoid the following:

- One chaupai = one permanent AKU rule
- Generic spiritual commentary
- Preaching tone
- Unsupported interpretation
- Overclaiming outcomes
- Mixing Schema.org ontology inside native corpus files
- Duplicate AKUs without governance
- Unclear ID references
- Missing evidence support
- Unbounded concepts
- Vague relationship names

---

# 26. Publication Readiness Standard

A corpus may be marked publication-ready when:

- Evidence Registry is complete
- AKU Registry is complete
- Concept Registry is complete
- Life Situation Registry is complete
- Practice Registry is complete
- Retrieval Registry is complete
- Relationship Registry is complete
- Anchor Registry is complete
- Manifest is complete
- License is complete
- Governance documents are complete
- Example objects are available
- ID patterns are consistent

---

# 27. Governance Status for Hanuman Chalisa Corpus

### Current Corpus

```text
HCAM-SPIRIT-HANUMAN-CHALISA-V1
```

### Current Status

```text
Completed Evaluation Corpus
```

### Current AKU Model

```text
40 Chaupais
40 Evidence Units
40 Primary AKUs
```

### Governance Note

This one-to-one mapping is valid for the evaluation corpus.

Future HCAM-SKG™ corpora may use many-to-one evidence-to-AKU mapping when concepts repeat across scriptures.

---

# 28. Canonical Governance Rule

An HCAM-AKU™ should never be treated as a loose summary.

It must function as:

> a governed knowledge object

with evidence, definition, boundaries, relationships, retrieval signals, and application logic.

This is what allows HCAM-SKG™ to become a scalable spiritual knowledge graph rather than a collection of spiritual notes.

---

# Status

| Attribute | Value |
|------------|------------|
| Document | HCAM-SKG™ AKU Governance |
| Version | 1.0 |
| Corpus | HCAM-SPIRIT-HANUMAN-CHALISA-V1 |
| Status | Active |
| Next File |  |

---
