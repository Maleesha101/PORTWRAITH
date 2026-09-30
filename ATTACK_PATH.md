# PORTWRAITH Attack Path

> Instructor/design document. Implementation-specific details should be added only after the application is built and verified.

## Intended chain
1. Recon the operations application.
2. Discover build/deployment metadata.
3. Identify the policy artifact workflow.
4. Notice the mutable artifact reference.
5. Investigate dependency/build provenance.
6. Identify the weakness in integrity/authenticity verification.
7. Produce or obtain a controlled modified policy artifact.
8. Reach the intended trusted deployment path.
9. Observe policy-driven application behavior.
10. Use the resulting trust change to access restricted operational information.
11. Correlate deployment, policy, routing, and audit timestamps.
12. Recover the final incident token.

Each step must provide enough evidence for a careful student to infer the next trust boundary.

## Final objective
Correlate container identity, route, deployment version, policy version, audit event, and incident token. The flag must live in application-controlled state rather than an obvious static file.
