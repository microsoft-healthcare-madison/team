# OKR Scratchpad

# Sept 2021 OKRs (HL7 WGM Sept 20-24)

## HL7-published SMART standards improve every year based on community feedback

### (0.25) SMART Web Messaging V1 is published
* P0 (0.6) Remaining ballot (and post-ballot) issues are resolved and applied
    * includes support for scratchpad query / read
* P0 (0.5) Demo app and library support the full Web Messaging spec
* P0 (0.0) Publication requested through HL7
* P1 (0.0) Migrate the client [library portion of the current repo](https://github.com/barabo/swm-dd-demo/tree/main/lib) into [microsoft-healthcare-madison](https://github.com/microsoft-healthcare-madison) (or smart-on-fhir, if possible)

### Bulk Data V2 is ready for publication
* P0 (1.0) All ballot comments triaged
* P1 (1.0) Dedicated telecon session is scheduled (or joint with App Launch) for all ballot comments requiring "in-person" discussion
* P1 (1.0) All ballot comments have proposed resolutions
* P1 (1.0) All ballot comments that can be block-voted are block-voted
* P2 (1.0) All ballot comments requiring in-perseon discussion are discussed and voted
* P2 (1.0) All decisions are applied in GitHub
* P2 (0.8) Publication requested through HL7

### SMART App Launch V2 is ready for publication
* P0 (1.0) All ballot comments triaged
* P1 (1.0) Dedicated telecon session (or joint with Bulk) is scheduled for all ballot comments requiring "in-person" discussion
* P2 (1.0) All ballot comments have proposed resolutions
* P2 (1.0) All ballot comments that can be block-voted are block-voted
* P2 (1.0) All ballot comments requiring in-person discussion are discussed and voted
* P3 (1.0) All decisions are applied in GitHub
* P3 (0.8) Publication requested through HL7

## Subscriptions are scalable and flexible
* P0 (1.0) Design / decide on a mechanism for including additional resources
* P0 (1.0) Design / decide on a mechanism for creating event-based subscription topics
* P1 (0.8) Document updated security guidelines for REST notifications
    * P1 (1.0) Review SMART backend services auth
    * P1 (1.0) Evaluate if additional elements are required to support auth
* P5 (0.8) Additional tooling for implementer support
* P5 (0.0) Prototype implementation of encrypted rest hook (e.g., by comparison with India's HealthStack)

### Subscription Backport IG is ready for publication
* P0 (0.8; websocket subprotocol still TBD) All January ballot comments applied
* P0 (1.0) Document and model mechanism for additional resources
* P0 (1.0) Document and model mechanism for event-based subscription topics
* P0 (0.9; still need to incorporate `SubscriptionTopic.notificationShape.revInclude`) Add new resources to R4B (SubscriptionTopic and SubscriptionStatus)
* P0 (1.0; some newer tickets still TODO) All approved tickets applied by end of August (included in connectathon snapshots)
* P0 (1.0) Run connectathon track to get 'last chance' feedback prior to IG publication
* P1 (1.0) Update RI prior to connectathon for testing
* P2 (0.5) Perform 1:1 content reviews with at least 2 implmenenters (not present on Argo calls, include both cloud and dedicated EHR vendors)

### Subscription R5 Content is ready for publication
* P0 (0.0; decided to prioritize design and backport over R5) Block-vote all open tickets that match R4 backport changes
* P0 (0.0) Apply all tickets to match updates from backport feedback
* P0 (0.0) Document and model mechanism for additional resources
* P0 (0.0) Document and model mechanism for event-based subscription topics
* P1 (0.0) All approved tickets applied by end of August (included in connectathon snapshots)
* P2 (1.0) Include in connectathon track for testing
* P3 (1.0) Update RI prior to connectathon for testing
    * P5 (0.0; but CS2 is no longer part of R5) Implement CapabilityStatement2

## Standards Incubation and Acceleration projects expand interoperability

### SMART Health Cards are widely available to consumers
* P0 (1.0) Consumer landing page is finalized including translations in at least English, Spanish, and French
* P1 (1.0) New issuers are subscribed to Zulip chat and bring questions to the community (at least three new issuers)
* P1 (0.4; discussions but no deployment) Issuers that are healthcare providers or pharmacies offer Immunization records for at least one vaccine type beyond COVID-19 (e.g., childhood vaccines or travel vaccines)
* P3 (0.0) HL7 PSS submitted for SMART Health Cards "Framework IG"
    * Joint copyright agreement in place with HL7 

### SMART Scheduling Links are widely available to consumers
* P1 (1.0) New pharmacies or healthcare providers are subscribed to Zulip chat and bring questions to the community (at least three new organizations)
* P1 (0.3; discussion only) Publishers begin to publish "granular appointment" data including specific
    * P1 product information for COVID-19 vaccines
    * P2 appointment times (rather than just dates)
* P2 (0.0; brief discussion of flu) Publishers begin to publish appointments for vaccines other than COVID-19

## Expand and engage the FHIR Community (including inside of Microsoft)

### Microsoft-internal teams review and provide HL7 ballot feedback
* P0 (0.4) Work with product team to identify a broad pool of at least five voting members
* P0 (0.4) Coordinate voting members (e.g., internal mailing list) prior to ballot registration (end of July), identifying at least one spec (and not more than three!) for each voting member to review
* P1 (1.0) Check in with voting members at least one week before ballot closes
* P1 (0.5) Check in with at least 2 orgs/teams for visibility

### Developers, students, and others learn FHIR through openly published content

* P1 (0.4; took suggestions from #implementers discussion) Solicit community topic suggestions in #social and with pointers to [Team Project Board](https://github.com/microsoft-healthcare-madison/team/projects/1)
* P2 (1.0) At least six new videos in Josh's "Guided Walk through FHIR" series
* P3 (0.0) Start a "Welcome to SMART App Launch V2" video series
  * P2 Explanation of granular scopes, including demo queries
  * P2 Explanation of PKCE, including demo
  * P2 Explanation of token introspection, including demo
  * P4 Explanation of asymmetric client authentication in SMART App Launch

* P1 (1.0) At least 10 new videos in Gino's "FHIR for Developer Series"
    * ?P?2 (0.0) Begin including TypeScript content (at least 2 videos)

## Advanced tooling addresses unmet community needs (e.g., library support, ergonomics, performance)

* P1 (0.3) SMART App Launcher has merged support for all SMARTv2 features
    * P1 (0.7; PR in place sans backend services) including UI and documentation for registering clients with asymmetric keys
    * P2 (0.3; some support but enforcement is all-or-nothing, doesn't yet support _include) including a mode for enforcing granular scopes (*only* allowing queries that ~directly match a granted scope, without enabling `_include`, `_has`, or other "advanced" features)

### C#
* P0 (0.2) Design / implement 'pluggable' serializer interfaces / factories to Firely
    * P0 (0.0) Published in NuGet (Firely Net API)
* P0 (0.6) System.Tex.JSON serializer/parser
    * P0 (0.0) Published in NuGet (Firely Net API)
    * P1 (0.4) Add option to either throw or 'do what you can' and return an OperationOutcome
    * P5 (?) Add support for `_summary`
    * P5 (?) Add support for `_elements`
* P1 (1.0) Discuss / design / evaluate updated target model definitions (e.g., IDictionary)
* P2 (0.2) Create tooling to better support use of IGs and Extensions
    * e.g., classes with ergonomic support for (complex) extensions defined in IG
* P5 (0.4) Design and implement a process for non-terminology validation (e.g., Fluent Validation)
    * P5 Support IG model validation
* P5 (0.0) Create a streaming JSON 'modification' transcoder (add/remove/modify elements in single pass)

### Python
* P1 (0.1) 1 week sprint - evaluate the current state of the [smart-on-fhir python client](https://docs.smarthealthit.org/client-py/index.html)
* P2? (0.0) fork that only supports Python3


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

---

# Other things we spent time on but didn't plan...

* Core FHIR spec / usability
* Da Vinci coordination?
* FAST coordination?
* FHIRCast coordination?
