# OKRs for March - May 2025

## Enhance HL7 Specifications
* P1 (BP) Foster the FHIRPath specification through the ballot process to get to the R3 release
* P1 (BP) Foster the SDC specification through the ballot process to get to the R4 release
* P2 (BP) Apply the Patient Administration R6 changes to the core specification
* P1 (BP) Draft new spec language describing how to resolve  canonical references in the context of a package. 
    * Land guidance in Confluence
    * Community review + feedback from developers working with FHIR Packages
* P1 (GC) Apply the Search and Subscriptions R6 changes to the core specification
* P6 (GC) Publish Subscriptions Backport IG 1.2
  * Depends on xver finalization + publication prior to May WGM
* P4 (BP) FML g4 approved into FHIR R6

## Provide Educational Content to support Users of HL7 specifications
* P1 (BP) Education Material supporting UploadFIG dependency management - YouTube clip(s) and blog post
  * Learning objective
      * understand FHIR package deps and the meaning of a dependency tree
      * Deploying an IG and its dependency tree to a reference server
* P1 (BP) Education Material supporting SDC extraction - At least 2 YouTube clips and 2 blog posts
  * Learning objectives
      * Understand and apply template-based extraction
      * Understand and apply definition-based extraction
* P1 (BP) Present on SDC Extract and what's New in FhirPath at DevDays

## Enhanced tooling to support IG creators and consumers
* P3 (BP) FML Tooling Updates for the cross version maps leveraging Gino's database and new extensions pack
    * Today, some FML transforms use cross-version extensions (but ad-hoc, may not match formal definitions)
    * Want to automatically inject backport extensions when mapping into a version where the necessary property is absent
* P4 (BP) UploadFIG to validate cross version extensions using the "new" extension pack
* Prototyping activities:
    * P3 (BP) FML Validator onto nuget - consider permanent home


## Authors and Implementers can use elements from FHIR versions outside their current version
* P2 (GC) Document "automatic" processing algorithm
* P0 (GC) Finish "automatic" processing pass of software to run comparisons and save to database
* P0 (GC) Generate markdown documentation of all mappings from the database
* P1 (GC) Review/coordinate review of all mappings
* P0 (GC) Generate FHIR Extensions based on the mappings in the database
* P0 (GC) Publish the cross-version extensions packages

## FHIR community has a concrete plan for R6+ resource development
* P0 (GC) Coordinate with Grahame to update proposal prior to Madrid WGM
    * [Overview thread from Grahame](https://chat.fhir.org/#narrow/channel/179280-fhir.2Finfrastructure-wg/topic/Proposed.20R6.20change.3A.20Opening.20up.20for.20other.20resources)
    * P1 (GC) Proposal for naming / registering name(spaces)
    * P1 (GC) Proposal for versioning best practices
    * P0 (GC) Prepare presentation
    * P5 (GC) Prepare prototype
    * P4 (BP) dotnet façade project updated with custom resource/module support
* P1 (GC) Work with Firely on plans for how to support this

## FHIR community is able to leverage AI productively and ethically
* P0 (GC) Build demo application to work with FHIR Search via AI
    * P0 Basic chat-style functionality
    * P1 Spec parsing for RAG
    * P5 LOINC / SNOMED / RxNorm for RAG (get FHIR definitions from [Josh](https://github.com/jmandel/fhir-concept-publication-demo))
    * P1 Define FHIR Operations for FHIR-server feedback (tool calls - MCP?)
        * e.g., "validate search", or "parse search"
    * P3 Simple way of comparing models / results
    * P0 Present at DevDays
    * P99 (BP) FHIRPath tools/resources available as MCP servers (tool calls)

## US Core Supports a Patient Data Feed

* P0 (JM) Achieve Argonaut consensus on subscription parameters/payload for US Core 'futures' page.
* P0 (JM) Drive consensus and planning through >=3 focused Argonaut calls.
* P1 (JM) Document plan for enhanced subscription topic metadata (computability, v2 maps).

## Prior Auth workflows are simplified with MCP-based Tools

* P0 Build functional MCP prototype using EHR sandbox API to initiate PA request.
* P0 Implement minimal simulated PA Tool endpoint for prototype interaction.
* P1 Record and share video demonstrating prototype PA initiation flow.
* P2 Draft feedback for active PA automation regulations/RFIs using prototype insights; else share demo/insights with >=2 policy contacts.
