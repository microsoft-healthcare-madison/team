# OKRs for March - May 2025

## Enhance HL7 Specifications
* P1 (BP) 1.0 Continue progress in reconciling FHIRPath specification toward R3 release
* P1 (BP) 1.0 Continue progress in reconciling SDC specification toward R4 release
* P2 (BP) 0.9 Apply the Patient Administration R6 changes to the core specification
* P1 (BP) 0.7 Draft new spec language describing how to resolve canonical references in the context of a package. 
    * 0.7 Land guidance in Confluence
    * 0.7 Community review + feedback from developers working with FHIR Packages
* P1 (GC) 1.0 Apply the Search and Subscriptions R6 changes to the core specification
* P6 (GC) 0.0 (dependency failed) Publish Subscriptions Backport IG 1.2
  * Depends on xver finalization + publication prior to May WGM
* P4 (BP) 0.0 (pending following on with Gino's xver work) FML g4 approved into FHIR R6

## Provide Educational Content to support Users of HL7 specifications
* P1 (BP) 0.0 Education Material supporting UploadFIG dependency management - YouTube clip(s) and blog post
  * Learning objective
      * understand FHIR package deps and the meaning of a dependency tree
      * Deploying an IG and its dependency tree to a reference server
* P1 (BP) 0.2 Education Material supporting SDC extraction - At least 2 YouTube clips and 2 blog posts
  * Learning objectives
      * 0.5 Understand and apply template-based extraction
      * Understand and apply definition-based extraction
* P1 (BP) 1.0 Present on SDC Extract and what's New in FhirPath at DevDays

## Enhanced tooling to support IG creators and consumers
* P3 (BP) 0.0 FML Tooling Updates for the cross version maps leveraging Gino's database and new extensions pack
    * Today, some FML transforms use cross-version extensions (but ad-hoc, may not match formal definitions)
    * Want to automatically inject backport extensions when mapping into a version where the necessary property is absent
* P4 (BP) 0.0 UploadFIG to validate cross version extensions using the "new" extension pack
* Prototyping activities:
    * P3 (BP) 0.0 FML Validator onto nuget - consider permanent home

* Unscheduled (BP): Fhirpath debugger-like experience in the FhirPath Lab
    * PRs for HAPI/FhirPath.js engines to provide injection interface
    * POC in DotNet engine
    * Enhancements in FhirPth Lab UI to step through the debug trace information
    * Presented experience at DevDays
    * *Born from experimentation to produce something similar for FML*

## Authors and Implementers can use elements from FHIR versions outside their current version
* P2 (GC) 0.5 Document "automatic" processing algorithm
* P0 (GC) 1.0 Finish "automatic" processing pass of software to run comparisons and save to database
* P0 (GC) 1.0 Generate markdown documentation of all mappings from the database
* P1 (GC) 0.3 (External review in-progress) Review/coordinate review of all mappings
* P0 (GC) 1.0 Generate FHIR Extensions based on the mappings in the database
* P0 (GC) 0.5 (nearing Snapshot 2) Publish the cross-version extensions packages

## FHIR community has a concrete plan for R6+ resource development
* P0 (GC) 1.0 Coordinate with Grahame to update proposal prior to Madrid WGM
    * [Overview thread from Grahame](https://chat.fhir.org/#narrow/channel/179280-fhir.2Finfrastructure-wg/topic/Proposed.20R6.20change.3A.20Opening.20up.20for.20other.20resources)
    * P1 (GC) 0.8 Proposal for naming / registering name(spaces)
    * P1 (GC) 0.5 Proposal for versioning best practices
    * P0 (GC) 0.0 (Grahame presented instead :) Prepare presentation
    * P5 (GC) 0.0 Prepare prototype
    * P4 (BP) 0.0 dotnet façade project updated with custom resource/module support
* P1 (GC) 1.0 Work with Firely on plans for how to support this

## FHIR community is able to leverage AI productively and ethically
* P0 (GC) 1.0 Build demo application to work with FHIR Search via AI
    * P0 ? (changed to MCP) Basic chat-style functionality
    * P1 ? (changed to extraction from xver DB) Spec parsing for RAG
    * P5 0.0 LOINC / SNOMED / RxNorm for ~~RAG~~ MCP (get FHIR definitions from [Josh](https://github.com/jmandel/fhir-concept-publication-demo))
    * P1 0.5 Define FHIR Operations for FHIR-server feedback (tool calls - MCP?)
        * e.g., "validate search", or "parse search"
    * P3 0.0 Simple way of comparing models / results
    * P0 1.0 Present at DevDays
    * P99 (BP) 0.5 FHIRPath tools/resources available as MCP servers (tool calls)

* Unplanned (JM): AI Club, Connectathon Planning

## US Core Supports a Patient Data Feed

* P0 (JM) 1.0 Achieve Argonaut consensus on subscription parameters/payload for US Core 'futures' page.
* P0 (JM) 0.75 Drive consensus and planning through >=3 focused Argonaut calls.
* P1 (JM) 0.2 Document plan for enhanced subscription topic metadata (computability, v2 maps).

## Prior Auth workflows are simplified with MCP-based Tools

* P0 (JM) 1.0 Build functional MCP prototype using EHR sandbox API to initiate PA request.
* P0 (JM) 1.0 Implement minimal simulated PA Tool endpoint for prototype interaction.
* P1 (JM) 1.0 Record and share video demonstrating prototype PA initiation flow.
* P2 (JM) 1.0 Draft feedback for active PA automation regulations/RFIs using prototype insights; else share demo/insights with >=2 policy contacts.

Other areas: A2A implmention, TEFCA analysis and QHIN design, quality measure PoC, CMS RFI. 
