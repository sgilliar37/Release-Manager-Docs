## Security Policy – Release Scheduler for Jira

### Overview

Security is a core priority of Release Scheduler for Jira. The application is built using modern security practices and leverages Atlassian Forge infrastructure where possible.

---

### Authentication & Authorization

- Jira access is handled via Atlassian Forge permissions
- Slack uses OAuth 2.0 and Bot Tokens
- All actions are validated against user permissions

---

### Data Protection

- All communication is encrypted via HTTPS (TLS 1.2+)
- No sensitive credentials are stored in plaintext
- Secrets are stored securely using environment variables or Forge secure storage

---

### Request Validation

- Slack requests are validated using signing secrets
- Webhook endpoints validate shared secrets or tokens
- Input validation is applied to all incoming payloads

---

### Least Privilege Access

The app only requests the minimum scopes required:

- Slack: chat:write
- Jira: issue read/write (as required for release workflows)

---

### Infrastructure

- Hosted using secure cloud infrastructure (Forge / managed hosting)
- No direct database exposure
- No inbound access without authentication

---

### Monitoring & Logging

- Errors and events are logged for debugging
- Logs do not contain sensitive data
- Suspicious activity can be investigated

---

### Incident Response

In the event of a security issue:

- Immediate investigation will be performed
- Affected users will be notified if necessary
- Fixes will be deployed promptly

---

### Responsible Disclosure

If you discover a vulnerability, please contact:

sgilliar37@yahoo.com
