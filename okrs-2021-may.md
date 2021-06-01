## OKRs for May 2021

## Standards publication and process (balloting, etc)

### SMARTv2
* P1 (1.0): Submit ballot request in time for May ballot cycle
    * P1: Content from "wip" page integrated and ready for ballot
    * P1: Changelog included in spec
* P2 (0.8): May 2021 Connectathon Track

### Web Messaging

* P0 (0.7): Submit IG publication request
    * P0 (0.9, need scratchpad query): Finalize reconciliation from 2020Sep ballot
* P2: Continue to engage the community with
    * P2 (0.7): a connectathon track, focusing on 1.0 published spec + specific design issues (e.g., capability discovery)
    * P2 (0.6): Continue regular SWM calls at less frequent cadence (monthly?) and shorter (60 min)

### Subscriptions

#### R4 "backport"
* P0 (0.7): Submit IG publication request
    * P0 (1.0): Triage all ballot comments (Jan 2021 ballot)
    * P0 (.53): Resolve all ballot comments (Jan 2021 ballot)
* P1 (0.2): Determine plans for R4 backport support in conversation with two cloud-hosted FHIR platforms
* P1 (0.0): Determine plans for R4 backport support in conversation with two EHR systems
* P2 (0.9): Test at May Connectathon (need to determine what this looks like)

#### R5
* P0 (1.0): Apply all approved Subscription Jira tickets (up through issue number 29315)
* P1 (1.0): Identify a track lead for May Connectathon (need to determine what this looks like)
* P2 (1.0): Update Subscription resources to FMM2+ (hard deadline is July 2021; now October 2021)

## Standards Acceleration / Rapid IG Development

### Argonaut

* P0 (1.0): Participate in project selection (targeting three or four 2021 projects)
* P0 (1.0): Commit to leading or co-leading projects (at least one; up to three)
* P1 (1.0): DevDays June 2021 presentation with project overview
* P1 (1.0): Kick off regular meetings; list details on HL7 conference call tracker; invite community participation
* P1 (0.6): Establish project scope

### CARIN

* P1 (0.4): Establish imaging access project participants
* P2 (0.4): (Pending staffing) Develop draft IG with FHIR, DICOM Web, SMART App Launch, and Token Introspection (updates to Sync for Science 2018 work)
* P3 (0.0): (Pending staffing) Develop reference implementation for consumer imaging access

### VCI: Health Cards

* P0 (0.9): Finalize an "implementation-ready" version of the specification with "v1.0" tag
* P0 (0.0): Re-record intro video and context, given recent updates (cut dependency on DID/SIOP)
* P0 (1.0): Open source tools to validate issuance (data formats, signatures, APIs)
* P1 (0.7): Work with VCI to determine an evaluation plan for UX
* P2 (0.3): Open source verifier SDK with data-driven rules, implementing current USA-based guidelines for products and immunization schedule
* P2 (0.0): Tooling to enable publication of >1 version of the spec to https://smarthealth.cards

## Outreach and communications

### MS Internal

* P1 (0.9): Develop guidance on how to interact with standards communities / bodies
* P1 (0.6): Schedule "check-in" meetings with at least 2 teams re: standards guidance
* P2 (0.1): Schedule "office hours" for open FHIR discussion (?)

### External FHIR community

* P1 (1.0): Gino to continue "FHIR for Developers" video series on intro topics for FHIR videos. E.g. for specific languages provide an overview of how to connect to a server or issue queries. Focus on the security + data connectivity >> UI.

* P1 (0.0): Clean up and publish an external-facing version of "how to interact with standards communities" in our public team repo

* P1 (0.4): Continue "guided walk through FHIR" youtube series with weekly content

## "Community" Tooling

### fhir-codegen

* P0 (1.0): Support Firely with updates and fixes as needed.
    * P? (0.7): Improve serialization / parsing performance
* P1 (1.0): Update parsing and serialization benchmarks to compare existing approaches, including latency to first pass + warmed-up throughput
* P1 (1.0): Update internal libraries to System.Text.Json and .Net 5.0
* P2 (1.0): Start creating tagged releases
    * Determine structure of releases
    * Determine schedule for releases
* P2 (1.0): Brian uses codegen for getting fhir interfaces added to TypeScript DefinitelyTyped repo
* P3 (0.5): Add support for parsing profiles.
    * Create C# code that integrates profiles and existing Firely models
* P5 (0.0): Build OpenAPI docs compliant with 'official' FHIR build.
    * Add to 'generated' for compatibility checking.
    * Pipeline for IGs -> OpenAPI

#### Not captured in OKR planning
 * Support for R4B / R5 new build tooling

### SMW library

* P0 (0.8): available library covers common message groups & discovery
* P0 (1.0): available in NPM
* P1 (0.5): codelab or educational materials to support developer experience
* P2 (0.0): SMART app launcher supports at least one Web Messaging feature
* P2 (0.0): CDS Hooks Sandbox supports at least one Web Messaging feature
