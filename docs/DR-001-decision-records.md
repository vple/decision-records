# DR-001: Decision Records

Vincent Le  
Accepted: 2018-09-01

## Context
Complex systems and organizations have various decisions and rules that evolve over time. It needs to be clear to everyone involved what decisions have been made and how they came to be. This info allows people to uphold these decisions and understand the rationale behind them. Additionally, it gives them the info necessary to analyze these decisions and make good decisions in the future.

## Decision
We will keep a record of significant decisions. We'll base our approach off of the one described by Michael Nygard for [documenting architecture decisions](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions). However, we're broadening this strategy to apply for any system or organization that we want to document, not just system architectures.

### Rules

A system's decision records should be grouped together in the same folder.

Records should be recorded in a lightweight text formatting language. This provides flexibility in how records are written and structured.

Decision records should be numbered sequentially. They may optionally be namespaced, preferably with a short (at most 3 letters) string, e.g. `DR-001`. This number, including the namespace, is the decision record's ID.

Decision records, once accepted, should not be modified. This ensures that there's a reliable record for future readers. It also allows people to see the decision at the time it was made and not a version that was updated in hindsight. Small edits to improve clarity are okay, but should generally be avoided and limited to recent decision records.

Decision records that are amended or superseded by other decisions will be updated to reflect this. It's important to show that something was a decision, but is no longer the decisions.

The decision record format should have as few parts as needed to convey the decision, in order to make it easy to digest. It should have as many parts as needed to ensure the decision is understood.

### Format

**Title**  
Each record should have a name that's a short noun phrase. The title should include the record's ID. For example, "DR-001: Decision Records".

**Metadata**  
The doc should include some basic metadata:

* It should include the author(s), with the primary author first. This makes it clear who to talk to if the record needs to be discussed.
* Acceptance date. This indicates when the decision took effect. If the decision hasn't been accepted, indicate this with an appropriate status.
* Related decisions, including the relationship between the decisions. Generally, this will be one of supersedes, superseded by, amends, or amended by.
  * The related decision should be linked and labelled in full, e.g. [DR-001: Decision Records](DR-001-decision-records.md). Subsequent references to these decisions can use just the decision record ID.
  * Supersedes / superseded by are special relationships indicating that the superseded decision is no longer applicable.

**Context**  
This section should describe the forces and motivations behind the decision. The descriptions here are value-neutral; they are just describing facts.

The context should clearly identify the issues / problems that the record addresses. It might also include assumptions, constraints, or previous decisions records. As much as possible, relevant information used in making the decision should be included in the context.

**Decision**    
This section describes the approach to be used to handle the issues described. It is stated in full sentences, with active voice. This section may be structured in any way needed to convey the decision.

The rationale behind the decision should also be included in this section. Readers should understand how the decision addresses the concerns described in the context section.

**Consequences**  
This section describes the resulting context after applying the decision. It should include all consequences, positive or negative. This section may also outline expected courses of actions for team members.

**Alternatives**     
This section should cover any significant alternative options that were considered and rejected. As with decisions, the rationale behind rejecting these alternatives should be included. It can sometimes make more sense to discuss these alternatives within the decision section.

**Experiences**     
This section should cover team members' experiences with the decision. It should focus on unexpected consequences of the decision, such as pain points caused by the decision.

The purpose of this section is to expose whether or not the decision had its expected impact. Having this info allows future decision records to provide more accurate consequences. It also provides additional context for future decisions.

Since this section describes things that occur after the decision is made, it is the only part of the decision record that can and should be freely modified after the decision is accepted.

**Resources**   
This section should include any relevant resources that influenced or are related to the decisions.

## Consequences
Decision records should allow team members to get up to speed faster and be able to better understand the rationale behind corresponding implementations and behaviors. They require more upfront work to keep an up-to-date record, but this effort should pay for itself in the long run.

## Resources
* [Documenting Architecture Decisions](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions), Michael Nygard