# API Contract Testing - Producers and Consumers

## Learning Goals
- Understand end-to-end contract testing workflows for integrated teams.
- Learn how producers and consumers collaborate using Pact.
- Implement a contract testing pipeline.

## Session Outline
  - **10 min connect**: Share team experiences with managing API dependencies
  - **20 min concept**: Pact workflow for integrated teams
  - **30 min do**: Simulate a complete producer-consumer workflow
  - **10 min reflect**: Review and discuss team-wide practices

### Connect - Share team experiences with managing API dependencies
- Goal: Highlight the challenges of managing both consumer and provider responsibilities in the same team.
- Activity:
    - Pose a hypothetical scenario: _Your team develops both a provider and a consumer for a shared API. A change in the provider breaks the consumer._
    - Discuss in groups:
        - How would you identify and resolve this issue?
        - What process changes could prevent such problems?
- Share key insights with the larger group.

### Concept - Pact workflow for integrated teams
- Explain the producer-consumer workflow:
    - Contract Negotiation: Iterative updates to match expectations
    - Benefits: Continuous feedback, synchronized changes
- Key components:
    - Pact Broker for collaboration
    - CI/CD pipelines integrating contract testing
- Tools: Pact CLI, libraries, and CI tools

### Do - Simulate a complete producer-consumer workflow
1. Simulate a full workflow:
    - Consumer defines and publishes a Pact contract.
    - Producer fetches and verifies the contract.
    - Producer makes changes and verifies updates.
2. Set up a Pact Broker (local or hosted) for sharing contracts.
3. Automate contract tests in a CI/CD pipeline:
    - Consumer tests generate and publish contracts.
    - Producer tests verify contracts against the API.

### Reflect - Review and discuss team-wide practices
- Goal: Emphasize the benefits of a cohesive testing strategy across consumer and provider responsibilities.
- Activity:
    - Ask participants:
        - What did you notice about the interactions between consumer and provider during the hands-on session?
        - How does having a shared contract benefit integrated teams?
        - What steps can your team take to improve collaboration and testing across these roles?
- Encourage participants to propose one improvement for their team, and record these ideas on a shared board.


### Next Steps
1. Establish Cross-Role Responsibilities:
    - Define clear roles for maintaining and validating contracts within integrated teams.
2. Set Up Bidirectional Testing:
    - Ensure consumer tests validate against provider contracts and vice versa.
3. Adopt a Unified Toolchain:
    - Use a shared contract testing tool (e.g., Pact) to simplify collaboration.
4. Schedule Team Syncs:
    - Regularly discuss contract changes during sprint planning or retrospectives to maintain alignment.
5. Follow-Up Activity:
    - Plan a sprint where teams implement a complete producer-consumer contract testing workflow and reflect on its impact in the next learning hour.
