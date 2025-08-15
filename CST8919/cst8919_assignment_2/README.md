# CST8919 – DevOps Security and Compliance  
## Assignment 2 – Cloud Service Alternatives Report  

**Author:** Daniel Karengera  
**Date:** August 15, 2025  
**Course:** CST8919 – DevOps Security and Compliance  

---

## 1. Introduction  
This report compares key Microsoft Azure services used in the course with their equivalent offerings in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**.  

The goal is to:  
- Identify functional equivalents across cloud providers.  
- Compare **core features**, **security/compliance capabilities**, **pricing models**, and **DevSecOps integration**.  
- Present findings in a concise, professional Markdown format for real-world documentation purposes.  

The Azure services reviewed:  
1. Azure Active Directory (SSO, IAM)  
2. Azure Monitor & Log Analytics  
3. Azure Policy  
4. Microsoft Defender for Cloud  
5. Azure Sentinel (SIEM/SOAR)  

---

## 2. Service Comparison Table (Quick Reference)  

| **Category** | **Azure** | **AWS Equivalent** | **GCP Equivalent** |
|--------------|-----------|--------------------|--------------------|
| Identity & Access | Azure Active Directory (Microsoft Entra ID) | AWS IAM & AWS IAM Identity Center (SSO) | Google Cloud Identity |
| Monitoring & Logging | Azure Monitor & Log Analytics | AWS CloudWatch & CloudWatch Logs | Google Cloud Observability (Cloud Logging, Cloud Monitoring) |
| Policy Enforcement | Azure Policy | AWS Config | Google Cloud Policy Intelligence |
| Cloud Security Posture Mgmt (CSPM) & Workload Protection | Microsoft Defender for Cloud | AWS Security Hub | Google Security Command Center |
| SIEM/SOAR | Microsoft Sentinel | AWS GuardDuty + AWS Security Hub | Google Security Command Center + Chronicle Security Operations |

---

## 3. Detailed Service Comparisons  

### 3.1 Azure Active Directory (Microsoft Entra ID)  
**Overview:**  
Cloud-based Identity and Access Management (IAM) service offering SSO, MFA, conditional access, and protection for both cloud and on-premises resources.  

| **Aspect** | **Azure Active Directory** | **AWS IAM & IAM Identity Center** | **Google Cloud Identity** |
|------------|---------------------------|------------------------------------|---------------------------|
| **Core Features** | Centralized user directory, SSO for SaaS apps, conditional access policies, MFA, Privileged Identity Management (PIM). | Fine-grained role-based permissions, temporary credentials, centralized SSO, federation with corporate directories. | Managed users/groups, SSO for Google Workspace and third-party apps, MFA, context-aware access. |
| **Security & Compliance** | SOC 2, ISO 27001, supports MFA, PIM, conditional access, identity protection. | IAM Access Analyzer for least privilege, SOC 2, ISO 27001, PCI DSS, FedRAMP. | Integrated with Security Center, ISO 27001, SOC 2, FedRAMP, context-aware security. |
| **Pricing Model** | Free tier + Premium P1/P2 per-user/month pricing for advanced features. | Free (costs apply for other AWS services using IAM). | Free tier; premium plans for advanced reporting & management. |
| **DevSecOps Integration** | Integrates with Azure DevOps/GitHub for identity-based access in pipelines. | IAM roles for CI/CD automation, integrates with CodePipeline, SAML/OIDC federation. | IAM roles & service accounts for Cloud Build & CI/CD services. |

---

### 3.2 Azure Monitor & Log Analytics  
**Overview:**  
Unified monitoring service for metrics, logs, and application performance, with Kusto Query Language (KQL) for deep log analysis.  

| **Aspect** | **Azure Monitor & Log Analytics** | **AWS CloudWatch & CloudWatch Logs** | **Google Cloud Observability** |
|------------|-----------------------------------|---------------------------------------|---------------------------------|
| **Core Features** | Metrics, dashboards, log aggregation (Log Analytics), Application Insights, alerting. | Metrics, dashboards, log storage (CloudWatch Logs), query with CloudWatch Logs Insights. | Cloud Logging, Cloud Monitoring, metrics dashboards, query support. |
| **Security & Compliance** | Centralized logging for security & compliance, supports audit trails. | Integrated with CloudTrail for auditing, alarms for compliance events. | Works with Security Command Center, audit logging, IAM-based access control. |
| **Pricing Model** | Per-GB ingestion & retention. Application Insights billed separately. | Free tier for basic metrics, logs charged per GB ingested and scanned. | Free tier includes a baseline; overage billed per GB. |
| **DevSecOps Integration** | Monitors pipeline health, logs deployment events for troubleshooting. | Alerts on CI/CD pipeline events, integrates with automation. | Real-time pipeline log monitoring with Cloud Build integration. |

---

### 3.3 Azure Policy  
**Overview:**  
Policy-as-code service to enforce compliance and governance across Azure resources.  

| **Aspect** | **Azure Policy** | **AWS Config** | **Google Cloud Policy Intelligence** |
|------------|------------------|----------------|---------------------------------------|
| **Core Features** | Audits & enforces resource compliance, built-in & custom policies, compliance dashboard. | Records configurations, evaluates compliance, supports remediation triggers. | Analyzes IAM policies, recommends optimizations, helps manage access. |
| **Security & Compliance** | Integrates with Defender for Cloud, CIS & PCI benchmarks. | CIS, PCI DSS checks, configuration change timeline. | Helps maintain least privilege, integrates with compliance workflows. |
| **Pricing Model** | No direct cost; charges may apply for remediation. | Charged per configuration item; free tier available. | Included with Cloud IAM (no separate pricing). |
| **DevSecOps Integration** | Validates IaC templates before deployment. | Validates CI/CD deployed resources, triggers Lambda for remediation. | Provides security insights for developers before changes go live. |

---

### 3.4 Microsoft Defender for Cloud  
**Overview:**  
A unified CSPM (Cloud Security Posture Management) and CWP (Cloud Workload Protection) solution.  

| **Aspect** | **Defender for Cloud** | **AWS Security Hub** | **Google Security Command Center** |
|------------|------------------------|----------------------|-------------------------------------|
| **Core Features** | Security score, threat protection, vulnerability scanning, multi-cloud support. | Centralized security alerts, automated compliance checks. | Asset inventory, vulnerability scanning, risk management. |
| **Security & Compliance** | HIPAA, PCI DSS, ISO 27001 compliance dashboard. | Consolidates compliance from AWS services (CIS, PCI, HIPAA). | Benchmarks like CIS, PCI DSS, FedRAMP support. |
| **Pricing Model** | Free CSPM tier, paid per protected resource for advanced features. | Free tier for first 10,000 findings; paid for extra checks/findings. | Free standard tier; premium billed per protected resource. |
| **DevSecOps Integration** | Container image scanning in pipelines, recommendations for developers. | Ingests CI/CD security findings, integrates with automation. | Integrates with Cloud Functions for auto-remediation in pipelines. |

---

### 3.5 Azure Sentinel (Microsoft Sentinel)  
**Overview:**  
Cloud-native SIEM/SOAR solution with AI-driven analytics and automated response playbooks.  

| **Aspect** | **Azure Sentinel** | **AWS GuardDuty + Security Hub** | **Google Security Command Center + Chronicle** |
|------------|--------------------|-----------------------------------|-----------------------------------------------|
| **Core Features** | Threat intelligence, centralized security analytics, playbooks for response. | GuardDuty detects threats; Security Hub aggregates findings. | Security Command Center + Chronicle for SIEM/SOAR capabilities. |
| **Security & Compliance** | Ingests security data for compliance, supports custom detection rules. | Machine learning threat detection, compliance data centralization. | Threat detection, vulnerability scanning, compliance tracking. |
| **Pricing Model** | Per-GB ingestion; commitment tiers for cost optimization. | GuardDuty billed per GB analyzed; Security Hub per check/finding. | Standard tier free; premium based on protected resources. |
| **DevSecOps Integration** | Monitors CI/CD pipelines for anomalous activity. | Tracks access key use in pipelines, provides feedback to developers. | Auto-remediation workflows triggered by findings. |

---

## 4. Conclusion  
While Azure, AWS, and GCP each provide similar **security, compliance, and DevSecOps** capabilities, their implementations and pricing differ.  
- **Azure** services are tightly integrated with Microsoft’s ecosystem (Azure DevOps, GitHub).  
- **AWS** offers granular control and integration flexibility with Lambda for automation.  
- **GCP** emphasizes AI-driven insights and Google Workspace integration.  

Choosing a provider depends on **organizational needs, existing cloud footprint, and integration requirements** for DevSecOps pipelines.  
