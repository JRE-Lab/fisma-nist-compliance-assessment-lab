diff --git a/data/system-facts.md b/data/system-facts.md
new file mode 100644
index 0000000000000000000000000000000000000000..d0c739d64da0f73fe8885f0da4adfc92adcc951f
--- /dev/null
+++ b/data/system-facts.md
@@ -0,0 +1,33 @@
+# CivicAccess Case Portal (CCP) - System Facts
+
+## Mission
+
+Support intake, investigation, and resolution of federal program cases submitted by external partners and citizens.
+
+## Data types
+
+- Personally Identifiable Information (PII): names, contact info, case narratives
+- Case metadata: status, assignment, workflow notes
+- Audit logs: access records, administrative actions
+- External partner directory data (business contact information)
+
+## Architecture summary
+
+- Cloud-hosted web application in a FedRAMP Moderate PaaS
+- Identity provider with MFA for staff and partners
+- API gateway for external integrations
+- Encrypted relational database for case data
+- Centralized logging to a SIEM
+
+## External dependencies
+
+- Cloud PaaS provider (FedRAMP Moderate)
+- Identity provider (SAML/OIDC)
+- Email notification service
+- Legacy data warehouse (read-only integration)
+
+## Assumptions
+
+- Availability target is 99.9% during business hours.
+- External partner access is limited to approved IP ranges.
+- Data retention policy requires 7 years of record storage.
