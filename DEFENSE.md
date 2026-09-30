# PORTWRAITH Defense Guide

## Artifact integrity
Vulnerable: mutable artifact reference, digest metadata from the same trust domain, no independent publisher authenticity.
Secure: immutable artifact identity, cryptographic signing, trusted verification key, provenance/attestation, controlled promotion.

## Dependencies
Vulnerable: insufficiently pinned dependency resolution.
Secure: lockfiles, exact versions where appropriate, trusted registry, dependency integrity verification, review and scanning.

## Policy integrity
Vulnerable: policy accepted because it came through a trusted-looking deployment path.
Secure: schema validation, signature verification, version/rollback controls, least-privilege deployment, audit logging.

## Container integrity
Prefer immutable image digests over mutable tags.

## Deserialization
Prefer strict JSON/schema validation and allowlisted fields over arbitrary object reconstruction.

## CI/CD
Treat CI runners and deployment credentials as privileged infrastructure: least privilege, isolated runners, protected branches, controlled secrets, artifact signing, reproducible builds where feasible, and provenance tracking.
