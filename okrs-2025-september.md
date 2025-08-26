# OKRs for July - September 2025


## Enhance HL7 Specifications
* P1 (BP) Continue progress in reconciling FHIRPath specification toward R3 release before Christmas 2025 (2 weeks)
    * All approved jira changes applied to the specification
    * All open jira issues have proposed dispositions pending committee time/approval
    * Additional unit test cases added for enhancements/changes to the fhirpath specification
* P1 (BP) Support the reconciliation of the SDC R4 specification, hoping to be complete, and changes applied for publication around Sept WGM (2 weeks)
* P2 (BP) Apply the Patient Administration R6 changes to the core specification (3 days)
* P2 (BP/GC) FML core spec issues identified and changes applied (1 week) 
* P1 (BP) Apply all approved core spec fhirpath page changes 
* P3 (BP) FML g4 approved into FHIR R6 (1 week)
* P3 (BP) Apply Gino's updated xver extensions database into the FML cross version maps, and validate consistency (2 weeks)
    * P3 FML Maps validated for consistency with xversion extensions/maps - tooling reports issues
    * P4 FML Maps updated to also include the xversion extensions


## Provide Educational Content to support Users of HL7 specifications
* P1 (BP) Education Material supporting SDC extraction - At least 2 YouTube clips and 2 blog posts (3 days)
  * Learning objectives
      * Understand and apply template-based extraction
      * Understand and apply definition-based extraction
* P2 (BP) Education Material supporting FHIRPath - At least 2 YouTube clips and 2 blog posts (3 days)
  * Learning objectives
      * Debugging FhirPath expressions
      * Understanding FhirPath $this, $focus and input collections


## Enhanced tooling to support IG creators and consumers
* P1 (BP) finish first pass of the FHIRPath debugger in dotnet, js and hapi (and Health Samuari?) (1 week)
    * [x] Debug Trace injection point available in public HAPI library
    * UI for Debugging released in production deployment of FhirPath Lab
    * Debug Trace injection point available in public FhirPath.js library
    * Debug Trace injection point available in public Firely SDK
    * P2 AST/Debug interface documented
    * P3 Health Samurai implements AST and debug trace support for the FhirPath Lab
* P2 (BP) Approved new FhirPath features applied to open source engines
    * coalesce
    * sort
    * (testing and education for $focus)
* P3 (BP) Continue discussions with Ewout to move my SDC project into Firely (3 days)
* Prototyping activities:
    * P3 (BP) 0.0 FML Validator onto nuget - consider permanent home
    * P4 (BP) POC FML Map transpilation into c#/typescript/js for more performant execution (1 week)
    * P5 (BP) Test tooling for x-fhir-query in the fhirpath lab? (2 days)

# GC Draft Section =)

## Objective: FHIR R6 is a high-quality release for Long-Term Use

### The following areas of the specification are clear, correct, concise, and have examples detailing use
* The following areas of the specification have no tickets in 'waiting for input' or 'unapplied' states.
    * P0 (GC): FHIR Search
    * P0 (GC): FHIR RESTful API
    * P0 (GC): Subscriptions Framework
* Review the following areas of the specification to ensure there are examples where they are needed, and that examples are correct.
    * P3 (GC): FHIR Search
    * P3 (GC): FHIR RESTful API
    * P3 (GC): Subscriptions Framework

### FMG and WGs are aligned on content for core and 'additional' resource development
* P2 (GC): FMG has concrete plan for improved communication with WGs moving forward (whether liasons or other framework)
* P0 (GC): FMG publishes a clear description of the process for *determining* whether content is 'core' or 'additional'
* P3 (GC): FMG publishes a clear description of the process for developing/publishing additional content
* P1 (GC): WGs responsible for core FHIR content understand the 'core' vs. 'additional' distinction for resources
* P2 (GC): WGs responsible for core FHIR content have the majority of their resources properly allocated (target: ~75%)
* P3 (GC): FMG publishes guidance for breaking change considerations between R4, R5, and R6.

## Objective: FHIR Implementers have a path for interoperably adopting features from outside 'their' FHIR version
* P0 (GC): Publish the cross-version extension packages in a milestone release
* Cross-Version artifacts have been reviewed
    * P2 (GC): ValueSets
    * P2 (GC): Extensions
    * P2 (GC): Profiles
* P3 (GC): Publish version 1.2 of the subscription backport IG
* P5 (GC): Argonaut R4-R6 transition work... (e.g., socialize with other accelerators, etc.)

## Objective: Patients and Implementers can use AI to interact with FHIR in reliable and ethical ways
? ## Objective: AI Tools can Understand, Consume, and Produce FHIR Reliably
* P0 (GC): `FHIR-MCP-Tools`: Start or support the start of a repo that contains MCP Tool definitions for common tools.
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
* P0 (GC): Add support to candle that exposes `FHIR-MCP-Tools`:
    * P0 In a general purpose way
    * P1 "About" an external FHIR server, i.e., constrainted by that server's
        * Capabilities
        * Search
        * SMART Launch / Scopes (tie in with Argo project)
        * Note: Determine if this type of implementation should even expose the FHIR API

## Objective: Lower the bar for implementers working through IG-based requirements
* P3 (GC): Update the IG-based C# generation to ensure complete support of:
    * P3 (GC): IG-based canonical URL listings
    * P3 (GC): IG-based extension accessors
    * P3 (GC): IG-based profile accessors (e.g., slice accessors)
* P9 (GC): Create a first pass of TypeScript IG-based export

## Objective: Improve analytics and AI-training workflows by improving the performance of FHIR content-extraction
* P∞: (GC/BP) Review FHIR-Net-SDK (v6) parse/serialize performance and look for optimization opportunities
* P∞: Implement a high-performance SQL-on-FHIR extraction utility
* P∞: Consider pre-extraction of _measure_ type data into discrete values for later use

## Objective: Secure a pathway for standards-based, patient-controlled data sharing

* P0 (0.0): The SMART Health Cards & Links specification is finalized and published through HL7.

* P1 (0.0): Clear principles guide policy development for trustworthy network exchange
    * P1 Conduct discussions with at least two TEFCA stakeholders to inform the paper's content.
    * P1 Draft paper to include clear principles and a proposed pathway from today's exchange networks.
    * P1 Publish the paper as a publicly accessible article

## Objective: Inspire the community and build momentum for AI in health interoperability

* P0 (0.0): A successful "Conversational Interop" connectathon track is hosted to demonstrate a practical AI use case.
    * P1 Develop and publish a v0.1 open-source reference implementation (client and server) for a conversational clinical referral workflow.
    * P0 Finalize and publish the connectathon track page with scope, scenarios, and links to the reference implementation.
    * P1 Attract between 10 and 30 participants to actively test the workflow.
    * P2 Synthesize connectathon feedback into a public summary document with key findings and recommendations.

* P1 (0.0): The HL7 "AI in Standards" Club is launched to build a community of practice.
    * P1 Draft and publish a charter for the group, outlining its goals and lightweight governance.
    * P1 Establish a dedicated public channel (`#ai-in-standards-club`?) on chat.fhir.org.
        * Maybe [Artificial Intelligence/Machine Learning (AI/ML)](https://chat.fhir.org/#narrow/channel/323443-Artificial-Intelligence.2FMachine-Learning-.28AI.2FML.29)
    * P1 Schedule and host the first two monthly meetings, focusing on practical prototypes and member-driven topics.

* P2 (0.0): The "EHI Showcase" research demo is published to inspire new thinking about complex health data.
    * P1 Develop and publish the open-source EHI toolkit on GitHub, including utilities to structure and de-identify data.
    * P2 Implement an AI-powered agentic workflow that dynamically generates at least three distinct clinical summary views (e.g., Medication History, Problem List).
    * P2 Record and publicly share a video walkthrough of the showcase and its underlying concepts.
