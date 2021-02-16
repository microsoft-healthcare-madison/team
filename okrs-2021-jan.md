## OKRs for Jan 2021

We're following a planning schedule that mirrors the HL7 working group meeting schedule -- in four-month intervals ending in September, January, and May. 
 
## Argonaut Project: SMART v2 

* P0 (.8): SMART IG Draft ready for Argonaut Review prior to January Connectathon, suitable for January testing + May ballot.  

* P1 (.8): Reference server and client implementation for v2 IG (including granular scopes and token introspection) merged into SMART App Launcher repo 

* P2 (0): Conduct 1:1 design reviews with two EHR vendors and two cloud vendors 

* P3 (0): Automated testing tool for EHR implementations (e.g. standalone CLI, or features on top of Inferno) 

 

## Argonaut Projects: Bulk Data 

* P0 (1.0): Wrap up Bulk Data 1.5 IG 

* P1 (0.5): Work with at least two certified EHRs for testing and support 

* P2 (0.7): Ensure the bulk data test suite covers new features 
 

## Argonaut Projects: Patient Lists  

* P0: Patient Lists IG Draft ready for Argonaut Review prior to January Connectathon, suitable for January testing 

* P1: Demo data collection representing full feature set of Patient Lists API  

   * Represent a "full experience" from a clinician's perspective – point in time snapshot. 

   * Synthea data loader released in a separate repo. 

* P1: Demo application exercises full feature set for Patient Lists API.  Demo App / Sandbox enhancements 

  * App deployment process includes at least one unit and at least one integration test. 

  * Developer panel provides data validation and API statistics. 

* P1: Determine scope / level of effort to add Synthea functionality  

  * that can generate Patient Lists data (populated groups of all types) 

  * evaluate improvements to Synthea suitable for fast / direct loading without duplicate providers, etc. 


* P2: Codelab complete and published, teaching developers how to implement all data flows for the demo app


## Argonaut Projects: SMART Web Messaging 

* P0: All ballot comments are triaged. 

* P0: Proposed dispositions for any spec edits are tied to GitHub pull requests. 

* P0: Shepherd proposals through FHIR-I 

* P2: SMART core JS library is augmented to support Web Messaging. 

* P3: Standalone test tool demonstrates API support.  

* P3: SMART app launcher supports at least one Web Messaging feature (e.g., app close) 

 

## Subscriptions in R4 + R5 

* P0: Subscriptions R5 is "ready to ballot at any time" 

   * Apply feedback from September 2020 Connectathon 

   * Complete documentation TODOs on existing areas of the spec including error discovery and recovery 

   * Update resources to FMM 2/3 and ensure build passes. 

* P1: Define an approach to requesting Graphs when creating a FHIR Subscription 

* P1: Host a deep-dive discussion with (at least) Carequality and two EHR vendors determine whether a new channel type is required to meet CMS encounter notification requirements 

* P1: Subscriptions "R4 Back-port IG" ballots in the January ballot cycle (ballot opens Dec 11) 

* P3: Add support for 'error' scenarios to subscriptions.argo.run system. 

  * Missing event / out-of-order delivery. 

  * Sending error state to client. 

* P1: Maintain the Argonaut Encounters IG with changes from the specifications. 

* P0: Presentation, demos, and Let's Build content ready for DevDays 

   * P3: Consider Push Notification routing for inclusion in DevDays demo 

 

## SMART Health Cards Framework 

* P1 (0.7): Freeze dependencies and publish a "1.0" implementation guide  

* P2 (0.7): Creates a plan with The Commons Project to pilot the IG with at least one US-based lab  

* P2 (1.0): Report feedback from early implementation to the DID SIOP and Sidetree projects in Identity Foundation 

* P3 (0.8): Identify gaps with MS Authenticator features and report feedback to internal teams 

 

## Expand the capabilities of fhir-codegen 

* P1 Define parsing and serialization benchmarks to compare existing approaches, including latency to first pass + warmed-up throughput. 

* P1 Improve time to first pass by 3x and improve throughput by __x without breaking API compatibility by leveraging System.Text.Json (vs NewtonSoft) for serialization and parsing.  

* P2 Codegen library is published in Nuget  

* P3 Add support for parsing profiles. 

* P3 Build OpenAPI docs compliant with 'official' FHIR build. 

    * Add to 'generated' for compatibility checking. 

    * Talk with MS PowerApps Custom Connector team 

* P4 Add API server and UI. 

* P4 Add support for loading from a local build (output) folder (depends on changes to FHIR core infrastructure in the R4b refactor) 

 

## Internal MS team connections 

* P1: Conduct FHIR office hours once in the month of December, open for questions and advertised through internal Teams channels 

* P2: Introduce the idea of a FHIR/SMART review and/or test process.  Some way for people doing work in the space to determine if what they are doing is 'ok'. 

* P3: Decide on a feature to prototype in MS FHIR Server 

 

## External community development 

* P1 Gino to Record a "Friday Afternoons" video series on intro topics for FHIR videos. E.g. for specific languages provide an overview of how to connect to a server or issue queries. Focus on the security + data connectivity >> UI. 

* P1 (1.0): Josh in October to solicit topics on #implementers + #social for a series of "Guided walk through the FHIR spec" livestreams 

* P2 (0.6): Josh by November to select one topic and run a "Guided walk through the FHIR spec" livestream 

* P2 Carl to record a Codelab working session (virtual session walking developers through the first part of the PL / PAMA codelab)? 

 

## Other ideas not captured in OKRs  

### FHIR Tooling 

* SMART proxy 'package' 

  * Server deployment to act as web-proxy. 

  * SMART on FHIR Client packages for languages that need them (C#:Nuget, Java?:Jar?). 

? Infrastrucutre, k8s deployment, dev ops to document publicly? 

 
