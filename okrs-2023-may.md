## Argonaut Assessmentsn project offers clear guidance for SDOH

* P0-BP Example content covering
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
* P1 Project includes the Assessment *recipient* perspective, by use case
    * Clinical reporting / measurement tools
    * Jurisdictional health departments
    * Clinical research?
* P1 US Core provides clear guidance and a diagram distinguishing
    * data collection (e.g., recorded as Observations)
    * problems actively tracked (e.g., Conditions)

## SMART on FHIR v2.1 is available for implementation
* P0-JM Resolve remaining open issues from Ballot
* P1-JM Request for publication
* P1-JM Published

## Consumers can access imaging data via SMART on FHIR

### Imaging Access Spec
Define and document the scopes and endpoints for imaging access in SMART on FHIR authorization flow by Q1 2023

* P0-JM Publish a draft spec on GitHub
* P1-JM Present the spec and use cases and refine over >=3 3 project calls
* P2-JM Collect feedback from at least 2 EHR vendors
* P2-JM Collect feedback from at least least 2 PACS or imaging network vendors
* (After May) Incorporate feedback and finalize the spec

### Demo Environment
Develop and deploy a demo environment with a facade over PACS that supports imaging access

* P0-JM Design and implement a facade over PACS that supports imaging access
* P0-JM Develop a sample data set for demo environment
  *  including at least 3 patients
  *  including at least 3 imaging modalities
* P1-JM Deploy the facade over PACS on a cloud platform that is world-accessible
* P1-JM Integrate deployed facade with SMART App Launcher
* P1-JM Develop a "basic mechanics" demonstration app that can run against SMART App Launcher
* P4-JM Develop a more playful and open-ended demonstration app like "make a 3D print of my brain"
* (After May) Collect feedback from at least five end users who use the demo environment

### Community, Education and Dissemination

Educate and disseminate the imaging specs and best practices to potential users and developers through libraries, tools, or examples

* P0-JM Quick blurb outlining imaging project, inviting participation, including telecon details
     5min video recording of the Argonaut pitch to go along with it
* P1-JM Argonaut call participation includes diverse perspectives
    * EHR
    * PACS / VNA
    * Imaging Network
    * HL7 Imaging WG
    * Application developers
* P2-JM Create a reusable client-side library that supports imaging access
* P2-JM Publish a video showing how to use the openly-hosted demo environment
* P2-JM Publish a video showing how to use the library in a demo app
* (After May) Host a Birds of a Feather session at DevDays for June


### Evaluation

Evaluate the spec with components running in a provider’s staging environment 

* P2-JM Identify and recruit at least one provider organization that is willing to participate in the evaluation
* (After May) Integrate the demo environment with the provider’s EHR’s SMART API and verify interoperability
* (After May) Collect feedback from at least five end users who use the staging environment

## SMART Health Insurance Cards
Placeholder(drop in OKRs from Pool Party Gdoc)

## Topic-based subscriptions are testable

* P0-GC: Sandbox is deployed that supports at least one of R4, R4B, R5
* P0-GC: Sandbox supports arbitrary fhirpath-based topics
  * UI supports SubscriptionTopic.eventTrigger via a "trigger this event" button 
  * Anyone can POST a SubscriptionTopic and subscribe to it
  * Any fhirpath expression over current/previous works
  * Any query expression will work
* P1-GC: Sandbox supports basic filtering of subscription events
  * Any equality filter works
* P1-GC: Sandbox is deployed that supports all of R4, R4B, R5
    * Review of Firely's v5 SDK and multiversion/base versionless support?
* P2-GC: Sandbox supports advanced filtering of subscription events
  * Any filter for any search parameter (with simple fhirpath expression) works
  * remove dependency on external fhir-server
* P2-GC/BP: Subscriptions sandbox integrates with FhirPathLab
    * for subscription topic editing
    * subscription topic debugging
* P5-GC: Sandbox supports multi-tenancy to isolate users
* P5-GC: Sandbox supports IG loading for search parameters
  * new SearchParameters can be installed via POST 
  
## FHIR R5 is published and available for community use
* P1 FHIR QA issues are applied and publication is out
* BP: Short video on ____________
* P2-GC: Host an 'R5 Changes' session with internal folks

## FHIR Community has access to high quality open source libraries
* P0-BP/GC: Support Firely in v5 SDK publication
* P1-BP: FHIR Net API supports Firely v5 SDK 
* P0-GC: @types/fhir is updated with R5 models
* P0-BP: fhirpath.js supports R5 models
* P0-BP: Dotnet Facade Project supporting R5

## FHIR community continually improves our processess

* P1-BP/JM: Start a conversation about preventing accumulation of backlog between publications
* P1-BP/JM Propose a short time span and narrow quality focus for FHIR R6 (socialize this with FMG)
* P4-GC/?: Evaluate suitability of an existing open-source NPM registry server for FHIR's needs
  * Understand where/how FHIR uses NPM
  * Document current capabilities and any custom behaviors of FHIR's NPM registry sever
      * Firely's packages.fhir.org
      * Grahame's packages-2.fhir.org

### Patient Request for Corrections IG is on a path toward real-world EHR implementation
* P4-GC: Finalize "project scope" section of IG
* P4-GC: Clean up diagrams and section references
* P4-GC: Clarify what implementation choices are required vs allowed
