# React API Builder Marketplace

[![Plugin](https://img.shields.io/badge/plugin-1-blue?style=flat-square)](https://github.com/your-username/react-api-builder-marketplace/tree/main/plugins)
[![Agents](https://img.shields.io/badge/agents-4-green?style=flat-square)](https://github.com/your-username/react-api-builder-marketplace/tree/main/plugins/react-api-builder/agents)
[![Commands](https://img.shields.io/badge/commands-3-orange?style=flat-square)](https://github.com/your-username/react-api-builder-marketplace/tree/main/plugins/react-api-builder/commands)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)](./LICENSE)

**GLM-4.6 powered React/Next.js frontend development with API integration**

A specialized plugin marketplace for building complete React/Next.js applications from API endpoints using GLM-4.6, shadcn/ui, Context7, and DeepWiki integration.

## 🚀 Quick Start

```bash
# Install the marketplace
/plugin marketplace add your-username/react-api-builder-marketplace

# The plugin is automatically available!
```

## 📦 Plugin: React API Builder

### Overview

Build complete React/Next.js applications from API endpoints with automatic component selection, API integration, and modern patterns using GLM-4.6.

### Key Features

- **API-First Development**: Accept API endpoints with request/response models
- **GLM-4.6 Powered**: All agents use GLM-4.6 for intelligent code generation
- **shadcn/ui Integration**: Automatic component selection and installation
- **Context7 & DeepWiki**: Research best practices and implementation patterns
- **Type Safety**: Complete TypeScript throughout
- **Modern Next.js**: App Router, Server Components, performance optimization

### Commands

#### `/build` - Complete Application Builder
Build complete React/Next.js applications from API endpoints.

**Usage:**
```bash
/build "api-endpoint" "request-model" "response-model" "requirements"
```

**Examples:**
```bash
/build "https://api.example.com/users" '{"name": "string", "email": "string"}' '{"id": "number", "name": "string", "email": "string"}' "Create user management dashboard"

/build "POST /api/auth/login" '{"username": "string", "password": "string"}' '{"token": "string", "user": {"id": "number", "name": "string"}}' "Build authentication flow"
```

#### `/component` - Component Generator
Create specific React components with shadcn/ui integration.

**Usage:**
```bash
/component "component-need" "data-structure" "requirements"
```

**Examples:**
```bash
/component "User data table with sorting" '{"users": [{"id": "number", "name": "string", "email": "string"}]}' "Add pagination and search"

/component "Product card with image" '{"product": {"id": "number", "name": "string", "price": "number", "image": "string"}}' "Make it responsive"
```

#### `/research` - Documentation Researcher
Research best practices and implementation patterns using Context7 and DeepWiki.

**Usage:**
```bash
/research "research-topic" "context" "specific-questions"
```

**Examples:**
```bash
/research "React Query data fetching patterns" "Next.js app router" "How to handle optimistic updates?"

/research "shadcn/ui component customization" "dark theme implementation" "Best practices for custom variants?"
```

## 🤖 GLM-4.6 Powered Agents

### API Integration Specialist
- **Expertise**: API integration, data flow architecture, state management
- **Focus**: Type-safe API clients, error handling, caching strategies
- **Tools**: Context7, DeepWiki for research and patterns

### shadcn Architect
- **Expertise**: shadcn/ui components, MCP server integration
- **Focus**: Component selection, composition patterns, accessibility
- **Tools**: shadcn/ui MCP server for component queries and installation

### Next.js Developer
- **Expertise**: Next.js 15, App Router, Server Components
- **Focus**: Application architecture, performance optimization
- **Tools**: Context7 for latest Next.js patterns and best practices

### Context Researcher
- **Expertise**: Documentation research, knowledge synthesis
- **Focus**: Context7 and DeepWiki MCP integration
- **Tools**: Both Context7 and DeepWiki for comprehensive research

## 🎯 Use Cases

### E-commerce Application
```bash
/build "GET /api/products" '{"category": "string"}' '{"products": [{"id": "number", "name": "string", "price": "number"}]}' "Product management dashboard with CRUD operations"
```

### Authentication System
```bash
/build "POST /api/auth/login" '{"email": "string", "password": "string"}' '{"token": "string", "user": {"id": "number", "name": "string"}}' "Complete authentication system with forms and protected routes"
```

### Analytics Dashboard
```bash
/build "GET /api/analytics" '{"dateRange": "string"}' '{"metrics": {"visitors": "number", "pageViews": "number", "conversion": "number"}}' "Analytics dashboard with charts and data visualization"
```

## 📁 Generated Project Structure

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

## 🔧 Integration Features

### MCP Server Integration
- **shadcn/ui MCP Server**: Component selection and installation
- **Context7 MCP**: Up-to-date documentation research
- **DeepWiki MCP**: Community knowledge and patterns

### Automatic Features
- **Component Selection**: Intelligent shadcn/ui component choice based on data patterns
- **API Integration**: Type-safe clients, error handling, loading states
- **Performance**: Core Web Vitals optimization, code splitting
- **Accessibility**: WCAG compliance and screen reader support

## 🚀 Installation

### Option 1: Complete Marketplace (Recommended)
```bash
# Install the marketplace
/plugin marketplace add your-username/react-api-builder-marketplace
```

### Option 2: Individual Plugin
```bash
# Install just the react-api-builder plugin
/plugin install your-username/react-api-builder-marketplace/plugins/react-api-builder
```

## 📋 Requirements

### Prerequisites
- **Claude Code**: Latest version with plugin support
- **Node.js**: 18+ (for shadcn/ui CLI)
- **shadcn/ui MCP Server**: Configured automatically
- **Context7 & DeepWiki**: MCP integration

### MCP Server Setup

The plugin will automatically configure the necessary MCP servers:

**shadcn/ui MCP Server:**
```bash
npx shadcn@latest mcp init --client claude
```

**Context7 & DeepWiki:**
These are built into the plugin workflow and used automatically during research phases.

## 🎨 Examples

### Complete CRUD Application
```bash
# Build user management system
/build "https://api.example.com/users" '{"name": "string", "email": "string", "role": "string"}' '{"users": [{"id": "number", "name": "string", "email": "string", "role": "string", "created_at": "string"}]}' "Complete user management dashboard with create, read, update, delete operations, search, filtering, and pagination"
```

This generates:
- User list with data table
- Create user form with validation
- Edit user functionality
- Delete confirmation dialogs
- Search and filter controls
- Pagination component
- Loading and error states
- TypeScript interfaces
- API integration hooks

### Component Generation
```bash
# Specific component for data display
/component "Analytics card with metrics" '{"metrics": {"visitors": {"count": "number", "change": "number"}, "pageViews": {"count": "number", "change": "number"}}}' "Include trend indicators and responsive design"
```

## 🔒 Quality Assurance

Each generated application includes:

- **Type Safety**: Complete TypeScript interfaces and validation
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Accessibility**: WCAG 2.1 AA compliance
- **Performance**: Optimized for Core Web Vitals
- **Error Handling**: Comprehensive error states and user feedback
- **Security**: Input validation and XSS protection

## 🤝 Contributing

We welcome contributions to the React API Builder marketplace!

### Adding New Features
1. Fork the repository
2. Create your feature branch
3. Add your improvements to the plugin
4. Submit a pull request

### Reporting Issues
Found a bug or have a feature request? Please [open an issue](https://github.com/your-username/react-api-builder-marketplace/issues) on GitHub.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

## 🔗 Links

- **Marketplace**: https://github.com/your-username/react-api-builder-marketplace
- **Issues**: [Report Problems](https://github.com/your-username/react-api-builder-marketplace/issues)
- **Discussions**: [Community Forum](https://github.com/your-username/react-api-builder-marketplace/discussions)

---

**Transform your API endpoints into complete React/Next.js applications with GLM-4.6 intelligence!** 🚀

Install the marketplace and start building production-ready applications from your API specifications in minutes.