# HCAM™ Spiritual Knowledge Graph (HCAM-SKG™)

**Structured Spiritual Wisdom Corpus for AI Retrieval, Knowledge Graphs, RAG, Fine-Tuning & Multilingual Cognition**

| Attribute | Value |
|------------|------------|
| Domain | Spirituality |
| Parent Framework | HCAM™ Atomic Knowledge Unit (HCAM-AKU™) |
| Parent Repository | HCAM-AKU™ Knowledge Graph |
| Folder | `hcam-skg` |
| Status | Active Development |

---

# What Is HCAM-SKG™?

HCAM™ Spiritual Knowledge Graph (HCAM-SKG™) is a structured, machine-readable spiritual knowledge architecture built using HCAM™ Atomic Knowledge Units (HCAM-AKU™).

It transforms wisdom literature, scriptures, philosophical texts, devotional works, spiritual teachings, and practice traditions into governed knowledge objects for:

- AI retrieval
- RAG systems
- Knowledge graph construction
- Fine-tuning datasets
- Multilingual cognition
- Educational systems
- Conversational AI grounding
- Voice query mapping
- Spiritual learning applications

HCAM-SKG™ is not a commentary project.

It is a corpus architecture project.

---

# Core Purpose

The purpose of HCAM-SKG™ is to convert spiritual knowledge from document form into structured concept-level intelligence.

Scripture
    ↓
Evidence
    ↓
Atomic Knowledge Unit
    ↓
Concepts
    ↓
Context
    ↓
Reasoning
    ↓
Retrieval
    ↓
Application

This allows spiritual knowledge to become:

- searchable
- explainable
- retrievable
- reusable
- multilingual
- AI-trainable
- graph-ready

---

# Why This Knowledge Graph Exists

Most spiritual texts exist as:

- books
- PDFs
- translations
- commentaries
- articles
- videos
- discourses

These formats are valuable for humans, but they are not optimized for machine interpretation.

AI systems need structured signals such as:

- concept identity
- evidence linkage
- life-situation mapping
- practice mapping
- retrieval queries
- reasoning logic
- scope boundaries
- relationship vocabulary
- multilingual anchors

HCAM-SKG™ provides this structure.

---

# HCAM-SKG™ Design Principle

> NOT merely digitize scripture.

Structure spiritual knowledge into machine-readable wisdom units.

Each corpus should preserve the source text while transforming its knowledge into structured HCAM-AKU™ objects.

---

# Current Corpus

## Hanuman Chalisa HCAM-AKU™ Spiritual Corpus

**Corpus ID**


HCAM-SPIRIT-HANUMAN-CHALISA-V1


**Status**


Completed Evaluation Corpus


**Coverage**

- 40 Chaupais
- 40 Evidence Units
- 40 Primary AKUs
- Concept Mappings
- Life Situation Mappings
- Practice Mappings
- Retrieval Mappings
- Relationship Mappings
- Anchor Mappings

**Purpose**


Proof of Concept
+
Evaluation Corpus
+
Feedback Corpus
+
Knowledge Graph Demonstration


---

# Current Folder Structure

# Current Folder Structure


hcam-skg/
├── README.md
├── future-corpora.md
└── hanuman-chalisa/
    ├── README.md
    ├── LICENSE.md
    ├── manifest.json
    │
    ├── corpus/
    │   ├── evidence.json
    │   ├── aku.json
    │   ├── aku-index.json
    │   ├── concepts.json
    │   ├── life-situations.json
    │   ├── practices.json
    │   ├── retrieval.json
    │   ├── relationships.json
    │   └── anchors.json
    │
    ├── docs/
    │   ├── corpus-methodology.md
    │   ├── ontology.md
    │   ├── hcam-aku-definition.md
    │   ├── jsonld-alignment.md
    │   ├── relationship-vocabulary.md
    │   └── aku-governance.md
    │
    └── examples/
        ├── chaupai-01-complete.json
        ├── chaupai-20-complete.json
        └── chaupai-40-complete.json


---

# HCAM-SKG™ Corpus Model

Each scripture or spiritual work may be converted into a corpus.

Each corpus contains:

- Evidence Registry
- AKU Registry
- Concept Registry
- Life Situation Registry
- Practice Registry
- Retrieval Registry
- Relationship Registry
- Anchor Registry
- Examples
- Documentation
- Manifest
- License



# Registry Files

## evidence.json

Contains source-based evidence units.

Each evidence unit preserves the source reference and connects it to supported AKUs.



## aku.json

Contains primary HCAM-AKU™ objects.

Each AKU represents a structured spiritual concept supported by one or more evidence units.



## aku-index.json

Provides lightweight lookup for:

- AKU ID
- AKU Name
- Evidence ID
- Chaupai Number
- Primary Theme

---

## concepts.json

Contains extracted concepts such as:

- Core Concepts
- Supporting Concepts
- Hidden Concepts
- Practical Concepts

---

## life-situations.json

Maps AKUs to real-life human situations such as:

- Fear
- Anxiety
- Self-Doubt
- Leadership Pressure
- Career Confusion
- Decision Making
- Purpose Seeking
- Relationship Challenges

---

## practices.json

Maps AKUs to relevant practices such as:

- Recitation
- Reflection
- Meditation
- Seva
- Japa
- Discipline
- Breath Awareness

---

## retrieval.json

Contains retrieval signals including:

- User Questions
- Search Queries
- Conversational Queries
- Voice Queries

---

## relationships.json

Defines graph relationships between:

- AKUs
- Concepts
- Evidence Units
- Life Situations
- Practices
- Opposing Concepts
- Supporting Concepts

---

## anchors.json

Contains HCAM cognitive anchors such as:

- Hindi Memory Anchors
- Hinglish Recall Anchors
- Story Anchors

---

# Naming Convention

## Domain Folder


hcam-skg


## Official Name


HCAM™ Spiritual Knowledge Graph


## Abbreviation


HCAM-SKG™

## Corpus ID Pattern


HCAM-SPIRIT-[SOURCE-WORK]-V[VERSION]

### Examples


HCAM-SPIRIT-HANUMAN-CHALISA-V1
HCAM-SPIRIT-BHAGAVAD-GITA-V1
HCAM-SPIRIT-SUNDAR-KAND-V1
HCAM-SPIRIT-RAMAYANA-V1
HCAM-SPIRIT-MAHABHARATA-V1
HCAM-SPIRIT-UPANISHAD-V1

---

## AKU ID Pattern


HCAM-SPIRIT-HC-0001


For future corpora, the short source code may change.

### Examples


HCAM-SPIRIT-BG-0001
HCAM-SPIRIT-SK-0001
HCAM-SPIRIT-RM-0001
HCAM-SPIRIT-MB-0001

---

# JSON Strategy

HCAM-SKG™ uses HCAM-native JSON for internal corpus storage.

The internal corpus files do not use Schema.org as the primary ontology.

Recommended internal structure:


{
  "schema_version": "HCAM-AKU-SPIRITUAL-CORPUS-V1.0",
  "corpus_id": "HCAM-SPIRIT-HANUMAN-CHALISA-V1",
  "registry_type": "AKU Registry"
}

Schema.org may be used separately as an external public discovery wrapper.

HCAM-KG™ custom context may be used for JSON-LD export when needed.

### Recommended Custom Context


https://ai.gurukulonroad.com/


### Recommended Namespace

https://ai.gurukulonroad.com

---

# Intended AI Use Cases

HCAM-SKG™ can support:

- Spiritual RAG systems
- AI knowledge assistants
- Fine-tuning dataset preparation
- Conversational spiritual search
- Voice-based spiritual guidance systems
- Educational content generation
- Multilingual spiritual learning
- Knowledge graph visualization
- Practice recommendation systems
- Life-situation based retrieval
- Comparative spiritual knowledge mapping

---

# Example Retrieval Pattern

A user may ask:


How can I overcome fear?


HCAM-SKG™ can retrieve:

- Relevant AKUs
- Supporting Chaupai
- Concepts
- Life Situation Mapping
- Practice Mapping
- Hindi Anchor
- Hinglish Recall Anchor
- Voice Query Match

This makes retrieval more grounded than a generic spiritual answer.

---

# Existing & Future Corpus Roadmap

Examples of HCAM-SKG™ already exists at Level 10 or may expand into many spiritual and wisdom traditions.

## Indic Examples

- Bhagavad Gita
- Sundar Kand
- Ramayana
- Mahabharata
- Upanishads
- Yoga Vasistha
- Srimad Bhagavatam
- Vishnu Sahasranama
- Lalita Sahasranama
- Durga Saptashati
- Gheranda Samhita
- Hatha Yoga Pradipika
- Shiva Samhita
- Tripura Rahasya

## Global Examples

- Dhammapada
- Tao Te Ching
- Bible
- Sufi Literature
- Stoic Literature
- Zen Texts
- Comparative Wisdom Literature

This roadmap is illustrative and not exhaustive.

---

# Commercial Separation

Public HCAM-SKG™ assets are intended for:

- evaluation
- research
- feedback
- educational reference
- knowledge graph demonstration
- methodology validation

Commercial deployments, custom scripture corpora, enterprise knowledge graphs, institutional learning systems, and production-grade HCAM-AKU™ systems may be governed under separate commercial agreements.

---

# License

Each corpus may contain its own license file.

The Hanuman Chalisa corpus uses:

HCAM™ Educational Reference, Research Use & Commercial Separation License (ERRCSL-1.0)

See the relevant corpus `LICENSE.md` file for permitted and restricted uses.

---

# Status

| Attribute | Value |
|------------|------------|
| Name | HCAM™ Spiritual Knowledge Graph |
| Abbreviation | HCAM-SKG™ |
| Parent Framework | HCAM™ Atomic Knowledge Unit |
| Repository | HCAM-AKU™ Knowledge Graph |
| Domain | Spirituality |
| Status | Active Development |
| Current Completed Corpus | HCAM-SPIRIT-HANUMAN-CHALISA-V1 |

---

# Canonical Definition

**HCAM™ Spiritual Knowledge Graph (HCAM-SKG™)** is a structured, machine-readable spiritual knowledge architecture built using **HCAM™ Atomic Knowledge Units (HCAM-AKU™)** that transforms wisdom literature, scriptures, philosophical texts, devotional works, and spiritual teachings into governed knowledge objects for retrieval, reasoning, education, multilingual cognition, and AI training.
