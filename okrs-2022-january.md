# OKRs for January 2022


## Balloted specifications flow smoothly through HL7 process/pipeline
* P0: SMART App Launch v2 is published
* P1: SMART Web Messaging ballot resolutions are applied
* P1: Argonaut committed to supporting publication 
* P1: Publication request submitted


## Open source tools and libraries make it easy to work with FHIR and related IGs
* P2: Support for SMARTv2 features is merged into SMART App Launcher
* P2: Support for SMARTv2 features is merged into SMART `client-js`


## Anyone in the FHIR community can easily learn about our team's work and the specs we contribute to
* P0: Ask #smart community for volunteeres to lead a SMART on FHIR Connectathon track
* P1: Record and publish four short videos on new features of SMART v2 (PKCE, Token Introspection, scopes, and asymmetric client auth)
* P1: Record and publish three "transparent consultation" videos from "everyday" interop discussions


## SMART Health Cards are widely available, recognized, and used
* P1: "Help Desk" support in place to offload this responsibility
* P2: An approach to SHC revocation is reviewed and published
* P2: SHC revocation is supported by at least one issuer
* P2: At least one state-based issuer supports non-COVID immunization data


## Subscriptions IG / R4B
* P0: Publish Backport IG v0.1.0 based on FHIR R4B
* P0: Make available for testing at the next connectathon


## Subscriptions R5
* P1: Sync changes from Backport IG and R4B
* P1: Make available for testing at the next connectathon


## Code-Gen: C# (Firely)
* P0: Implementation of IDicionary model definitions
    * P0: Published in NuGet (Firely Net API)
* P0: Customized serializers and parsers
    * P0: For JSON, based on `System.Text.Json`
    * P2: For XML, based on [`System.Xml` (?)]
    * P0: Published in NuGet (Firely Net API)
    * P1: Add option to either throw or 'do what you can' and return an OperationOutcome
    * P2: Support for `_summary`
    * P2: Support for `_elements`
* P2: Create tooling to better support use of IGs and Extensions
    * e.g., classes with ergonomic support for (complex) extensions defined in IG
    * P5: A better story than OpenAPI (e.g., discovery, unit testing)
* P5: Design and implement a process for non-terminology validation (e.g., Fluent Validation, CUE)
    * P5 Support IG model validation
* P5: Create a streaming JSON 'modification' transcoder (add/remove/modify elements in single pass)


## Lay groundwork for a community-supported comprehensive TS/JS FHIR library [TBD]

* Propose a roadmap of features
* Identify candidates for a community lead
    * point person for decision making
    * committed to active development work
    * depending on this library for real-world projects
* Select a community lead
* Establish a 'home' for the project

## Madison Team

* P1: Expand the team by posting a job req for at least one new software engineering position (Madison-based or remote)
* P1: Dedicate time for a "hack week" project (could be .NET tooling, QR links, structuredefinition editor UI, maybe as a VC Code Browser-based extension)
* P2: Publish source on GitHub
* P2: Share a short video project video with FHIR community
