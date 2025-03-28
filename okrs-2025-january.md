# OKRs for October 2024 - January 2025

## Continuous Glucose Monitoring (CGM) 2024 Project

### Objective: Argo 2024 CGM IG is ready for implementation and positioned within OO for further development

* P0 (.9): Successfully conduct the November Connectathon with:
    * At least 2 organizations implementing the client interface
    * At least 2 organizations implementing the server interface
    * At least 1 organization representing researchers participating
    * P2 (0.0): (Stretch goal) At least 1 organization testing SMART Health Link capabilities

* P0 (1.0): Incorporate Connectathon feedback into the draft Implementation Guide (IG) within 2 weeks of the event

* P0 (1.0): Transition the project to HL7 Orders and Observations (OO) workgroup:
    * Host at least 2 calls under the OO workgroup by year-end
    * Work with OO to formally vote on importing the draft content, clearing the path for incremental future work

* P1 (0.0): Create a long-lived reference snapshot of the specification that implementers can reference indefinitely

* P2 (1.0): Prepare the draft IG for future HL7 ballot process:
    * Ensure all sections are complete and reviewed
    * Address any known issues or ambiguities
    * OO workgroup agrees on a timeline for the ballot process

## Imaging Access

### Objective: Patients can easily access their imaging data in an app of their choice, alongside their clinical data

* P0 (1.0): Conduct a follow-up call with EHR developer to discuss:
    * Approach for separate authorization servers with shared patient accounts
    * Potential solutions for streamlined app registration across systems
    * Document key insights and action items from the call

* P2 (1.0): Identify at least one potential testing site willing to explore implementation of a pragmatic approach to patient imaging access

* P3 (1.0): Secure commitment from at least one imaging vendor to participate in the testing process.


## US Core Subscriptions

### Objective: US Core applications receive timely updates when clinical data changes

* P0 (0.5): Conclude the consensus process for US Core subscription data feed:
    * Achieve agreement on core subscription parameters and payloads
    * Document any remaining areas of contention

* P1 (0.2): Formally propose incorporation of subscription content into US Core:
    * Present proposal to US Core working group
    * Drive decision on inclusion in the next US Core release

* P1 (0.2): Evaluate R6 subscription enhancements based on US Core work:
    * Assess need for hierarchical topics
    * Determine if additional flexibility is required for topic implementations that restrict the set of filters defined in a canonical topic

* P2 (0.0): Create and publish a tutorial video providing an overview of core concepts behind the US Core subscription data feed

## AI for HL7 Spec Editors

### Objective: HL7 specification editors share their experiences with AI tools to enhance their work

* P1 (0.8) : Organize and conduct an "AI for Spec Editors" roundtable:
    * Send invitations to all HL7 work group chairs and known spec editors
    * Secure at least 5 experienced spec editors to share their AI usage tips and tricks
    * Ensure representation from at least 3 different HL7 work groups
    * Achieve attendance of at least 15 participants
    * Record the session and share the recording with all HL7 work group chairs within one week

## Authors and Implementers can use elements from FHIR versions outside their current version
* P0 (0.1): A single slide process flow explaining how we get from Ra/Rb definitions --> a-vs-b diff  --> [manual review] --> xver extensions
* P0 (0.7): Complete a pass of Cross-Version IG content for review (note this is not balloted, but needs review)
    > [name=Josh Mandel]"RC1?"
    > [name=Gino Canessa] 👍
    * Canonical resource content:
        * Difference-based Value Set definitions
        * Extension definitions
        * Narrative content
    * Site / page content
        * All the element-wise diffs for all elements with changes
    * Package structure and contents
* P? (0.6): Basic tooling to enable faster review and simpler Cross-Version IG content
    * View + edit of concept-domain changes (exist in ConceptMaps)
    > [name=Josh Mandel] e.g., semantics defining what content belongs in an element. The "concept of what the element means."
    * View of value-domain changes (exist in StructureMaps / FML)
    > [name=Josh Mandel] e.g. changing type, cardinality, binding... the stuff that appears in an ElementDefinition. The "validatable constraints that apply to an element"
    * View + edit of renamed code/elements (exist in ConceptMaps and StructureMaps / FML)
* P? (0.0): Publish
* P4 (0.0): (BP) Basic tooling to update cross-version maps to inject/validate the new extensions
    * All the existing cross version maps are updated and published

## FHIR community has a concrete plan for R6+ versioning issues 
* P0 (0.4): Document three alternative approaches for how FHIR is published
    * Explain the desirable properties (which are the subject of tradeoffs) 
    * Definitions of the three approaches
        * Published core (6.0.0) plus modules + Singular modules package (e.g., published once per quarter - Experimental module package)
        * Published core (6.0.0) plus modules + Independent module packages (e.g., published by WGs)
        * Published minor releases with unchanged stable and breaking 'newer' content
    * Document the differences in the approaches (pros/cons) for the following tasks / stakeholders:
        * Core spec authoring (WG process and effort)
        * Core spec balloting and publication (WG process, HL7 staff process and effort, reviewer effort)
        * IG authoring and maintenance (accelerator and WG process and effort)
        * IG balloting and publication
        * Regulatory authorities (cycle time, version pinning concerns, core vs IG)
        * Tooling / SDK implementers
        * EHR/facade and native server implementers
        * Provider organizations (production servers)
        * Client implementers (app developers, integration projects)
    * Answers the following questions for each approach:
        * What does the standard process (e.g., 'normal' content development, consensus review, and publication) look like?
        * What do patches and unballoted updates look like for each category - e.g., would we need 6.0.1 and 6.1.1?
        * What does future-proofing look like in each solution - e.g., resources that do not exist yet?
    * Reflect on a comparison with R4B - was it successful? was the effort worth it?
        * Same question regarding R5
* P1 (1.0): Make another presentation deck to summarize (due for FHIR Camp)
* P1 (0.0): Schedule and record a roundtable discussion
* P5 (0.0): Record overview video
* Prototyping activities:
    * P3 (0.0): (BP) FML Validator onto nuget
    * P2 (0.0): (BP) FML g4 approved into FHIR R6
    * P2 (0.0): (BP) façade project updated with custom resource/module support
    * P5: (??) GH Build Status Check for `hl7/fhir`: "detected breaking change! Please fill out this form explaining why it's justified"? Active for FMM>=4 content.

## Implementers are able to leverage SDC extract in more cases
* P0 (1.0): (BP) Enhance Definition-based extract to support extraction of multiple resources, removing the following current limitations:
    * Need to create hidden "shadow" properties in questionnaire
    * No access to QR.subject, author, or encounter (header props) - resulting in duplicating in hidden props
    * Linking the multiple resources together is impractical
* P0 (1.0): (BP) The Definition based extract documentation is clearer and some known gaps working with multiple resources and updating existing resources are reduced/removed
* P0 (1.0): (BP) Document capabilities and limitations of Template-based $extact
    * (Current proposal)
        * https://jira.hl7.org/browse/FHIR-39498
        * https://hackmd.io/@brianpos/extract-template
    * Create examples of template-based extractions
    * Bring analysis back to SDC committee (FHIR Infrastructure)
* P1 (0.0): (BP) Produce at least 2 education artifacts supporting the use of $extract from the SDC IG (e.g. blog posts, YouTube clips)
* P2 (1.0): (BP) Implementers are able to efficiently test multiple $extract implementations using the fhirpath lab
* P2: (BP) Collaborate with others to produce a library of Questionnaire/QuestionnaireResponse $extract examples
    * (1.0) Published on github
    * (1.0) At least 2 contributors
    * (1.0) At least 5 examples
* P2 (0.5): (BP) fhirpath lab supports:
    * Questionnaire definitions include context of
        * Which patient (subject)
        * Who is completing the form (user)
    * This context can drive pre-population of (e.g.) demographics, conditions
    * The same context can drive extraction into derived resources
 
## Implementers can efficiently work with geo-spatial information and FHIR content
Location information is widely available inside and outside FHIR in multiple representations.
This diversity of information is currently un-managed and only done in an ad-hoc manner.
https://confluence.hl7.org/display/PA/Location+Service

* P1: (BP) Document the way this information is currently represented (in summary form)
    * FHIR - Locations (points, areas, named spaces), Terminologies (named spaces + relationships)
    * GIS - points, named shapes
    * Excel Spreadsheets or other simple lists/relationships (roughly terminologies)
* P1: (BP) Document how implementers are currently utilizing this information (in summary form)
    * Several simple use cases that the project seeks to support
* P1: (BP) Recruit additional participants to work on a potential implementation guide (beyond myself and Nathan)
* P2: (BP) Complete preparation of a HL7 Project Scope statement describing the scale of the work to be undertaken
* ^ The above was considered, whitepaper discussion around how to do this with terminologies and decided was not a new project.

## Unplanned 

* (BP) IG Dependency Canonical version resolution
    * (0.8) Clarify how resolution of canonical resources works between packages 
    * (1.0) Extensive processing in UploadFIG to handle package dependencies
        * "tree shake" resources from dependent packages
        * Patch the canonical URLs to be versioned while processing
        * Enhanced the unit testing to better support updates into the future
        * Investigate migrating into Microsoft GitHub Organization
* (BP) VhDir finally published

* (GC) FHIR-Candle work: Compartments, arch-images, transactions, and more.

* (JM) Imaging authz: Connectathon with prototypes across vendors
