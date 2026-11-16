# PARAGON TECHNOLOGY

### BEYOND THE STOREFRONT.
### ARCHITECTURE. EVIDENCE. EXPERIMENTATION.

An interconnected technology programme by Paragon Elite Fight Group, Athens, Greece.

We are developing Paragon as more than a place to buy fight equipment: a destination for useful knowledge, inspectable technical work and documented product development.

Our architecture brings together commerce, supplementary agent tools, source-backed information, browser-verifiable records, linked data and research-publication workflows.

Different systems serve different purposes. Their boundaries are part of the design.

---

## EXPLORE THE ECOSYSTEM

- [Technology and architecture](https://paragonelitefight.com/pages/paragon-fight-technology-security)
- [Verification and evidence](https://paragonelitefight.com/pages/verification)
- [AI Agent Gateway](https://paragonelitefight.com/pages/ai-agent-gateway)
- [Product-development R&D](https://paragonelitefight.com/pages/paragon-research-development)
- [R&D technical documents](https://github.com/paragonelitefight/paragon-r-and-d)

This repository is the technical documentation hub for selected parts of that ecosystem.

It is not a release of our complete production infrastructure.

---
## OPEN THE ENGINEERING

### Follow the architecture. Inspect the evidence.

Choose your route into the Paragon technology ecosystem:

- **[Documentation atlas](docs/INDEX.md)**  
  The starting point for technical readers: architecture, evidence, examples and publication boundaries.

- **[Inside OhYeah](docs/OHYEAH.md)**  
  Follow a source quotation from a stored snapshot to a signed record and browser-side verification.

- **[The sixteen-component systems map](docs/SYSTEMS_MAP.md)**  
  Explore the responsibilities and boundaries of our discovery, evidence, guidance and publication infrastructure, including disabled and retired components.

- **[The FightPulse implementation report](docs/CASE_STUDY.md)**  
  Examine how a reviewed historical release becomes consistent machine-readable publication representations.

- **[Publication architecture](docs/ARCHITECTURE.md)**  
  Understand the selected pipeline, its data flow and failure-handling boundaries.

- **[Evidence ledger](docs/EVIDENCE.md)**  
  Read the dated observations and distinguish verified behaviour from unconfirmed scope.

- **[Reproducibility notes](docs/REPRODUCIBILITY.md)**  
  Review the proposed bounded checks and their limitations.

- **[Experimental showcase roadmap](docs/ROADMAP.md)**  
  Explore proposed demonstrations and useful tools, clearly separated from deployed capabilities.

### Structured documentation artifacts

[Publication-record schema draft](schemas/publication-record.schema.json) · [Expected-contract example](examples/expected-contract.json) · [Rights and reuse](RIGHTS_AND_REUSE.md)

The schema is a documentation draft. The example contains selected expected facts, not a captured live response. Neither is a production SDK or a claim of validated conformance.

---
## 01 / OHYEAH

### “Oh, yeah?” is a useful engineering question.

OhYeah connects product-page statements with inspectable source quotations and Paragon-issued signed records.

The implemented product experience includes an on-demand modal for selected product templates, source references and browser-side signature verification.

### Documented publication

- 17 IBJJF source quotations.
- 3 WBC source quotations.
- 20 published quotation records in the documented collection.
- Separate treatment of BJJ uniform context and professional boxing context.

The product-template integration has been demonstrated with the relevant IBJJF and WBC record sets.

### What the browser checks

The implemented verification profile uses Ed25519 signatures, canonicalized record content and a proof-service public key.

A successful check establishes that the displayed record verifies against that key.

It does not independently establish:

- The truth or continuing applicability of a quotation.
- The independent identity of its issuer.
- Product approval or sporting-body endorsement.
- Product safety, legal compliance or competition eligibility.

The signature profile is application-specific: ParagonQuoteProof-v1. It must not be described as a W3C Data Integrity implementation.

### Inspect the public records

- [Readable source quotations](https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof)
- [Published records as JSON](https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/facts)
- [Proof-service public key](https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/key)

OhYeah is implemented, but implementation does not imply that every device, accessibility condition or failure path has been exhaustively validated.

---

## 02 / CORNERMAN

### From source material to reviewable evidence.

Cornerman provides components for working with selected source material, stored snapshots, proposed quotations, review decisions and signed publication.

Its documented workflows include:

- Source registration and snapshot storage.
- Content hashes and retrieval provenance.
- Candidate extraction from a selected stored HTML source.
- Curated, page-located passages from a selected boxing PDF.
- Owner review and publication decisions.
- Signed quotation records.
- Public HTML and JSON representations.
- Stored-content comparison.

Source approval, quotation approval, signature creation and public presentation are distinct operations.

A stored snapshot is not proof that the original source remains unchanged today.

Curated PDF passages are not a general-purpose automated PDF interpretation engine.

The broader verification-system vision remains only partly implemented. This repository will distinguish completed components from proposed automation.

---

## 03 / FIGHTPULSE

### Historical research, published with explicit boundaries.

FightPulse is a research-publication project based on source-page attention and a documented processing method.

It is not an official athlete ranking, competition-results service or assessment of athletic ability.

### Selected boxing release

Observation window: 16 October–12 November 2026.

The published release included all 43 tracked entries, with zero pending and zero failed entries in that release.

This is a historical snapshot, not a live ranking.

### Publication pipeline

Reviewed historical release
→ Stored public JSON and recorded SHA-256
→ Unsigned publication record
→ JSON / Markdown / HTML representations
→ Validated, cached consumer
→ Selected machine-readable discovery outputs

### Inspect the release

- [Historical source JSON](https://paragon-cornerman.delicate-fire-83f8.workers.dev/fight-pulse/boxing-20261016-20261112.json)
- [Unsigned publication record](https://paragon-cornerman.delicate-fire-83f8.workers.dev/fight-pulse/boxing-20261016-20261112.json?view=publication)
- [Markdown representation](https://paragon-cornerman.delicate-fire-83f8.workers.dev/fight-pulse/boxing-20261016-20261112.json?view=publication&format=md)
- [HTML fragment](https://paragon-cornerman.delicate-fire-83f8.workers.dev/fight-pulse/boxing-20261016-20261112.json?view=publication&format=html)
- [Published report](https://paragonelitefight.com/pages/paragon-fight-technology-security#paragon-fightpulse-boxing-20261112)
- [Publication evidence](https://paragonelitefight.com/pages/verification#fightpulse-boxing-release-2026-11-16)

The source SHA-256 identifies the released bytes. It is not a signature or a guarantee of the underlying research claims.

### Observed discovery integration

On 16 November 2026, bounded acceptance checks confirmed the publication-source connection in:

- llms.txt
- llms-full.txt
- verification.md
- .well-known/verification.json

The agents.md check returned HTTP 403 to the checker. Its updated bridge output was not verified by that check. This does not establish a universal access failure.

Shopify page bodies and Knowledge Base answers remain separately maintained.

---

## 04 / AGENT INTERFACES

### Supplementary advice and native commerce are separate.

Paragon's supplementary MCP service exposes six read-only tools for selected boxing and BJJ guidance.

Public endpoint:

https://paragonelitefight.com/api/mcp

This advice service is not a payment processor and does not replace native commerce or checkout.

### Public discovery records

- [Official MCP Registry record](https://registry.modelcontextprotocol.io/v0.1/servers?search=com.paragonelitefight&limit=100)
- [Glama connector listing](https://glama.ai/mcp/connectors/com.paragonelitefight/paragon-boxing-and-bjj-gear-advisor)
- [Usage context and interface boundaries](https://paragonelitefight.com/pages/ai-agent-gateway)

The documented supplementary server version is 2.0.3.

Registry publication and directory ownership verification are discovery records, not security certifications, endorsements or guarantees of traffic.

Native Shopify commerce remains a separate integration with its own responsibilities and authoritative transaction context.

---

## 05 / IDENTITY, PROVENANCE AND LINKED DATA

### Connected information with explicit trust boundaries.

The broader architecture includes public identity references, a signed credential, verification documentation and a reference knowledge graph.

These serve different purposes:

- Identity references describe the publisher.
- Signatures support checks against identified keys.
- Hashes support content-integrity comparisons.
- Provenance records describe sources and processing.
- Linked data connects concepts and external identifiers.

None of these mechanisms independently makes a statement true.

### Reference graph

The documented 12 November 2026 graph release contains:

- 24 product groups.
- 72 variants.
- 1,585 RDF statements.
- 180 Wikidata links.

It is a dated reference dataset, not an automatically synchronized inventory or price feed.

Public representations include:

- [Turtle](https://paragonelitefight.com/data/graph.ttl)
- [JSON-LD](https://paragonelitefight.com/data/graph.jsonld)
- [LOD Cloud dataset entry](https://lod-cloud.net/dataset/paragon-elite-fight-group-reference-graph)

The LOD Cloud entry records a dataset listing. It does not establish inclusion in the LOD diagram, independent validation or continuous download availability.

Existing signed identity material is separate from the unsigned FightPulse publication pipeline.

---

## 06 / GUIDANCE AND CATALOG CONTEXT

### Useful interfaces, not duplicate sources of commercial truth.

The ecosystem also includes:

**Gear Advisor**

An interactive guidance interface. Demonstrated responses are not evidence of universal device reliability, unlimited availability or independently validated advice.

**Sizing knowledge**

Structured sizing information and supplementary guidance. Nominal glove weight, shipping weight and measured equipment properties must not be treated as interchangeable data.

**Product representations**

Catalog-derived product information for selected machine-readable surfaces. Representation consistency requires careful handling of units, variant context and freshness.

**Price-history snapshots**

Recorded catalog-price observations. A snapshot system is not automatically a complete, immutable price history or a legal-compliance determination.

**Product passport and safety-information presentation**

Storefront mechanisms for displaying supplied product information. The presence of fields or badges is not independent certification or proof of regulatory compliance.

---

## 07 / THE 16-COMPONENT LIFECYCLE MAP

The following is the documented Worker/component inventory.

It is a lifecycle map, not a claim that all 16 components are active, independently audited or fully documented in this repository.

### Discovery and publication

1. **llm-cache-headers**
   Selected machine-readable publications, discovery responses and publication-source integration.

2. **robots-txt-injector**
   Robots-response customization within its configured scope.

3. **paragon-well-known**
   Selected public discovery, identity and ownership-proof responses.

### Observation and evidence

4. **paragon-heartbeat**
   Heartbeat-related infrastructure. Its name alone does not establish monitoring coverage or an uptime guarantee.

5. **paragon-cornerman**
   Source snapshots, selected evidence workflows, quotation publication and FightPulse components.

6. **pef-canary-stamp**
   Canary/reference-stamp mechanism. A recorded interaction must not be presented as reliable visitor identity or universal crawler attribution.

### Product and agent interfaces

7. **paragon-product-sync**
   Product-representation infrastructure within its configured scope, not proof of whole-platform synchronization.

8. **paragon-agent**
   Supplementary six-tool advice MCP service.

9. **paragon-ucp-mcp-worker**
   Custom commerce-related integration component retained in the existing architecture. It must not be confused with the read-only advice service or described as independently proven end-to-end payment processing.

### History, notifications and guidance

10. **paragon-price-history-workerjs v2**
    Catalog-price snapshot infrastructure.

11. **paragon-doorbell**
    Discovery-notification infrastructure, including IndexNow/WebSub-related work. Notification attempts and accepted submissions are not proof of indexing.

12. **paragon-gear-advisor**
    Interactive equipment-guidance infrastructure.

### Feed-specific components

13. **paragon-openai-feed**
    OpenAI-oriented feed component. Its inclusion in this inventory does not establish current ingestion, approval or visibility.

14. **paragon-google-feed**
    Google-oriented feed component. Its inclusion does not establish product approval or resolution of account-side integration issues.

### Inactive lifecycle entries

15. **paragon-google-indexing**
    Retired legacy indexing component.

16. **pef-keeper-v2**
    Deployed but disabled. Warming remains off; no current warming benefit is claimed.

Per-component documentation should identify purpose, data boundaries, dependencies, lifecycle status, dated evidence and known limitations.

Private bindings, credentials and production secrets are outside publication scope.

---

## 08 / PRODUCT-DEVELOPMENT R&D

### Advanced fight equipment. Documented development.

Our equipment projects have their own repository and publication context:

**PARAGON CÆSTUS ZERO**

ANTIGRAVITY SERIES · PRO BOXING GLOVE PROJECT

**PARAGON UNTOUCHABLE NØ-G**

ZERO-GRAVITY SERIES · HYBRID BJJ GI PROJECT

The published technical packs describe proposed construction, design targets and planned validation.

They do not establish completed prototypes, comparative superiority, injury reduction, competition approval or production readiness.

The project and series names are working presentation names, not claims of physical antigravity or weightlessness.

- [Explore the R&D programme](https://paragonelitefight.com/pages/paragon-research-development)
- [Read the technical documents](https://github.com/paragonelitefight/paragon-r-and-d)

---

## 09 / EXPERIMENTAL SHOWCASE ROADMAP

The following are candidate extensions, not deployed capabilities claimed by this README:

- Interactive architecture and evidence-path exploration.
- Controlled proof-verification demonstrations.
- Reference-graph exploration.
- A useful boxing/BJJ round timer.
- An embeddable sizing interface reusing reviewed sizing data.
- Additional reproducible publication examples.

Experimental interfaces should remain separate from the shopping-critical path.

Proposed measurement datasets require real measurements, documented methods and appropriate publication rights. We do not invent physical test results.

No roadmap item is presented as unique, world-first or guaranteed to improve search or AI visibility.

---

## 10 / ENGINEERING RULES

### Preserve meaningful boundaries

Commerce, advice, identity, evidence and experimentation have different authorities.

### Keep dates honest

Observation period, source retrieval, publication, documentation and cache-read timestamps are not interchangeable.

### Fail visibly

Missing records, hash mismatches, stale sources and unsupported verification must not silently become successful results.

### Publish selectively

Public documentation does not require exposing private keys, customer data, internal candidate records or complete production Workers.

### Distinguish implementation from ambition

Working components, partial workflows, disabled systems, retired components and proposed features must be labelled accordingly.

---

## DOCUMENTATION AND RELEASE STATUS

Documentation baseline: 16 November 2026.

This initial documentation edition presents selected implementation reports, dated evidence and clearly labelled experimental directions.

The first supporting technical package focuses on the FightPulse publication pipeline. Other components in this overview do not yet imply an equivalent level of repository documentation.

The package is a publisher-authored implementation report, not a peer-reviewed paper, independently audited protocol, production SDK or complete open-source platform.

No reuse licence is granted by this README. Publication rights and reuse terms must be stated explicitly for the released material.

Dated observations are not continuous health checks.

No universal indexing, search ranking, traffic, security or compliance guarantee is made.

---

## PARAGON ELITE FIGHT GROUP

Athens, Greece.

[Website](https://paragonelitefight.com) · [Technology](https://paragonelitefight.com/pages/paragon-fight-technology-security) · [Verification](https://paragonelitefight.com/pages/verification) · [AI Agent Gateway](https://paragonelitefight.com/pages/ai-agent-gateway)
---

## PUBLISHED TECHNICAL REPORT

### From Reviewed Snapshots to Machine-Readable Publications

The standalone Paragon FightPulse implementation report is published on Zenodo as version 1.0.0.

It expands the publication-pipeline explanation with retained implementation observations, timestamp discipline, integrity boundaries and limitations.

[Read the published report](https://doi.org/10.5281/zenodo.24279360)

### Cite the report

Paragon Elite Fight Group. (2026). *From Reviewed Snapshots to Machine-Readable Publications: A Paragon FightPulse Implementation Report* (Version 1.0.0). Zenodo. https://doi.org/10.5281/zenodo.24279360

The report is licensed under CC BY 4.0. This does not change the licensing of this repository, linked equipment technical packs or underlying datasets.

The report is a separate publication associated with the Paragon Technology v0.1.0 documentation release, not an identical copy or a DOI assigned to the entire technology ecosystem.

Repository hosting and a DOI do not establish peer review, independent certification or the truth of every reported observation.
