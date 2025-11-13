# Cloud Migration Reference Guide

**My personal checklist for planning cloud migrations**

This isn't a framework or automation tool—it's a reference document I compiled over 3+ years of cloud work. It covers the migration strategies, tools, and decision points I use when planning AWS/Azure/GCP migrations.

## What This Is

A 417-line checklist organized by migration phase:
- **Pre-Migration Planning** - Asset inventory, dependency mapping, compliance checks
- **Cloud Strategy** - IaaS vs PaaS vs SaaS, cost analysis, vendor selection
- **Security & Compliance** - IAM, encryption, GDPR/HIPAA/SOC 2 considerations
- **Architecture Design** - Networking, storage, compute, HA/DR planning
- **Migration Planning** - Rehosting vs refactoring vs rearchitecting

## Why I Made This

After my third cloud migration project, I realized I was Googling the same things every time:
- "What's the difference between AWS Snowball and Azure Data Box again?"
- "Which compliance frameworks do I need for healthcare data?"
- "What's the 6 Rs of migration?" (Rehost, Replatform, Refactor, Repurchase, Retire, Retain)

So I compiled everything into one document. It's basically the outline I follow when scoping a migration engagement.

## What's Inside

**Migration Strategy Comparison Table:**
- Rehosting (Lift & Shift) - Fast but misses optimizations
- Replatforming - Minor changes (e.g., switch to RDS)
- Refactoring - Full rebuild for cloud-native
- Repurchasing - Replace with SaaS (Salesforce, Office 365)
- Retiring - Decommission legacy systems
- Retaining - Keep on-prem (for now)

**Tool Reference Tables:**
- Cloud platforms: EC2, Azure VMs, GCP Compute Engine
- Migration tools: AWS Migration Hub, Azure Migrate, Google Migrate
- Networking: Direct Connect, ExpressRoute, Cloud Interconnect
- Security: IAM services, KMS, DDoS protection
- Monitoring: CloudWatch, Azure Monitor, Stackdriver

**Migration Template (The Bulk of the Doc):**
- Pre-migration planning checklist
- Business case & ROI analysis
- Current state assessment
- Application suitability matrix
- Compliance requirements
- Network design patterns
- Storage strategies
- HA/DR architecture
- Cutover planning
- Post-migration validation

## How I Use This

1. **Kickoff meeting** - Reference the business case section to align stakeholders
2. **Assessment phase** - Use the asset inventory checklist
3. **Architecture design** - Pull relevant design patterns (networking, storage, compute)
4. **Migration execution** - Follow the cutover checklist
5. **Post-migration** - Validation and optimization steps

Most of these sections are just organized checklists. I don't follow them linearly—I jump to whichever section is relevant for the current phase.

## What This Isn't

**Not automation:** No Terraform modules, no scripts, no CI/CD pipelines. This is documentation, not code.

**Not comprehensive:** It covers the common scenarios I encounter (AWS-heavy, some Azure, minimal GCP). There are gaps—no mainframe migrations, no SAP-specific guidance, light on containerization strategies.

**Not prescriptive:** Every migration is different. This is a starting point, not a playbook. You'll need to adapt it.

## Real-World Use

I've referenced this on:
- 3 enterprise cloud migrations (financial services, healthcare, e-commerce)
- 5+ smaller lift-and-shift projects
- Architecture design reviews
- Vendor selection discussions

The most-used sections:
- Migration strategy comparison (helps explain trade-offs to non-technical stakeholders)
- Compliance checklist (GDPR, HIPAA, PCI DSS requirements)
- Tool comparison tables (when evaluating vendors)
- Cutover planning template (night-of-migration coordination)

## Contributing

This is a living document. If you spot an error or want to suggest additions, open an issue or PR. Just know that I'm optimizing for "useful reference" over "exhaustive encyclopedia."

---

**Last updated:** 2024  
**Status:** Active reference, updated as I learn new patterns  
**Best used for:** AWS/Azure migrations, compliance-heavy environments, enterprise-scale projects
