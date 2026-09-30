# PORTWRAITH Architecture

## System
HarborMind Autonomous Logistics operates an autonomous container terminal.

    Developer Repository
            |
            v
       CI/CD Pipeline
            |
            v
        Policy Builder
            |
            v
       Artifact Registry
            |
            v
       Deployment Agent
            |
            v
       Port Control API
      /       |        \
     v        v         v
 Yard Logic Customs Logic Crane Logic

## Planned Docker services

| Service | Responsibility | Trust zone |
|---|---|---|
| nginx | Entry point/reverse proxy | public |
| frontend | Operations console | public |
| api | Business logic | application |
| postgres | Persistent state | data |
| registry | Local artifact store | internal |
| ci-simulator | Build/publish simulation | internal |
| deployment-agent | Policy deployment | internal |

## Key entities
users, roles, containers, yards, routes, inspection_records, policies, policy_deployments, build_artifacts, audit_events.

## Policy lifecycle
Policy source -> CI build -> dependency resolution -> artifact creation -> registry publication -> deployment verification -> policy activation -> application behavior -> audit event

## Trust-boundary objective
A checksum proves bytes match a digest, but does not by itself establish who authored or published those bytes. Artifact identity, provenance, signing, and authorization must be considered together.

## Network intent
The public surface should be narrow. Internal registry, CI simulation, and deployment services should not be directly exposed unless a challenge clue requires it.
