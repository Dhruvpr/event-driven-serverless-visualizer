🌐 Event-Driven Serverless Order Processing System

An immersive 3D visualization platform that demonstrates the lifecycle of an order within a serverless cloud environment. Built using Three.js, Tailwind CSS, and AWS Service Architecture principles.

🚀 Project Overview

This project serves as an educational and monitoring tool to visualize the flow of data across a distributed serverless system. It bridges the gap between static architecture diagrams and real-world execution by animating the "events" that drive modern cloud applications.

✨ Key Features

3D Interactive Pipeline: A high-fidelity 3D scene where users can watch data packets navigate through a series of AWS services in real-time.

Event-Driven Flow: Demonstrates the asynchronous "Fan-out" pattern, showing how a single process triggers parallel actions like database logging and email notifications.

Observability & Monitoring: Simulated integration with Amazon CloudWatch to show how logs are generated at every step for system health tracking.

Synchronized Context UI: A dynamic information panel that updates descriptions and highlights the active service as the animation progresses.

Bright Mode Design: A clean, professional aesthetic using glassmorphism, fluid typography, and standard AWS iconography.

🛠️ Tech Stack

Engine: Three.js (WebGL-based 3D Rendering)

Styling: Tailwind CSS (Responsive Layouts & UI Components)

Visuals: AWS Architecture Icons (PlantUML)

Logic: Vanilla JavaScript (ES6+)

📋 Architectural Workflow

The application simulates the following seven-step event-driven sequence:

Entry Point: User interaction starts via a Web Form or REST API call.

API Gateway: The secure front-door that receives the HTTPS request and routes it to the backend.

Order Validation (Lambda): A serverless function performs syntax checks and authorization logic.

Resilience Queue (SQS): The order is stored in a message queue to decouple the producer from the consumer, ensuring no data loss during spikes.

Process Engine (Lambda): The core logic function that consumes the queue message and triggers downstream events.

Fan-out Execution:

Persistence: Data is logged permanently into Amazon DynamoDB.

Notification: A confirmation email is dispatched via Amazon SES.

CloudWatch Logs: Centralized monitoring tracks every transaction for full system transparency.

💻 Local Setup & Deployment

Since this is a client-side web application, no backend installation or API keys are required to run the visualization.

Clone the repository:

git clone [https://github.com/your-username/serverless-order-system.git]( https://dhruvpr.github.io/event-driven-serverless-visualizer/)


Navigate to the folder:

cd serverless-order-system


Run the Project:
Simply open index.html in any modern browser (Chrome, Safari, Firefox, or Edge).
