# Decision management

Use decision records (ADR) for decisions with lasting impact.

States:
- `proposed`: not yet approved;
- `approved`: authorized;
- `rejected`: will not be adopted;
- `superseded`: a later decision took its place.

An approved decision should not be rewritten to erase its history. Create a new decision that replaces it and explain the relationship.

Record approver, date, scope, version or exact description of the proposal and verifiable reference to the source of approval. Confirm the source before running; without verifiable evidence, keep the decision pending. Material change to the proposal requires new approval.

Require explicit approval: stack or architecture change; database or persistence strategy; public contract/API; authentication/authorization; security; infrastructure and network exposure; data policy; critical integration; relevant recurring cost; change in scope or committed deadline.

Small internal changes can be made within existing rules. If in doubt, propose first.

Always record positive and negative consequences. Include a migration and rollback plan when there is operational or data risk.
