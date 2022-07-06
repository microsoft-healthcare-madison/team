# OKRs for June-September 2022

## FHIR-based software uses topic-based subscriptions to avoid polling
* P0-GC: R4B Backport IG is published
    * P0-GC: (1.0) Publication request approved by FHIR-I, FMG
    * P0-GC: Specification is Published
* P1-GC: Have connectathon track available, either as a standalone track or part of an Argo-wide track (?)
* P3-GC: Subscriptions sandbox supports more SubscriptionTopics (e.g., arbitrary fhirpath-based topics, or a "button push event" topic)
* P0-GC/BP: RI is up to date with R4B+IG and R5
  * P0-GC: With final R4B/IG version
* P2-GC: Track usage for Subscription sandbox (counts by R4B vs R5, standard channel types or "any custom channel")
* P2-GC/BP: Develop SubscriptionTopic content from at least one of the following:
  * Public health
      * MedMorph for public
      * National Center for Health Statistics (NCHS) Reporting
  * DaVinci Notifications IG?
* P2-BP: Create a cloud messaging channel type (e.g., azure event grid)
  * Draft channel def, docs for compatibility with existing notifications
  * Prototype from an existing FHIR server
* P2-GC: Follow up with at least 2 potential implementers (e.g., cloud vendors, EHRs)

## Developers, students, and others learn FHIR through openly published educational content
* P0-GC: Publish at least 2 videos the usage of the new typescript SDK
* P0-GC/BP: Publish at least 2 videos about developing in FHIR using C#
* P0-BP: Publish educational content on writing FHIRPath and tooling available
* P2-BP: Publish educational content on integrating FHIR Servers and FHIR Terminology Services
* P2-JM-GC: Review and "groom" educational content ideas at https://github.com/microsoft-healthcare-madison/team/projects/1 
* P1-JM: Publish at least 2 videos from the content backlog

## Open source tools and libraries make it easy to work with FHIR and related IGs

### SMART on FHIR tooling
* P0-JM: Decide on path forward for SMART v2, from the following options
    * Seek commitment from BCH?
    * Take over maintenance short or long term
    * Fork
    * Create something new (fhir-typescript?)
* P1-JM: Client-JS supports SMARTv2
* P1-JM: Launcher supports SMARTv2
* P2-JM: Review analytics from SMART Launcher

### FHIRPath is easy to learn, debug, and use
* P0-BP: Tooling to simplify writing/debugging fhirpath expressions
* P0-BP: Contribute to aligning the variances in implementations/conformance (e.g. comment support in .NET, Join in HAPI)
* P4-BP: Prepare a foundation for a library of fhirpath expressions
  * Announce the creation of an openly licensed fhirpath library
  * Develop initial content sing the FHIR Library resource
  * Allow users to create/contribute to the library content
  * Provide an easy way to open any branch/fork of the library in the editor
* P2-BP: Contributions to open source `fhirpath.js` to support split/join/encode/decode/trace

### Changes between versions of specification publications are easy to discover
* Technical implementers can access tooling to compare the contents of package versions
    * P0-GC: Implement software that finds and categorizes changes in all relevant artifacts.
    * P4-GC/BP: Packaged deployment of tooling
* Non-technical implementers can access tooling to compare the contents of package versions
    * P2-GC/BP: Hosted solution for common package+version combinations
    * P2-GC: CSV or Excel export of contents

### Typescript/JS (DT and SDK)
* Developers can use tooling quickly after specification packages are published
    * P0-GC: Expand build tooling to reduce maintenance burden (e.g., daily automatic checks?).
    * P0-GC: Publish contents for all 'common' versions of FHIR.
    * P2-GC: Choose a strategy for publication of pre-prelease and CI builds of packages.
* Improved quality and correctness of runtime SDK
    * P1-GC: Support invariant testing in the core specification
    * P5-GC: Implement custom JSON serializer/parser
* Expanded scope of 'core' SDK functionality
    * P1-GC: Determine path for 'expected' functionality (develop or build integrations) and implement at least 2 of:
        * P1: FHIRPath
        * P1: SMART App Launch
        * P1: HTTP Client (e.g., fetch, query)
        * P5: XML Support
* Simplify usage of Implementation Guides for SDK developers
    * P3-GC: Create tooling for IG-based NPM packages
* SDK has a low barrier to entry
    * P0-GC: Create documentation site for SDK / API
* Build a community around SDK use
    * P1-GC: Determine 'primary' feedback mechanism
    * P3-GC: Build and publish roadmap
    * P4-GC: Develop 'feedback' form and solicit responses from users and non-users in the JS/TS space

### .NET (Firely) SDK
* Expanded scope of 'core' SDK functionality
    * P2-BP: Provide a "validator" or SDK for search parameter input (e.g., evaluate querystring for valid FHIR syntax, modifiers, values)
* Simplify usage of Implementation Guides for SDK developers
    * P5-BP/GC: Create tooling for IG-based NuGet packages
* SDK users understand and are comformtable with the long-term FHIR versioning strategy
    * P1-BP/GC: Coordinate with Firely

## The FHIR specs are clear, concise, correct, and new-user friendly

### Important and high-traffic areas of the FHIR Core spec receive special attention
* P0-GC: Search Page rewrite is ready for QA
* P0-GC: QA full FHIR Specification going into September R5 ballot
* P0-BP/GC: Assisting in applying the backlog of approved changes to the core FHIR R5 specification
* P1-GC/BP: Search Page rewrite is QA'd for ballot
* P2-all: Review tickets submitted by our team and apply or submit PRs to apply the resolutions
* P2-JM: Propose to HL7 and discuss feasibility of usability metrics from the official HL7 web server (logs or JS analytics) and build.fhir.org
* P2-GC/BP: Engage a MS documentation or usability team for review
* P2-JM: Propose a WGM quarter with Education Advisory Council (reach out to Viet, Virginia), topics to include...
  * Understand level of interest in spec usability
  * Consider role for survey and/or individual interviews
  * Discuss possible roadmap, usability practices

## The extended FHIR Community (including MS-internal stakeholders) understands our team and mission
* P1-JM: Develop a short bullet list of talking points (MSR org; focus on spec; interop across clouds)
* P3-all: Incorporate these into our various decks/docs/demos?
* P2-??: Organize a cross-org FHIR users group ("FHIR at Microsoft" Teams team? mailing list? meeting?) within MS
  * Invite all relevant/known orgs to join
  * Include a recorded session on our team's work including demos / showcase
  * Include a session on Ballot process and why to participate
  * Include links to educational content
  * Invite others to reciprocate, share their work, build awareness 

## Our team consistently advocates for patient rights
* P2-JM: Outline principles for patients under TEFCA (transparency / AoD, consent based access, partitioning of data across personas)
* P2-JM: Interview QHINs to understand their plans for these
* P3-JM: Write a brief or blog post

## SMART Health Links are adopted for use cases beyond the scope of SHCs
* P0-JM: Argonaut launches with project scope that includes lifetime immunization record
* P1-JM: Open invitation to participate
* P1-JM: At least one EHR vendor participates
* P1-JM: At least one state registry or state IIS vendor participates
* P2-JM: Connectathon testing provides feedback for the spec

## Argonaut projects reach consensus with a pragmatic, productive, and inclusive process that leads to real-world implementation
* P0-JM: SMART App State connectathon includes 2+ EHRs and 2+ Clients
* P1-JM: SMART App State spec incorporates connectathon feedback
* P2-JM: SMART App State is proposed for inclusion as "experimental capability" in SMARTv2 STU Update
* P5-JM: Patient Access Brands spec is suppored by 2+ EHRs in production

