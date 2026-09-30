# Contributing to PORTWRAITH

## Workflow
1. Create a focused branch.
2. Make one coherent change.
3. Add/update tests.
4. Update relevant security documentation.
5. Run the local test suite.
6. Open a pull request with a concise security impact summary.

## Branch naming
feature/api-foundation
feature/policy-engine
lab/registry-simulator
security/secure-mode
docs/attack-path

## Commit style
Prefer conventional messages: feat:, fix:, security:, docs:, test:, chore:

## Vulnerability changes
When changing intentionally vulnerable behavior, update the vulnerability map, instructor guide, solution, secure-mode behavior, and tests.

Never introduce real credentials or external destructive behavior.
