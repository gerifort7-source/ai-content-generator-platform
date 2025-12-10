# ai-content-generator-platform
AI-powered platform for generating photos and videos with multiple AI models. Includes Stable Diffusion, Pika, Runway integration with user file uploads and prompt library.

## Quick Start

### Prerequisites
- Docker & Docker Compose
- Node.js 18+
- PostgreSQL 15

### Installation

```bash
git clone https://github.com/gerifort7-source/ai-content-generator-platform.git
cd ai-content-generator-platform
docker-compose up -d
```

## Features

- Photo Generation with Stable Diffusion, SDXL, Flux
- Video Generation with Pika, Runway, Luma
- User File Uploads & Portfolio Management
- Comprehensive Prompt Library
- JWT Authentication
- PostgreSQL Database
- Docker Deployment Ready

## Tech Stack

**Frontend:** React 18, Vite, TailwindCSS
**Backend:** Node.js, Express.js, PostgreSQL
**AI Services:** Replicate API, Pika API, Runway API
**Deployment:** Docker, AWS/Heroku Ready

## API Endpoints

- `/api/auth` - Authentication
- `/api/images` - Photo Generation
- `/api/videos` - Video Generation
- `/api/prompts` - Prompt Library
- `/api/uploads` - File Management

## Documentation

See [Google Doc](https://docs.google.com/document/d/1zEjUL2PBsuKMOH6YJBts3SL8j-HFqetyM1CGvqRZxDA/edit) for detailed setup guide.
