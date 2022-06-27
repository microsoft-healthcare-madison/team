# OKRs for May 2022

## SMART specs move through the HL7 publication pipeline
* P0: (1.0) SMART Web Messaging publication request in place
* P0: (1.0) SMART Web Messaging publication request approved by FHIR-I, FMG
* P0: (1.0) SMART Web Messaging published
* P4: (0.1) SMART App Launch Technical Correction requested
    * only if Vassil is willing to carry the torch

## Open source tools and libraries make it easy to work with FHIR and related IGs
* P0: (0.0) Vlad has reviewed outstanding PR for SMART Launcher
    * P3: PR Merged
* P0: (0.2) Vlad has reviewed outstanding PR for SMART Client-JS
    * P3: PR Merged

## Argonaut "Patient Access Endpoints" project enables a "connect to my provider" UX
* P0: (1.0) Propose design for patient access endpoints and branded organizations
* P0: (0.8) At least one Argonaut EHR vendor commits to implementing design
* P1: (1.0) Demo JSON file and .smart-configuration files supporting discovery
* P2: (1.0) Demo app rendering tiles from sample data

## Argonaut "EHI Export" project defines a wrapper API for vendor EHI export capabilities
* P0: (1.0) Design feedback shared on weekly calls
* P3: (0.0) Prototype server implementing a bare-bones export on top of static data
    * P3: Automated approvals so clients can test the UI
    * P5: Provider-side "queue" UX simulating HIM staff view of pending requests

## Argonaut "SMART Health Links" project is ready for summer launch
* P0: (1.0) Define initial use case for public health ("all my immunizations")
* P1: (0.5) Define one more initial use case
    * Candidate: Insurance data (link to CARIN BB Profile)
    * Candidate: COVID lab results from at-home test kit
* P2: (1.0) Choose a top candidate from our three API designs (OAuth, Redirects, GNAP)

## Define a new pattern for community collaboration upstream from the standards space (e.g., to support work from cloud vendors) -- e.g., "Amplifier"

* Pitch: if you've got a project that needs rough consensus and isn't ready for a formal SDO process (e.g., how we started CDS Hooks and SMART Health Cards), Amplifier provides a home and a template to help you launch a community project, including guidelines for running the project, a namespace for publishing your materials, and a framework for lightweight governance
* P0: One-pager explaining triage process to determine what should happen in FHIR "core" vs HL7 IGs, vs "community collaboration", vs "one company's IGs"
  * Clinical vs mechanical specs: are both in scope? Could clinical projects be advertised for Argonaut participation?
  * How does each project define its relevant "rough consensus" community?
  * Long-term home in community space vs consensus space
  * Transition plan: explicit expectation when a project stars explaining the intended disposition
  * Governance / editorial process: for this to be a meaningful effort, it's important that we  focus on projects where the set of editors spans more than one company, and where some level of rough consensus is required to label a spec as "published" -- see, e.g., https://github.com/cds-hooks/docs/blob/master/GOVERNANCE.md from CDS Hooks, or https://infra.apache.org/new-committers-guide.html
* P0: (0.0) Review proposed process: with at least two cloud vendors
* P1: (0.0) Define naming conventions for canonical URLs in "community IG space"
* P4: (0.0) Establish licensing conventions for "community IG space"
* P4: (0.0) Decide on a home
    * Candidate: FHIR Community Process (https://www.fhir.org/community/process)
    * Candidate: new FHIR Acclerator
    * Candidate: an existing FHIR Accelerator

## Subscriptions
* P0: (0.8) Sync all changes between R4B+IG and R5 until R4B+IG are published
* P0: (1.0) R5 QA Completed
* P0: (0.8) Publish Backport IG (depends on R4B publication)
    * P0: (1.0) QA Completed
    * P0: (1.0) Publication request in place
    * P0: (0.5) Publication request approved by FHIR-I, FMG
    * P0: (0.0) Published
* P?: (0.7) Have connectathon track available, either as a standalone track or part of an Argo-wide track (?)
* P0: (0.9) RI is up to date with R4B+IG and R5
    * P1: (1.0) Prior to connectathon
    * P0: (0.9) With final R4B/IG version

## Code-Gen
* P0: (0.5) Define 'IG Export Language' interface
    * P0: (0.1) At least one language implemented: Firely C#, TypeScript, HAPI Java
    * P5: (0.0) All of: Firely C#, TypeScript, HAPI Java are implmenented
* P5: (0.0) Create basic Rust language export
* P5: (0.3) Design and implement a process for non-terminology validation (e.g., Fluent Validation, CUE)
    * P5: (0.1) Support IG model validation

### TS/JS FHIR library
* P0: (1.0) Complete MVP of TypeScript (v2) library
* P0: (1.0) Establish a 'home' for the project
* P1: (0.0) Record basic educational content
    * P1: Client application (React?)
    * P3: Server applicaiton (Node?)
* P4: (0.5, Gino *de facto*) Select a community lead

## FHIR Core Specification
* P0: (0.6) Complete pass of FHIR Search Page
* P?: (0.0) Review tickets submitted by our team and apply or submit PRs to apply the resolutions
* ?P?: (0.0) Identify 3 key areas of the spec that we want to improve and apply outstanding tickets to resolve them (targeting 40 hours of "community service" work)?

## Specs balloted through HL7 receive productive critical feedback
* P1: (0.4) Coordinate MS-internal review plan for May ballot cycle 
  * P1: (0.5) call to review candidate specs and identify "matchmaking" opportunities with product teams
  * P2: (0.5) Review/comment/vote on at least '##' ballot publications

----

# Work that wasn't covered in OKRs

## SMART App State
* Design, reference implementation

## Brian joined the team!
* .NET facade
* Terminology services integration to support serach
* Fhirpath testing
* PA and SDC editorial work
