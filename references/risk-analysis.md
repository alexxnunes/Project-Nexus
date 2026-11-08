# Risk analysis

Consider categories:
- product and scope;
- architecture and technical debt;
- security and privacy;
- data, migration, backup and recovery;
- infrastructure, availability and costs;
- dependencies and suppliers;
- integration and compatibility;
- quality, testing and operation;
- team, knowledge and continuity.

Register risk as a scenario: cause → event → consequence. Assess probability and impact (low/medium/high), evidence, mitigation, contingency, responsible party and review trigger.

Common pitfalls to check for, not assume:
- secret exposed in repository or log;
- backup without test restoration;
- destructive migration without rollback;
- external dependency without timeout/retry/limit;
- absence of idempotence in repeatable operations;
- excessive permissions;
- divergence between local, staging and production environments;
- incompatible runtime or library version;
- circular coupling or module with excessive responsibility;
- lack of observability;
- variable cost without limit/alert;
- documentation deviating from the code.

Do not declare a risk as an incident without evidence.
