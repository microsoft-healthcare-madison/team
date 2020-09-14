# OKRs for May 2020

*(Scoring note: COVID! We wound up putting significant effort into projects not planned in the previous cycle, including SANER + SMART Health Cards framework. For many of our "not completed" tasks, these are things we'll want to carry forward, +/- adjustment for virtual rather than in-person meetings.)*


## Objective: Subscriptions spec + reference implementation are feature complete and ready for testing at Connectathon (i.e., something we believe is ready, even if the community process introduces further changes)
* P0: 1.0: Design in place and communicated to FHIR-I that addresses all known feedback (March 15)
* P0: 0.8 (gaps were for low-maturity channels): Merge current pass of models and documentation in time for May Connectathon (March 31 ;-)
    * Resources include Bundle, Subscription, SubscriptionTopic, SubscriptionStatus
    * Channels include rest-hook, websocket, email, messaging
* P1: (0.9m; no support for messaging channel): Update reference implementation prior to May Connectathon (May 1), supporting
    * All channel types (current channels + new support for messaging channel)
    * SubscriptionTopics for `encounter-start` and `encounter-end`
* P2: (0 -- still FAQs on spec level to address how this works): Extra features for reference implementation
    * Missing event workflow testing
    * Simulation of error states (e.g., messages not sent; messages delayed)
* P0: (1.0 as of April; new ones now) Complete all "Resolved, Changed Required" Jira issues (April 1?)
    * (Some are already done and just need to be marked as such)
* P0: (1.0 as of April; new ones now): Triage all "Triaged" and "Waiting for inputs" Subscription-related Jira issues (April 1?)
* P0: (1.0 - FHIR-I incorporated these): Create required Jira issues (e.g., for creation of SubscriptionTopic)
* P0: (1.0 - addressed in-band on FHIR-I):Schedule an ad-hoc FHIR-I call for Subscription issues (early April?)


## Objective: SMART Web Messaging is a formally published specification
* P0 (0.4 -- missed May but included in Sept, no/low participation): Track definition submitted for May connectathon (deadline late March/early April), either standalone or piggybacking on CDS Hooks
* P0: 0: Tested at May connectathon
* P0: 1.0: NIB completed and approved in time for September ballot cycle (~ mid June, given holidays etc. [Calendar here](https://confluence.hl7.org/display/HL7/HL7+Calendars#a024f57c-d5fc-4f39-8b26-bf9f1e280100-35717170))
* P1: 1.0: FHIR Implementation Guide is published on "CI Server"
* P0: 1.0: FHIR Implementation Guide snapshot is ready for ballot
* P1: 0: Testing harness in place that performs the EHR side of the SMW interaction, maybe built on top of SMART App Launcher; maybe standalone. (Ready by May 1)
    * Includes support for authentication protocol (haven't had any implementation of this pre-2020)
* P1: 0: Developers Guide / codelab describing how to use the test harness


## Objective: Lead the launch of Argo 2020 "Granular Permissions" Project
* P0: 0.8: Establish an open community process to ensure that meeting schedules, meeting notes, and Zulip discussions are discoverable from Argonaut project homepage
* P0: 0.75 (TBD still are chaining & operations, but *could* omit if needed): Define goals and non-goals for granular permissions, with group-wide consensus
* P0: 0.6: Draft updates to SMART scope language to satisfy goals, and document these in a draft "SMART v2" IG, starting from the existing SMART IG repository
* P2: (0.2 -- discustions but not formal review): Conduct design review with at least two cloud technology providers to ensure a path toward real-world implementation
* P2: (0.5 -- got feedback from two vendors, but didn't run one-on-one review sessions): Conduct design review with at least two EHR technology providers to ensure a path toward real-world implementation
* P3: (0.75 -- core features in SMART app launcher) Build reference implementation. Probably build into an open-source FHIR server (e.g., HAPI or Microsoft FHIR Server), but also see what can be done in a proxy or gateway


## Objective: Support the launch of Argo 2020 "Bulk Data $export" Project
* P0: 0.8: Launch project using the open community process described above
* P0: 0.9: Define goals and non-goals for incremental updates to Bulk Data $export
* P1: 0.7 (impl is keeping in sync, but no formal process around it): Work with team at Boston Children's Hospital CHIP to ensure reference servers are up-to-date as specification evolves
* P1: 1.0: Schedule a May WGM Connectathon track and advertise participation to key stakeholders including at least two server developers and at least two client developers


## Objective: Support the launch of Argo 2020 "Patient Lists" Project
* P0: 0.8: Launch project using the open community process described above
* P1: 0.6 (small data set in place; need clearer mapping to use cases): Support draft specification development with a set of sample data in bundles, suitable for loading into any FHIR server. Bundles should include pre-defined lists for each use case identified in the project goals (e.g., "which patients is Provider X responsible for today?", "Which patients are in Location Y right now?", or possibly "Which patients are in Cohort Z?"), and each resource should be tagged to facilitate updates or resets
* P1: 0.4 (some scripts, not wired into automated updates): Support draft specification development by keeping a public server up-to-date, with scripts to bulk-replace our example data (e.g., in https://test.fhir.org)
* P1: 0.5 (demo app with some queries, not a standalone collection): Support draft specification development by publishing a list of queries that exercise the full scope of the draft specification (e.g., as a [Postman collection](https://blog.postman.com/2015/07/02/introducing-postman-collection-format-schema/))


## Objective: FHIR Codegen
* Parse FHIR specification into an intermediate type model
    * P0: 1.0: R4, STU3, DSTU2
    * P2: 1.0: R5
* P0: 0.8 (generating; still learning about specific / idiosyncratic requirements): Generate OpenAPI {interaction, model, complete} files.
* P0: 1.0: Release open-source on GitHub
* P0: 0.5 (zulip yes, blog post no): Announce project on Zulip and in blog post
* P1: 1.0 (Firely + MS internal groups): Get feedback from at least one external user. 
* P1: 0.5 (Delivered tools for this work; team priorities unclear): Ensure that the team can generate (Power Platform) M-code successfully.
* P2: 1.0: Generate C# models.
* P2: 1.0: Generate TypeScript models.
* Retrieve Capability Statements from FHIR servers to restrict outputs based on types, interactions, and search parameters supported
    * P1: 1.0: R4, STU3, DSTU2
    * P2: 1.0: R5
* P1: 0.0: Build an API server to accept configuration options and return a desired code file.
* P2: 0.0: Build a UI on top of the API server to allow a user to configure code generation and download the generated code file


## Objective: Maintain community presence through education, communications
* P0: 1.0: Present on 2+ team projects at FHIR Dev Days (note, this is reflected in other objectives, too)
* P0: 1.0: Lead tracks for 2+ team projects at FHIR Connectathon (note, this is reflected in other objectives, too)
* P1: 0.0 (some work on one code lab): Create a collection of codelabs/tutorials at a new site
    * similar to: https://codelabs.developers.google.com/
    * register https://fhir.how/to/ (or something)
* P1: 0.0: Publish two blog posts on MS Open Source Blog
* P2: 0.0: Create a list of potential blog post topics as a team (below is a starter list)
    * PAMA Imaging
    * Decentralized Identity
    * Argonaut projects for 2020
    * AllOfUs participation experience & project overview
    * Creation of a collection of codelabs/tutorials at a new site
* P2: 0.0 (COVID): Get Wild - Engage the Madison Healthcare Tech community
    * Define target community for a meet-up at Microsoft in Madison
    * Attend any Madison-area health tech meetups
    * Host a social / offsite for Madison area Argonaut participants
* (Scoring note: other activities -- participated in Authz meetup, ONC Dev Forum as community events)


## Objective: Commit to a "Team Madison Core Project"
* P0: 0.0: Conduct a brainstorming session to explore projects that emphasize these key goals
    * We can make progress at our own pace without external (standards body) dependencies
    * Expand frictionless data access for consumers
    * Leverage existing and emerging open standards
    * Tackle challenges that are "under-served" in industry today

* P1 (0.5 -- in this span, focused on SMART Health Cards Framework): Scope out and make a decision among the following project ideas
    * Consumer access to query networks, using self-owned identifiers
    * Consumer access to imaging data, using "glue" services between EHR FHIR implementations and cloud-hosted DICOM services
    * Placeholder -- other project ideas?


## Objective: Maintain connections within and across MS teams working on healthcare 
* P1: 0.0 (COVID): Schedule travel and draft (or glom onto!) a project plan for team particiaption in the Microsoft June OneWeek hackathon
* P2: 0.2 (Several ad-hoc, but not advertized): Offer a "health standards office hours" or "FHIR workshop" to internal teams, advertising and hosting one session with a broad invite list
* P2: 0.2 (Again, ad-hoc discussions for data mapping, anonymization tagging, but not planned/advertised): Host an internal a "wishlist" or brainstorming session to solicit experiences and gaps across internal teams
