# Meta Prompt

As an expert prompt engineer and software architect.

I need to create an ATS (Applicant-Tracking System) system for a startup company called LTI. The full cycle of this systems are:

1. Creating Jobs
2. Jobs published on Job boards, website, Social Media, etc
3. Job Applications recieved
4. Applications are reviewed
5. Online Tests are conducted
6. Interviews are scheduled
7. Selected applicants are hired

For this new system we need to create the following artifacts:

* Software Brief description, its added value and competitive advantages
* Explanation of main functions
* Lean canvas diagram to illustrate the business model
* Describe the 3 main uses cases with a diagram for each case
* ER Data model with entities, attributes and relationships
* High level system design, explanation and diagram
* C4 diagram going deep into one of the system's component. Please ask me which one.

Your task is to create a prompt to accomplish these goals. Keep in mind the following:

* All diagrams must be in mermaid format 
* Create a unique document with all the information in markdown format with the name "LTI-em.md"

For C4 diagram, it showed me 5 different components and made me choose with one to diagram. I chossed "Application Review & Scoring Module"

---

## Prompt 1

You are an expert software architect and technical writer. Your task is to produce 
a complete, professional software documentation artifact for a new Applicant Tracking 
System (ATS) built for a startup company called **LTI**.

The ATS covers the following end-to-end hiring lifecycle:
1. Creating Jobs
2. Publishing Jobs on boards, websites, and social media
3. Receiving Job Applications
4. Reviewing Applications
5. Conducting Online Tests
6. Scheduling Interviews
7. Hiring Selected Applicants

---

## OUTPUT REQUIREMENTS

Produce a **single Markdown document** named `LTI-em.md` containing ALL of the 
following sections, in order. Every diagram MUST be written in valid **Mermaid** 
syntax inside a mermaid code fence (```mermaid ... ```).

---

### SECTION 1 — Software Brief, Added Value & Competitive Advantages

Write a concise but compelling overview of the LTI ATS that includes:
- What the system does (2–3 paragraphs)
- Its core added value for HR teams and hiring managers
- At least 5 concrete competitive advantages over existing ATS solutions 
  (e.g., Workday, Greenhouse, Lever), focusing on: AI-assisted screening, 
  multi-channel job distribution, integrated testing, real-time analytics, 
  and scalability for startups

---

### SECTION 2 — Main Functions

Describe in detail the **7 main functional modules** of the system, one per 
subsection, mapping directly to the hiring lifecycle steps above. For each module 
provide:
- Module name and purpose
- Key features (bullet list)
- Primary actors/users involved

---

### SECTION 3 — Lean Canvas Diagram

Create a Lean Canvas business model for LTI ATS with all 9 standard boxes:
1. Problem
2. Customer Segments
3. Unique Value Proposition
4. Solution
5. Channels
6. Revenue Streams
7. Cost Structure
8. Key Metrics
9. Unfair Advantage

Represent this as a Mermaid diagram. Use a `graph TD` or `block-beta` layout 
to approximate the Lean Canvas grid structure, clearly labeling each of the 
9 boxes with their content.

---

### SECTION 4 — Top 3 Use Cases with Diagrams

Identify and describe the **3 most critical use cases** of the LTI ATS system. 
For each use case provide:
- Use Case Name & ID
- Brief description (2–3 sentences)
- Actors involved (primary and secondary)
- Preconditions and postconditions
- Main flow (numbered steps)
- A Mermaid **sequence diagram** illustrating the interaction flow between 
  actors and system components

The 3 use cases must be:
1. **Job Creation & Multi-Channel Publishing**
2. **Application Ingestion & AI-Assisted Review**
3. **Interview Scheduling & Candidate Notification**

---

### SECTION 5 — Entity-Relationship (ER) Data Model

Design a comprehensive ER model for the LTI ATS. It must include at minimum 
the following entities with their key attributes and all relationships 
(one-to-many, many-to-many, etc.):

Entities: Company, Job, JobPosting, Channel, Candidate, Application, 
Resume, OnlineTest, TestResult, Interview, InterviewFeedback, Recruiter, 
HiringManager, Offer

Represent this as a Mermaid `erDiagram` with:
- All entities and their typed attributes
- All cardinality relationships clearly labeled with action verbs

---

### SECTION 6 — High-Level System Design

#### 6.1 — Written Explanation
Describe the high-level architecture of the LTI ATS covering:
- Architectural style chosen (e.g., microservices, event-driven) and rationale
- Main system layers (presentation, API gateway, services, data, integrations)
- Key external integrations (LinkedIn, job boards, calendar APIs, email/SMS, 
  AI/ML scoring engine, cloud storage)
- Non-functional considerations: scalability, security, availability

#### 6.2 — Architecture Diagram
Produce a Mermaid `graph TD` (or `flowchart TD`) high-level architecture diagram 
showing all major components, layers, and their interactions, including:
- Frontend clients (Web App, Mobile App)
- API Gateway
- Core microservices (Job Service, Application Service, Review & Scoring Service, 
  Testing Service, Interview Service, Notification Service, Analytics Service)
- Message broker / event bus
- Databases (per service)
- External integrations
- Cloud infrastructure layer

---

### SECTION 7 — C4 Diagram: Application Review & Scoring Module

Produce a **full C4 model drill-down** into the **Application Review & Scoring 
Module**, covering all four C4 levels:

#### Level 1 — System Context Diagram
Show how the Application Review & Scoring Module fits within the broader LTI ATS 
system and its external actors (Recruiter, Hiring Manager, AI/ML Engine, 
Candidate, Email Service).
Use Mermaid `graph TD`.

#### Level 2 — Container Diagram
Decompose the system into its containers:
- Web UI (React)
- Backend API (Node.js / REST)
- Review & Scoring Service
- AI/ML Scoring Engine (Python microservice)
- PostgreSQL Database
- Redis Cache
- Message Queue (e.g., RabbitMQ or Kafka)
Use Mermaid `graph TD`.

#### Level 3 — Component Diagram
Zoom into the **Review & Scoring Service** container and show its internal 
components:
- Application Intake Handler
- Resume Parser
- AI Score Orchestrator
- Manual Review Controller
- Scoring Rules Engine
- Notification Dispatcher
- Audit Logger
Use Mermaid `graph TD`.

#### Level 4 — Code Diagram
Model the key classes/interfaces of the **AI Score Orchestrator** component:
- Classes: ApplicationScorer, ScoringStrategy (interface), 
  KeywordMatchStrategy, MLModelStrategy, WeightedScoreAggregator, 
  ScoreResult, ApplicationDTO
- Show methods, properties, and relationships (implements, uses, returns)
Use a Mermaid `classDiagram`.

---

## FORMATTING RULES

- Use `#` for the document title, `##` for section headers, `###` for 
  subsections
- Every Mermaid diagram must be preceded by a short explanatory paragraph
- Use tables where comparing features or listing structured data
- Use bold for key terms on first use
- The document must be self-contained and read as a professional deliverable
- Begin the document with a title page block containing: document name 
  (LTI-em.md), version (1.0), date, and authors (LTI Engineering Team)

---

Now generate the complete `LTI-em.md` document following all instructions above.

---

## Prompt 2

Can you please recheck the Lean Canvas diagram. When I try to open it in Mermaid Live Editor I got an error:

```
Error: Error: Parse error on line 5:
...    subgraph Row1[""]            P["**1
-----------------------^
Expecting 'TAGEND', 'STR', 'MD_STR', 'UNICODE_TEXT', 'TEXT', 'TAGSTART', got 'SQE'
Sample Diagrams
FlowchartClassSequenceEntity RelationshipStateMindmapArchitectureBlockC4GanttGitKanbanPacketPieQuadrantRadarRequirementSankeyTimelineTreemapUser JourneyXYZenUML
Actions
```
