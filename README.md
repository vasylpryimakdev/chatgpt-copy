# ChatGPT Clone

A simple ChatGPT-like application with a React client and a Node.js server.

## Project Structure

- `client/` - React application
- `server/` - Express and Socket.IO server

## Requirements

- Node.js 18 or newer
- An OpenAI Platform API key for AI responses

## Installation

Install dependencies in both applications:

```bash
cd client
npm ci

cd ../server
npm ci
```

## Environment Variables

Create `server/.env`:

```env
PORT=5000
OPEN_AI_API_KEY=your_api_key
OPEN_AI_ORG=your_organization_id
```

The client currently connects to the server at `http://localhost:5000`, so
use port `5000` when running both applications locally.

Never commit `.env` files or expose an API key in client-side code.

## Running Locally

Start the server in one terminal:

```bash
cd server
node index.js
```

Start the client in another terminal:

```bash
cd client
npm start
```

Open [http://localhost:3000](http://localhost:3000) in a browser.

## OpenAI API Billing

The OpenAI API is billed separately from ChatGPT Free or Plus subscriptions.
API requests require an available quota or billing setup on the OpenAI
Platform. A `429 Too Many Requests` response usually indicates an exhausted
quota, missing billing, or a rate limit.

## Build

Create a production client build with:

```bash
cd client
npm run build
```
