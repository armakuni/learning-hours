# Intro to API Contracts

## Learning Goals
 - Understand what API contracts are and their importance
 - Learn the key components of an API contract.
 - Explore tools and best practices for creating and maintaining API contracts.

## Session Outline
  - **10 min connect**: exploring existing API challenges
  - **10 min concept**: defining API contracts and their components
  - **20 min do**: hands-on API contract creation
  - **10 min reflect**: summarizing benefits and key takeaways

### Connect - exploring existing API challenges
- Divide participants into pairs or small groups.
- Ask them to discuss:
    - Challenges they’ve faced while consuming or building APIs.
    - Instances where unclear or missing API documentation caused issues.
- After a few minutes, have a few pairs share their experiences with the group. Note the common pain points on a whiteboard or shared document.

### Concept - defining API contracts and their components
- Define an API contract:
    - A formal agreement between the provider and consumer of an API that outlines the API's structure, behavior, and constraints.
- Explain key components of an API contract:
    - Endpoints: URLs for accessing resources.
    - Methods: HTTP verbs (GET, POST, PUT, DELETE, etc.).
    - Request structure: Input fields and formats.
    - Response structure: Expected data and status codes.
    - Error handling: Standardized error responses.
- Highlight the importance:
    - Improves collaboration between teams.
    - Reduces misunderstandings and integration issues.
    - Ensures consistency and reliability across API versions.

### Do - hands-on API contract creation
- Provide a simple scenario, such as a “To-Do List API” with endpoints like adding, updating, deleting, and retrieving tasks.
- Ask participants to work in pairs or groups to draft a basic API contract using tools like:
    - OpenAPI/Swagger specification - automated tools for different languages you create and consume APIs in
    - A simple markdown table for API details
- Encourage teams to include endpoints, methods, request/response structure, and an example error message.
- After 20 minutes, have each group briefly present their contract to the room.

### Reflect - summarizing benefits and key takeaways
- Discuss:
    - How the exercise helped address some of the API challenges noted earlier.
    - Key benefits of having a well-defined API contract, such as faster onboarding for developers and smoother integrations.
- Ask participants to share one key takeaway or action item they plan to apply in their work.

### 10 min Q&A and open discussion
- Open the floor for questions and concerns.
- Address common challenges like:
    - Maintaining contracts as APIs evolve.
    - Choosing tools for documenting contracts.
    - Testing API contracts.

### Next Steps
- Encourage teams to start using API contracts for new projects.
- Share resources, such as OpenAPI/Swagger tutorials or documentation templates.
- Schedule a follow-up session to dive deeper into advanced tools or real-world API contract examples.
