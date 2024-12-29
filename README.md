# Netspective Unified Solutions Architecture

Netspective Unified Solutions Architecture is a robust, SOC2-compliant framework designed to provide reliable, scalable, and secure solutions for enterprise needs. This architecture integrates multiple components into a cohesive system, ensuring seamless interoperability, high performance, and compliance with stringent security standards. The architecture underpins all Netspective offerings, facilitating efficient operations and delivering unmatched customer value.

## Unified Solutions Infrastructure (USI)

### 1. Unified Publishing Infrastructure (UPI)

The Unified Publishing Infrastructure (UPI) serves as the foundation for publishing content and functionality across all Netspective solutions targeting the web. It ensures:
- Consistent content delivery
- High scalability
- Reusability across projects

### 2. Unified Data Infrastructure (UDI)

**SQL-First Approach:** All Netspective solutions prioritize SQL for data management, using SQLite as the primary database and PostgreSQL as a secondary option.

**SQL Aide Library:** The UDI relies on the SQL Aide library to:
- Generate SQL Data Definition Language (DDL), Data Query Language (DQL), and Data Manipulation Language (DML).
- Streamline database operations through stored procedures and functions.

### 3. UDI for Service Integration and Interoperability (SII)

To bridge the gap between UPI-based user experiences and UDI-based data stores, the UDI-SII component acts as a critical glue layer. 

**Key Features:**
- Resource Surveillance and Integration Engine (`surveilr`): Facilitates SQL-first ELT (Extract, Load, Transform) operations for data preparation and ingestion.
- Ensures efficient coordination between UPI and UDI boundaries.

### 4. Unified Content Infrastructure (UCI)

Netspective solutions embrace a Markdown-first approach through the Unified Content Infrastructure (UCI):
- **Content Governance:** Git-backed, type-safe frontmatter for maximum reusability.
- **Preferred Formats:** Markdown, MDX, and HTML.
- **Content Layer:** Built on Astro 5.x+ for seamless integration and management.

### 5. Infrastructure as Code (IaC)

Netspective’s IT infrastructure is defined and managed programmatically to minimize human intervention and errors:
- Automates deployment and configuration.
- Enables consistent and reproducible setups.

### 6. Unified "X as Code" Strategy

Beyond IaC, Netspective extends the principle to other business processes and documents, transforming them into revision-controlled coding artifacts for enhanced traceability.

### 7. Machine Queryable Evidence

All security control assertions and compliance evidence are stored as machine-queryable rules and code, enabling automated validation through SQL or similar query languages.

### 8. Multiple Deployment Destinations

Netspective solutions can be deployed in various environments:
- Bare metal
- Virtual Machines (VMs)
- Cloud
- Serverless edge networks

## Customer Hub

The minimal instantiation of the Unified Solutions Architecture is the "Netspective Customer Hub" pattern. This architecture forms the backbone for delivering customized portals for each customer, offering a unified interface to all Netspective capabilities. The "Opsfolio Hub" is one specific example of a "Customer Hub," tailored to compliance-related services.

Each Customer Hub is a multi-instance multi-tenant software platform, customized for each customer as their primary portal to access all Netspective capabilities, including Opsfolio Suite and other services.

**Customer Hub:** Each customer receives a dedicated portal at `https://<customer-Id>.hub.X.com`, tailored to their needs and preferences:
- **Customizability:**
  - High-end clients receive fully bespoke services.
  - Lower-tier clients receive basic configurations, including white labeling.
- **Portability:**
  - Hosted by Netspective with the option to migrate to other environments upon request.

**Technical Details:**
- **Framework:** Astro 5.x+ for seamless site development.
- **Containerization:** Docker-based deployments for flexibility and scalability.
- **Databases:** Default SQLite with optional PostgreSQL, SQL Server, ORACLE, or others (based on customer requirements).

### Key Features

1. **Customer Portal:**
   - Unified access to all Netspective services and products.
   - A visual centerpiece for customer trust and transparency.

2. **Integration Capabilities:**
   - Launch multiple instances of `surveilr web-ui` for RSSDs.
   - Proxy SQLPage outputs through custom Astro components for enhanced functionality.

---

The Netspective Unified Solutions Architecture and SOC2-compliant infrastructure provide a reliable foundation for enterprise-grade solutions. By integrating publishing, data, and content infrastructures, along with robust compliance capabilities, Netspective ensures seamless service delivery across multiple environments. 

