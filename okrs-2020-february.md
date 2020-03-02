## OKRs for Feb 2020

We follow a planning schedule that mirrors the HL7 workging group meeting
schedule -- in four-month intervals ending in September, January, and May.
(In 2020, the "January" meeting is later than usual, so this doc is scoped
to February 2020.)

## Objective: Wrap up Argonaut Encounter Subscriptions IG

P0: Finalize canonical SubscriptionTopics for Encounter events
* Score: 0.8 (Will still need to keep updated with R5 evolution)

P0: Complete conformance language in the Argonaut Encounter IG
* Score: 0.8 (One more piece of feedback to incorporate; the occasional updates with R5 evolution)
 
P0: Ensure complete support in Reference Implementation
* Score:  0.5 (Still need to align Topic names and add "encounter-end")

P1: Format the IG for publication using HL7's publisher template ("or something")
* Score: 0.0 (Deferred; WIP given R5 status)

P1: Publish the guide through Argonaut
* Score: 0.5 (Hard to find the spec from Argonaut wiki; no deep links to the Encounters IG)

P2: Prepare a community tutorial showing how to build a well-behaved
    Encounter Subscriptions client, including error handling (e.g.,
    missed message detection, out-of-order delivery).
* Score: 0.5 (Have core content from Lets Build at Dev Days; need narrative structure explaining how to think about / approach error handling, etc.)

Notes:
* Work on the Argonaut project was derailed by focus on core model redesign.
* Work on the Reference Implementation has been reduced by untracked projects (e.g., codegen).

## Objective: Prepare FHIR R5 Topic-based Subscriptions for ballot

P0: Solicit design review from at least two cloud engineering teams
    (e.g., re: "eventCount" or other scaling concerns)
* Score: 1.0 (in-depth review with Google + Azure teams, incorporated feedback)

P0: Complete definition for "built-in" channel types (including Web Sockets, E-mail)
* Score: 0.5 (Defined REST, e-mail; need to define Messaging, Web Sockets; nixed SMS from the list.)

P0: Ensure full support for built-in channel types in Reference Implementation
* Score: 0.75 (Supporting REST, e-mail so far; draft Web Sockets ahead of what's documented)

P1: Document how developers can use our tooling and deploy their own copies of
    the core components of our reference implementation (server, client, and test
    harness) including locally via docker
* Score: 0.4 (Some slideware from DevDays; no published docs)

P2: Blog post explaining rationale for and technical details of R5 Topic-based Subscriptions
* Score: 0.8 (Wrote a Subscriptions blog, focused pre/post state)

P3: Build out tooling for arbitrary (computable) SubscriptionTopic definition / testing.
* Score: 0.0

Notes:
* Too ambitious on timeline - will likely need the entire R5 timeline to get right.

## Objective: Wrap up Argonaut PAMA IG

P0: Complete a last-call for participant feedback
* Score: 1.0 (Not much actual feedback...)

P0: Format the IG for publication (e.g. using mkdocs or HL7's publisher template)
* Score: 0.7 (mkdocs sites now exists; nav / structure / polish still TODO)

P1: Prepare a community tutorial with code samples and end-to-end walk-through
    demonstrating the three key PAMA interactions.
* Score 0.75 (https://aka.ms/pama-codelab has App Launch, suggestion cards; not yet support for automated ratings via `systemActions` response)

P1: Put SMART Web Messaging onto HL7's standards track with a Project Scope Statement,
    and a "standard for trial use" ballot
* Score: 0.4 (PSS written, approved; no NIB)

P1: Establish a documentation go-to spot for state-of-the world information, IGs, contact
    info, etc.
* Score: 0.0 (Could be folded into IG)

P2: Build a markdown matrix showing which EHR vendors support which CDS hooks to be
    maintained by the community.
* Score: 0.0 (We have a list of names in Excel, but nothing summarized/published)

P2: Build a markdown matrix showing which qCDSMs support which PLE's guidelines to be
    maintained by the community.
* Score: 0.0 (We have a list of names in Excel, but nothing summarized/published)


## Objective: Establish Argonaut 2020 project for "SMART Scheduling Links"

P0: Submit 2020 project proposal for "SMART Scheduling Links"
* Score: 1.0

P1: Develop a list of supporting organizations including at least three Argonaut participants
* Score 0.75 (We had >3 supporting orgs, but this didn't get selected as a 2020 project :-( )


## Objective: Develop an open-source Patient On-ramp to TEFCA access

P0: Determine the right organizational entry-point (e.g., within Carequality, Commonwell)
* Score: 0.2 (Conversations with CW, CEQ leadership, but no strategy to take this forward)

P0: Discuss opportunities to co-develop with at least two outside organizations
* Score: 0.2 (Conversations within CARIN; no concrete plans developed)

P0: Publish a design document that covers identity proofing plug-ins, app registration
    allowing for public client registration, developer-facing questionnaires, published
    app lists, and a SMART proxy to TEFCA.
* Score: 0.0

P1: Hire two software engineers to begin work on MVP
* Score: 0.2 (Job req published; interviews not started)

P1: Conduct a "design sprint" or similar session to establish MVP user experience
* Score: 0.0 (Brainstorming session scheduled post-HIMSS)

