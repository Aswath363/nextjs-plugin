---
model: glm-4.6
allowed-tools: mcp__context7__resolve-library-id, mcp__context7__get-library-docs, mcp__deepwiki__read_wiki_structure, mcp__deepwiki__read_wiki_contents, mcp__deepwiki__ask_question
argument-hint: <research-topic> [context] [specific-questions]
description: Research best practices, patterns, and implementation approaches using Context7 and DeepWiki
---

# Research Command

Research latest best practices, implementation patterns, and technical documentation using Context7 and DeepWiki MCP integration.

## Arguments

**$1 (Required)**: research-topic - The technology, pattern, or library to research
**$2 (Optional)**: context - Specific context or use case for the research
**$3 (Optional)**: specific-questions - Specific questions to answer during research

## Examples

```bash
/research "React Query data fetching patterns" "Next.js app router" "How to handle optimistic updates with server components?"

/research "shadcn/ui component customization" "dark theme implementation" "What are the best practices for custom variants?"

/research "Next.js 15 performance optimization" "e-commerce dashboard" "How to optimize for Core Web Vitals with dynamic data?"

/research "TypeScript type safety for API responses" "Zod integration" "How to generate types from OpenAPI specs?"

/research "authentication patterns in Next.js" "JWT tokens with middleware" "Best practices for token refresh and session management?"
```

## Research Process

### 1. Context7 Research Phase
The `context-researcher` will:
- Resolve library names to Context7-compatible IDs
- Fetch up-to-date documentation from official sources
- Search for specific implementation patterns
- Get code examples and usage guidelines
- Research library-specific best practices

### 2. DeepWiki Research Phase
The `context-researcher` will:
- Access comprehensive GitHub repository knowledge
- Research real-world implementation examples
- Find community discussions and solutions
- Access advanced technical knowledge
- Synthesize information from multiple projects

### 3. Knowledge Synthesis
The `context-researcher` will:
- Combine information from multiple MCP sources
- Filter outdated information from current patterns
- Identify trends and emerging best practices
- Provide context-aware recommendations
- Create actionable implementation guides

## Research Categories

### Technology Research
- Library and framework documentation
- Version-specific features and changes
- Migration guides and breaking changes
- Performance characteristics and benchmarks

### Pattern Research
- Architectural patterns and approaches
- Implementation best practices
- Anti-patterns and common pitfalls
- Industry standards and conventions

### Integration Research
- Library compatibility and integration patterns
- Configuration and setup guidelines
- Common use cases and solutions
- Troubleshooting and debugging approaches

## Output Structure

Each research session provides:

### 1. Executive Summary
- Key findings and recommendations
- Current best practices summary
- Important considerations and caveats

### 2. Detailed Findings
- Comprehensive documentation synthesis
- Code examples and implementation patterns
- Configuration and setup instructions
- Performance and security considerations

### 3. Practical Recommendations
- Specific implementation guidance
- Tool and library recommendations
- Configuration examples
- Next steps and action items

### 4. References and Sources
- Links to official documentation
- Community resources and tutorials
- Example projects and repositories
- Additional reading and learning materials

## Sample Research Outputs

### React Query Research Example
```markdown
## React Query with Next.js App Router Research

### Key Findings
- Use React Query v5 with React 19 for最佳 compatibility
- Implement proper hydration handling for SSR
- Consider TanStack Query for React Server Components

### Implementation Pattern
```tsx
// Recommended pattern for app router
'use client'

import { useQuery } from '@tanstack/react-query'
import { getServerSession } from 'next-auth'

function UserProfile() {
  const { data: user, isLoading, error } = useQuery({
    queryKey: ['user'],
    queryFn: () => fetch('/api/user').then(res => res.json()),
    staleTime: 5 * 60 * 1000, // 5 minutes
  })

  // Component implementation
}
```

### Recommendations
- Implement proper error boundaries
- Use suspense for loading states
- Configure proper cache strategies
```

## Quality Assurance

Research outputs include:

- **Current and verified information** from official sources
- **Practical code examples** that can be directly used
- **Context-aware recommendations** based on specific use cases
- **Cross-referenced information** from multiple sources
- **Actionable guidance** for immediate implementation

Invoke the context-researcher agent with: $ARGUMENTS