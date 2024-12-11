# API Contract Testing - Consumers

## Learning Goals
- Understand the consumer's role in contract testing.
- Learn how to create and publish Pact contracts.
- Ensure contracts accurately represent consumer expectations.

## Session Outline
  - **10 min connect**: Discuss consumer challenges with APIs
  - **15 min concept**: Introduction to Pact for consumers
  - **25 min do**: Hands-on with creating and publishing a contract
  - **10 min reflect**: Review and takeaways

### Connect - Discuss producer challenges in maintaining API contracts
- Goal: Highlight the difficulties consumers face when APIs don't meet expectations.
- Activity:
    - Ask participants:
        - “Have you ever consumed an API that didn’t work as expected?”
        - “What assumptions did you make, and how did you test those assumptions?”
- Break into pairs or small groups and share their experiences.
- Consolidate key pain points on a shared board (e.g., missing fields, unclear error messages).


### Concept - Introduction to Pact for producers
- Explain Pact from the consumer's perspective:
    - Contract Creation: Defining expectations for API behavior.
    - Benefits: Clear communication of requirements, reducing misalignment.
- Key components:
    - Mock provider: Simulate API responses during development.
    - Pact Broker: Publish and share contracts.
- Tools: Pact libraries and testing frameworks for the consumer's stack.

### Do - Hands-on with creating and verifying a contract
1. Set up a simple consumer application (e.g., a web app fetching product details).
2. Write test cases to:
    - Define expected interactions with the API.
    - Generate a Pact file.
3. Run tests to mock API responses using the Pact mock server.
4. Publish the generated Pact file to a local Pact Broker.


### Reflect - Review and takeaways
- Goal: Reinforce the benefits of contract testing for consumers.
- Activity:
    - Ask participants to reflect on:
        - What did you learn from creating and publishing a - contract as a consumer?
        - How does contract testing help ensure reliable API integrations?
        - What’s one specific consumer-side test you would like to implement next?
    - Facilitate a brief discussion about how this approach reduces integration risks.


### Next Steps
1. Implement Consumer Contracts:
    - Assign each team member to write a consumer-side contract for an existing API they use.
2. Collaborate with Providers:
    - Share your contracts with provider teams to establish a feedback loop and ensure compatibility.
3. Integrate Tests into Workflow:
    - Automate the verification of contracts against the provider APIs during integration testing.
4. Follow-Up Activity:
    - Conduct a review session where teams showcase their consumer contracts and discuss lessons learned.
