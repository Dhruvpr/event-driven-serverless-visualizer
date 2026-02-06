Serverless Order System Architecture Visualization

An interactive, live-animated dashboard built with React and Tailwind CSS that visualizes an event-driven AWS serverless architecture. This tool allows developers and stakeholders to understand the lifecycle of an order—from ingestion to fulfillment—through real-time simulations.

🚀 Key Features

Live Flow Simulation: Click "Run Simulation" to watch data packets physically travel through the system tracks.

Interactive Component Inspector: Click any service (Lambda, SQS, DynamoDB) to see its specific role, availability settings, and technical metadata.

Real-time Console: A monospaced terminal that logs system events (HTTP status, polling activity, DB commits) as they happen.

System Health HUD: A visual heads-up display showing mock metrics like Latency, Queue Depth, and Error Rates.

Modern Blueprint Aesthetic: A crisp light-theme design with a professional dot-grid canvas and Lucide-icon integration.

🏗️ The Architecture

This project visualizes a standard high-availability serverless pattern:

Ingress: A Web Client sends a POST request to API Gateway.

Validation: A SubmitOrder Lambda validates the payload and immediately returns a 202 Accepted while pushing the message to the queue.

Buffering: Amazon SQS acts as a durable buffer to decouple the front end from the back end.

Processing: The ProcessOrder Lambda polls the queue in batches to handle fulfillment.

Storage & Notifications: Successful orders are written to DynamoDB, customers are notified via Amazon SES, and metrics are emitted to CloudWatch.

Error Handling: Failed messages are automatically routed to a Dead Letter Queue (DLQ) for investigation.

🛠️ Tech Stack

Framework: React

Styling: Tailwind CSS

Icons: Lucide React

Animations: CSS Keyframes & Tailwind Transitions

📥 Getting Started

Prerequisites

Node.js (v18 or higher)

npm or yarn

Installation

Clone the repository:

git clone [https://github.com/your-username/serverless-arch-viz.git](https://github.com/your-username/serverless-arch-viz.git)


Install dependencies:

npm install


Start the development server:

npm start


📝 License

This project is open-source and available under the MIT License.

Built to make cloud architecture more accessible.
