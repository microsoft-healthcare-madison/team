## SMART Imaging Access is widely available for access (JM)

### Argonaut specification is finalized
* P0 (0.8): Connectathon includes at least 2 PACS and at least 2 consumer app participants
* P0 (0.7): Connectathon lessons learned are incorporated into spec
* P2 (0.0 -- did not get traction even for the "simple" async of "please try again"): Update `async` functionality to match https://hl7.org/fhir/async-bundle.html

### Initial implementers are on a path to deployment
* P0 (0.0 -- not for lack of trying): Identify at least one real-world clinical organization to deploy imaging access
* P1 (0.0, missing prereq) : Establish deployment plan and support efforts with "high touch" engagement
* P4 (0.0): Pre-production environment is ready for testing

##  SMART ~~Patient~~User Access Brands (JM)
* P0 (1.0): Branding Extensions on track for Jan ballot of FHIR Extensions IG
* P1 (1.0): PAB updated to use Branding Extensions
  * Profiles in PAB, extensions in Extensions IG
  * Examples updated
* P2 (1.0): PAB on track for Jan ballot
* P5 (0.0): Identify a champion for "Shorthand in FHIR Extensions IG" -- it should be easier to write and review content for the extension IG, and FSH would help!

##  Standards-based data serve as a foundation for clinical analytics (JM)

### SQL-on-FHIR v2 spec is widely implemented
* P2 (0.8): Frozen draft spec
* P2 (1.0): At least two implementations designed for use at scale
* P3 (0.2 -- conversations started): Internal participation
* P5 (0.0 -- but we have JSON Schema + FHIR Logical Model) Typescript definition for ViewDefinition
* P5(BP) (0.0): DSL concepts?

###  Digital quality measures are based on real-world EHR data (JM)
* (0.3 -- drafted): Publish perspective highlighting use of real data to design lightweight measures
* (1.0): Advocate for simplification of measures with ARPA-H leadership

##  Interop community understands and leverages LLMs where applicable (JM)

### "Future of interop" perspective is submitted for academic publication
* P0 (0.5 -- WIP): Outline
* P1 (1.0): Authors on board
* P2 (0.6): Draft reviewed with comments
* P2 (0.0): Draft submitted for publication

### Open source demos and examples are widely available
* P1(all) (1.0): HACK WEEK
    * Scheduled time in early December
    * P1(all) Questionnaire-filling as a focus (end result is a QuestionnaireResponse)
* P5 (0.3 -- schema creation + instance data formatting): Data format conversion from EHI exports?
* P5 (0.3) Manual data abstraction with GPT-4?

## FHIRPath Lab Supports Cross-Implementation Testing
* P0(BP) (1.0): Community-maintained test cases are up-to-date; broken content is eliminated from  https://github.com/FHIR/fhir-test-cases/pull/151 
* P0(BP) (1.0): Library-wrapped test cases are updated with to the latest content
* P1(BP) (1.0): fhirpath-lab extensibility is documented
    - Git Repo includes documentation explaining how other engines can be incorporated
    - Health Samurai team is aware
* P1(BP) (0.1): FhirPath-lab subscription supports subscription topic editing
	- FhirPath-lab supports "Topic Editing", starting from new or existing topic
	    - Notification shape
	    - Filters
    - All fields of SubscriptionTopic can be created/edited, with basic schema validation in place
	- More complete support for editing triggers
        - `fhirpathCriteria` can be edited and validated
        - `fhirpathCriteria` can be evaluated against sample instances *(basically done)*
* P1(BP/GC) (0.2): FhirPath-lab subscription editor can be launched from fhir-candle
	- Launch from fhir-candle subscription topic window
	- Launch from fhir-candle test case window (with specific expression windows)
	- Launch includes `fhirserver` parameter to ensure correct server
* P5(BP) (0.5): FhirPath-Lab AI Chat


## FHIR Questionnaires are robust and easy to use (BP)

### Educational material makes Questionnaires (including SDC pre-populated content) easy to adopt
* (0.0): Introductory content for new users
* P0 (0.0): Series of feature-focused videos including
    * Basic structuring simple questionnaires
    * Several pre-pop videos covering increasingly complex use cases
        * P0 Observation based
        * P0 fhirpath based
        * P2 StructureMap based
* P1 (0.7): A standalone IPS pre-pop demonstration shows how to use SDC pre-population
    - published as separate repo
    - supports swappable renderers (lforms/csiro)
        - Responsibility of a renderer is maintaining the form and managing interactions
        - Renderer essentially uses:
            - `Renderer.render(domElement, questionnaire, [questionnaireResponse])` - can be partial or complete
            - `Renderer.retrieveCurrentStatus() => QR`
        - Hack week to try auto-populating forms embedding?
            - Populate a "best guess" above some threshold
            - Populate an extension with "other suggestions"?
    
### Open-source tools support advanced validation of Questionnaires
* P2 (0.0): QuestionnaireResponse validation merged into Firely SDK

##  FHIR community continually improves our processes (BP)
* P0 (1.0): Keep PA backlog low - particularly changes applied
	- (1.0): Core build to support new resources (again) - sent to GG in PR - done
	- (0.0): VhDir STU1 published
    
## Open-source tooling makes FHIR easy to use (BP)

* P1 (0.0): Upload-FIG is published as a MS open source project + Nuget package
  * Internal application submitted
  * Repository migrated
  * Internal build pipelines configured
  * Signing keys established
  * Automated publication to Nuget
* P1 (0.0): MS FHIR Server POC materials shared with Server team (and my branch deployed - including the below features)
    * New Firely SDK 5.x parser
    * SDC Validation
    * SDC pre-pop
    * StructureMap/FML parser/serializer
    * StructureMap evaluator
    * fhirpath validation
    * current canonical processing
    * General feedback reviews
* P3 (0.0): FHIR Canonical Resource Management Interface (CRMI) IG has independent reference implementation.
    * POC packaging server implementing https://build.fhir.org/ig/HL7/crmi-ig/OperationDefinition-crmi-package.html
    * Minimal use case: Moving questionnaires from a (development --> production) environment. Example deployment scenario:
        * Source server supports `$crmi.package`
        * Source server has `Questionnaire/example|2.0.0`, a new Questionnaire, which in turn depends on ... ValueSets and other Questionnaires (via `import-questionnaire` extensions)
        * User calls `$crmi.package( Questionnaire/example|2.0.0)` to produce an importable bundle
        * UploadFIG supports the uploading of a "package" prepared by the `$crmi.package` operation
    * As a reference implementation to test the IG
    * Key areas to implement
        * create package https://build.fhir.org/ig/HL7/crmi-ig/OperationDefinition-crmi-package.html

* P2 FHIR-PATH Validator - symbol table merge with Firely SDK
    - (0.0): Update the SDK to better support leveraging the fhirpath symbol table for external usage
    - (0.0): Leverage the enhanced symbol table in the fhirpath validator
    - (0.7): Encourage if this validator can be adopted into the SDK
    - (0.3): comments parsing integrated into SDK (complete/merge existing work)
    - (0.9): Position information in fhirpath expression parsing - mostly complete
    - (0.9): Include `CustomExpression` capability into the SDK - done, needs to be merged in
    - (0.9): Brackets `()` to be able to be included in the expression tree (via the new CustomExpression) which then can enable round-tripping expressions to/from strings
    
* P1 (1.0): Prepare `withVariable` proposal to add to fhirpath for consideration by HL7
    https://dev.fhirpath-lab.com/FhirPath?libaryId=7775d5cf3df540a38b34e83b27f8f284


## Open-source tooling makes FHIR easy to use (GC)

* P1: (0.3): Publish a package resolution and local FHIR cache management tool
  * P1: .Net Library is available in NuGet
  * P1: .Net tool is available in NuGet
  * P6: Investigate the MS policies around publishing AOT compiled native binaries
  * P5: Create a PoC NPM facade that indexes the contents of CI Builds (core and IG)
* P1: (0.3): Publish `fhir-codegen`
  * P1: .Net Library is available in NuGet
  * P1: .Net tool is available in NuGet
* P0: (0.8) Update the `fhir-codegen` Firely language to output FHIR Interfaces
    * Background: Firely [hand-maintains the `IVersionableConformanceResource` interface](https://github.com/FirelyTeam/firely-net-sdk/blob/71269dfa12511b6c8372d8e540281ed5cd06014f/src/Hl7.Fhir.Base/Model/IConformanceResource.cs#L56)

* P0: (0.5) Create .Net interfaces corresponding to FHIR's
    * `CanonicalResource` 
    * `MetadataResource` (sub-interface of `CanonicalResource`)
    * P0: (0.2) Add partial class definitions to resource model classes that implement the interfaces for each version of FHIR
        * Background: Firely [hand-maintains implementations of the `IVersionableConformanceResource` interface](https://github.com/FirelyTeam/firely-net-sdk/blob/main/src/Hl7.Fhir.R4/Model/IConformanceResource.cs)
        * Add stub properties for elements that do not exist (i.e., getter returns null, setter throws exception).
    * For later: Expose .NET interfaces for FHIR's patterns (Request, Event, Definition)

## Make IGs more testable with Reference Implementations (GC)

* Create an RI for vitals-write for the virtual connectathon (Nov 15)
    * Non-goal: Full SMART on FHIR reference implementation
    * P1: (0.8): feature set: 
        * Complete the SMART standalone patient launch flow
            * Client app registration is implicit
            * Symmetric and Asymmetric authn both work, but no auth is actually checked
            * Works with SMARTv1 clients, using `patient/Observation.*` (or `.write`)
            * Works with SMARTv2, using IG-specified `patient/Observation.crs` (or further restricted per https://hackmd.io/@argonaut/SkGWnfQdn#Scopes-for-patient-facing-apps)
                * OK if we don't validate PKCE
            * Instead of users, login allows for selecting a patient or practitioner
        * Restrict read and write based on scopes
        * Host at: `vitals-server.ri.argo.run`
        * Include directions for local run (GH readme)
        * Allow apps to test error conditions like "can only write one blood pressure per ___ time per patient"
        * Walkthrough tour
            * Client perspective
            * Include creating a new patient ("clone" a sample patient)
    * P3: (0.5): feature set: 
        * Include 'practitioner view' into written vitals
        * Check auth tokens
        * Additions to SMART access
            * Works with SMARTv2 clients, using `patient/Observation.u` (or further restricted per https://hackmd.io/@argonaut/SkGWnfQdn#Scopes-for-patient-facing-apps)
    * P5: (0.5): feature set:
        * Allow/deny the requested scopes
        * Explicit client app registration
        * Internal Provenance generation
        * External Provenance handling

* P2: (0.0): Subscription RI include client-oriented page to allow testing of other Subscription servers.

## FHIR Subscriptions meet use case needs and are implementable (GC)

### Add required features to cover TA Notified Pull use case
* P0: (1.0): Design mechanism for sending authorization information with subscription notifications
* P0: (0.6): Add support for sending authorization information with subscription notifications
  * P0: (1.0): Backport for FHIR R4/R4B
  * P5: (0.5): FHIR R5
  * P1: (0.5): FHIR R6
* P0: (0.6): Design mechanism for sending 'pull' (query/request) information with notifications
  * P0: (1.0): Backport for FHIR R4/R4B
  * P5: (0.5): FHIR R5
  * P1: (0.5): FHIR R6

## FHIR Specifications Improve Across Releases

### Subscriptions Framework
* P0: (1.0): Apply all outstanding TC tickets to backport IG
* P0: (0.5): Add mechanism for tagging notification events by FHIR interaction/event 
    * e.g., differentiate between a create and update in a topic that allows both
    * e.g., different events in a topic with more than one event trigger
    * e.g., define a topic with several triggers on the same resource and be able to tell them apart
* P0: (1.0): Define operation to *resend*/*replay* notifications (instead of just accessing them)
* P0: (1.0): Ballot Subscriptions backport IG in January cycle
* P2: (0.0): Ballot (for comment) FHIR R6 changes in January cycle
* P5: (1.0): Determine path for maintaining feature parity in FHIR R5

### Prepare FHIR R6 content for comment ballot
* P0: (1.0): Ensure submitted search and http page tickets are voted on.
* P0: (1.0): Apply all search page tickets approved on or before November 27
* P0: (1.0): Apply all http page tickets approved on or before November 27
* P0: (1.0): Ensure new 'delete' functionality is documented
  * P0: (0.2): Reach out to at least 4 implementers to review draft content before content freeze (December 4)


# FHIR-Candle
* P1(GC) (1.0): Add support for IG-loading
    * Published packages
    * CI Builds
* P1(GC) (1.0): Complete at least two items from the 'high priority' queue
* P?(GC) (0.5) Extract `fhir-codegen`'s package resolution +  `~/.fhir`cache management into a library
    * Something similar exists  in Firely.Fhir.Packages (https://www.nuget.org/packages/Firely.Fhir.Packages)
    * If that's good enough, no need to do this task.
        * It does not handle CI builds (due to how simplifier works, they are not motivated to add that support)
    * Sort out MS Signing and Publishing requirements
    * Package as NuGet library for developer consumption
    * Package as dotnet tool for end-users
* P4(GC) (0.1): Add support for at least 50 of the remaining search-modifier-element type combinations (187 remaining)

----
##  Unplanned work done:
* BP FhirPath Spec migration & apply approved backlog! (which I guess could be in the prepare FHIR R6 content bucket)
* BP Enhance uploadfig (dependency processing)
* BP Enhance fhirpath-lab (questionnaires & co-pilot tweaks, java mapping engine, location navigator)
* GC `_lastUpdated` Argo project
* JM Deep dives on EHI, VCL
