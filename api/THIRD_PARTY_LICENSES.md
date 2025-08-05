# Third-Party Components and Open Source Software License Report
## Harold API Server

**Document Date:** August 1, 2025  
**Application Version:** 1.0.0  
**Repository:** harold-waste/harold-api  
**Branch:** staging-v2  

---

## Executive Summary

This document provides a comprehensive list of all third-party modules, proprietary components, and open source software incorporated into the Harold API server. The application is built using Node.js with TypeScript and includes numerous third-party services and open source dependencies.

---

## License Distribution Summary

| License Type | Count | Percentage |
|--------------|-------|------------|
| MIT | 1,778 | ~80% |
| Apache-2.0 | 133 | ~6% |
| ISC | 126 | ~6% |
| BSD-3-Clause | 96 | ~4% |
| BSD-2-Clause | 34 | ~2% |
| Custom License | 1 | <1% |
| UNLICENSED | 1 | <1% |
| Other | 41 | ~2% |

**Total Dependencies**: 2,210+ packages (including transitive dependencies)

---

## 1. Production Dependencies (72 packages)

### 1.1 Proprietary/Third-Party Services & SDKs

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @apollo/server | ^4.11.0 | MIT | GraphQL server |
| @apollo/server-plugin-response-cache | ^4.1.3 | MIT | Apollo response caching |
| @google-cloud/storage | ^5.0.1 | Apache-2.0 | Google Cloud Storage integration |
| @june-so/analytics-node | ^8.0.0 | MIT | Analytics tracking |
| @knocklabs/node | 0.6.1 | MIT | Multi-channel notifications |
| @luzmo/nodejs-sdk | ^2.0.0 | MIT | Business intelligence and data visualization |
| @magic-sdk/admin | ^1.8.0 | MIT | Magic Link authentication |
| @sendgrid/mail | ^7.4.0 | MIT | Email delivery service |
| @sentry/node | 5.11.1 | BSD-3-Clause | Error tracking and monitoring |
| @slack/webhook | ^5.0.3 | MIT | Slack webhook integration |
| carbone | ^3.2.3 | ⚠️ Custom | Document and report generation |
| dd-trace | ^5.18.0 | Apache-2.0 OR BSD-3-Clause | Application performance monitoring |
| firebase | ^7.14.6 | Apache-2.0 | Firebase services integration |
| permitio | ^2.0.2 | MIT | Authorization and permissions management |

### 1.2 GraphQL & API Framework

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @graphql-tools/load-files | ^7.0.0 | MIT | GraphQL file loading |
| @graphql-tools/merge | ^9.0.7 | MIT | GraphQL schema merging |
| @graphql-tools/schema | ^10.0.6 | MIT | GraphQL schema utilities |
| express | ^4.18.3 | MIT | Web framework |
| express-rate-limit | ^7.5.0 | MIT | Rate limiting middleware |
| graphql | 17.0.0-alpha.2 | MIT | GraphQL implementation |
| graphql-jit | ^0.7.1 | MIT | GraphQL execution optimization |
| graphql-scalars | ^1.5.0 | MIT | Custom GraphQL scalar types |
| graphql-tag | ^2.11.0 | MIT | GraphQL template literals |

### 1.3 Database & ORM

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @wwwouter/typed-knex | ^4.4.0 | MIT | TypeScript support for Knex |
| ioredis | ^5.4.1 | MIT | Redis client |
| ioredis-mock | 7.4.0 | MIT | Redis mocking for tests |
| knex | 0.95.6 | MIT | SQL query builder |
| pg | ^8.6.0 | MIT | PostgreSQL client |
| prisma | ^4.9.0 | Apache-2.0 | Database toolkit |
| redis-dataloader | ^1.0.2 | MIT | Redis-backed DataLoader |
| sql-tag | ^1.0.1 | MIT | SQL template literals |

### 1.4 Security & Authentication

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| bcrypt | ^5.1.0 | MIT | Password hashing |
| google-auth-library | ^9.11.0 | Apache-2.0 | Google authentication |
| helmet | ^8.0.0 | MIT | Security middleware |
| jsonwebtoken | ^8.5.1 | MIT | JWT implementation |
| jwt-decode | ^3.1.2 | MIT | JWT decoding |

### 1.5 File Processing & Storage

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| basic-ftp | ^4.6.6 | MIT | FTP client |
| pdf-lib | ^1.17.1 | MIT | PDF generation and manipulation |
| ssh2-sftp-client | ^8.0.0 | MIT | SFTP client |
| xlsx | ^0.16.8 | Apache-2.0 | Excel file processing |

### 1.6 Data Processing & Utilities

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| axios | ^0.19.0 | MIT | HTTP client |
| base-64 | ^0.1.0 | MIT | Base64 encoding/decoding |
| bluebird | ^3.7.2 | MIT | Promise library |
| body-parser | ^1.19.0 | MIT | Request body parsing |
| chalk | ^2.4.2 | MIT | Terminal string styling |
| chunk-promise | ^1.2.1 | MIT | Promise chunking utility |
| compression | ^1.7.4 | MIT | Response compression |
| concurrency-promise | ^1.0.1 | MIT | Promise concurrency control |
| core-js | ^3.6.5 | MIT | JavaScript standard library |
| cors | ^2.8.5 | MIT | CORS middleware |
| dataloader | ^2.0.0 | MIT | Data loading utility |
| easy-soap-request | ^4.1.3 | MIT | SOAP client |
| handlebars | ^4.7.8 | MIT | Template engine |
| handlebars-utils | ^1.0.6 | MIT | Handlebars utilities |
| lodash | ^4.17.15 | MIT | Utility library |
| moment | ^2.24.0 | MIT | Date manipulation |
| moment-business-days | ^1.2.0 | MIT | Business day calculations |
| moment-timezone | ^0.5.33 | MIT | Timezone support |
| node-fetch | ^2.6.0 | MIT | Fetch API implementation |
| numeral | ^2.0.6 | MIT | Number formatting |
| object-hash | ^2.0.3 | MIT | Object hashing |
| path | ^0.12.7 | MIT | Path utilities |
| tiny-lru | ^7.0.6 | MIT | LRU cache implementation |
| to-words | ^3.4.0 | MIT | Number to words conversion |
| ts-deepmerge | ^1.0.6 | MIT | Deep object merging |
| uuid | ^9.0.0 | MIT | UUID generation |
| winston | ^3.3.3 | MIT | Logging library |
| xml-js | ^1.6.11 | MIT | XML processing |
| xmlbuilder | ^15.1.1 | MIT | XML builder |

### 1.7 Message Queue & Communication

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| amqplib | ^0.7.1 | MIT | RabbitMQ client |

### 1.8 Task Scheduling

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| cron | ^1.8.2 | MIT | Cron job scheduling |
| cron-parser | ^3.3.0 | MIT | Cron expression parsing |

### 1.9 Location Services

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| google-place-provider | ^1.3.4 | MIT | Google Places API integration |

---

## 2. Development Dependencies (54 packages)

### 2.1 TypeScript & Compilation

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @babel/core | ^7.2.0 | MIT | Babel compiler core |
| @babel/plugin-proposal-class-properties | ^7.10.4 | MIT | Babel plugin |
| @babel/plugin-proposal-decorators | ^7.6.0 | MIT | Babel plugin |
| @babel/plugin-proposal-nullish-coalescing-operator | ^7.8.3 | MIT | Babel plugin |
| @babel/plugin-proposal-optional-chaining | ^7.6.0 | MIT | Babel plugin |
| @babel/preset-env | ^7.2.0 | MIT | Babel environment preset |
| @babel/preset-typescript | ^7.10.4 | MIT | TypeScript preset |
| @babel/types | ^7.11.5 | MIT | Babel AST types |
| babel-eslint | ^10.1.0 | MIT | Babel ESLint parser |
| babel-jest | ^26.6.1 | MIT | Babel Jest transformer |
| babel-loader | ^8.0.4 | MIT | Babel webpack loader |
| ts-jest | ^26.4.2 | MIT | TypeScript support for Jest |
| ts-loader | ^8.0.4 | MIT | TypeScript loader for Webpack |
| ts-node | ^10.9.2 | MIT | TypeScript execution |
| ts-node-dev | ^1.0.0 | MIT | TypeScript development server |
| typescript | 4.9.5 | Apache-2.0 | TypeScript compiler |

### 2.2 GraphQL Code Generation

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @graphql-codegen/cli | ^2.3.0 | MIT | GraphQL code generation CLI |
| @graphql-codegen/fragment-matcher | ^3.2.0 | MIT | GraphQL fragment matcher |
| @graphql-codegen/introspection | ^2.1.0 | MIT | GraphQL introspection |
| @graphql-codegen/typescript | ^2.4.1 | MIT | TypeScript code generation |
| @graphql-codegen/typescript-operations | ^2.2.1 | MIT | TypeScript operations |
| @graphql-inspector/cli | ^3.4.16 | MIT | GraphQL schema inspection |
| @graphql-inspector/core | ^4.2.1 | MIT | GraphQL inspection core |

### 2.3 Testing Framework

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @jest/test-sequencer | ^25.1.0 | MIT | Test sequencing |
| jest | ^26.6.1 | MIT | Testing framework |
| jest-fetch-mock | ^3.0.3 | MIT | Fetch mocking for Jest |
| jest-transform-graphql | ^2.1.0 | MIT | GraphQL transformer for Jest |

### 2.4 Code Quality & Linting

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @typescript-eslint/eslint-plugin | ^5.2.0 | MIT | TypeScript ESLint plugin |
| @typescript-eslint/parser | ^5.2.0 | BSD-2-Clause | TypeScript ESLint parser |
| eslint | ^7.10.0 | MIT | JavaScript linter |
| eslint-config-airbnb | ^16.1.0 | MIT | Airbnb ESLint configuration |
| eslint-import-resolver-typescript | ^2.3.0 | ISC | TypeScript resolver for ESLint |
| eslint-plugin-deprecation | ^2.0.0 | MIT | Deprecation ESLint plugin |
| eslint-plugin-import | ^2.9.0 | MIT | Import ESLint plugin |
| eslint-plugin-jsx-a11y | ^6.2.3 | MIT | Accessibility ESLint plugin |
| eslint-plugin-react | ^7.14.3 | MIT | React ESLint plugin |
| eslint-plugin-sort-keys-fix | ^1.1.1 | MIT | Sort keys ESLint plugin |
| prettier | ^2.1.2 | MIT | Code formatter |
| sql-formatter | ^4.0.2 | ISC | SQL code formatter |

### 2.5 Build Tools & Bundling

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| thread-loader | ^3.0.4 | MIT | Multi-threaded webpack loader |
| util | ^0.12.5 | MIT | Node.js util module |
| webpack | ^5.64.2 | MIT | Module bundler |
| webpack-cli | ^4.9.1 | MIT | Webpack CLI |
| webpack-node-externals | ^2.5.2 | MIT | Webpack externals for Node.js |

### 2.6 Development Utilities

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| clinic | ^13.0.0 | MIT | Performance monitoring |
| nodemon | ^2.0.6 | MIT | Development server monitoring |
| npm-run-all | ^4.1.5 | MIT | Parallel script runner |
| omit-deep-lodash | ^1.1.6 | MIT | Deep object omission |
| patch-package | ^6.2.2 | MIT | Package patching tool |
| postinstall | ^0.7.0 | MIT | Postinstall script runner |
| postinstall-postinstall | ^2.1.0 | MIT | Postinstall helper |
| timezone-mock | ^1.3.4 | MIT | Timezone mocking for tests |

### 2.7 Database Tools

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| database-types | Custom Fork | BSD-3-Clause | Custom database type definitions (Harold Waste fork) |

### 2.8 TypeScript Definitions

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @types/amqplib | ^0.5.13 | MIT | TypeScript definitions |
| @types/axios | ^0.14.0 | MIT | TypeScript definitions |
| @types/base-64 | ^0.1.3 | MIT | TypeScript definitions |
| @types/bcrypt | ^3.0.0 | MIT | TypeScript definitions |
| @types/cors | ^2.8.17 | MIT | TypeScript definitions |
| @types/cron | ^1.7.2 | MIT | TypeScript definitions |
| @types/easy-soap-request | ^4.1.0 | MIT | TypeScript definitions |
| @types/express | ^4.17.8 | MIT | TypeScript definitions |
| @types/ioredis | ^4.17.4 | MIT | TypeScript definitions |
| @types/jest | ^26.0.15 | MIT | Jest TypeScript definitions |
| @types/jsonwebtoken | ^8.5.0 | MIT | TypeScript definitions |
| @types/lodash | 4.14.165 | MIT | Lodash TypeScript definitions |
| @types/node | 18.19.1 | MIT | Node.js TypeScript definitions |
| @types/node-fetch | ^3.0.3 | MIT | TypeScript definitions |
| @types/numeral | ^0.0.28 | MIT | TypeScript definitions |
| @types/object-hash | ^1.3.3 | MIT | TypeScript definitions |
| @types/omit-deep-lodash | ^1.1.1 | MIT | TypeScript definitions |
| @types/ssh2-sftp-client | ^7.0.1 | MIT | TypeScript definitions |
| @types/uuid | ^9.0.2 | MIT | TypeScript definitions |

---

## 3. Patched Dependencies

The following packages have been modified with custom patches located in the `/patches` directory:

| Package | Version | Patch File | Purpose |
|---------|---------|------------|---------|
| @knocklabs/node | 0.6.1 | @knocklabs+node+0.6.1.patch | Custom modifications for Harold Waste integration |
| @types/lodash | 4.14.165 | @types+lodash+4.14.165.patch | Custom TypeScript definitions |
| knex | 0.95.6 | knex+0.95.6.patch | Custom database query modifications |

---

## 5. REST API Third-Party Service Integrations

The Harold API server includes several REST endpoints that integrate with external third-party services. These integrations require active service agreements and API access:

### 5.1 Direct API Integrations (Non-NPM)

| Service | Integration Type | API Endpoints | Description | Documentation |
|---------|------------------|---------------|-------------|---------------|
| **Weavy** | Direct REST API | `/weavy-token` | Collaboration platform integration for user authentication and token management | [Weavy API Documentation](https://www.weavy.com/docs) |
| **Shipsy** | Webhook/API Integration | `/container-tracking`, `/shipment-tracking` | Logistics and supply chain tracking platform for container and shipment monitoring | [Shipsy Platform](https://shipsy.io/) |
| **SendGrid** | Webhook Receiver | `/sendgrid` | Email event tracking and status updates via webhooks | [SendGrid Event Webhook](https://docs.sendgrid.com/for-developers/tracking-events/event) |

### 5.2 Service Integration Details

#### 5.2.1 Weavy Integration
- **Purpose**: Provides collaboration and communication features
- **Implementation**: Direct API calls using axios
- **Environment Variables**: `WEAVY_URL`, `WEAVY_KEY`
- **Authentication**: Bearer token-based authentication
- **Features**: User management, token generation for client-side integration

#### 5.2.2 Shipsy Integration
- **Purpose**: Logistics tracking and supply chain management
- **Implementation**: Webhook receivers for tracking updates
- **Database Integration**: `shipsy_org_to_jules_org` table for organization mapping
- **Features**: Container tracking, shipment tracking, ETA updates
- **Slack Integration**: Automated notifications via Slack webhook

#### 5.2.3 SendGrid Webhook Integration
- **Purpose**: Email delivery status tracking
- **Implementation**: Webhook receiver for email events
- **Features**: Mail tracking, delivery status updates, shared suggestion notifications
- **Event Types**: Delivery, bounce, open, click, unsubscribe events

### 5.3 Security Considerations

1. **API Key Management**: All service integrations use environment variables for API key storage
2. **Organization Filtering**: Middleware implementation for organization-based access control
3. **Webhook Validation**: Input validation and error handling for incoming webhook data
4. **Rate Limiting**: Express rate limiting middleware applied to REST endpoints

---

## 6. Proprietary/Custom Components

### 6.1 Harold Waste Proprietary Components

| Component | Source | License | Description |
|-----------|--------|---------|-------------|
| database-types | https://github.com/harold-waste/database-types#7fbd7fd6bb9abee70d1615c419a9989c369a2485 | BSD-3-Clause | Custom database type definitions for Harold Waste (Fork of Gajus Kuizinas' work) |

---

## 7. License Summary

### 7.1 Critical License Requirements

#### ⚠️ IMPORTANT: Custom Proprietary License
- **Carbone (carbone@3.5.6)**: Uses a custom proprietary license available at https://carbone.io/
- **Legal Review Required**: This package requires legal review and may have usage restrictions

### 7.2 Third-Party Service Provider

The following third-party services require valid service agreements:

| Service | Package | Agreement Type | API Documentation |
|---------|---------|----------------|-------------------|
| Google Cloud Platform | @google-cloud/storage, google-auth-library, google-place-provider | Service Agreement | [Cloud Storage API](https://cloud.google.com/storage/docs/apis), [Auth Library](https://cloud.google.com/docs/authentication), [Places API](https://developers.google.com/maps/documentation/places/web-service) |
| SendGrid/Twilio | @sendgrid/mail | Service Agreement | [SendGrid API](https://docs.sendgrid.com/api-reference) |
| Sentry | @sentry/node | Service Agreement | [Sentry API](https://docs.sentry.io/api/) |
| Datadog | dd-trace | Service Agreement | [Datadog APM](https://docs.datadoghq.com/tracing/) |
| Magic Labs | @magic-sdk/admin | Service Agreement | [Magic Admin API](https://magic.link/docs) |
| Slack | @slack/webhook | Service Agreement | [Slack Webhooks API](https://api.slack.com/messaging/webhooks) |
| Firebase | firebase | Service Agreement | [Firebase API](https://firebase.google.com/docs/reference) |
| Permit.io | permitio | Service Agreement | [Permit.io API](https://docs.permit.io/) |
| Luzmo | @luzmo/nodejs-sdk | Service Agreement | [Luzmo API](https://developer.luzmo.com/api/overview) |
| Knock Labs | @knocklabs/node | Service Agreement | [Knock API](https://docs.knock.app/reference) |
| Weavy | Direct API Integration | Service Agreement | [Weavy API](https://www.weavy.com/docs) |
| Shipsy | Direct API Integration | Service Agreement | [Shipsy Logistics Platform](https://shipsy.io/) |

### 7.3 License Compatibility Analysis

| License Category | Risk Level | Notes |
|------------------|------------|-------|
| MIT (1,778 packages) | ✅ Low | Most permissive, commercial use allowed |
| Apache-2.0 (133 packages) | ✅ Low | Permissive with patent grants |
| ISC (126 packages) | ✅ Low | Similar to MIT |
| BSD-3-Clause (96 packages) | ✅ Low | Permissive with attribution requirement |
| BSD-2-Clause (34 packages) | ✅ Low | Permissive with attribution requirement |
| Custom License (1 package) | ⚠️ High | Carbone requires legal review |
| UNLICENSED (1 package) | ⚠️ Medium | Unclear licensing status |

---

## 8. Compliance Notes

### 8.1 Required Attributions

The following actions are required for license compliance:

1. **Apache-2.0 Components**: Include full license text in distribution
2. **MIT Components**: Include copyright notices and license text
3. **BSD Components**: Include copyright notices and license terms
4. **Custom Patches**: Document and maintain all applied patches

### 8.2 Copyleft Assessment

✅ **No GPL Dependencies**: No copyleft licenses were identified in the dependency tree, meaning there are no obligations to open-source the Harold API code.

### 8.3 Patent Considerations

Apache-2.0 licensed components include explicit patent grants, providing protection against patent litigation.

---

## 9. Maintenance Recommendations

### 9.1 Immediate Actions Required

1. **Legal Review**: Review Carbone custom license terms
2. **Service Agreements**: Ensure all third-party service agreements are current
3. **Patch Documentation**: Document purpose and necessity of all custom patches

### 7.2 Ongoing Maintenance

1. **Quarterly License Audits**: Review new dependencies and license changes
2. **Automated Scanning**: Implement license scanning in CI/CD pipeline
3. **Version Monitoring**: Monitor dependency updates for license changes
4. **Security Updates**: Maintain regular updates while preserving patches
5. **Custom Fork Maintenance**: Keep database-types fork updated and documented

### 7.3 Risk Mitigation

1. **Carbone Alternative**: Consider alternatives to Carbone with standard open source licenses
2. **Service Diversification**: Plan for service provider changes
3. **Patch Reduction**: Work to eliminate custom patches where possible
4. **License Monitoring**: Track license changes in dependency updates

---

*This report was automatically generated on August 1, 2025, and reflects the current state of the Harold API server's dependencies as of commit staging-v2.*
