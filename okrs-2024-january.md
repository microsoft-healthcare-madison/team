## SMART Imaging Access is widely available for access (JM)

### Argonaut specification is finalized
* P0: Connectathon includes at least 2 PACS and at least 2 consumer app participants
* P0: connectathon lessons learned are incorporated into spec
* P2: Update `async` functionality to match https://hl7.org/fhir/async-bundle.html

### Initial implementers are on a path to deployment
* P0: Identify at least one real-world clinical organization to deploy imaging access
* P1: Establish deployment plan and support efforts with "high touch" engagement
* P4: Pre-production environment is ready for testing

##  SMART Patient Access Brands (JM)
* P0: Branding Extensions on track for Jan ballot of FHIR Extensions IG
* P1: PAB updated to use Branding Extensions
  * Profiles in PAB, extensions in Extensions IG
  * Examples updated
* P2: PAB on track for Jan ballot
* P5: Identify a champion for "Shorthand in FHIR Extensions IG" -- it should be easier to write and review content for the extension IG, and FSH would help!


##  Standards-based data serve as a foundation for clinical analytics (JM)

### SQL-on-FHIR v2 spec is widely implemented
* P2 Frozen draft spec
* P2 At least two implementations designed for use at scale
* P3 Internal participation
* P5 Typescript definition for ViewDefinition
* P5(BP) DSL concepts?

###  Digital quality measures are based on real-world EHR data (JM)
* Publish perspective highlighting use of real data to design lightweight measures
* Advocate for simplification of measures with ARPA-H leadership

##  Interop community understands and leverages LLMs where applicable (JM)

### "Future of interop" perspective is submitted for academic publication
* P0: Outline
* P1: Authors on board
* P2: Draft reviewed with comments
* P2: Draft submitted for publication

### Open source demos and examples are widely available
* P1(all) HACK WEEK
    * Scheduled time in early December
    * P1(all) Questionnaire-filling as a focus (end result is a QuestionnaireResponse)
* P5 Data format conversion from EHI exports?
* P5 Manual data abstraction with GPT-4?


## FHIRPath Lab Supports Cross-Implementation Testing
* P0(BP) Community-maintained test cases are up-to-date; broken content is eliminated from  https://github.com/FHIR/fhir-test-cases/pull/151 
* P0(BP) Library-wrapped test cases are updated with to the latest content
* P1(BP) fhirpath-lab extensibility is documented
    - Git Repo includes documentation explaining how other engines can be incorporated
    - Health Samurai team is aware
* P1(BP) FhirPath-lab subscription supports subscription topic editing
	- FhirPath-lab supports "Topic Editing", starting from new or existing topic
	    - Notification shape
	    - Filters
    - All fields of SubscriptionTopic can be created/edited, with basic schema validation in place
	- More complete support for editing triggers
        - `fhirpathCriteria` can be edited and validated
        - `fhirpathCriteria` can be evaluated against sample instances *(basically done)*
* P1(BP) FhirPath-lab subscription editor can be launched from fhir-candle
	- Launch from fhir-candle subscription topic window
	- Launch from fhir-candle test case window (with specific expression windows)
	- Launch includes `fhirserver` parameter to ensure correct server
* P5(BP) FhirPath-Lab co-pilot


## FHIR Questionnaires are robust and easy to use (BP)

### Educational material makes Questionnaires (including SDC pre-populated content) easy to adopt
* Introductory content for new users
* P0 Series of feature-focused videos including
    * Basic structuring simple questionnaires
    * Several pre-pop videos covering increasingly complex use cases
        * P0 Observation based
        * P0 fhirpath based
        * P2 StructureMap based
* P1 A standalone IPS pre-pop demonstration shows how to use SDC pre-population
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
* P2 QuestionnaireResponse validation merged into Firely SDK

##  FHIR community continually improves our processes (BP)
* P0 Keep PA backlog low - particularly changes applied
	- Core build to support new resources (again) - sent to GG in PR - done
	- VhDir STU1 published
    
## Open-source tooling makes FHIR easy to use (BP)

* P1 Upload-FIG is published as a MS open source project + Nuget package
  * Internal application submitted
  * Repository migrated
  * Internal build pipelines configured
  * Signing keys established
  * Automated publication to Nuget
* P1 MS FHIR Server POC materials shared with Server team (and my branch deployed - including the below features)
    * New Firely SDK 5.x parser
    * SDC Validation
    * SDC pre-pop
    * StructureMap/FML parser/serializer
    * StructureMap evaluator
    * fhirpath validation
    * current canonical processing
    * General feedback reviews
* P3 FHIR Canonical Resource Management Interface (CRMI) IG has independent reference implementation.
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
    - Update the SDK to better support leveraging the fhirpath symbol table for external usage
    - Leverage the enhanced symbol table in the fhirpath validator
    - Encourage if this validator can be adopted into the SDK
    - comments parsing integrated into SDK (complete/merge existing work)
    - Position information in fhirpath expression parsing - mostly complete
    - Include `CustomExpression` capability into the SDK - done, needs to be merged in
    - Brackets `()` to be able to be included in the expression tree (via the new CustomExpression) which then can enable round-tripping expressions to/from strings
    
* P1 Prepare `withVariable` proposal to add to fhirpath for consideration by HL7
    https://dev.fhirpath-lab.com/FhirPath?libaryId=7775d5cf3df540a38b34e83b27f8f284


## Open-source tooling makes FHIR easy to use (GC)

* P1: FHIR cache management tool is published with binaries
* P1: codegen is published with binaries
* P0: Complete a pass of FHIR Interface support from `fhir-codegen`
    * Background: Firely hand-maintains `IVersionableConformanceResource` interface by hand
    * P0: Expose .NET interfaces automatically through codegen, corresponding to FHIR's
        *  `CanonicalResource` 
        *  `MetadataResource` (sub-interface of `CanonicalResource`)
    * For later: Expose .NET interfaces for FHIR's patterns (Request, Event, Definition)
* P4: Improve the multi-version story of code-gen
    * Caller requests an export specifying multiple FHIR versions
    * Propose / sketch codgen interface with access to cross-version details, which can be used to determine and output things like diffs, since/not-mapped annotations
* P5: PoC NPM facade over CI Builds

## Support projects with Reference Implementations (GC)

* P0: fhir-candle supports SMART authorization
* P1: RI for vitals-write for Connectathon (Nov 15)
* P2: Subscription RI include client-focused page

## FHIR Subscriptions meet use case needs and are implementable (GC)

### Add required features to cover TA Notified Pull use case
* P0: Design mechanism for sending authorization information with subscription notifications
* P0: Add support for sending authorization information with subscription notifications
  * P0: Backport for FHIR R4/R4B
  * P3: FHIR R5
  * P1: FHIR R6
* P0: Design mechanism for sending 'pull' (query/request) information with notifications
  * P0: Backport for FHIR R4/R4B
  * P3: FHIR R5
  * P1: FHIR R6

## Improve and maintain FHIR Specifications

### Subscriptions Framework
* P0: Apply all outstanding TC tickets to backport IG
* P0: Add known 'quality of life' requests
* P0: Ballot Subscriptions backport IG in January cycle
* P2: Ballot (for comment) FHIR R6 changes in January cycle
* P3: Determine path for maintaining feature parity in FHIR R5

### Prepare FHIR R6 content for comment ballot
* P0: Apply all search page tickets approved on or before November 27
* P0: Expand examples for 'range' searches
* P0: Apply all http page tickets approved on or before November 27
* P0: Ensure new 'delete' functionality is documented
  * P0: Reach out to at least 4 implementers to review draft content before content freeze (December 4)

