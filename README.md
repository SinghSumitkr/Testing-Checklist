Here is the cleaned-up and consolidated Production Deployment Checklist for moving Qlik Sense dashboards to the Production environment. I've removed duplicates and combined similar items for clarity and brevity, while preserving coverage of all key areas such as UAT validation, data integrity, code quality, environment readiness, and approvals.

✅ Production Deployment Checklist – Qlik Sense Dashboard
1. UAT Validation
 Has the dashboard been successfully executed in UAT, with success logs and evidence (e.g., screenshots, logs, timestamps) captured?

 Has the dashboard been tested for performance in UAT (including load time, rendering, responsiveness)?

 Has the dashboard been load-tested with production-like data volumes (e.g., ≥15 GB for high-volume dashboards)?

 Are filters, selections, and navigation working as expected in UAT?

 Has user acceptance testing (UAT) been signed off by both business and technical stakeholders (e.g., CCS team)?

 Has QA/Test team approved the UAT results?

2. Data Integrity & Validation
 Is historical data concatenating accurately with AWS data in the Transform Layer?

 Is reference data in UAT sourced from EMEA or Ref DB, and will it switch appropriately in PROD?

 Are Common and Securities Common QVDs being pulled from correct AWS locations?

 Are all data load conditions (e.g., incremental loads, row counts, duplication checks) working correctly?

 Is sensitive data masked or encrypted as per compliance requirements (e.g., GDPR, CCPA)?

3. Code Quality & Configuration
 Has the load script and logic been peer-reviewed for efficiency, correctness, and security?

 Are all hardcoded values removed or parameterized appropriately using variables/configs?

 Are debug/logging statements removed or turned off in production scripts?

 Are naming conventions for fields, sheets, variables, and objects consistent with team standards?

 Are data reduction rules and access controls (e.g., region-wise filters, Section Access) tested and working correctly?

 Are environment-specific variables (e.g., API keys, DB paths) working correctly in DEV and UAT?

4. Infrastructure & Monitoring
 Has the dashboard been validated in a staging/PROD-like environment using final AWS data sources?

 Is a monitoring mechanism in place to track reload success/failure (e.g., logs, alerts)?

 Are automated data backups scheduled and tested for successful recovery?

 Is a failover or recovery mechanism documented for critical components (e.g., AWS Aurora, Athena)?

5. Documentation & Post-Deployment Readiness
 Is a runbook or support documentation (e.g., error handling, known issues, contact details) available?

 Has a named support contact been assigned for post-deployment monitoring?

 Has a post-release review or checkpoint meeting been scheduled?

6. Approvals & Governance
 Has the deployment request been submitted and approved through the Change Management or JIRA system?

 Has final approval for go-live been obtained from the Technical Lead and Product/Data Owner?

 Is a rollback plan documented and validated in case of deployment failure?

 Has a backup of the current PROD dashboard/data been taken before deployment?
