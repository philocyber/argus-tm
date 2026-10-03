# Security

The supported scope is a local, single-operator PoC with an interface bound to the loopback address. Do not expose it directly to the Internet or a shared network. The current service mode requires further evaluation before being used as a multi-user platform; see [deferred decisions](docs/security/deferred-decisions.md).

Credentials are configured via the environment or the local interface. The `.env.local` file, documents in `knowledge_base/`, and local projects contain private information and are not part of the distribution. Use approved sources for RAG. External providers receive the selected context for each analysis; verify internal authorization before enabling them.

Local mutations require the same-origin policy and loopback access. In PostgreSQL mode, analysis tokens do not allow modification of credentials or the global corpus. These restrictions do not replace SSO, resource-level authorization, or multi-user isolation.

Do not include secrets or private documents when reporting vulnerabilities in open issues. In the event of an exposure, revoke the affected credential and follow the incident response process of the organization controlling the data.

Continuous integration runs tests, dependency audits, and an independent secrets scan. An audit with no findings does not certify the product's security.
