# Sept 2021 OKRs (HL7 WGM Sept 20-24)

## HL7-published SMART standards improve every year based on community feedback

### SMART Web Messaging V1 is published
* P0 Remaining ballot (and post-ballot) issues are resolved and applied
    * includes support for scratchpad query / read
* P0 Demo app and library support the full Web Messaging spec
* P0 Publication requested through HL7
* P1 Migrate the client [library portion of the current repo](https://github.com/barabo/swm-dd-demo/tree/main/lib) into [microsoft-healthcare-madison](https://github.com/microsoft-healthcare-madison) (or smart-on-fhir, if possible)

### Bulk Data V2 is ready for publication
* P0 All ballot comments triaged
* P1 Dedicated telecon session is scheduled (or joint with App Launch) for all ballot comments requiring "in-person" discussion
* P1 All ballot comments have proposed resolutions
* P1 All ballot comments that can be block-voted are block-voted
* P2 All ballot comments requiring in-perseon discussion are discussed and voted
* P2 All decisions are applied in GitHub
* P2 Publication requested through HL7

### SMART App Launch V2 is ready for publication
* P0 All ballot comments triaged
* P1 Dedicated telecon session (or joint with Bulk) is scheduled for all ballot comments requiring "in-person" discussion
* P2 All ballot comments have proposed resolutions
* P2 All ballot comments that can be block-voted are block-voted
* P2 All ballot comments requiring in-person discussion are discussed and voted
* P3 All decisions are applied in GitHub
* P3 Publication requested through HL7

## Subscriptions are scalable and flexible
* P0 Design / decide on a mechanism for including additional resources
* P0 Design / decide on a mechanism for creating event-based subscription topics
* P1 Document updated security guidelines for REST notifications
    * P1 Review SMART backend services auth
    * P1 Evaluate if additional elements are required to support auth
* P5 Additional tooling for implementer support
* P5 Prototype implementation of encrypted rest hook (e.g., by comparison with India's HealthStack)

### Subscription Backport IG is ready for publication
* P0 All January ballot comments applied
* P0 Document and model mechanism for additional resources
* P0 Document and model mechanism for event-based subscription topics
* P0 Add new resources to R4B (SubscriptionTopic and SubscriptionStatus)
* P0 All approved tickets applied by end of August (included in connectathon snapshots)
* P0 Run connectathon track to get 'last chance' feedback prior to IG publication
* P1 Update RI prior to connectathon for testing
* P2 Perform 1:1 content reviews with at least 2 implmenenters (not present on Argo calls, include both cloud and dedicated EHR vendors)

### Subscription R5 Content is ready for publication
* P0 Block-vote all open tickets that match R4 backport changes
* P0 Apply all tickets to match updates from backport feedback
* P0 Document and model mechanism for additional resources
* P0 Document and model mechanism for event-based subscription topics
* P1 All approved tickets applied by end of August (included in connectathon snapshots)
* P2 Include in connectathon track for testing
* P3 Update RI prior to connectathon for testing
    * P5 Implement CapabilityStatement2

## Standards Incubation and Acceleration projects expand interoperability

### SMART Health Cards are widely available to consumers
* P0 Consumer landing page is finalized including translations in at least English, Spanish, and French
* P1 New issuers are subscribed to Zulip chat and bring questions to the community (at least three new issuers)
* P1 Issuers that are healthcare providers or pharmacies offer Immunization records for at least one vaccine type beyond COVID-19 (e.g., childhood vaccines or travel vaccines)
* P3 HL7 PSS submitted for SMART Health Cards "Framework IG"
    * Joint copyright agreement in place with HL7 

### SMART Scheduling Links are widely available to consumers
* P1 New pharmacies or healthcare providers are subscribed to Zulip chat and bring questions to the community (at least three new organizations)
* P1 Publishers begin to publish "granular appointment" data including specific
    * P1 product information for COVID-19 vaccines
    * P2 appointment times (rather than just dates)
* P2 Publishers begin to publish appointments for vaccines other than COVID-19

## Expand and engage the FHIR Community (including inside of Microsoft)

### Microsoft-internal teams review and provide HL7 ballot feedback
* P0 Work with product team to identify a broad pool of at least five voting members
* P0 Coordinate voting members (e.g., internal mailing list) prior to ballot registration (end of July), identifying at least one spec (and not more than three!) for each voting member to review
* P1 Check in with voting members at least one week before ballot closes
* P1 Check in with at least 2 orgs/teams for visibility

### Developers, students, and others learn FHIR through openly published content

* P1 Solicit community topic suggestions in #social and with pointers to [Team Project Board](https://github.com/microsoft-healthcare-madison/team/projects/1)
* P2 At least six new videos in Josh's "Guided Walk through FHIR" series
* P3 Start a "Welcome to SMART App Launch V2" video series
  * P2 Explanation of granular scopes, including demo queries
  * P2 Explanation of PKCE, including demo
  * P2 Explanation of token introspection, including demo
  * P4 Explanation of asymmetric client authentication in SMART App Launch

* P1 At least 10 new videos in Gino's "FHIR for Developer Series"
    * ?P?2 Begin including TypeScript content (at least 2 videos)

## Advanced tooling addresses unmet community needs (e.g., library support, ergonomics, performance)

* P1 SMART App Launcher has merged support for all SMARTv2 features
    * P1 including UI and documentation for registering clients with asymmetric keys
    * P2 including a mode for enforcing granular scopes (*only* allowing queries that ~directly match a granted scope, without enabling `_include`, `_has`, or other "advanced" features)

### C#
* P0 Design / implement 'pluggable' serializer interfaces / factories to Firely
    * P0 Published in NuGet (Firely Net API)
* P0 System.Tex.JSON serializer/parser
    * P0 Published in NuGet (Firely Net API)
    * P1 Add option to either throw or 'do what you can' and return an OperationOutcome
    * P5 Add support for `_summary`
    * P5 Add support for `_elements`
* P1 Discuss / design / evaluate updated target model definitions (e.g., IDictionary)
* P2 Create tooling to better support use of IGs and Extensions
    * e.g., classes with ergonomic support for (complex) extensions defined in IG
* P5 Design and implement a process for non-terminology validation (e.g., Fluent Validation)
    * P5 Support IG model validation
* P5 Create a streaming JSON 'modification' transcoder (add/remove/modify elements in single pass)

### Python
* P1 1 week sprint - evaluate the current state of the [smart-on-fhir python client](https://docs.smarthealthit.org/client-py/index.html)
* P2? fork that only supports Python3

---

# Future scope / Ideas Scratchpad

* SMART Proxy (simplify SMART workflow from desktop apps)
* Generic FHIR UI / browser (from code-gen?)

### Argonaut provides specifications for individual level "Full EHI Export" API
* P0 A telecon series of at least three calls is scheduled
* P0 In telecon calls, review "default" vendor plans
 * UX and/or APIs for consumer
 * Expected data formats
 * Expected export size ranges (e.g., 99th percentile export size might be ... ?)
 * Expected workflow for moving data (e.g., something allowing resume/recover?)
* P1 Draft an API definition as a thin wrapper supporting diverse vendor plans

### CARIN / Consumer Access to Imaging

### TypeScript
* Design 'library' style FHIR models (coordinate with community)
    * P4 Extension handling (primitive and complex types)
    * P5 Runtime validation (non-terminology) / schema-based

### OpenAPI
* Support definitions that are useful for tools such as ReDoc
