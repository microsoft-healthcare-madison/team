## OKRs for September 2019
We're following a planning schedule that mirrors the HL7 workging group meeting schedule --
in four-month intervals ending in September, January, and May.

## Objective: Make sure the community is ready for a successful Subscriptions connectathon track 
P0: Ensure that all necessary changes to Subscription and Topic are merged into the main FHIR build before Sunday, August 11 (to make the R5 Connectathon snapshot for tooling).
P0: Prepare connectathon track descriptions including descriptions for Argonaut scenarios

P1 Prepare and publish tutorials for connectathon participants and others to learn about Subscriptions

P1: Document how developers can use our tooling and deploy their own copies of the core components of our reference implementation (server, client, and test harness) including locally via docker

P2: Blog post in early September about our work and its relevance

P1: Solicit feedback on our work by including relevant links for ratings/questions/comments in our published guides

P2: Solicit feedback on our work by creating a survey that at least 50% of connectathon participants re: what worked/didn’t. 

P1/2: Prepare and deliver a Webinar covering all the tutorial information 
 - (Should record / make available to the public, and tie to blog post) 
 

P1: Ensure that participation in connectathon includes representatives from at least three EHR vendors

P1: Ensure that participaiton in connectathon includes at lesat 15 or more participants 


## Objective: Build technical documentation and reference implementation for Subscriptions 

P0: Merge relevant changes into the FHIR core (FHIR CI Build) – targeting FHIR R5
- Work with Firely and HAPI to get changes in snapshot build 

P0: Create a draft Argonaut IG for subscriptions that includes
- P0 specific admissions and discharge topic 
- P0 a profile for single-patient subscriptions (consumer use case )
- P0 a profile for group-based subscriptions (health system, payer, or clearinghouse use case)

P0: Build, document, and publicly deploy a subscriptions server reference implementation to 
 - P0 accept FHIR calls re: Subscriptions 
 - P0: Handle sending notifications to clients via REST-hook and Websocket 
 - P2: Implement Server Side Events (SSE) 
 - P3: Support creation of arbitrary client-defined topics
 - P4: Support additional (extension) channel types 

P0:  Build, document, and publicly deploy a subscriptions client reference implementation to
 - P0 create listener endpoints
 - P0 create subscriptions and register/receive/display notifications 
 - P1: configure filters with for more prescise subscriptions (e.g., by patient or group)

P0: Build, document, and publicly deploy a testing harness for client / server to
- P1: trigger various Topic events by issuing a FHIR operations (e.g., `POST /Encounter`)
- P1: enablie triggering manually and by schedule 
- P1 generate any necessary data on-the-fly or load from pre-buily Synthea exports
