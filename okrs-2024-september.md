# OKRs for July - Sept 2024

## Competing Interests / Keeping the Lights On
* JM
    * Argo CGM lead-up to connectathon 
    * Security Waves
* GC
    * Cross-version extension work
    * Backport IG work
    * R6 content (https://confluence.hl7.org/pages/viewpage.action?pageId=234784975#FHIRInfrastructureMinutesWGM202405Dallas-TuesdayQ4)
        * Ballot Content Freeze deadline July 30
        * Final Content Deadline August 11
        * Subscriptions (resources + Framework page)
    * FHIR Candle work (+ finish move to FCP)
    * FHIR Codegen work (IG, Firely v6, Cross-Version, Ruby, TS)
    * Security Waves
* BP
    * PA Extensions Applied
    * PA R6 Changes Applied
    * FHIRPath spec normative ballot
        - Spec updates
        - Tooling/testing updates to support evidence of normative
    * FhirPath-Lab pre-pop/extract refinements?
    * Pre-pop/extract education clips?
    * FhirPath-Lab AI chat more open/released

---
## Objective: FHIR enables cross-version compatibility, with a clear division of responsibilities and helpful tooling

Note: We'll focus initially on Core versioning rather than IG versioning.

### Create a Versioning Strategy Document

- **[P0] Problem Statement:**
  - **Challenges from R2 to R5:**
    - Identify specific challenges in the R4B cycle focusing on Subscriptions and medication knowledge resources.
  - **Impact on Stakeholders:**
    - Discuss impacts on EHRs, app developers, standards developers, and regulators.
  - **Transition Issues from R4 to R6:**
    - Explore the challenges and regulatory landscapes in transitioning to R6, and propose improvements for future versions.

- **[P0] Proposed Model for Managing Version Changes:**
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
- **[P0] Stakeholder Responsibilities:**
  - **Roles and Expectations:**
    - Outline specific roles for HL7 Workgroups and the FHIR Management Group.
    - Define expectations for implementers, data providers, and regulators regarding asynchronous cutover.

### Subscriptions Module Case Study (by September 2024)
- **[P0] Repository Development:**
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
      
- **[P1] Structure Maps:**
  - Develop detailed structure maps demonstrating upgrade paths for each version increment.
  
- **[P0] Example Resource Management:**
  - [P0] Include example resources that evolve with the spec.
  - [P2] Show how sample resources can be updated via standalone script running up-conversion from spec maps.

- **[P1] JS/C#? Server Implementation:**
  - P0 Request/Response examples showing how feature negotiation and feature mandating works
  - P1 Set up JS server that evolves with the Subscriptions module.
  - P1 Add support for each new release
  - P1 Enables version negotiation across the full span, returning content according to the requested version
  - P1 Supports search + create (any other behaviors can be canned)
  - P1 Supports R4
  - P3 Supports R5 also

- **[P1] JS Client Implementation:**
  - Build a JS client capable of version negotiation with the server.
  - Evolves along with the Subscriptions module but ahead of the server
  - Configure client settings to manage the version range for negotiation.
  - Demonstrate client operations such as creating and searching over Subscription resources, and handling notifications in requested versions.
  
- **[P1] Timeline Visualization / Slide:**
  - Show fictional dates of spec development + release
  - Show lag to server support
  - Show lag to client support
  - Demonstrate that server + client remain compatible throughout

### Proof of Concept: Version Management Toolkit
- **Implementer Toolkit:**
  - **[P1] Up/Down Conversion Utility:**
    - Create utilities that transform resources between different FHIR versions.
  - **Version Negotiation support in Client SDK:**
    - P1 Develop an approach for a library that facilitates client-server communication to determine compatible FHIR versions. Can be used by JS client above.
    - P2 PoC that handles parsing and generation of resources for different versions
        - Takes a resource in a specified version, and a library of maps, and applies the maps in sequence to create the target output
  - **[P3] Version-Aware Validation Tool:**
    - Q. What context does a validator need to resolve (e.g., collection of modules/versions) prior to validation?
    - P? Exercise existing Firely SDK functionality to show validation of content from Subscription module at various versions
    - Q. What context does a validator need to resolve (e.g., collection of modules/versions) prior t

- **Spec Editorial Toolkit:**
  - **[P1] Change Intent Capture System:**
    - Create a format to document change rationale, impact, including converters, potential data loss, deprecation schedules, and "backport" extension needs.
    - [P1] Simple markdown format with no executable behavior
    - [P2] Show "close enough" examples from WIP tooling to communicate how this *could work*
  - **[P5] Automated Test Case Generator:**
    - Develop a system that generates test cases to validate backward compatibility of changes.
- **[P5] Cross-Version Difference Display Tool:**
  - Develop a tool that visually displays differences between versions of a resource or element.
