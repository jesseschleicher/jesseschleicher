## Jesse Schleicher

I build data platforms that outlive the person who wrote them.

Eighteen years at a managed services provider, owning the systems the business runs on:
the data warehouse, the billing platform, the client portal, and the security analytics
product. Most of my work lives in private repositories; here's what it consists of.

### Data platform
Two generations of an enterprise warehouse, both designed and built solo. The current
one I rebuilt from bare metal in 2021-22: server, ingestion framework, processing engine,
temporal storage model, config database, monitoring. In continuous production since
January 2022.

**13** source systems · **221** tables (**103** system-versioned temporal) · **850M+**
rows · **90** import pipelines

Stack: SQL Server, T-SQL, system-versioned temporal tables, partitioning, MERGE-based
upsert ETL, PowerShell module architecture.

### Things I care about
- **Full history, always.** Every row carries its temporal record. A trigger-generation
  framework produces 265 triggers across 89 tables, capturing 7.9M field-level changes
  over 20 years. It cost more up front and it has paid for itself at every audit since.
- **Idempotency.** Every pipeline can be re-run without damage; dedup, scoped deletes,
  staleness thresholds, per-source controls.
- **Config over code.** New sources are configuration, not new programs.
- **Documentation an engineer can run without me.** Standards, templates, contracts,
  change playbooks. Written so a human or a model can pick up a project cold.

### Security analytics
Conceived and delivered an XDR analytics product end to end with no project manager —
architecture, ingestion, ETL, data model, delivery. 90 security measures computed nightly
for every client tenant across SentinelOne, Stellar Cyber, Duo, Fortra VM, Active
Directory, and ConnectWise. 99.4% run success, 47-second median runtime.

### Governed AI tooling
Four Node.js MCP servers that give AI coding agents SQL access inside the same permission
boundaries engineers get: read-only and execute separated, scoped logins, per-database
routing, statement timeouts. Agents work under the same constraints as people. I use it
daily, behind acceptance lists and per-commit review.

### Currently
Angular 21 / TypeScript 5.9 platform rebuild · governed agent workflows · looking for the
next place to own something end to end.

📫 jesse.pro@schleicher.us · [LinkedIn](https://linkedin.com/in/jesseschleicher)
