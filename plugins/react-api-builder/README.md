# React API Builder

**GLM-4.6 powered React/Next.js frontend development with API integration**

A specialized plugin for building complete React/Next.js applications from API endpoints using GLM-4.6, shadcn/ui, Context7, and DeepWiki integration.

## 🎯 Commands

- **`/build`** - Build complete React/Next.js applications from API endpoints
- **`/component`** - Create specific React components with shadcn/ui integration
- **`/research`** - Research best practices and implementation patterns

## 🚀 Quick Start

### Installation

```bash
# Add the plugin to your Claude Code instance
# Copy the plugin files to your Claude plugins directory
# Restart Claude Code to load the new plugin
```

### Basic Usage

```bash
# Build a complete application from an API endpoint
/build "https://api.example.com/users" '{"name": "string", "email": "string"}' '{"id": "number", "name": "string", "email": "string"}' "Create user management dashboard with CRUD operations"

# Create a specific component
/component "User data table with sorting" '{"users": [{"id": "number", "name": "string", "email": "string"}]}' "Add pagination and search"

# Research best practices
/research "React Query data fetching patterns" "Next.js app router" "How to handle optimistic updates?"
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

## 🔧 Key Features

### API-First Development
- Accept API endpoints with request/response models
- Generate type-safe API clients automatically
- Implement proper error handling and loading states
- Support for REST APIs and GraphQL

### shadcn/ui Integration
- Automatic component selection from shadcn/ui registry
- MCP server integration for component queries
- Responsive design with Tailwind CSS
- Accessibility and dark mode support

### Modern Next.js Patterns
- App Router with Server/Client components
- Optimized data fetching and caching
- Performance and SEO optimization
- TypeScript throughout

### Research-Powered Development
- Context7 integration for up-to-date documentation
- DeepWiki access to real-world implementation patterns
- Best practices synthesis from multiple sources
- Continuous learning from community knowledge

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

## 🎨 Component Examples

### Data Table Component
```tsx
// Auto-generated with shadcn/ui integration
import { DataTable } from "@/components/ui/data-table"
import { columns } from "./columns"

interface UserTableProps {
  data: User[]
  loading?: boolean
}

export function UserTable({ data, loading }: UserTableProps) {
  return (
    <DataTable
      columns={columns}
      data={data}
      loading={loading}
      searchable={true}
      sortable={true}
    />
  )
}
```

### Form Component
```tsx
// Auto-generated with validation
import { useForm } from "react-hook-form"
import { zodResolver } from "@hookform/resolvers/zod"
import { Button } from "@/components/ui/button"
import { Form, FormControl, FormField, FormItem, FormLabel, FormMessage } from "@/components/ui/form"

const formSchema = z.object({
  name: z.string().min(2, "Name must be at least 2 characters"),
  email: z.string().email("Invalid email address"),
})

export function UserForm() {
  const form = useForm<z.infer<typeof formSchema>>({
    resolver: zodResolver(formSchema),
  })

  // Form implementation with API integration
}
```

## 🔍 MCP Integration

### shadcn/ui MCP Server
```bash
# Automatic component queries
mcp__shadcn-ui__search_components("data table")
mcp__shadcn-ui__get_component_details("table")
mcp__shadcn-ui__install_component("table")
```

### Context7 MCP Integration
```bash
# Research best practices
mcp__context7__resolve-library-id("react-query")
mcp__context7__get-library-docs("/tanstack/query", "data-fetching")
```

### DeepWiki MCP Integration
```bash
# Access community knowledge
mcp__deepwiki__read_wiki_contents("vercel/next.js")
mcp__deepwiki__ask_question("shadcn-ui/ui", "component patterns")
```

## 📋 Use Cases

### E-commerce Dashboard
```bash
/build "GET /api/products" '{"category": "string"}' '{"products": [{"id": "number", "name": "string", "price": "number"}]}' "Product management dashboard with CRUD operations"
```

### Authentication Flow
```bash
/build "POST /api/auth/login" '{"email": "string", "password": "string"}' '{"token": "string", "user": {"id": "number", "name": "string"}}' "Complete authentication system with forms and protected routes"
```

### Analytics Dashboard
```bash
/build "GET /api/analytics" '{"dateRange": "string"}' '{"metrics": {"visitors": "number", "pageViews": "number", "conversion": "number"}}' "Analytics dashboard with charts and data visualization"
```

## 🛠️ Development Workflow

1. **Provide API Specification**: Give endpoint URLs and data models
2. **Automatic Research**: Plugin researches best practices using Context7/DeepWiki
3. **Component Selection**: shadcn/ui components auto-selected based on data patterns
4. **Code Generation**: Complete Next.js application generated with proper patterns
5. **Quality Assurance**: TypeScript, accessibility, and performance built-in

## 🎯 Benefits

- **Speed**: Build complete applications in minutes, not days
- **Quality**: Modern patterns, TypeScript, and best practices built-in
- **Consistency**: shadcn/ui ensures consistent design system
- **Maintainability**: Clean architecture and proper separation of concerns
- **Performance**: Optimized for Core Web Vitals and modern browsers
- **Accessibility**: WCAG compliance and screen reader support

## 📄 License

MIT License - see LICENSE file for details

## 🌟 Part of Custom Plugin Ecosystem

This is a custom plugin designed specifically for GLM-4.6 integration with modern React/Next.js development workflows, combining the power of:
- **GLM-4.6** for intelligent code generation
- **shadcn/ui** for beautiful, accessible components
- **Context7** for up-to-date documentation
- **DeepWiki** for community knowledge and patterns

---

**Ready to build your next React/Next.js application?** Use the `/build` command with your API endpoint and data models to get started!