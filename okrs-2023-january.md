# OKRs for Oct 2022 - Jan 2023

## Argonaut convenes and drives consensus on high-impact interop projects

### Patient Access Branding information is available for certified EHR endpoints
* P0-JM (0.8): Document current implementation support based on EHRs listed in CHLP
* P2-JM (0.0): Meet with EHRs to determine value of editing tools or auto-suggestions to bootstrap publication of branding information
* (Also: IG content incorporated into SMART branch; connectathon late March)

### SMART App State is available for real-world apps
* P0-JM (1.0): Merge "Persisting App State" functionality into SMART App Launch
* P0-JM (1.0): Reach a go/no-go decision about including App State in STU2.1 update (choices: do not include in 2.1; include in 2.1 as a balloted update; include in 2.1)
* (Also: Resolved all the ballot comments)

### Consumers can access and share health data with standardized links (SMART Health Links)
* P0-JM (0.8): Participation in Argonaut workgroup includes diverse perspectives from public health, state immunization registry software, and insurance providers
* P0-JM (1.0): SHL testing and validation tools are openly available to the community
* P1-JM (0.7): Specification stablilized at "1.0 RC" stage (ready to commit to backward compatibility)
* P1-JM (1.0): Focused discussions with 2 immunization registries or registry vendors to document deployment plans
* P1-JM (0.0): Ask for presentation slot on a monthly Da Vinci call to present background on SHL and a digital insurance card use case. Invite CARIN and Argonaut members to join.

### Social needs screening results are shared across software systems
* P0-JM (0.6): Conduct interviews with at least five EHR and social needs platform vendors to document current capabilities
* P1-JM (1.0): Current-state platform capabilities are documented publicly on HL7 wiki
* P0-JM (1.0): Conduct interviews with at least two health systems to document current use of screening tools
* P1-JM (1.0): Current-state usage is documented publicly on HL7 wiki
* P2-JM/BP (0.1): Example responses for 2 LOINC-coded surveys in QR and Observation format, consistent with latest US Core specs
* P3-JM (N/A -- rolled into Assessments Sprint): Propose Argonaut project for 2023 to enhance US Core for social needs submissions
* P3-BP (0 -- but may come up in Assessments Sprint): Discuss with EHR vendors the opportunity to configure their sandbox env (or a customer's sandbox env) to test existing capabilities

### Patient Request for Corrections use case is on a path toward real-world EHR implementation
* P2-GC (0.5): Small-group discussion on feasibility / scoping
* P2-GC (0.5 -- now "choose your own adventure"): Propose scope (perhaps narrower than current PE IG) / changes
* P2-GC (1.0): Submit as Argo23 project proposal

## The FHIR specs are clear, concise, correct, and new-user friendly
* Canonical functionality is consistently supported in generic FHIR servers
    * P0-BP (1.0): `$current-canonical` operation applied to the R5 specification (approved HL7 change)
    * P0-BP (1.0): `$current-canonical` operation is implemented in .net and available in reference implementation(s)
    * P2-BP (0.5 -- written but not contributed): contribute unit tests to the [core test packages](https://github.com/FHIR/fhir-test-cases) for the f`$current-canonical`
    * P0-BP: Blog posts discussing:
        * (1.0) usage for registries (pretty well covered)
        * (0.5 -- written, awaiting feedback) usage for health institutions (basically not covered at all)

* P1-GC (0.2): Standard reverse proxy headers from https://www.rfc-editor.org/rfc/rfc7239#section-5 are documented in FHIR's http.html
* P2-JM/GC/BP (1.0 -- this wound up being a much bigger lift, very long tail of unapplied issues, often duplicative or contradictory): FHIR R5 Ballot comments are addressed for areas of the spec that we maintain

## Topic-based subscriptions are testable
* P0-GC (0.5 -- WIP on new server, unreleased): Subscriptions sandbox supports more SubscriptionTopics
  * "button push event" topic
  * arbitrary fhirpath-based topics 
* P2-GC (0.0 -- .NET build works locally, but nothing new): Subscriptions sandbox has a local-deployment story (e.g., Docker image)
* P2-GC/BP (0.25 -- ability to test SubscriptionTopic expressions in Lab): Subscriptions sandbox integrates with FhirPathLab for subscription topic editing
* P5-BP/GC (0.5 -- WIP on new server): In memory only fhir-server for testing (cache policy?)

## Open source tools and libraries make it easy to work with FHIR and related IGs

### FHIRPath is easy to learn, debug, and use
* P1-BP (0.1 -- current integration status documented): FHIRPath Lab supports an "Edit this expression" mode where:
  * inputs: sample data / context (if any), starting expression (possibly blank), caller name
  * outputs: button like `Return to ${caller}` with the edited expression --> window.opener.postMessage()
  * document the "API" for integrating the edit/debug fhirpath window *experimental
* P3-BP (1.0): Discuss with Firely if using this tighter integration with Simplifier would be practical/useful
* P1-BP (0.1 -- some infrastructure work): Prepare a foundation for a library of fhirpath expressions
  * Announce the creation of an openly licensed fhirpath library
  * Develop initial content using the FHIR Library resource
  * Allow users to create/contribute to the library content (simplify sharing/managing content)
  * Provide an easy way to open any branch/fork of the library in the editor
* P3-BP (0.7): Contributions to open source `fhirpath.js` to support accessing the **path** of the returned values where available (facilitates diagnosing where content came from)
* P5-BP (0.0): Enhanced fhirpath expression debugging/visualizing features (e.g., AST summarization / viz, to show explanations or warnings about behaviors)

### Changes between versions of specification publications are easy to discover
* P0-GC (0.1): Technical implementers can access diff tooling to compare the contents of package versions, without having to compile code
* P1-GC (1.0): Change detection covers all definitional resource types (e.g., canonical resources)
* P1-GC (0.0): The Diff-tooling is well-documented
    * Documentation Site
    * Video walkthrough/tutorial

### Technical implementers have access to specification-based tooling
* P0-GC (0.25 -- docs updated for current capabilities, but users still need to compile): Technical implementers can access code-generation tooling, without having to compile code
    * Documentation Site
    * Video walkthrough/tutorial
* P0-GC (1.0): OpenAPI supports:
  * Azure API Management
  * Swagger definitions in aspnet (for developer documentation and testing)
  * CapabilityStatement conformance-expectations
* P1-GC (0.4 -- internal session; no public content): Setup and record show & tell for OpenAPI
* P3-GC (0.2 -- some infrastructure): Web-UI can show/display/download exports
* PX-BP (1.0 loader tool + repo): Server support for loading IGs, followed up with Firely

### FHIR community has a shared long-term versioning strategy
* P1-BP/GC (0.0): Published educational content (youtube/blog) series evaluating options, including discussion of:
    * Up/down converting using FHIR Mapping language and other techniques
    * GC/BP impact on server implementers
    * impact on client implementers
    * impact on health institutions (pure FHIR vs. facade)
    * Later...
        * Presentation to ... FMG? FHIR-I?
        * POC implementations of some of the approaches
        * Impact on toolchains/software packages/packaging

### .NET (Firely) SDK
* Firely SDK incorporates SDC Functionality (Hl7.Fhir.StructuredDataCapture)
    * SDC Validator
        * P1-BP (0.0): Work is underway to merge component into Firely SDK (R4/R4B)
        * P4-BP (0.0): Decide with Firely on approach to R5 implementation
    * SDC Extrator
        * P1-BP (0.0): Include/Enhance the QuestionnaireResponse SDC $extract functionality to also cover Definition as well as Observation functionality (supporting future use in SDOH based implementations - social needs screenings)
* Simplify usage of Implementation Guides for SDK developers
    * P5-BP/GC (0.1 -- some upstream work on core spec): Create tooling for IG-based NuGet packages to support easier adoption  (e.g., codegen to provide accessors for extensions)
* P1-GC (0.0): Building internal Firely models is a separate step during export, within the Firely `ILanguage` implementation
* P0-BP/GC (1.0 from Jan connectathon snapshot + R5 candidate): Each time FHIR publishes a new shapshot or ballot candidate, we run codegen, validate results, repair bugs, and notify Firely that it is ready for packaging/release

## Our team consistently advocates for patient access rights
* P0-JM (1.0): Published set of principles for patient access under TEFCA
* Blog or "op-ed" on the case for consumer access in healthcare
    * P2-JM (0.1): Draft and shared internally
    * P3-JM (0.0): Published

## Team Communication
* P1-GC (0.9): Create or piggyback on some "FHIR Friends" Team, inviting relevant folk
  * 30+ participants
  * 3+ teams
* P1-JM/GC/BP (1.0 -- two sessions including Argonaut review): coordinate cross-team show-and-tell or Q&A on "hot topics"

---

Also spent time on: team hack week, OpenAI integration examples
