# API Contract Testing - Producers

## Learning Goals
- Understand the producer's role in contract testing.
- Learn how to write and verify Pact contracts as a producer.
- Ensure API changes do not break consumer expectations.

## Session Outline
  - **10 min connect**: Discuss producer challenges in maintaining API contracts
  - **15 min concept**: Introduction to Pact for producers
  - **25 min do**: Hands-on with creating and verifying a contract
  - **10 min reflect**: Review and takeaways

### Connect - Discuss producer challenges in maintaining API contracts
- Goal: Understand the challenges of maintaining compatibility in provider APIs.
- Activity:
    - Ask participants to think of a time when an API change caused issues for consumers (e.g., a breaking change or misaligned expectations).
    - Form small groups and discuss:
        - What was the issue?
        - How did it affect the consumer?
        - How was it resolved?
- After 5 minutes, ask a few groups to share their stories with the larger group.

### Concept - Introduction to Pact for producers
- Explain Pact from the producer's perspective:
    - Contract Verification: Ensuring the provider API adheres to the contract created by the consumer.
    - Benefits: Early detection of breaking changes, faster feedback loops.
- Key components:
    - Pact file: JSON representation of the contract.
    - Pact Broker: Sharing contracts between teams.
- Tools: Pact libraries for the chosen language/framework.

### Do - Hands-on with creating and verifying a contract
1. Set up a simple API (e.g., a product catalog API).
2. Load an existing Pact file (simulating a contract from a consumer).
3. Write test cases to verify the API meets the contract:
    - Configure Pact to verify endpoints.
    - Run the verification and interpret results.
4. Break the API intentionally (e.g., change response fields) and observe test failures.


### Reflect - Review and takeaways
- Goal: Reinforce the importance of contract testing for providers.
- Activity:
    - Pose these reflection questions to participants:
        - What challenges did you face in the hands-on exercise?
        - How does contract testing improve provider-consumer collaboration?
        - What’s one step your team can take to adopt contract testing effectively?
    - Have participants write down one action item for improving contract testing in their teams on a shared board or post-it notes.

### Next Steps
1. Define Ownership:
    - Identify the team or individuals responsible for maintaining provider-side contracts.
    - Set up regular reviews to ensure contracts remain aligned with consumer needs.
2. Automate Contract Validation:
    - Integrate contract validation into your CI/CD pipeline to catch breaking changes early.
3. Document Provider Expectations:
    - Use tools like Swagger or OpenAPI to document API behavior and expectations.
    - Ensure documentation is automatically updated with API changes.
4. Follow-Up Activity:
    - Assign teams to implement a contract test for one of their APIs and present their results in a follow-up session.
