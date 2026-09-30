# PORTWRAITH Threat Model

## Assets
- container routing records
- customs inspection records
- operational policies
- deployment history
- audit events
- incident token

## Actors
### External attacker
Can interact with the public application and discover exposed information.

### Developer
Creates and publishes policy changes through CI/CD.

### CI service
Builds and publishes artifacts.

### Deployment service
Promotes artifacts and activates policies.

## Trust boundaries
1. External client -> web application
2. Web application -> internal services
3. CI -> dependency source
4. CI -> artifact registry
5. Registry -> deployment agent
6. Deployment agent -> policy store
7. Policy -> authorization/business logic

## Threats
- artifact substitution
- dependency substitution
- mutable-tag confusion
- insufficient authenticity verification
- policy tampering
- unauthorized trust propagation
- audit inconsistency

## Security goal
Ensure software and operational data are accepted only when origin, integrity, version, and authorization are sufficiently established.
