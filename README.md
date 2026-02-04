# 🚀 OrderPulse: Event-Driven Serverless Visualizer

A high-fidelity interactive simulation of an **AWS Event-Driven Architecture**. This project visualizes how a customer order moves through a serverless backend, demonstrating decoupling, asynchronous processing, and real-time monitoring.

## 🏗️ Architecture Overview
The system simulates the following AWS workflow:
1.  **User Ingress:** A web form submits an order via an API Gateway.
2.  **AWS Lambda (Validator):** Performs immediate schema validation.
3.  **Amazon SQS:** Decouples the system by buffering the order event.
4.  **AWS Lambda (Processor):** Triggered by SQS to handle business logic.
5.  **Amazon DynamoDB:** Persists the final order state.
6.  **Amazon SES:** Dispatches a transactional confirmation email.
7.  **Amazon CloudWatch:** Ingests logs and metrics from every step of the process.

## ✨ Key Features
- **Neon-Glow UI:** Professional dark-mode interface with high-intensity visual feedback.
- **Asynchronous Logic:** Visualizes the "fire-and-forget" nature of SQS buffering.
- **CloudWatch Telemetry:** High-glow logs and reactive metrics (Invocations, Latency, Queue Depth).
- **SVG Path Animation:** Dynamic energy pulses that trace the event lifecycle in real-time.

## 🛠️ Technology Stack
- **Frontend:** HTML5, Tailwind CSS, FontAwesome 6.
- **Animations:** CSS3 Keyframes & SVG Path Data.
- **Logic:** Vanilla JavaScript (Event-loop simulation).
- **Icons:** FontAwesome Pro-style branding for AWS services.

## 📖 How to Run
1. Simply open `index.html` in any modern web browser.
2. Enter a customer email and select a resource plan.
3. Click **"Dispatch Order"** to witness the serverless trace.
