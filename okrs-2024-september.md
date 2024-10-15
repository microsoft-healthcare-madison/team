# OKRs for July - Sept 2024

## Competing Interests / Keeping the Lights On
* JM
    * Argo CGM lead-up to connectathon 
    * Security Waves
    * (Unplanned: HTI-2 Responses ;)
    * (Unplanned: Argo Subscriptions for US Core)
* GC
    * Cross-version extension work
    * Backport IG work
    * R6 content (https://confluence.hl7.org/pages/viewpage.action?pageId=234784975#FHIRInfrastructureMinutesWGM202405Dallas-TuesdayQ4)
        * Ballot Content Freeze deadline July 30
        * Final Content Deadline August 11
        * Subscriptions (resources + Framework page)
    * FHIR Candle work (+ finish move to FCP)
    * FHIR Codegen work (IG, Firely v6, Cross-Version, Ruby, TS, (FHIR Shorthand, CQL))
    * Security Waves
    * FHIR packaging (Firely Packaging project)
* BP
    * (1.0) PA Extensions Applied
    * (1.0) PA R6 Changes Applied
    * FHIRPath spec normative ballot
        - (0.8) Spec updates
        - (0.0) Tooling/testing updates to support evidence of normative
    * (0.9) FhirPath-Lab pre-pop/extract refinements?
    * (0.0) Pre-pop/extract education clips?
    * (0.7) FhirPath-Lab AI chat more open/released

---
## Objective: FHIR enables cross-version compatibility, with a clear division of responsibilities and helpful tooling

Note: We'll focus initially on Core versioning rather than IG versioning.

### Create a Versioning Strategy Document

- **[P0] (1.0) Problem Statement:**
  - **Challenges from R2 to R5:**
    - Identify specific challenges in the R4B cycle focusing on Subscriptions and medication knowledge resources.
  - **Impact on Stakeholders:**
    - Discuss impacts on EHRs, app developers, standards developers, and regulators.
  - **Transition Issues from R4 to R6:**
    - Explore the challenges and regulatory landscapes in transitioning to R6, and propose improvements for future versions.

- **[P0] (0.8) Proposed Model for Managing Version Changes:**
  - ? **Versioning Alternatives:**
    - Review versioning strategies used in other standards including DICOM.
        - What works, what does not, what *could* be used, what cannot...
  - **Modularity of Spec Components:**
    - Enable development of content as part of independent modules, rather than a monolithic specification
  - **Granular Change Management:**
    - Develop a system to track and categorize individual element changes during specification development.
    - Define "normative" versus "trial use" changes and their management implications.
  - **Mechanisms for Version Negotiation:**
    - Propose how data producers and consumers can negotiate using "supported version ranges."
    - Show how an individual interaction can invoke module/version-specific behaviors
  - **Compatibility Guarantees:**
    - Specify compatibility guarantees and annotate potential breaking changes.
  - **Extension Mechanisms:**
    - Describe appropriate uses for extensions to handle "elements from the future."
  - **Asynchronous Cutover:**
    - Enable stakeholders to upgrade on their own schedules and allow regulators to manage minimum standards independently.

- **[P0] (0.5) Stakeholder Responsibilities:**
  - **Roles and Expectations:**
    - Outline specific roles for HL7 Workgroups and the FHIR Management Group.
    - Define expectations for implementers, data providers, and regulators regarding asynchronous cutover.

### Subscriptions Module Case Study (by September 2024)
- **[P0] (0.3 - started, but it was too much detail to be useful) Repository Development:**
  - Create and maintain a Git repository simulating the evolution of the Subscriptions module with detailed versioning and release notes.
  - Include multiple commits leading up to each "release"
  - Include major, minor, and patch releases showing spec evolution
      * Original Subscription model (simplified for clarity)
      * Bug fixes (patch release)
      * Rework to add Topic (simplified for clarity, major release)
      * Addition of `$event` and `$status` (minor release)
      * Addition of new data element + search param (minor release)
      * Bug fixes (patch release)
      * Include comparisons of structures (clean proposed vs Basic + Extensions)
      
- **[P1] (0.3 -- developed a general framework but not maps for Subscriptions case study) Structure Maps:**
  - Develop detailed structure maps demonstrating upgrade paths for each version increment.
  
- **[P0] (0.1 -- did not build these into a repo, did not automate) Example Resource Management:**
  - [P0] Include example resources that evolve with the spec.
  - [P2] Show how sample resources can be updated via standalone script running up-conversion from spec maps.

- **[P1] (0.0) JS/C#? Server Implementation:**
  - P0 Request/Response examples showing how feature negotiation and feature mandating works
  - P1 Set up JS server that evolves with the Subscriptions module.
  - P1 Add support for each new release
  - P1 Enables version negotiation across the full span, returning content according to the requested version
  - P1 Supports search + create (any other behaviors can be canned)
  - P1 Supports R4
  - P3 Supports R5 also

- **[P1] (0.0) JS Client Implementation:**
  - Build a JS client capable of version negotiation with the server.
  - Evolves along with the Subscriptions module but ahead of the server
  - Configure client settings to manage the version range for negotiation.
  - Demonstrate client operations such as creating and searching over Subscription resources, and handling notifications in requested versions.
  
- **[P1] (0.4 -- created a slide with publication timeline but not server/client support) Timeline Visualization / Slide:**
  - Show fictional dates of spec development + release
  - Show lag to server support
  - Show lag to client support
  - Demonstrate that server + client remain compatible throughout

### Proof of Concept: Version Management Toolkit
- **Implementer Toolkit:**
  - **[P1] (0.2 -- PoC for mapping, execution in unit testing, execution in fhirpath lab) Up/Down Conversion Utility:**
    - Create utilities that transform resources between different FHIR versions.
    - (Done but not planned for) Validation tooling for cross version maps (to ensure map/model validity)
  - **Version Negotiation support in Client SDK:**
    - [P1] (0.1 -- submitted comments on App Feature IG) Develop an approach for a library that facilitates client-server communication to determine compatible FHIR versions. Can be used by JS client above.
    - [P2] (0.7) PoC that handles parsing and generation of resources for different versions
        - Takes a resource in a specified version, and a library of maps, and applies the maps in sequence to create the target output
        - https://github.com/brianpos/fhir-net-mappinglanguage/tree/main/VersionConversionTester
  - **[P3] (0.1) Version-Aware Validation Tool:**
    - Q. What context does a validator need to resolve (e.g., collection of modules/versions) prior to validation?
    - P? Exercise existing Firely SDK functionality to show validation of content from Subscription module at various versions
    - Q. What context does a validator need to resolve (e.g., collection of modules/versions) prior to validation?

- **Spec Editorial Toolkit:**
  - **[P1] (0.1 -- still hoping much of this can be determined automatically outside of editorial flow) Change Intent Capture System:**
    - Create a format to document change rationale, impact, including converters, potential data loss, deprecation schedules, and "backport" extension needs.
    - [P1] Simple markdown format with no executable behavior
    - [P2] Show "close enough" examples from WIP tooling to communicate how this *could work*
  - **[P5] (0.0) Automated Test Case Generator:**
    - Develop a system that generates test cases to validate backward compatibility of changes.
  - (Done but not planned for) Updating existing cross version maps to be consistent/valid

- **[P5] (0.3 -- draft UI, will be ripped/replaced) Cross-Version Difference Display Tool:**
  - Develop a tool that visually displays differences between versions of a resource or element.
