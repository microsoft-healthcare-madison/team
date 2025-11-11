# OKRs for Oct 2025 - Jan 2026

## Enhance HL7 Specifications

### Objective: FHIR R6 is a high-quality release for Long-Term Use
  * P1 BP: All jira issues related to fhirpath extensions to FHIR are resolved and applied
  * P1 BP: All jira issues related to FHIR Mapping Language (FML) are resolved and applied
  * P1 BP: All approved jira issues related to Patient Administration are applied (core specification)
  * P1 BP: All approved jira issues related to Patient Administration are applied (extensions)
  * P1 BP: All approved jira issues related to Patient Administration are applied (terminology)

### Objective: FHIR Mapping Language is complete and ready for R6 conversions
  * P2 BP: FML g4 approved into FHIR R6 (1 week)
  * P2 BP: Apply Gino's updated xver extensions database into the FML cross version maps, and validate consistency (2 weeks)
      * P3 FML Maps validated for consistency with xversion extensions/maps - tooling reports issues
      * P4 FML Maps updated to also include the xversion extensions
  * P3 BP(/GC?): First draft maps to R6 prototyped (using Gino's tooling)

### Objective: FHIRPath is published as STU3 and ready for use by R6 and others, and on track for another normative release
  * P1 BP: All fhirpath jira issues are resolved
  * P1 BP: All approved fhirpath jira issues are applied to the specification
  * P1 BP: The fhirpath specification is published as STU3
  * P2 BP: Additional test cases are added to the FHIR unit test library covering the updated specification
  * P2 BP: fhirpath test cases are marked with the FHIRPath version they were introduced in where required (e.g. STU3)
  * P3 BP: the fhirpath test cases are verified as accurate according to the updated specification, and "contested" tests are marked as such
  * P3 BP: The test runner for evaluating the fhirpath test cases is verified
  * P3 BP: The test result matrix for all engines is executed against all engines and results published openly


## Objective: Provide Educational Content to support Users of HL7 specifications
  * P1 BP: Education Material supporting SDC extraction - At least 2 YouTube clips and 2 blog posts
    * Learning objectives
        * Understand and apply template-based extraction
        * Understand and apply definition-based extraction
  * P2 BP: Education Material supporting FHIRPath - At least 2 YouTube clips and 2 blog posts
    * Learning objectives
        * Debugging FhirPath expressions
        * Understanding FhirPath $this, $focus and input collections
        * Building invariants
        * Building search parameters
        * First part(s) of "fhirpath by example" published
  * P1 GC?/BP?: Blog post/clip(?) Understanding the R6 additional resources - walkthrough of an Additional Resources IG (e.g., Testing IG)?


## Enhanced tooling to support IG creators and consumers
### Objective: Demonstrate prototype functionality for the .NET stack implementing R6 additional resources

  * ??? Pick or develop an IG (Testing IG? / SQL on FHIR)
  * Code generation, parsing, serialization, incoproration of mixed resource content into bundles
  * Example REST API support for CRUDS, including:
      * search params defined on the additional resources
      * at least one operation
      * capability statement / feature ig support
  * Discussions with Firely on approach, comparison with Java approach

### Objective: Research suitability and "need" for a standardized SMART web messaging profile for SDC/forms
  * P2 BP: Prepare draft content for what this could look like
  * P2 BP: Extend the POC to demonstrate the concept as appropriate
  * P2 BP: Socialize draft and hold at least 2 meetings covering the content and develop a possible future plan

### Objective: The FHIRPath Lab is able to safely integrate external SDC renderers 
  * P2 BP: The FHIRPath Lab integrates the Aidbox Forms engine

### Objective: The FHIRPath Lab usage continues to grow meeting the needs of the broader FHIR community
  * P3 BP: Usage increases through educational use and content promotion
  * P4 BP: POC usage with logical models, or other models i.e. CDA/CCDA/OpenEHR/custom
  * P5 BP: Supporting external terminology services better
  * P5 BP: Test tooling for x-fhir-query in the fhirpath lab?

### Objective: Open Source tooling supports updated FHIRPath specification
  * P2 BP: Approved new FhirPath features applied to open source engines (Firely/Java/FhirPath.js)
      * coalesce
      * sort
      * others
      * Other implementations are aware of changes required, and have feedback via unit test engine results
  * P2 BP: The FHIRPath unit test runner is more easily used locally by others to verify their engines

### Objective: Users on the .NET stack are able to more easily implement SDC and FHIRPath static validation functionality
  * P2 BP: Support Firely in migrating the FHIRPath static validator into the core Firely SDK
  * P3 BP: Prepare an agreed timeline with Firely to transition my SDC project into Firely

### Objective: FML Prototyping activities - supporting broader implementation/use of FML in other languages
  * P4 BP: FML Validator onto nuget - consider permanent home
  * P5 BP: POC FML Map transpilation into c#/typescript/js for more performant execution

----
## Standards Development: Process and Publication

### **Objective:** Implementers are able to reliably pre-adopt features from other versions of FHIR
- **P0** (GC): Cross-version tooling updated for ease of maintenance
    - **P4**: Update installation and usage instructions

- **P0** (GC): Cross-version definitions cover all provided feedback and scenarios
    - **P0**: All extension definitions have proper constraints (`value` cardinality, `open` slicing, etc.)
    - **P0**: Review and validate vs. the manual diff pages between versions (e.g., R4/diff.html)
    - **P0**: Add 'reasoning'/justification narrative content to extensions
    - **P5**: Update technical messages with detailed mapping decisions and comparisons

- **P0** (GC): IG 'Lookup' pages provide reader-friendly and comprehensive guidance to consumers
    - **P0**: Add Lookup files for Value Sets with parent extension inclusion
    - **P0**: Pages include links to: profiles of 'full resources', value set comparisons in relevant element lookups, etc.
    - **P2**: Improve lookup file support for display of multiple mapping targets
    - **P4**: ValueSet comparisons include 'escape-valve' code documentation

- **P0** (GC): Computable resources for version transitions are defined
    - **P0**: Computable representation of "Lookup Page" content -- e.g., Map/Parameter resources for structures and elements to 'outcome' (use element same name, renamed, extension, extension of backbone)
    - **P0**: ConceptMap resources for mapping ValueSet codes between versions
    - **P8**: (GC/BP) StructureMap / FML for mapping structures (see line 17)

- **P4** (GC): Cross-version support content is managed in a database instead of code
    - **P4**: Move all content-file source into DB (IG Parameters, Suppression messages, change log, index, downloads, etc.)
    - **P4**: Add processing outcomes to a database
    - **P4**: Add invariants/constraints for extensions via database tables

- **P0** (GC): Cross-Version extensions are published in a milestone release

- **P7** (GC): Developer experience enhanced with a UI
    - **P7**: Complete UI updates for various database content (pages, parameters, etc.)
    - **P7**: Add "not reviewed by me" filter for collaborative review
    - **P7**: Add dedicated page for replacement URLs (Extension Substitutions)


### **Objective:** FHIR R6 is a quality publication
- **P0** (GC): FMG has tooling to automate the bulk of detection and flagging of issues in FHIR Core that WGs need to review
    - **P0**: Document guidance for core specification pages and artifacts for review
    - **P0**: Create tooling for automatic review of items that _can_ be reviewed programmatically
    - **P0**: At least 80% of WGs have reviewed the content and applied changes based on the reports
    - **P4**: Develop tooling to create/read/update review checklists in Confluence

- **P0** (GC): Outstanding tickets as of November 1 are applied and all content has been reviewed for:
    - FHIR Search (page and definitional artifacts)
    - FHIR HTTP (page)
    - Subscriptions Framework (page and related resources)
    - Versions

### **Objective:** Implementers are able to interoperably use topic-based subscriptions
- **P0** (GC): Publish STU 2 of the Backport IG
    - **P0**: STU 1.2 Ballot tickets are applied
    - **P0**: Updated with official cross-version extensions
        - Map existing backport extensions into the cross-version extension substitutions
        - Update IG with cross-version extensions and remove unnecessary artifacts
    - **P0**: Workgroup process --> publication of STU2
    - **P0**: Engage with at least 3 downstream implementers and/or authors to streamline adoption

### **Objective:** HL7 Processes are current, discoverable, and support standards development
- **P0** (GC): Documented proposal for an updated HL7 Standards process and present to TSC
    - **P0**: Document our real-life processes for project and publication lifecycle (Project Proposal -> PSS -> IG proposal -> publication 'life' -> retirement) 
        - i.e., the things that are in fact routinely checked/enforced by committees and tools 
        - avoiding misconceptions / wishful thinking, and pointing out where "real-life" processes are misaligned with the "official process".
    - **P0**: Draft of policies and expectations around change management match maturity
        - e.g., establish a terminal-state "standard publication level" that's shy of normative
        - e.g., establish a project lifecycle independent of publication lifecycle
    - **P0**: Documents presented to TSC for review

- **P2** (GC): Documented ballot consensus pool requirements that match desired participation expectations
    - **P2**: Reviewed existing guidance to distill principles/intentions and document concisely
    - **P2**: Draft of guiding principles for new framework
    - **P3**: Draft of requirements for successful ballot participation
    - **P3**: Documents presented to TSC for review

### **Objective:** FHIR and openEHR implementers have a path toward interoperability
- **P2** (GC): FHIR and openEHR data types have documented guidance to map content between formats
    - **P2**: Document mappings on [existing Confluence page](https://confluence.hl7.org/spaces/FHIRI/pages/391646604/Current+Mapping+Decisions) with expectations on loss, decision points, etc.
    - **P4**: Computable definitions are available online to allow easier use (e.g., on GitHub)

----
## Lowering the Bar: Education and Tooling

### **Objective:** FHIR is accessible to implementers and newcomers
- **P0** (GC): Educational content is published and freely available
    - **P0**: Review existing content and requests and document plan for next sequence of recordings
    - **P0**: Publish at least 5 new videos to YouTube


### **Objective:** FHIR Implementers have access to open and high-quality tooling
- **P0** (GC): fhir-codgen completes move to FHIR Foundation
    - **P0**: Project contents (code, documentation, license, etc.) are clean of Microsoft branding
    - **P0**: Project contents (code, documentation, license, etc.) are conformant with FHIR Foundation policy
    - **P0**: Repository has been moved to FHIR GitHub org (with prior location as a forward pointer)
    - **P6**: Libraries and tools are publicly published via NuGet


------

## Conversational Interoperability: From Connectathon to Community

**Objective:** Build sustained community of practice around conversational interoperability
* **P0** (JM): Host a community call
  * Host monthly "COIN Office Hours" on AI Zulip stream
  * Attract ≥5 participants per session
  * Document discussions and action items publicly
* **P1** (JM): Evolve Banterop based on Connectathon learnings
  * Address participant feedback on scenario testing (e.g. A2A REST transport)
  * Improve deployment documentation
* **P1** (JM): Submit scholarly perspective for publication
  * Draft paper on conversational interoperability patterns
  * Submit to academic venue or industry publication
  * Include co-authors from Connectathon participants
---

## HL7 Financial Interest Transparency: From Proposal to Implementation
**Objective:** Establish transparent financial disclosure framework for HL7 governance and standards leadership
* **P0** (JM): Secure Board approval for GOM amendments
  * Present proposal at [Month] Board meeting
  * Address Board member questions and concerns
  * Incorporate feedback and achieve majority support
* **P1** (JM): Build coalition of supporting Board members
  * Conduct 1:1 discussions with ≥5 Board members prior to vote
  * Address concerns about implementation burden and privacy
  * Demonstrate alignment with nonprofit best practices
* **P2** (JM): Develop implementation infrastructure
  * Draft disclosure form and submission process
  * Design public register website interface
  * Create guidance materials for affected individuals
* **P2** (JM): Prepare community communications
  * Write blog post explaining rationale and approach
  * Develop FAQ addressing common concerns
  * Create timeline for phased rollout

---

## Electronic Health Information Export: Close the Gap Between Policy and Practice
**Objective:** Transform EHI Export from compliance checkbox to genuinely useful patient capability
* **P1** (JM): Complete updated personal EHI export
  * Request and obtain current EHI export from [Hospital]
  * Identify persistent barriers and new issues
* **P2** (JM): Develop prompt library for EHI analysis
  * Create reusable prompts for common patient questions
  * Document effective multi-step workflows for complex queries
  * Test across ≥2 different LLM providers for robustness
