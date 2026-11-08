# Environment management

Document:
- supported operating systems and runtimes;
- versions of languages, frameworks, database and tools;
- system dependencies;
- local services and containers;
- environment variables by name and purpose, never by secret value;
- ports, networks and dependencies between services;
- installation, execution, testing, build and deploy commands;
- differences between development, testing, approval and production;
- backup, restoration, migration and rollback strategy;
- minimum requirements and known limitations.

Do not copy `.env`, tokens, credentials, keys, private certificates or dumps with personal data for documentation or handoff. If you find an exposed secret, do not reproduce it; signal the need for revocation/rotation.

Before changing the production environment, infrastructure, firewall, DNS, volumes or database, request explicit approval.
