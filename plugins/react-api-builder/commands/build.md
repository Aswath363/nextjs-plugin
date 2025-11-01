---
model: glm-4.6
allowed-tools: Task, mcp__context7__resolve-library-id, mcp__context7__get-library-docs, mcp__deepwiki__read_wiki_structure, mcp__deepwiki__read_wiki_contents, mcp__deepwiki__ask_question
argument-hint: <api-endpoint> <request-model> <response-model> <requirements>
description: Build complete React/Next.js frontend application from API endpoints
---

# Build Command

Build complete React/Next.js frontend application from API endpoints with automatic component selection, API integration, and modern patterns.

## Arguments

**$1 (Required)**: api-endpoint - The API endpoint URL or description
**$2 (Required)**: request-model - Request payload structure (JSON schema or description)
**$3 (Required)**: response-model - Response payload structure (JSON schema or description)
**$4 (Required)**: requirements - Additional requirements and specifications

## Examples

```bash
/build "https://api.example.com/users" '{"name": "string", "email": "string"}' '{"id": "number", "name": "string", "email": "string", "created_at": "string"}' "Create user management dashboard with CRUD operations"

/build "POST /api/auth/login" '{"username": "string", "password": "string"}' '{"token": "string", "user": {"id": "number", "name": "string"}}' "Build authentication flow with form validation"

/build "GET /api/products/search?q={query}" '{"query": "string"}" '{"products": [{"id": "number", "name": "string", "price": "number"}]}' "Create product search interface with filters"
```

## Workflow

### 1. Analysis & Research Phase
The `context-researcher` will:
- Research best practices for the specific API patterns using Context7
- Find examples of similar implementations using DeepWiki
- Identify optimal libraries and patterns for the use case

### 2. Architecture Design Phase
The `api-integration-specialist` will:
- Analyze the API endpoints and data models
- Design optimal data fetching strategies
- Plan error handling and loading states
- Select appropriate state management approach

### 3. Component Selection Phase
The `shadcn-architect` will:
- Query shadcn/ui MCP server for optimal components
- Design component composition patterns
- Plan responsive layouts and interactions
- Configure component installation strategy

### 4. Next.js Implementation Phase
The `nextjs-developer` will:
- Design the App Router structure
- Implement Server/Client component patterns
- Configure data fetching and caching
- Optimize for performance and SEO

## Generated Application Structure

```
app/
├── layout.tsx              # Root layout with providers
├── page.tsx               # Main application page
├── globals.css            # Global styles and theme
├── components/
│   ├── ui/                # shadcn/ui components (auto-installed)
│   ├── forms/             # Form components for API requests
│   ├── data-display/      # Tables, cards, lists for API data
│   └── layout/            # Layout components
├── lib/
│   ├── api/               # API client configuration
│   ├── hooks/             # Custom React hooks
│   ├── types/             # TypeScript type definitions
│   └── utils/             # Utility functions
└── (dashboard)/           # Route groups for organization
    ├── layout.tsx
    └── page.tsx
```

## Key Features

### Automatic API Integration
- Type-safe API client generation
- Error handling and loading states
- Optimistic updates and caching
- Form validation and submission

### Modern UI Components
- shadcn/ui components auto-selected based on data patterns
- Responsive design with Tailwind CSS
- Dark mode support
- Accessibility features

### Performance Optimization
- Server-side rendering where appropriate
- Code splitting and lazy loading
- Image and font optimization
- Core Web Vitals optimization

### Developer Experience
- TypeScript throughout
- ESLint and Prettier configuration
- Hot reload in development
- Comprehensive error handling

Invoke the multi-agent workflow to build your complete React/Next.js application with: $ARGUMENTS