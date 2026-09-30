# AGENT.md — PORTWRAITH

## Mission
PORTWRAITH is an intentionally vulnerable cybersecurity training lab. Build a coherent autonomous-port platform demonstrating Software or Data Integrity Failures through a deterministic, locally isolated attack chain.

## Core rules
- Keep the lab self-contained and reproducible.
- Never require real cloud credentials, real package registries, or external infrastructure.
- Do not create real malware or destructive payloads.
- Vulnerable behavior must be deterministic and documented for instructors.
- Secure mode must demonstrate concrete remediation.
- Preserve realistic trust boundaries between web application, CI/CD, registry, deployment, policy store, and database.
- Do not turn the challenge into an unrelated vulnerability collection.

## Planned services
nginx, frontend, api, postgres, registry, ci-simulator, deployment-agent.

## Trust chain
Source -> CI/CD -> dependency resolution -> artifact -> registry -> deployment -> policy -> application behavior

## Vulnerability themes
1. Weak artifact integrity/authenticity verification
2. Mutable artifact references
3. Dependency integrity weakness
4. Insufficient policy/configuration integrity
5. Optional unsafe deserialization/parsing

## Development rules
- Prefer small, testable components.
- Keep security-sensitive behavior explicit.
- Use environment variables for mode/configuration.
- Never use real secrets.
- Provide vulnerable and secure modes where practical.
- Add tests for intended vulnerable behavior and secure remediation.
- Seed realistic timestamps so the incident can be investigated as a timeline.

## API
Use versioned routes under /api/v1 and realistic role-based authorization. Avoid artificial vulnerability endpoints.

## Docker
All services must start with Docker Compose. Runtime must not depend on internet access. Network separation should reflect the trust model.

## Documentation
Student-facing documents must not reveal the complete exploit chain. Instructor documentation may contain the full solution.

## Verification
Before implementation milestones are complete:
docker compose build
docker compose up

Then run tests and verify reset/seed functionality.

## Security boundary
This repository is for authorized CTF/AppSec training. Keep exploitation contained within the intentionally vulnerable lab.
