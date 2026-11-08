# Decision management

Use decision records (ADR) for decisions with lasting impact.

States:
- `proposed`: not yet approved;
- `approved`: authorized;
- `rejected`: will not be adopted;
- `superseded`: a later decision took its place.

An approved decision should not be rewritten to erase its history. Create a new decision that replaces it and explain the relationship.

Approval evidence follows the **valid approval** rule in `SKILL.md`, section C. Without it, keep the decision `proposed`.

Which changes require approval is defined by the change levels in `SKILL.md`, section C.

Always record positive and negative consequences. Include a migration and rollback plan when there is operational or data risk.
