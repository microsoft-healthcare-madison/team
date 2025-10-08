# OKRs for July - Sept 2025

## Enhance HL7 Specifications
* P1 (BP) Continue progress in reconciling FHIRPath specification toward R3 release before Christmas 2025 (2 weeks)
    * [x] (1.0) All approved jira changes applied to the specification - *remaining tickets need clarifications/re-opening*
    * (0.9) All open jira issues have proposed dispositions pending committee time/approval
    * (0.1) Additional unit test cases added for enhancements/changes to the fhirpath specification
* [x] P1 (BP) (1.0) Support the reconciliation of the SDC R4 specification, hoping to be complete, and changes applied for publication around Sept WGM (2 weeks)
* P2 (BP) (0.5) Apply the Patient Administration R6 changes to the core specification (3 days)
* P2 (BP/GC) (0.0) FML core spec issues identified and changes applied (1 week) 
* P1 (BP) (0.1) Apply all approved core spec fhirpath page changes 
* P3 (BP) (0.0) FML g4 approved into FHIR R6 (1 week)
* P3 (BP) (0.0) Apply Gino's updated xver extensions database into the FML cross version maps, and validate consistency (2 weeks)
    * P3 FML Maps validated for consistency with xversion extensions/maps - tooling reports issues
    * P4 FML Maps updated to also include the xversion extensions

## Provide Educational Content to support Users of HL7 specifications
* P1 (BP) Education Material supporting SDC extraction - At least 2 YouTube clips and 2 blog posts (3 days)
  * Learning objectives
      * (0.5) Understand and apply template-based extraction
      * Understand and apply definition-based extraction
* P2 (BP) Education Material supporting FHIRPath - At least 2 YouTube clips and 2 blog posts (3 days)
  * Learning objectives
      * (0.5) Debugging FhirPath expressions
      * Understanding FhirPath $this, $focus and input collections
  * unplanned (0.1) started building learning material for fhirpath "fhirpath-by-example"


## Enhanced tooling to support IG creators and consumers
* P1 (BP) finish first pass of the FHIRPath debugger in dotnet, js and hapi (and Health Samuari?)
    * [x] (1.0) Debug Trace injection point available in public HAPI library
    * [x] (1.0) UI for Debugging released in production deployment of FhirPath Lab
    * (0.9 *PR in progress*) Debug Trace injection point available in public FhirPath.js library
    * [x] (1.0) Debug Trace injection point available in public Firely SDK
    * [x] P2 (1.0) AST/Debug interface documented
    * P3 (0.0 *though they are considering it*) Health Samurai implements AST and debug trace support for the FhirPath Lab
* P2 (BP) Approved new FhirPath features applied to open source engines
    * (0.5) coalesce
    * (0.5) sort
    * (0.2) (testing and education for $focus)
* [x] P3 (BP) (1.0) Continue discussions with Ewout to move my SDC project into Firely (3 days)
* Prototyping activities:
    * P3 (BP) (0.0) FML Validator onto nuget - consider permanent home
    * P4 (BP) (0.0) POC FML Map transpilation into c#/typescript/js for more performant execution (1 week)
    * P5 (BP) (0.0) Test tooling for x-fhir-query in the fhirpath lab? (2 days)
* Unplanned extras (BP)
    * [x] (1.0) Inclusion of new fhirpath engines from Heleos Software (rust), OctoFHIR(rust), AtomicEHR(ts) and Damedic(go)
    * (0.8) CQL-Facade Proof Of Concept in advanced developer mode
    * Exploration of SMART Web Messaging to integrate forms engines


## Objective: FHIR R6 is a high-quality release for Long-Term Use

### The following areas of the specification are clear, correct, concise, and have examples detailing use
* The following areas of the specification have no tickets in 'waiting for input' or 'unapplied' states.
    * P0 (GC) (0.3): FHIR Search
    * P0 (GC) (0.5): FHIR RESTful API
    * P0 (GC) (0.5): Subscriptions Framework
* Review the following areas of the specification to ensure there are examples where they are needed, and that examples are correct.
    * P3 (GC) (0.2): FHIR Search
    * P3 (GC) (0.1): FHIR RESTful API
    * P3 (GC) (0.5): Subscriptions Framework

### FMG and WGs are aligned on content for core and 'additional' resource development
* P2 (GC) (0.75): FMG has concrete plan for improved communication with WGs moving forward (whether liasons or other framework)
* P0 (GC) (0.8): FMG publishes a clear description of the process for *determining* whether content is 'core' or 'additional'
* P3 (GC) (0.25): FMG publishes a clear description of the process for developing/publishing additional content
* P1 (GC) (0.75): WGs responsible for core FHIR content understand the 'core' vs. 'additional' distinction for resources
* P2 (GC) (1.0): WGs responsible for core FHIR content have the majority of their resources properly allocated (target: ~75%)
* P3 (GC) (0.2): FMG publishes guidance for breaking change considerations between R4, R5, and R6.

## Objective: FHIR Implementers have a path for interoperably adopting features from outside 'their' FHIR version
* P0 (GC) (0.75): Publish the cross-version extension packages in a milestone release
* Cross-Version artifacts have been reviewed
    * P2 (GC) (?): ValueSets
    * P2 (GC) (?): Extensions
    * P2 (GC) (?): Profiles
* P3 (GC) (0.5): Publish version ~~1.2~~ 2.0 of the subscription backport IG
* P5 (GC) (0.5): Argonaut R4-R6 transition work... (e.g., socialize with other accelerators, etc.)

## Objective: Patients and Implementers can use AI to interact with FHIR in reliable and ethical ways
? ## Objective: AI Tools can Understand, Consume, and Produce FHIR Reliably
* P0 (GC) (0.25): `FHIR-MCP-Tools`: Start or support the start of a repo that contains MCP Tool definitions for common tools.
    * Definitions include:
        * Desriptions of definitional content (e.g., resources, search types, etc.)
        * Input and output schemas
        * ...
    * Example tools include:
        * Validate a search query
        * Look up definitions from a FHIR Core version
        * Look up definitions from an IG Version
        * Answer questions based on a capability statement (and feature)
        --
        * Validate a FHIR resource against specific FHIR + IG versions
* P0 (GC) (0.5): Add support to candle that exposes `FHIR-MCP-Tools`:
    * P0 (0.5): In a general purpose way
    * P1 (0.0): "About" an external FHIR server, i.e., constrainted by that server's
        * Capabilities
        * Search
        * SMART Launch / Scopes (tie in with Argo project)
        * Note: Determine if this type of implementation should even expose the FHIR API

## Objective: Lower the bar for implementers working through IG-based requirements
* P3 (GC) (0.0): Update the IG-based C# generation to ensure complete support of:
    * P3 (GC): IG-based canonical URL listings
    * P3 (GC): IG-based extension accessors
    * P3 (GC): IG-based profile accessors (e.g., slice accessors)
* P9 (GC) (0.0): Create a first pass of TypeScript IG-based export

## Objective: Handle unplanned work
* (GC) (0.65): Transition fhir-codegen to a FHIR Foundation project
* (GC) (1.0): Meeting coordination tasks (internal)
* (GC) (0.75): FMG has tooling available to help WGs process all of their FHIR content
* (GC) (1.0): Create tooling to generate SQL databases based on specification content (in fhir-codegen)
* (GC) (0.4): FHIR and openEHR have sensible and usable data type mappings between specifications

## Objective: Improve analytics and AI-training workflows by improving the performance of FHIR content-extraction
* P∞: (GC/BP) Review FHIR-Net-SDK (v6) parse/serialize performance and look for optimization opportunities
* P∞: Implement a high-performance SQL-on-FHIR extraction utility
* P∞: Consider pre-extraction of _measure_ type data into discrete values for later use

## Objective: Secure a pathway for standards-based, patient-controlled data sharing

* P0 (JM) (1.0): The SMART Health Cards & Links specification is finalized and published through HL7.

* P1 (JM) (0.0): Clear principles guide policy development for trustworthy network exchange
    * P1 Conduct discussions with at least two TEFCA stakeholders to inform the paper's content.
    * P1 Draft paper to include clear principles and a proposed pathway from today's exchange networks.
    * P1 Publish the paper as a publicly accessible article
* [Unplanned] LinkedIn versions of this :-)  

## Objective: Inspire the community and build momentum for AI in health interoperability

* P0 (JM/GC?) (1.0): A successful "Conversational Interop" connectathon track is hosted to demonstrate a practical AI use case.
    * P1 (1.0) Develop and publish a v0.1 open-source reference implementation (client and server) for a conversational clinical referral workflow.
    * P0 (1.0) Finalize and publish the connectathon track page with scope, scenarios, and links to the reference implementation.
    * P1 (1.0) Attract between 10 and 30 participants to actively test the workflow.
    * P2 (1.0) Synthesize connectathon feedback into a public summary document with key findings and recommendations.
    * [Unplanned] (0.8) Submit a scholarly publication proposing conversational interoperability and sharing early experience

* P1 (JM/GC?) (0.0): The HL7 "AI in Standards" Club is launched to build a community of practice.
    * P1 Draft and publish a charter for the group, outlining its goals and lightweight governance.
    * P1 Establish a dedicated public channel (`#ai-in-standards-club`?) on chat.fhir.org.
        * Maybe [Artificial Intelligence/Machine Learning (AI/ML)](https://chat.fhir.org/#narrow/channel/323443-Artificial-Intelligence.2FMachine-Learning-.28AI.2FML.29)
    * P1 Schedule and host the first two monthly meetings, focusing on practical prototypes and member-driven topics.

* P2 (JM) (0.0): The "EHI Showcase" research demo is published to inspire new thinking about complex health data.
    * P1 Develop and publish the open-source EHI toolkit on GitHub, including utilities to structure and de-identify data.
    * P2 Implement an AI-powered agentic workflow that dynamically generates at least three distinct clinical summary views (e.g., Medication History, Problem List).
    * P2 Record and publicly share a video walkthrough of the showcase and its underlying concepts.

* [Unplanned] (1.0): Kiln for synthetic FHIR data!
* [Unplanned]: CMS Health Tech Pledge Ecosystem
