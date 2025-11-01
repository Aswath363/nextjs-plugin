---
model: glm-4.6
allowed-tools: Task, mcp__context7__resolve-library-id, mcp__context7__get-library-docs, mcp__deepwiki__read_wiki_structure, mcp__deepwiki__read_wiki_contents, mcp__deepwiki__ask_question
argument-hint: <component-need> <data-structure> <requirements>
description: Create specific React components with shadcn/ui integration
---

# Component Command

Create specific React components with automatic shadcn/ui selection, TypeScript types, and API integration patterns.

## Arguments

**$1 (Required)**: component-need - Description of what the component should do
**$2 (Required)**: data-structure - The data model the component will work with
**$3 (Optional)**: requirements - Additional specifications and constraints

## Examples

```bash
/component "User data table with sorting and filtering" '{"users": [{"id": "number", "name": "string", "email": "string", "role": "string"}]}' "Add pagination and search functionality"

/component "Product card with image and details" '{"product": {"id": "number", "name": "string", "price": "number", "image": "string", "description": "string"}}' "Make it responsive and add to cart button"

/component "Contact form with validation" '{"contact": {"name": "string", "email": "string", "message": "string"}}' "Add real-time validation and error handling"

/component "Navigation bar with user menu" '{"user": {"name": "string", "avatar": "string"}, "navigation": [{"label": "string", "href": "string"}]}' "Include dark mode toggle and mobile responsiveness"
```

## Component Generation Process

### 1. Requirements Analysis
The `shadcn-architect` will:
- Analyze the component requirements and data structure
- Query shadcn/ui MCP server for optimal base components
- Design component composition and variant strategy
- Plan accessibility and responsive behavior

### 2. API Integration Design
The `api-integration-specialist` will:
- Design how the component interacts with data
- Plan loading and error states
- Define prop interfaces and TypeScript types
- Ensure proper state management patterns

### 3. Best Practices Research
The `context-researcher` will:
- Research current best practices for the component type
- Find implementation examples and patterns
- Identify potential accessibility considerations
- Provide context on performance optimizations

### 4. Implementation Generation
The `nextjs-developer` will:
- Generate the complete component code
- Ensure proper Server/Client component usage
- Implement proper TypeScript types
- Add comprehensive error handling

## Generated Component Features

### Automatic shadcn/ui Integration
- Base components selected from shadcn/ui registry
- Proper theming and styling with Tailwind CSS
- Responsive design patterns
- Accessibility features built-in

### Type Safety
- Complete TypeScript interfaces
- Prop validation and default values
- Generic types for reusable components
- Proper typing for event handlers

### State Management
- Local state with useState/useReducer
- Integration with global state when needed
- Optimistic updates for API interactions
- Proper cleanup and memory management

### Error Handling
- Loading states and skeletons
- Error boundaries and fallbacks
- Validation feedback
- Graceful degradation patterns

## Component Structure Examples

### Data Table Component
```tsx
// Generated component structure
components/data-display/user-table.tsx
├── TypeScript interfaces
├── shadcn/ui Table components
├── Sorting and filtering logic
├── Pagination controls
├── Loading skeleton
└── Error handling
```

### Form Component
```tsx
// Generated component structure
components/forms/contact-form.tsx
├── Form validation schema
├── shadcn/ui Form components
├── Real-time validation
├── Submit handling
├── Loading and error states
└── Success/error feedback
```

### Card Component
```tsx
// Generated component structure
components/data-display/product-card.tsx
├── TypeScript props interface
├── shadcn/ui Card components
├── Image optimization
├── Interactive elements
├── Responsive layout
└── Accessibility features
```

## Quality Assurance

Each generated component includes:

- **Comprehensive TypeScript typing**
- **Responsive design with Tailwind CSS**
- **Accessibility compliance (WCAG guidelines)**
- **Error handling and loading states**
- **Performance optimizations**
- **Documentation and usage examples**
- **Integration hooks for easy consumption**

## Usage Integration

Generated components are designed to:
- Work seamlessly with your existing application
- Integrate with your state management solution
- Support Server/Client component patterns
- Include proper data fetching hooks
- Provide consistent API interfaces

Invoke the shadcn-architect agent with: $ARGUMENTS