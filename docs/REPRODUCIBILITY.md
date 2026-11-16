# Optional read-only review procedure

These are proposed future checks. They have NOT been executed as part of creating this package. Do not schedule them or retry blocked endpoints automatically.

1. Download the existing public source JSON as raw bytes. If the endpoint returns a non-success status, HTML challenge or redirect requiring review, stop and record that result. Do not weaken protections or spoof a crawler identity.
2. Compute SHA-256 on those exact bytes, before parsing/reformatting, and compare to the source digest in examples/expected-contract.json. Matching bytes are not independent verification of the underlying measurements.
3. Parse the source and check the historical window, selected article coverage, source/method declarations and limitations. This package does not include the raw observations or a complete statistical re-computation tool.
4. Read the publication JSON. Validate with the proposed documentation schema using a compatible JSON Schema Draft 2020-12 validator. Enable format assertions if supported. Schema validation alone is insufficient: enforce date order, coverage arithmetic and the release-specific expected contract separately.
5. Compare its declared source digest, dates, coverage and links to the selected expected facts. The projection publisher's source_bytes_verified_for_this_response flag is its assertion; a consumer who only reads the projection has not independently hashed the dataset.
6. Optionally read Markdown and HTML representations and compare the shared facts and limitations. Their bytes and hashes naturally differ from the source and JSON projection.
7. Record timestamp, client, status and scope. Do not infer global accessibility, search ingestion, uptime or independent scientific validation from one success.

No authenticated calls, mutations, approvals, signing, paid requests, submissions, or checkout tests are needed for this procedure. The production Worker validators remain authoritative for their own behavior; the documentation schema is an explanatory draft, not a replacement.
