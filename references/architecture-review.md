# Architectural review

Assess, when applicable:

- limits of modules and responsibilities;
- permitted dependencies and direction of the dependencies;
- contracts between frontend, backend, services and agents;
- data model, ownership and data lifecycle;
- authentication, authorization and isolation between users/organizations;
- error handling, idempotence and consistency;
- observability: logs, metrics, tracking and alerts;
- required scalability versus introduced complexity;
- resilience to external service failures;
- unit, integration, contract and end-to-end testing;
- security, privacy, retention and recovery;
- deploy, migration, rollback and compatibility.

For each finding, rate severity, evidence, impact and recommendation. Differentiate proven defect from potential risk.

Don't redesign the entire architecture out of aesthetic preference. Prioritize demonstrable problems and project objectives.
