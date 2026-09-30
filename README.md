# PORTWRAITH

**PORTWRAITH** is an intentionally vulnerable, locally runnable CTF/AppSec lab focused on **Software or Data Integrity Failures**.

## Scenario

HarborMind Autonomous Logistics operates an autonomous container terminal. PORTWRAITH models the trust chain between source code, CI/CD, dependencies, policy artifacts, deployment services, and the port-control application.

The lab is designed around a chained integrity failure rather than isolated vulnerability demos.

## Planned attack-chain theme

```
Recon
  -> build/update discovery
  -> artifact workflow
  -> mutable artifact / dependency integrity weakness
  -> manipulated policy
  -> insufficient verification
  -> trusted deployment
  -> changed application behavior
  -> restricted operational data
  -> incident token
```

## Project status

This repository currently contains the **initial architecture and lab-design documentation**. Application implementation will be added incrementally.

## Planned stack

- FastAPI or Node.js backend
- PostgreSQL
- Lightweight frontend
- Docker Compose
- Simulated CI/CD pipeline
- Local artifact registry
- Deployment agent

## Security themes

- Software/artifact integrity
- CI/CD trust boundaries
- Dependency integrity
- Mutable artifact references
- Policy/configuration integrity
- Secure vs vulnerable deployment behavior
- Optional unsafe deserialization

## Safety

The lab is intentionally vulnerable but designed for isolated, authorized local training. It must not depend on real external package registries, credentials, or destructive payloads.

## Planned documentation

- `AGENT.md`
- `ARCHITECTURE.md`
- `ATTACK_PATH.md`
- `DEFENSE.md`
- `THREAT_MODEL.md`
- `CONTRIBUTING.md`
- `docs/student-guide.md`
- `docs/instructor-guide.md`
- `docs/vulnerability-map.md`
- `docs/solution.md`

## License

To be decided before the first public release.
