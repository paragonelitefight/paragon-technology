# From Reviewed Snapshots to Machine-Readable Publications
## A Paragon FightPulse Case Study

Draft 0.1.0-review, 16 November 2026. Publisher-authored implementation report. Named authors and institutional attribution await owner confirmation.

### Abstract

Paragon FightPulse provides a bounded example of publishing a reviewed historical snapshot without silently changing its bytes, dates or meaning. The implementation separates an approved release from an unsigned publication projection and from a cached discovery consumer. A first Boxing release covers 43 tracked English Wikipedia articles over 16 October to 12 November 2026. This report describes the implemented boundaries and recorded acceptance observations. It does not evaluate causal effects on search visibility, AI use, conversion or athlete performance.

### 1. Motivation

Copying the same research facts into multiple formats can create inconsistent dates, counts and limitations. Updating descriptive metadata directly inside an already published source file also changes its hash. The design therefore treats source bytes as one object and publication metadata as a separate derived record.

### 2. Data and method

The source concerns English Wikipedia all-access, user-agent-class user daily pageviews for a selected set of 43 articles. This describes Wikimedia's user-classified requests, not necessarily unique human visitors. The fixed UTC observation window is 16 October to 12 November 2026, inclusive. Collection was recorded at 2026-11-13T11:37:30.882Z. Each included article has 28 daily observations in the accepted release.

Ordering uses the smoothed recent-week ratio (last7 + 500) / (previous7 + 500). Raw percentage change is a separate quantity and is null for a zero baseline. The result is a historical attention proxy for the selected English-language article set, not a ranking of boxing ability, total popularity, sentiment or the entire sport. Article selection and language scope constrain generalization; external events can affect pageviews.

### 3. Publication design

The owner-approved release was recorded as published at 2026-11-16T08:02:58.654Z. A read-only projection derives coverage, dates, method, limitations and source digest from that stored release. It renders JSON, Markdown and an escaped HTML fragment without changing the source JSON bytes. Public report/evidence links are presentation configuration, not independently discovered evidence.

A separate bridge reads the unsigned publication record using bounded fetches, contract validation and age-limited caching. It supplies selected machine-readable documentation. Shopify HTML pages and Knowledge Base content are not automatically synchronized by that bridge.

### 4. Recorded observations

The accepted Boxing release contained 43 unique article rows with 28 daily values each. The recorded review checked weekly arithmetic, smoothed ordering, percentage treatment and source links. At 11:03 EET on 16 November, bounded acceptance reads observed the source and three projection formats returning HTTP 200; the source byte digest matched the expected value. At 11:17 EET, four selected machine outputs returned HTTP 200 with the expected historical metadata and available_cached source state.

The fifth documentation path, /agents.md, returned HTTP 403 to the checker. This does not establish a global crawler block or confirm that path's then-current bridge output. Earlier browser evidence for an earlier version is not substituted for this check.

Local mocked tests previously recorded for the projection and bridge covered selected integrity, formatting, cache and error cases. They are not an independent audit. This package does not ship those development fixtures, re-run those tests or report a new live acceptance result.

### 5. Interpretation

The implementation demonstrates a narrow publication pipeline with explicit source/date boundaries and failure states. It does not demonstrate universal format synchronization, continuous new research, guaranteed availability, truth from hashes, or automatic distribution into third-party AI systems.

### 6. Limitations and reproducibility

The project is publisher-authored; there is no independent replication, controlled visibility experiment, full penetration test or performance benchmark in this report. Public access can differ by client and protection rules. The source JSON and public projection endpoints support optional read-only comparison, but source retention and future access are not guaranteed by this draft. A public reference URL is not a licence to redistribute underlying data.

See EVIDENCE.md for exact recorded observations and REPRODUCIBILITY.md for a future review procedure. Source code and the raw 43-row dataset are deliberately not bundled pending separate rights and release review.

### 7. Conclusion

Separating reviewed data, derived unsigned publication records and cached consumers allows an implementation to publish consistent selected representations without redefining historical observations as live data. The useful contribution is the explicit boundary, not a claim of a new universal standard or verified search advantage.
