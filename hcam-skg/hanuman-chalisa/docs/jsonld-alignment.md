# HCAM-KG™ JSON-LD Alignment Note

| Attribute | Value |
|------------|------------|
| File | `docs/jsonld-alignment.md` |
| Framework | HCAM™ Spiritual Knowledge Graph (HCAM-SKG™) |
| Corpus | `HCAM-SPIRIT-HANUMAN-CHALISA-V1` |
| Version | 1.0 |

---

# 1. Purpose

This document explains how JSON, JSON-LD, Schema.org, and HCAM-KG™ ontology should be used inside the HCAM™ Spiritual Knowledge Graph.

The purpose is to prevent ontology confusion.

HCAM-AKU™ is not a Schema.org ontology.

HCAM-AKU™ is a custom knowledge architecture designed for concept-level knowledge representation, retrieval, reasoning, AI training, multilingual cognition, and knowledge graph construction.

---

# 2. Core Decision

The internal corpus files should not use:

```json
{
  "@context": "https://schema.org"
}
```

because the internal objects are not pure Schema.org objects.

The internal corpus contains HCAM-specific entities such as:

- EvidenceUnit
- AtomicKnowledgeUnit
- ConceptLayer
- LifeSituation
- PracticeMapping
- RetrievalLayer
- ReasoningLayer
- EvaluationLayer
- BoundaryLayer
- AnchorLayer
- PackagingLayer

These are HCAM ontology objects.

Therefore, the preferred internal model is:

```json
{
  "schema_version": "HCAM-AKU-SPIRITUAL-CORPUS-V1.0",
  "corpus_id": "HCAM-SPIRIT-HANUMAN-CHALISA-V1"
}
```

not Schema.org JSON-LD.

---

# 3. Recommended Context Strategy

HCAM-KG™ should use its own context when JSON-LD export is required.

## Recommended Custom Context

```json
{
  "@context": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html"
}
```

## Alternative Namespace Options

```json
{
  "@context": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html"
}
```

or

```json
{
  "@context": {
    "hcam": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#",
    "skg": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#"
  }
}
```

---

# 4. Three-Layer Publishing Model

HCAM-KG™ should follow a three-layer model.

---

## Layer 1: Native HCAM JSON

This is the main corpus format.

Used for:

- RAG
- AI training
- internal graph construction
- GitHub dataset hosting
- corpus governance
- fine-tuning preparation

### Example

```json
{
  "schema_version": "HCAM-AKU-SPIRITUAL-CORPUS-V1.0",
  "corpus_id": "HCAM-SPIRIT-HANUMAN-CHALISA-V1",
  "registry_type": "AKU Registry"
}
```

No @context is required in this layer.

---

## Layer 2: HCAM JSON-LD Export

This is used when the corpus needs graph interoperability.

Used for:

- linked data export
- knowledge graph import
- RDF conversion
- ontology mapping
- semantic graph tools

### Example

```json
{
  "@context": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html",
  "@type": "hcam:AtomicKnowledgeUnit",
  "@id": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#HCAM-SPIRIT-HC-0001",
  "hcam:aku_id": "HCAM-SPIRIT-HC-0001",
  "hcam:aku_name": "Wisdom And Virtue As Foundational Excellence"
}
```

---

## Layer 3: Schema.org Discovery Wrapper

Schema.org may still be used for external web discoverability.

Used for:

- Google indexing
- AI crawler discovery
- dataset discoverability
- webpage metadata
- public catalog pages

### Example

```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "HCAM Spiritual Knowledge Graph - Hanuman Chalisa Corpus",
  "description": "A machine-readable HCAM-AKU spiritual corpus built from Hanuman Chalisa.",
  "url": "https://github.com/GurukulOnRoad/hcam-aku-kg/tree/main/hcam-skg"
}
```

This Schema.org wrapper should describe the dataset.

It should not replace the HCAM ontology.

---

# 5. Why Schema.org Should Not Be the Internal Context

Schema.org is useful for public web description.

However, it does not fully model:

- AKU reasoning layer
- life-situation mapping
- practice mapping
- boundary layer
- retrieval intent layer
- Hinglish cognitive anchors
- fine-tuning pairs
- RAG chunks
- HCAM evidence logic

Using Schema.org as the internal context would force HCAM concepts into generic web vocabulary.

That would reduce precision.

HCAM-KG™ requires its own ontology because it models knowledge for machines, not only webpages for search engines.

---

# 6. Recommended Naming

## Preferred Ontology Namespace

```text
hcamkg
```

## Preferred Domain Ontology

```text
hcam-skg
```

## Preferred Custom Context URL

```text
https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html
```

## Preferred Namespace URI

```text
https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#
```

## Preferred Spiritual Graph Namespace

```text
https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#
```

---

# 7. Suggested HCAM Context Skeleton

A future hcam-kg-v1.jsonld context may define:

```json
{
  "@context": {
    "hcam": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#",
    "skg": "https://ai.gurukulonroad.com/p/hcam-atomic-knowledge-unit.html#",

    "AtomicKnowledgeUnit": "hcam:AtomicKnowledgeUnit",
    "EvidenceUnit": "hcam:EvidenceUnit",
    "Concept": "hcam:Concept",
    "LifeSituation": "hcam:LifeSituation",
    "Practice": "hcam:Practice",
    "RetrievalUnit": "hcam:RetrievalUnit",
    "AnchorUnit": "hcam:AnchorUnit",
    "RelationshipUnit": "hcam:RelationshipUnit",

    "aku_id": "hcam:akuId",
    "aku_name": "hcam:akuName",
    "evidence_id": "hcam:evidenceId",
    "corpus_id": "hcam:corpusId",
    "source_work": "hcam:sourceWork",
    "supported_by": {
      "@id": "hcam:supportedBy",
      "@type": "@id"
    },
    "has_concept": {
      "@id": "hcam:hasConcept",
      "@type": "@id"
    },
    "maps_to_life_situation": {
      "@id": "hcam:mapsToLifeSituation",
      "@type": "@id"
    },
    "maps_to_practice": {
      "@id": "hcam:mapsToPractice",
      "@type": "@id"
    },
    "has_retrieval_unit": {
      "@id": "hcam:hasRetrievalUnit",
      "@type": "@id"
    },
    "has_anchor": {
      "@id": "hcam:hasAnchor",
      "@type": "@id"
    }
  }
}
```

---

# 8. Recommended File Strategy

The repository should contain native JSON first.

```text
corpus/evidence.json
corpus/aku.json
corpus/concepts.json
corpus/life-situations.json
corpus/practices.json
corpus/retrieval.json
corpus/relationships.json
corpus/anchors.json
```

Future export files may be added separately:

```text
exports/jsonld/hcam-skg-hanuman-chalisa.jsonld
exports/rdf/hcam-skg-hanuman-chalisa.ttl
exports/schemaorg/dataset-wrapper.jsonld
```

This separation prevents format confusion.

---

# 9. Canonical Rule

Use:

```text
HCAM-native JSON
```

for corpus storage.

Use:

```text
HCAM custom @context
```

for JSON-LD graph export.

Use:

```text
Schema.org
```

only for public discovery wrappers.

---

# 10. Final Alignment Statement

HCAM-KG™ and HCAM-SKG™ should not depend on Schema.org as their internal ontology.

Schema.org may describe the corpus externally, but HCAM-KG™ should define the knowledge internally.

The correct architecture is:

```text
HCAM Ontology
=
Knowledge Meaning Layer

Schema.org
=
Public Web Discovery Layer
```

This preserves HCAM-AKU™ as an independent, governed, machine-readable knowledge architecture.

---

# Status

| Attribute | Value |
|------------|------------|
| Decision | Locked |
| Internal Corpus Format | HCAM-native JSON |
| JSON-LD Context | HCAM-KG™ custom context |
| Schema.org Usage | External discovery wrapper only |
| Version | 1.0 |

---
