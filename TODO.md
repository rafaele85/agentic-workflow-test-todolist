# Todo List Application - Development Tasks

## Project Overview
Full-stack Todo list application with React frontend and Fastify backend, using TypeScript throughout and NPM workspaces monorepo structure.

## Tech Stack
- **Frontend**: React, TypeScript, CSS Modules
- **Backend**: Fastify, TypeScript
- **Storage**: JSON file persistence
- **Quality Gates**: ESLint, TypeScript type checking
- **Version Control**: Git with Gitflow workflow

---

## Phase 1: Project Foundation

### 1.1 Monorepo Setup
- [x] Initialize git repository with main branch
- [x] Create root package.json with NPM workspaces configuration
- [x] Create `packages/` directory structure
- [x] Create `.gitignore` for node_modules, build artifacts, and data files
- [x] Set up gitflow: create develop branch from main

### 1.2 Backend Workspace Setup
- [ ] Create `packages/backend/` directory
- [ ] Initialize backend package.json with Fastify and TypeScript dependencies
- [ ] Create basic TypeScript configuration (tsconfig.json)
- [ ] Create minimal Fastify server entry point (src/index.ts)
- [ ] Add start script to run server locally
- [ ] Commit: "feat: initialize backend workspace"

### 1.3 Frontend Workspace Setup
- [ ] Create `packages/frontend/` directory
- [ ] Initialize frontend package.json with React, TypeScript, and Vite
- [ ] Create TypeScript configuration for React
- [ ] Create basic Vite configuration
- [ ] Create minimal React App component
- [ ] Add dev script to run frontend locally
- [ ] Commit: "feat: initialize frontend workspace"

---

## Phase 2: Quality Gates

### 2.1 ESLint Setup
- [ ] Install ESLint and TypeScript ESLint parser at root level
- [ ] Create root ESLint configuration
- [ ] Add ESLint script to backend package.json
- [ ] Add ESLint script to frontend package.json
- [ ] Add root-level lint script that runs both
- [ ] Commit: "chore: add ESLint configuration"

### 2.2 TypeScript Type Checking
- [ ] Add type-check script to backend package.json
- [ ] Add type-check script to frontend package.json
- [ ] Add root-level type-check script that runs both
- [ ] Commit: "chore: add TypeScript type checking scripts"

### 2.3 Quality Gate Validation
- [ ] Create root-level quality-check script (lint + type-check)
- [ ] Test quality gates run successfully
- [ ] Commit: "chore: add quality gate validation script"

---

## Phase 3: Backend Core - Data Layer

### 3.1 Todo Data Model
- [ ] Create `packages/backend/src/types/todo.ts` with Todo interface
- [ ] Define Todo structure: id, text, done, createdAt
- [ ] Export TodoList type as array of Todos
- [ ] Commit: "feat: define Todo data model"

### 3.2 File Storage Service
- [ ] Create `packages/backend/src/services/storage.ts`
- [ ] Implement `loadTodos()` function to read from JSON file
- [ ] Implement `saveTodos()` function to write to JSON file
- [ ] Handle file not found gracefully (return empty array)
- [ ] Create `data/` directory in .gitignore
- [ ] Commit: "feat: implement JSON file storage service"

### 3.3 Storage Service Testing
- [ ] Manually test storage service with sample data
- [ ] Verify JSON file creation and reading
- [ ] Commit: "test: validate storage service"

---

## Phase 4: Backend Core - API Layer

### 4.1 Get All Todos Endpoint
- [ ] Create `packages/backend/src/routes/todos.ts`
- [ ] Implement GET /api/todos endpoint
- [ ] Return all todos from storage
- [ ] Register route in main server file
- [ ] Test endpoint with curl or Postman
- [ ] Commit: "feat: add GET todos endpoint"

### 4.2 Create Todo Endpoint
- [ ] Implement POST /api/todos endpoint
- [ ] Accept todo text in request body
- [ ] Generate unique ID (timestamp or UUID)
- [ ] Set done to false, add createdAt timestamp
- [ ] Save to storage and return created todo
- [ ] Test endpoint with curl or Postman
- [ ] Commit: "feat: add POST todo endpoint"

### 4.3 Update Todo Endpoint
- [ ] Implement PATCH /api/todos/:id endpoint
- [ ] Accept done status in request body
- [ ] Find and update todo by ID
- [ ] Return updated todo or 404 if not found
- [ ] Save changes to storage
- [ ] Test endpoint with curl or Postman
- [ ] Commit: "feat: add PATCH todo endpoint"

---

## Phase 5: Backend Polish

### 5.1 CORS Configuration
- [ ] Install @fastify/cors plugin
- [ ] Configure CORS to allow frontend origin
- [ ] Test cross-origin requests work
- [ ] Commit: "feat: enable CORS for frontend"

### 5.2 Error Handling
- [ ] Add try-catch blocks to all route handlers
- [ ] Return appropriate HTTP status codes
- [ ] Add request validation for POST/PATCH endpoints
- [ ] Commit: "feat: improve error handling"

### 5.3 Backend Quality Check
- [ ] Run ESLint on backend code
- [ ] Run TypeScript type check
- [ ] Fix any issues found
- [ ] Commit: "fix: resolve linting and type issues in backend"

---

## Phase 6: Frontend Core - Components

### 6.1 Basic App Structure
- [ ] Create `packages/frontend/src/App.tsx` with basic layout
- [ ] Add heading "Todo List"
- [ ] Create placeholder for todo list and input
- [ ] Apply basic CSS module styling
- [ ] Commit: "feat: create basic app layout"

### 6.2 Todo List Component
- [ ] Create `packages/frontend/src/components/TodoList.tsx`
- [ ] Accept todos array as prop
- [ ] Render list of todo items
- [ ] Create corresponding CSS module
- [ ] Import and use in App component
- [ ] Commit: "feat: add TodoList component"

### 6.3 Todo Item Component
- [ ] Create `packages/frontend/src/components/TodoItem.tsx`
- [ ] Accept todo and onToggle callback as props
- [ ] Render checkbox and todo text
- [ ] Style completed todos differently
- [ ] Create corresponding CSS module
- [ ] Use in TodoList component
- [ ] Commit: "feat: add TodoItem component"

### 6.4 Add Todo Form Component
- [ ] Create `packages/frontend/src/components/AddTodoForm.tsx`
- [ ] Create controlled input field
- [ ] Add submit button
- [ ] Accept onAdd callback prop
- [ ] Create corresponding CSS module
- [ ] Use in App component
- [ ] Commit: "feat: add AddTodoForm component"

---

## Phase 7: Frontend Core - API Integration

### 7.1 API Client Setup
- [ ] Create `packages/frontend/src/api/client.ts`
- [ ] Define base URL for backend API
- [ ] Create fetchTodos() function
- [ ] Create addTodo(text: string) function
- [ ] Create toggleTodo(id: string) function
- [ ] Commit: "feat: create API client"

### 7.2 State Management in App
- [ ] Add useState for todos array in App component
- [ ] Add useEffect to load todos on mount
- [ ] Implement handleAddTodo function
- [ ] Implement handleToggleTodo function
- [ ] Pass handlers to child components
- [ ] Commit: "feat: integrate API with React state"

### 7.3 Loading and Error States
- [ ] Add loading state to App component
- [ ] Show "Loading..." while fetching todos
- [ ] Add error state for failed requests
- [ ] Display error messages to user
- [ ] Commit: "feat: add loading and error states"

---

## Phase 8: Frontend Polish

### 8.1 Styling Improvements
- [ ] Create global styles in App.module.css
- [ ] Add responsive layout
- [ ] Style input and button elements
- [ ] Add hover and focus states
- [ ] Improve visual feedback for completed todos
- [ ] Commit: "style: improve UI appearance"

### 8.2 User Experience Enhancements
- [ ] Clear input field after adding todo
- [ ] Focus input field after adding todo
- [ ] Disable submit button when input is empty
- [ ] Add transition animations for todo items
- [ ] Commit: "feat: enhance user experience"

### 8.3 Frontend Quality Check
- [ ] Run ESLint on frontend code
- [ ] Run TypeScript type check
- [ ] Fix any issues found
- [ ] Commit: "fix: resolve linting and type issues in frontend"

---

## Phase 9: Integration Testing

### 9.1 End-to-End Manual Testing
- [ ] Start backend server
- [ ] Start frontend dev server
- [ ] Test adding multiple todos
- [ ] Test marking todos as done/undone
- [ ] Test page refresh (persistence)
- [ ] Verify data in JSON file

### 9.2 Bug Fixes
- [ ] Document any bugs found during testing
- [ ] Fix bugs one at a time with individual commits
- [ ] Retest after each fix

---

## Phase 10: Documentation and Deployment Prep

### 10.1 Documentation
- [ ] Create root README.md with project overview
- [ ] Add setup instructions (npm install, start commands)
- [ ] Document NPM workspace scripts
- [ ] Add architecture overview
- [ ] Document API endpoints
- [ ] Commit: "docs: add project documentation"

### 10.2 Build Configuration
- [ ] Add build script to backend package.json
- [ ] Add build script to frontend package.json
- [ ] Add root-level build script
- [ ] Test production builds
- [ ] Commit: "chore: add production build scripts"

### 10.3 Final Quality Gate
- [ ] Run full quality check script
- [ ] Run all builds
- [ ] Verify no errors or warnings
- [ ] Test built artifacts locally
- [ ] Commit any final fixes

### 10.4 Release Preparation
- [ ] Merge develop branch to main via gitflow release
- [ ] Tag version 1.0.0
- [ ] Push to remote repository

---

## Notes
- Each checkbox represents a small, focused task
- Commit after completing each task or small group of related tasks
- Run quality gates (ESLint + type-check) before each commit
- Create feature branches from develop for each phase if desired
- Test locally after each increment before moving to the next task
