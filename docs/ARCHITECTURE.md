# Architecture and trust boundaries

## Existing flow

Reviewed historical source -> owner-approved stored public release -> read-only hash-checked publication projection -> JSON / Markdown / escaped HTML fragment.

A separate discovery bridge reads the publication JSON with a pinned contract and bounded caching, then supplies selected existing machine publications. It does not update every page, FAQ or feed.

## Three distinct layers

1. The source release is the historical data object, with an expected SHA-256 over its original bytes. Adding metadata to those bytes would change that digest.
2. The unsigned projection derives public publication facts and representations. Publication time is separate from the collection time and observation window.
3. The consumer reads and validates that projection. It pins the source digest declared in the projection; it does not independently download and hash the source dataset on every render.

## Current publisher behavior

The reviewed helper permits GET/HEAD and JSON/Markdown/HTML formats, uses the existing release storage, checks the stored source digest and validates the release-specific contract before rendering. It bounds stored source bytes at 1 MiB. Invalid or unavailable content yields an explicit non-success response rather than fabricated zero observations. This is a description of the inspected implementation, not a complete security assessment.

The projection's synchronization.machine_discovery value says not_connected_by_this_module. That describes this helper's scope, not the absence of the separately deployed discovery bridge. Preserve this distinction when reading the record.

## Current consumer budgets

The inspected bridge allows only five documentation paths on GET/HEAD. Its source read uses manual redirects, a 3-second deadline and a 64 KiB streaming limit. It has isolate-local 5-minute fresh caching, 60-second retry backoff, single-flight loading and a maximum 24-hour last-good fallback. These are configured implementation limits, not measured uptime or latency guarantees. Cache state is not globally coordinated durable storage.

States distinguish available_cached, stale_last_successful_read and unavailable_historical_reference_only. Last successful read time is not a new collection, publication or independent evidence date. Existing HTTP caching may also affect what a client sees.

## Integrity boundaries

A matching hash establishes byte consistency relative to an expected digest. It does not establish factual truth, physical stock, sporting merit, independent accreditation or authorship. The publication record is unsigned. Existing separate identity/signature infrastructure is not a signature on this record and is not redistributed here.

## Deliberate exclusions

No automatic collection, approval, signing, scheduler activation, customer processing, transaction, storefront page rewrite or Knowledge Base write is performed by this publication unit. No universal crawler access, indexing, AI recommendation, search ranking or commercial uplift is claimed.
