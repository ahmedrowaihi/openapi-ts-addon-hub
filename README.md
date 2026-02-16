# OpenAPI TS Addon Hub

A collection of plugins and addons for OpenAPI TS.

## Plugins

- **orpc** - OpenAPI TS oRPC plugin - Generate type-safe RPC clients and servers
- **faker** - OpenAPI TS Faker plugin - Generate realistic mock data factories

## References

This repository references external plugins:

- **orpc** - [OpenAPI TS oRPC Plugin](https://github.com/ahmedrowaihi/openapi-ts-orpc-plugin)

## Getting Started

Clone the repository:
```bash
git clone https://github.com/ahmedrowaihi/openapi-ts-addon-hub.git
```

To use the orpc plugin, clone it separately:
```bash
git clone https://github.com/ahmedrowaihi/openapi-ts-orpc-plugin.git plugins/orpc
```

## Structure

```
openapi-ts/   # Main OpenAPI TS repository
plugins/      # Plugin implementations
├── orpc/     # oRPC plugin (external reference)
└── faker/    # Faker.js mock data generator plugin
```

## Plugin Details

### oRPC Plugin

Generates type-safe oRPC contracts, routers, and clients from OpenAPI specs.

- [Documentation](./plugins/orpc/README.md)
- [npm package](https://www.npmjs.com/package/@ahmedrowaihi/openapi-ts-orpc)

### Faker Plugin

Generates Faker.js factory functions for realistic mock data.

- [Documentation](./plugins/faker/README.md)
- Status: Beta

**Features:**
- Smart field detection (email → faker.internet.email())
- Type-safe factories with overrides
- Batch generators (create multiple objects)
- Respects schema constraints (min/max, etc.)
- Works with MSW, Storybook, tests, and more

**Example:**
```typescript
import { createMockUser } from './generated/faker/factories.gen'

const user = createMockUser({
  email: 'custom@example.com'
})
```
