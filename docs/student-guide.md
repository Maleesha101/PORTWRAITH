# PORTWRAITH Student Guide

## Mission
HarborMind reports an unexplained routing anomaly in its autonomous terminal. You have authorized access to the training environment and must investigate the software and data trust chain.

## Objectives
- Discover how policy artifacts reach the application.
- Determine why a policy changed.
- Identify the affected operational record.
- Recover the final incident token.

## Suggested toolkit
- browser
- Burp Suite or ZAP
- curl/httpie
- jq
- git
- standard Linux utilities
- Docker

## Rules
Stay inside the local PORTWRAITH environment. Do not attack external infrastructure.

## Hint philosophy
The application, build metadata, policy history, and audit trail should provide enough evidence to reconstruct the incident.
