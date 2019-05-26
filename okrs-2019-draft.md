# Draft 2019 OKRs for “Team Madison” 
jmandel@microsoft.com, May 2019 

## Mission: unlock health data to enable better decisions and care 

The thesis for OKRs below is that we’re uniquely positioned to contribute by advancing open standards, tools, and practices. We can’t do it alone, but we can have outsize impact working with the community. 

---
 
#### Accelerate development of health interop standards and improve their quality... 

#### … via Argonaut: Develop an implementation guide for [admission/discharge Subscriptions](http://bit.ly/argo19-subscriptions) (P0) 

Incorporate R5 Subscriptions proposal (Topic + Subscription resource) into FHIR CI build 

Build a FHIR proxy server to implement R5 Subscriptions proposal in front of an R4 “data-only” server 

Develop or extend a tool to generate V2 ADT messages, based on simulated patients (e.g., Synthea) 

Generate and openly publish a set of sample messages for 100 Patients + medium or large population 

Configure or build tooling to broadcast these ADT message over a simulated timeline (with speed-up) 

Develop a sample Web application to demonstrate client-side subscription API 

Develop a test suite to determine if FHIR Servers are compliant with admission/discharge Subscriptions 

Develop an open-source “server bridge” that can receive FHIR deliveries and forward them to at least one flavor of non-web-accessible endpoints (e.g., by Mobile Push APIs on Android + iOS) 

Publish blog post describing our contributions to the FHIR core spec (Subscriptions) + Argonaut Project 

Draft proposal for “catch up on missed messages” operations 

 
 ---

#### Accelerate development of health interop standards and improve their quality...  

#### … via Argonaut: Develop a spec for [SMART Web Messaging and CDS Hooks for radiology orders](http://bit.ly/argo19-messaging) (P0) 

Implement support for radiology ordering in CDS Hooks Sandbox 

Implement support for order-select and order-sign hooks in CDS Hooks Sandbox 

Develop a demonstration CDS Hooks Service that implements user-configurable behaviors to facilitate testing (e.g., “always report appropriate,” or “always report inappropriate”)  

Implement general orders scratchpad UX in CDS Hooks Sandbox 

Develop a demonstration “companion app” for the CDS Hooks Service, that implements UX  (e.g., a flow chart or navigation sequence for gathering information and listing appropriate order choices) 

Publish Argonaut specification for CDS Hooks v1 

Publish SMART Web Messaging specification including “scratchpad.*” messages 

Develop a test suite to determine if EHRs are compatible with SMART Web Messaging 

 
---
#### Accelerate development of health interop standards and improve their quality...  

#### … via HL7: Use and improve the FHIR implementation guide framework (P3) 

Apply the FHIR IG publisher to at least one project ourselves (e.g., one Argonaut Guide) 

Contribute at least one performance improvement or bug fix, to begin exploring the codebase 

Interview 3 users (1 MITRE, 1 Argonaut, 1 international) about experience with the tool and publish an open summary of our findings 

 
 ---
#### Accelerate development of health interop standards and improve their quality...  

#### … via HL7:  Evaluate and improve the usability of the FHIR specification by developers (P3) 

Conduct preliminary UX research on the FHIR Spec + IG template. Interview three software developers in the Madison area who agree to be screen + voice recorded, answering "simple" questions about the specification 

Identify MS Healthcare staff resources to provide 1-2 days of UX consulting to assess and suggest an improvement plan for usability of FHIR IG template and core specification. 

 
---
#### Accelerate development of health interop standards and improve their quality... 

#### … via CARIN Alliance: Drive support for frictionless consumer access (P3) 

Participate in CARIN community + board meetings

Support CARIN publication of an implementation guide for consumer access to healthcare financial data

Send a representative to June 4 DC Identity Summit

[Others TODO]


---

#### Leverage our unique position in Madison to build relationships and grow the team (P1) 

Host one meet-up, educational session, or whiteboarding/brainstorming session per quarter, with at least 10 attendees 

Invite developers from the community to participate in UX testing sessions (e.g., on FHIR specification) 

Build a Madison-area FHIR channel on chat.fhir.org as a local community hub, with 25 subscribers 

Schedule workshop with 2-6 local developers re: their needs for testing, libraries, tools (on Argonaut) 

Identify one or more local companies or health systems that can contribute to a public, heterogeneous collection of real-world-derived HL7 V2 data 

Interview 3 local candidates for a position on our team 
 
---
#### Expand and communicate Microsoft Healthcare’s commitment to open standards (P2) 
[Not published publicly]

 
---
#### Reinforce Microsoft’s internal alignment on open healthcare standards (P2) 

[Not published publicly]

 
