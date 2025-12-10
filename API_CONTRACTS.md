# API Contracts

## Base URL
`http://localhost:5000/api`

## Authentication Endpoints

### POST /auth/register
Register new user

**Request:**
```json
{
  "email": "user@example.com",
  "password": "secure_password",
  "name": "John Doe"
}
```

**Response:**
```json
{
  "token": "jwt_token_here",
  "user": {"id": 1, "email": "user@example.com"}
}
```

## Image Generation

### POST /images/generate
Generate image from prompt

**Headers:**
```
Authorization: Bearer {token}
Content-Type: application/json
```

**Request:**
```json
{
  "prompt": "A beautiful landscape",
  "model": "stable-diffusion",
  "width": 512,
  "height": 512
}
```

**Response:**
```json
{
  "id": "img_123",
  "url": "https://cdn.example.com/images/img_123.png",
  "status": "completed"
}
```

## Video Generation

### POST /videos/generate
Generate video from prompt

**Request:**
```json
{
  "prompt": "A cat dancing",
  "service": "pika",
  "duration": 5
}
```

**Response:**
```json
{
  "id": "vid_456",
  "status": "processing",
  "progress": 0
}
```

## Prompt Library

### GET /prompts
Get all prompts with filtering

**Query Parameters:**
- `type`: photo|video
- `model`: stable-diffusion|flux|pika|runway
- `tags`: comma-separated tags

**Response:**
```json
{
  "prompts": [
    {
      "id": 1,
      "title": "Cinematic Portrait",
      "text": "A detailed portrait...",
      "type": "photo",
      "model": "stable-diffusion"
    }
  ]
}
```
