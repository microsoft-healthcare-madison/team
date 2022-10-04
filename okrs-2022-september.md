# OKRs for June-September 2022

## FHIR-based software uses topic-based subscriptions to avoid polling
* P0-GC: (1.0) R4B Backport IG is published
    * P0-GC: (1.0) Publication request approved by FHIR-I, FMG, and TSC
    * P0-GC: (1.0) Specification is Published
    * P1-GC: (1.0) Have connectathon track available, either as a standalone track or part of an Argo-wide track (?)
* P3-GC: (0.0) Subscriptions sandbox supports more SubscriptionTopics (e.g., arbitrary fhirpath-based topics, or a "button push event" topic)
* P0-GC/BP: (0.75 -- need to review R5) RI is up to date with R4B+IG and R5
  * P0-GC: (1.0) With final R4B/IG version
* P2-GC: (0.0) Track usage for Subscription sandbox (counts by R4B vs R5, standard channel types or "any custom channel")
* P2-GC/BP: (0.0) Develop SubscriptionTopic content from at least one of the following:
  * Public health
      * MedMorph for public
      * National Center for Health Statistics (NCHS) Reporting
  * DaVinci Notifications IG?
* P2-BP: (0.0) Create a cloud messaging channel type (e.g., azure event grid)
  * Draft channel def, docs for compatibility with existing notifications
  * Prototype from an existing FHIR server
* P2-GC: (0.5) Follow up with at least 2 potential implementers (e.g., cloud vendors, EHRs)

## Developers, students, and others learn FHIR through openly published educational content
* P0-GC: (0.0) Publish at least 2 videos the usage of the new typescript SDK
* P0-GC/BP (0.0 -- we did blog content though): Publish at least 2 videos about developing in FHIR using C#
* P0-BP (0.1 -- but did broadly publicize/promote tooling at WGM/others): Publish educational content on writing FHIRPath and tooling available
* P2-BP (0.7): Publish educational content on integrating FHIR Servers and FHIR Terminology Services
* P2-JM-GC (0.5): Review and "groom" educational content ideas at https://github.com/orgs/microsoft-healthcare-madison/projects/1
* P1-JM (0.5): Publish at least 2 videos from the content backlog

## Open source tools and libraries make it easy to work with FHIR and related IGs

### SMART on FHIR tooling
* P0-JM: (1.0) Decide on path forward for SMART v2, from the following options
    * Seek commitment from BCH?
    * Take over maintenance short or long term
    * Fork
    * Create something new (fhir-typescript?)
* P1-JM: (1.0) Client-JS supports SMARTv2
* P1-JM: (0.2) Launcher supports SMARTv2
* P2-JM: (0.1) Review analytics from SMART Launcher

### FHIRPath is easy to learn, debug, and use
* P0-BP: (1.0) Tooling to simplify writing/debugging fhirpath expressions
* P0-BP: (1.0) Contribute to aligning the variances in implementations/conformance (e.g. comment support in .NET, Join in HAPI)
* P4-BP: (0.1) Prepare a foundation for a library of fhirpath expressions
  * Announce the creation of an openly licensed fhirpath library
  * Develop initial content using the FHIR Library resource
  * Allow users to create/contribute to the library content
  * Provide an easy way to open any branch/fork of the library in the editor
* P2-BP: (0.9 PR review in-progress) Contributions to open source `fhirpath.js` to support split/join/encode/decode/trace

### Changes between versions of specification publications are easy to discover
* Technical implementers can access tooling to compare the contents of package versions
    * P0-GC: (.75 -- need to go deeper on CapabilityStatement including SHOULD/SHALL/MAY annotations) Implement software that finds and categorizes changes in all relevant artifacts.
    * P4-GC/BP: (0.5 docs in place, internal deployment infra WIP) Packaged deployment of tooling
* Non-technical implementers can access tooling to compare the contents of package versions
    * P2-GC/BP: (0.0) Hosted solution for common package+version combinations
    * P2-GC: (0.3 -- JSON in place) CSV or Excel export of contents

### Typescript/JS (DT and SDK)
* Developers can use tooling quickly after specification packages are published
    * P0-GC: (0.2) Expand build tooling to reduce maintenance burden (e.g., daily automatic checks?).
    * P0-GC: (1.0) Publish contents for all 'common' versions of FHIR.
    * P2-GC: (0.0) Choose a strategy for publication of pre-prelease and CI builds of packages.
        * e.g., to express 5.0.0-ballot in sdk version 0.0.3 *versus* 5.0.0-snapshot2 in sdk 0.0.3
        * package `@fhir-typescript/r4-core` (lib version: `0.0.12-beta.18`)
        * package `@fhir-typescript/r5-core` (lib version: `0.0.12-beta.18`)
            * ??package `@fhir-typescript/r5-core-snapshot2` (lib version: `0.0.12-beta.18`)
* Improved quality and correctness of runtime SDK
    * P1-GC: (0.5 - WIP) Support invariant testing in the core specification
    * P5-GC: (0.0) Implement custom JSON serializer/parser
* Expanded scope of 'core' SDK functionality
    * P1-GC: (0.0) Determine path for 'expected' functionality (develop or build integrations) and implement at least 2 of:
        * P1: FHIRPath
        * P1: SMART App Launch
        * P1: HTTP Client (e.g., fetch, query)
        * P5: XML Support
* Simplify usage of Implementation Guides for SDK developers
    * P3-GC: (0.2) Create tooling for IG-based NPM packages
* SDK has a low barrier to entry
    * P0-GC: (0.0) Create documentation site for SDK / API
* Build a community around SDK use
    * P1-GC: (0.0) Determine 'primary' feedback mechanism
    * P3-GC: (0.0) Build and publish roadmap
    * P4-GC: (0.0) Develop 'feedback' form and solicit responses from users and non-users in the JS/TS space

### .NET (Firely) SDK
* Expanded scope of 'core' SDK functionality
    * P2-BP: (0.0) Provide a "validator" or SDK for search parameter input (e.g., evaluate querystring for valid FHIR syntax, modifiers, values)
* Simplify usage of Implementation Guides for SDK developers
    * P5-BP/GC: (0.2) Create tooling for IG-based NuGet packages
* SDK users understand and are comfortable with the long-term FHIR versioning strategy
    * P1-BP/GC: (0.2 - BoF and Working Group Meeting discussions) Coordinate with Firely

## The FHIR specs are clear, concise, correct, and new-user friendly

### Important and high-traffic areas of the FHIR Core spec receive special attention
* P0-GC: (1.0) Search Page rewrite is ready for QA
* P1-GC/BP/JM: (1.0) Search Page rewrite is QA'd for ballot
* P0-BP/GC/JM: (1.0) Assisting in applying the backlog of approved changes to the core FHIR R5 specification
* P2-all: (1.0) Review tickets submitted by our team and apply or submit PRs to apply the resolutions
* P2-JM: (0.5) Propose to HL7 and discuss feasibility of usability metrics from the official HL7 web server (logs or JS analytics) and build.fhir.org
* P2-GC/BP: (0.0) Engage a MS documentation or usability team for review
* P2-JM: (0.0) Propose a WGM quarter with Education Advisory Council (reach out to Viet, Virginia), topics to include...
  * Understand level of interest in spec usability
  * Consider role for survey and/or individual interviews
  * Discuss possible roadmap, usability practices

## The extended FHIR Community (including MS-internal stakeholders) understands our team and mission
* P1-JM: (1.0) Develop a short bullet list of talking points (MSR org; focus on spec; interop across clouds)
      * Added https://github.com/microsoft-healthcare-madison/team/blob/master/team-overview.md
* P3-all: (0.2) Incorporate these into our various decks/docs/demos?
* P2-??: (0.8 ran "intro" session) Organize a cross-org FHIR users group ("FHIR at Microsoft" Teams team? mailing list? meeting?) within MS
  * Invite all relevant/known orgs to join
  * Include a recorded session on our team's work including demos / showcase
  * Include a session on Ballot process and why to participate
  * Include links to educational content
  * Invite others to reciprocate, share their work, build awareness 

## Our team consistently advocates for patient rights
* P2-JM: (0.75 -- re-submitted manuscript) Outline principles for patients under TEFCA (transparency / AoD, consent based access, partitioning of data across personas)
* P2-JM: (0.25) Interview QHINs to understand their plans for these
* P3-JM: (0.0 -- dependency on paper?) Write a brief or blog post

## SMART Health Links are adopted for use cases beyond the scope of SHCs
* P0-JM: (1.0) Argonaut launches with project scope that includes lifetime immunization record
* P1-JM: (1.0) Open invitation to participate
* P1-JM: (1.0) At least one EHR vendor participates
* P1-JM: (1.0) At least one state registry or state IIS vendor participates
* P2-JM: (0.0 but we do have feedback) Connectathon testing provides feedback for the spec

## Argonaut projects reach consensus with a pragmatic, productive, and inclusive process that leads to real-world implementation
* P0-JM: (0.8 -- lacking real EHR implementations) SMART App State connectathon includes 2+ EHRs and 2+ Clients
* P1-JM: (1.0) SMART App State spec incorporates connectathon feedback
* P2-JM: (0.1 -- don't have consensus) SMART App State is proposed for inclusion as "experimental capability" in SMARTv2 STU Update
* P5-JM: (0.0) Patient Access Brands spec is supported by 2+ EHRs in production
