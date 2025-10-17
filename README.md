# CloudPulse: Event-Driven Uptime Monitoring System

## Overview
CloudPulse is a scalable backend system for uptime monitoring built using NestJS and AWS cloud services. It features an event-driven architecture that enables real-time health checks and alert notifications for monitored systems. The project processes asynchronous monitoring tasks using AWS SQS for reliable message queuing and AWS Lambda for serverless event processing, ensuring fast and efficient backend operations.

Containerized with Docker, CloudPulse offers consistent development and production environments, easing deployment and scalability challenges.

---

## Features
- Built with **NestJS** and **TypeScript** for robust, maintainable backend code.
- Utilizes **AWS SQS** for asynchronous, event-driven message queuing.
- Uses **AWS Lambda** to handle scheduled and triggered processing tasks.
- Stores monitoring logs and metadata in **PostgreSQL** relational database.
- Packaged with **Docker** for consistent environment setup and deployment portability.
- Modular codebase for easy extensibility and maintenance.

---

## Technologies Used
- Node.js & TypeScript
- NestJS framework
- AWS SQS (Simple Queue Service)
- AWS Lambda (serverless functions)
- PostgreSQL (relational database)
- Docker (containerization)

---

## Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- Docker (optional, for containerized deployment)
- AWS account with permissions for SQS, Lambda, and RDS (PostgreSQL)

### Installation & Setup

1. Clone the repository:
```
git clone https://github.com/yourusername/cloudpulse.git
cd cloudpulse
```
2. Install dependencies:
```
npm install
```
3. Configure environment variables based on `.env.example` (set AWS credentials, DB connection, SQS queue URLs).

4. Run locally without Docker:
```
npm run start:dev
```
5. Or build and run with Docker:
```
docker build -t cloudpulse .
docker run -p 3000:3000 cloudpulse
```
---

## Architecture & Workflow

- External health check requests or schedules push messages to AWS SQS.
- AWS Lambda functions are triggered by SQS messages for task processing.
- Monitoring data and logs are saved into PostgreSQL for persistence.
- NestJS services consume SQS messages and manage the workflow asynchronously.
- Docker provides a reproducible environment both locally and in production.

---

## Future Enhancements
- Add Redis caching layer for faster response times and reduced DB load.
- Integrate Elasticsearch for advanced search & analytics capabilities.
- Implement real-time notification via SNS or other push services.
- Extend multi-cloud support and automate deployment via Infrastructure as Code (IaC).

---

## Contributing
Contributions are welcome! Please open issues or pull requests to suggest improvements.

---

## License
MIT License
