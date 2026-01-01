# @subagents-test/backend

Fastify-based backend server for the Todo application.

## Features

- Built with TypeScript and Fastify
- JSON file-based persistence
- RESTful API endpoints for todo management
- Structured logging with Pino

## Development

```bash
# Install dependencies (from root)
npm install

# Start development server with hot reload
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Type check
npm run type-check
```

## API Endpoints

### Health Check
- `GET /health` - Returns server health status

### Todos (Coming Soon)
- `GET /api/todos` - Get all todos
- `POST /api/todos` - Create a new todo
- `PATCH /api/todos/:id` - Update a todo

## Configuration

Environment variables:
- `PORT` - Server port (default: 3000)
- `HOST` - Server host (default: 0.0.0.0)
