# Audit during development

Compare the implementation with:
- requirements and acceptance criteria;
- architecture and approved contracts;
- stack and registered versions;
- code and security rules;
- current decisions;
- documented integrations and environment.

Look for:
- divergence between documentation and code;
- dependency or new unregistered service;
- unapproved contract change;
- migration or change of data without a plan;
- secret or sensitive data in file/log;
- missing, fragile or not executed tests;
- insufficient handling of errors and external failures;
- functionalities out of scope;
- technical debts introduced without registration.

Report must contain: finding, evidence (file/line/command), severity, impact, recommendation and whether approval is required.

Never claim that tests passed if they were not executed. If there is no access to the repository or environment, declare the limitation.
