# OhYeah / Inspect the claim, then inspect the record

Documentation baseline: 16 November 2026.

## The interaction

OhYeah adds an on-demand source-quotation modal to selected product templates. It connects a reader to quotation text, source context and browser-side checks of Paragon-issued signed records. Plain source links provide a separate path to the public proof service.

The documented collection contains 20 published quotations: 17 IBJJF and 3 WBC. These are selected quotations, not complete rulebooks. BJJ uniform and professional championship boxing contexts must remain separate. They are not product certifications or general sparring-size recommendations.

## Evidence path

Selected source → stored snapshot and hash → candidate passage → owner publication decision → signed record → public service → browser verification.

Approval is editorial responsibility, not independent review. The initial IBJJF set was owner-approved in bulk without individual quotation review; the three WBC passages received explicit owner approval. A quotation's signature does not independently validate that decision.

## Public interfaces

- Readable collection: https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof
- Record collection: https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/facts
- Public key: https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/key
- Product-widget adapter: https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/widget-data?source=ibjjf
- Boxing-widget adapter: https://paragon-cornerman.delicate-fire-83f8.workers.dev/proof/widget-data?source=wbc

These links are retained references, not fresh availability checks.

## Verification profile

The application-specific profile is ParagonQuoteProof-v1. The widget adapter identifies its response as ParagonProofWidget-v1. These identifiers describe different layers, not competing signature standards.

The implementation uses Ed25519 and an application-specific canonical representation containing the payload and proof metadata with the signature excluded. The public-key fingerprint is derived from the decoded public key. Signature and fingerprint checks use the documented profile; merely hashing a quotation is not signature verification.

This document is an architectural explanation, not a complete normative cryptographic specification or a replacement verifier implementation. Do not implement a verifier from this prose alone.

The proof key is served by the proof service. Successful verification establishes consistency with that key, not independent issuer identity, source truth, current rule applicability or regulatory approval. The profile is not W3C Data Integrity and does not reuse the store's canonical signed credential as its quotation proof.

## Retained implementation evidence

On 15 October 2026, retained diagnostic observations recorded three WBC records passing signature checks against the live adapter's public key. Product-template previews subsequently showed the three WBC records and the 17 IBJJF records verifying in the relevant product contexts. Template-save evidence is recorded separately from preview observations.

These observations are not a new 16 November revalidation, exhaustive device test or independent audit.

## Limits and improvement backlog

Retained code-review notes identified issues around unsupported-crypto handling, retry after fetch failure, pagination/completeness field handling, lifecycle cleanup and fallback visibility. Later work includes accepted widget/modal improvements, but this document has not freshly reconciled every historical issue against current generated code. Treat universal accessibility, mobile coverage, retry behaviour and exhaustive tamper handling as unconfirmed, not as verified defects or completed fixes.

Keep source access available outside JavaScript-only interactions. A failed, unsupported or incomplete verification must not be labelled valid. Signatures do not remove the need to read scope, dates and original sources.
