## FHIR Community builds on high-quality open source tools, libraries, and sandboxes

### Working with Profiles (e.g., national and regional base profiles) is easy and error-free

* P0-GC/BP: (0.0) Short series of "problem statements", as tiny programs solving a "real" problem the hard way --> the easy way
  * GC: (0.0) app searching for and displaying data when you _think_ the content will be in US Core
  * GC: (0.0) service mapping your internal structures into US Core for a FHIR API service
  * BP: (0.0) Compare implementing a small slice of SDC behavior (say, "execute FHIR REST queries driven by pre-pop extensions") on top of SDC-enabled Questionnaires with helpers or raw typescript

* P0-BP: (1.0) [FHIR IG uploader](https://github.com/brianpos/UploadFIG) works everywhere
  * Without recompiling, users can supply CLI arguments for...
    * P0 Target server address
    * P0 Source package id (defaults to public registries)
    * P0 Local package file
    * P0 Remote package file by URL
    * P0 By default, all major canonical resources are loaded
    * P5 Some kind of filter to say which artifacts should be loaded?
  * P0 Documentation and introduction video explain usage
  * P0 Published as dotnet tool, invokable with `dotnet tool install ...`
  * P3 Tool can generate a report to verify content in server/package
  * Note: example usage of System.CommandLine package in [fhir-candle](https://github.com/GinoCanessa/fhir-candle/blob/main/src/fhir-candle/Program.cs)

* P2-GC: (0.3) Complete a pass of IG package export for Firely C#
  * Goal: IG-based helper packages work alongside Firely .NET SDK (`Hl7.Fhir.R5` .NET package)
  * Prior work: [sdc-helpers](https://github.com/brianpos/fhir-sdc-helpers), [CS-Profiling](https://github.com/GinoCanessa/FHIR-CS-Profiling-Basic/tree/main/src)
  * Decide what the package contents should look like
    * P0: (1.0) Define namespaces to use within pacakges and for artifacts
    * P0: (1.0) Define Level 0 functionality for constants (e.g., extension URLs)
    * P1: (0.3) Define Level 1 functionality for getters/setters to wrap extensions (e.g., patient.UsCoreRace)
    * P2: (0.0) Define non-terminology validation against profile
  * P0: (0.5) Decide what the package names, versions and publication process should look like. Examples to think through:
    * `dotnet add package Hl7.Fhir.Uv.Sdc_3_0_0`
    * `dotnet add package Hl7.Fhir.Us.Core.6.0.0`
  * Support generation with codegen
    * P1: (0.2) Generate namespaces to use within pacakges and for artifacts
    * P1: (0.2) Generate Level 0 functionality for constants (e.g., extension URLs)
    * P2: (0.2) Generate Level 1 functionality for getters/setters to wrap extensions (e.g., patient.UsCoreRace)
    * P3: (0.0) Generate non-terminology validation against profile
    * P3-BP: (0.0) Experimental cut of SDC Helpers functionality  using this framework
    * PX: (0.0) Experimental cut of subscription backport library using this framework
  * P3: (0.3 discussions started) Work with Firely to establish long-term publication + management plan for these packages

### Firely .NET SDK users have access to FHIR's "interface" system (e.g., CanonicalResource)
* P0-GC: (0.2 design discussion) Complete a pass of FHIR Interface support from `fhir-codegen`
    * Background: Firely hand-maintains `IVersionableConformanceResource` interface by hand
    * P0-GC: Expose .NET interfaces automatically through codegen, corresponding to FHIR's
        *  `CanonicalResource` 
        *  `MetadataResource` (sub-interface of `CanonicalResource`)
    * For later: Expose .NET interfaces for FHIR's patterns (Request, Event, Definition)

### Tooling helps SDK authors work with multiple versions of FHIR
* Background: today normative resource classes (and a few others) in Firely  use hand-authored annotations like
  * "since version x.y.z" (on Resources, Elements)
  * "not mapped after version x.y.z" (on Resources, Elements)
* P0-GC: (0.8) Complete refactoring of internal models to use C# record types
* P3-GC: (0.2) Improve the multi-version story of code-gen
    * Caller requests an export specifying multiple FHIR versions
    * Propose / sketch codgen interface with access to cross-version details, which can be used to determine and output things like diffs, since/not-mapped annotations

### Tooling improves the quality of specifications/applications
* P1-BP: (0.8) Static Analysis Tool for FhirPath C#
    * Ability to verify: 
        * Already done: all core spec Search Parameters
        * P1: (1.0) all core spec Invariants
        * P1: (1.0) CLI supports passing package to trigger testing of invariants/search parameters
        * *(Note: verifier may not have full coverage of language)*
    * P2: (0.7 discussed; no decision yet) Discuss with Firely for inclusion in the SDK
    * (Extra: supported validation of fhirpath in UploadFIG, validation of IG content pre-publication)
    * P5: (0.7) POC inclusion in Facade/Microsoft FHIR Server
    * P5: (0.0) Support scanning Quesitonnaire/SDC linkIds in expressions

## FHIR Community has access to high-quality demo environments

### Subscriptions reference stack
* P0-GC: (0.5) Complete the subscriptions client page in the UI and have it deployed
    * P6-GC: (0.2) Add support for 'localhost' routing
* Build and post a 'subscription topic' "on-ramp" (HL7 terminology for confluence pages)
    * Key concepts:
        * P1-GC: (0.0) For IG authors: Getting started with subscriptions / using the RI
        * For later: 
            * For IG consumers: Getting started with subscriptions / using the RI 
            * Designing topics: Concepts / basics / advanced?
    * Video walkthrough / tutorial covering
    * Documentation / written instructions
* Detect and reject POSTed `SubscriptionTopic`s that are invalid or not supported because of:
    * P0: (1.0) Query-based triggers with unsupported modifiers
    * P0: (1.0) `canFilterBy` with unsupported modifiers
    * P5: (1.0) invalid fhirpath expressions (compile)
    * *(Point users to zulip to share their use case for prioritization)*
* P4-GC/BP: (0.0 -- in-person opportunity!) Topic authoring UI - integration/linkage between RI and FHIRPath Lab.
  * GC: Add a button to each topic view (e.g., https://subscriptions.argo.run/store/resource-viewer?store=r4b&type=SubscriptionTopic&id=encounter-complete) with "Explore in FHIRPath Lab"
  * BP: Process URL parameters passed from the subs UI

### FHIR Facade
* P2-BP: (1.0) Keep pace with the Firely SDK releases
* P3-BP: (0.0) POC Canonical Packaging IG to show support to be a downstream server
    * implement the [packaging]( http://build.fhir.org/ig/HL7/crmi-ig/packaging.html) in support of SDC content distribution and loading
    * Support for `GET Questionnaire/:id/$crmi.package` based on http://build.fhir.org/ig/HL7/crmi-ig/index.html
        * Output includes Questionnaire
        * Output includes all external ValueSets needed for Questionnaire ("where practical")
        * Output includes all external CodeSystems needed for Questionnaire ("where practical")
    * Blog post covering the how and why of this functionality (extending on my existing posts)

### FHIRPath-Lab
* P1-BP: (1.0) Support to validate fhirpath expressions (using static analysis)
* P1-BP: (0.5 -- draft material) Short video on using the FHIRPath-Lab
* P2-BP: (0.0) Better support for Subscription Topic editing and testing
* P3-BP: (0.2) Introduction of the co-pilot style AI
* P5-BP: (0.0) Experiment with design choices to evaluate all engines at once
* P5-BP: (0.0) Run the HL7 fhirpath unit test suite via the tool and view output
* P5-BP: (0.5 -- discussed; they plan to implement) Followup with Health Samurai and MayJuun on integrating their fhirpath engines

## FHIR community continually improves our specifications and our processes
* P1: (0.3) Schedule a session to discuss quality plan for "path to R6". Brief retrospetive:
    * Unmanageable backlog of unapplied changes
    * Double-application of changes from R5 + R4B
    * Late-breaking changes
    * *With suggested mitigations*
* P1-BP (0.5) Keep PA/FHIR R6 on track (maintain low backlog)
* P1-GC (0.5) Keep FHIR Infrastructure R6/Subscriptions on track (maintain low backlog)

## FHIR community offers high-quality openly licesned educational content

### Create annotated examples of HL7 specifications
* P0-BP: (0.2) Extend the `SDC by Example` content
    * (Extra: built Questionnaires for IPS-based prepopulation demo)
    * Observation extraction
    * Observation & fhirpath pre-population
    * Assemble operation
* P0-BP: (0.0) Example content covering
    * External form to be "ingested" into an EHR for ...
    * "PRAPARE Prime" (i.e., locally modified PRAPARE hide fields, add some extras) --> FHIR Questionnaire
        * Not technically required by US Core, but we have to write it *somehow*
    * "PRAPARE Prime Response" --> QR
        * Not technically required by US Core, but we have to write it *somehow*
    * "PRAPARE Prime Response" --> Observation tree (the current "SHALL")
        * Required by US Core, so we need to make sure it works
        * Include examples of local codes for the "invented" questions
    * Conditions derived from this assessment (e.g., food insecurity)
        * Following current US Core spec's requirements / Must-Supports
* P1-BP: (0.0) US Core provides clear guidance and a diagram distinguishing
    * data collection (e.g., recorded as Observations)
    * problems actively tracked (e.g., Conditions)
* P1-BP: (0.2) Short video series on SDC: (4-5 clips)
    * SDC Basics + Terminologies
    * Data Extraction - Obs/StructureMap
    * Pre-Population - Obs/FhirPath

## Health apps integrate with EHR data + workflows

### SMART apps can access imaging data

* P1-JM: (0.6) Imaging specification reviewed with at least 2 PACS/network vendors
* P1-JM (1.0) Connectathon scheduled for Argo Imaging participants
  * P2: (0.6) Includes at least 2 imaging servers
  * P2: (0.6) Includes at least 2 imaging apps
* P2-JM: (0.0) Deployment plan is finalized for at least 1 clinical site
* SMART App Launcher supports "associated_endpoints" discovery
   * P1-JM: (1.0) In the Imaging fork
   * P3-JM: (1.0) In the upstream project
* SMART Client JS fork supports "associated_endpoints" retrievals
   * P2-JM: (1.0) In the Imaging fork
   * P4-JM: (0.0) In the upstream project

### SMART apps can write blood pressures to EHR

* P1-JM: (1.0) Argonaut "Write Vitals" project has launched
  * P2-JM: (1.0) Participants include at least 2 EHRs
  * P2: (1.0) Participants include at least 2 apps
  * P3: (0.6) Participants include at least 2 health systems
* P1-JM: (1.0) Consensus on use cases
  * P2: (1.0) clinician-triggered writes
  * P2: (1.0) patient-triggered writes
  * P1: (1.0) record the device used
  * P3: (1.0) convey external provenance (from outside provider)
  * P3: (1.0) convey app used to capture data
  * P3: (1.0) convey app used to submit data
---

## Extra things we worked on

* SQL on FHIR -- reference implementation, tests, example
* IPS Prepopulation examples incluing SHLink
* Work with CSIRO renderer for Questionnaires
* `fhir-candle` infrastructure, tooling for IG-based reference implementations (CDEX, PAS)
* Publication support for Patient Corrections IG
