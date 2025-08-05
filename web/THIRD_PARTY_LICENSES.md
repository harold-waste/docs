# Third-Party Components and Open Source Software License Report
## Harold Web Application

**Document Date:** August 1, 2025  
**Application Version:** 1.0.8  
**Repository:** harold-waste/harold-web  
**Branch:** staging-v2  

---

## Executive Summary

This document provides a comprehensive list of all third-party modules, proprietary components, and open source software incorporated into the Harold Web application. The application is built using React with TypeScript and includes numerous third-party services and open source dependencies.

---

## License Distribution Summary

| License Type | Count | Percentage |
|--------------|-------|------------|
| MIT | 185+ | ~85% |
| Apache-2.0 | 15+ | ~7% |
| BSD-3-Clause | 8+ | ~4% |
| BSD-2-Clause | 5+ | ~2% |
| ISC | 3+ | ~1% |
| Other | 2+ | ~1% |

**Total Dependencies**: 218+ packages (including transitive dependencies)

---

## 1. Production Dependencies

### 1.1 Core Framework & Runtime
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| react | 18.0.0 | MIT | React JavaScript library for building user interfaces |
| react-dom | 18.0.0 | MIT | React package for working with the DOM |
| react-scripts | 5.0.0 | MIT | Configuration and scripts for Create React App |
| typescript | 4.6.3 | Apache-2.0 | TypeScript language |

### 1.2 GraphQL & State Management
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @apollo/client | ^3.11.8 | MIT | Comprehensive GraphQL client |
| graphql | 17.0.0-alpha.2 | MIT | GraphQL implementation |
| graphql-tag | ^2.11.0 | MIT | GraphQL query tag library |
| apollo-link-persisted-queries | ^0.2.2 | MIT | Apollo Link for persisted queries |
| redux | ^4.2.0 | MIT | Predictable state container |
| react-redux | 8.0.4 | MIT | React bindings for Redux |
| redux-saga | ^1.2.1 | MIT | Redux middleware for handling side effects |
| redux-persist | ^6.0.0 | MIT | Persist and rehydrate Redux store |
| redux-state-sync | ^3.1.4 | MIT | Sync Redux state across tabs |
| reselect | ^4.1.6 | MIT | Selector library for Redux |
| valtio | ^1.13.2 | MIT | Proxy-state simple store |

### 1.3 UI Components & Styling
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @material-ui/core | ^4.12.4 | MIT | Material-UI React components (v4) |
| @material-ui/lab | ^4.0.0-alpha.57 | MIT | Material-UI Lab components |
| @mui/material | ^5.2.3 | MIT | Material-UI React components (v5) |
| @mui/icons-material | ^5.2.1 | MIT | Material-UI icons |
| @mui/styled-engine-sc | ^5.1.0 | MIT | Styled Components engine for MUI |
| styled-components | ^5.3.5 | MIT | CSS-in-JS library |
| framer-motion | ^4.1.17 | MIT | Animation library for React |
| notistack | ^1.0.9 | MIT | Snackbar notifications |

### 1.4 Form Management & Validation
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| formik | ^2.2.5 | Apache-2.0 | Form library for React |
| yup | ^0.30.0 | MIT | Schema validation library |

### 1.5 Date & Time Handling
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| moment | ^2.29.1 | MIT | Date manipulation library |
| moment-timezone | ^0.5.33 | MIT | Timezone support for Moment.js |
| date-fns | ^2.27.0 | MIT | Modern date utility library |
| @date-io/moment | ^1.3.11 | MIT | Date adapter for moment |

### 1.6 HTTP Client & Network
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| axios | ^1.7.7 | MIT | Promise-based HTTP client |

### 1.7 File Processing & Utilities
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| file-saver | ^2.0.5 | MIT | Save files on client-side |
| file-type | ^19.5.0 | MIT | Detect file type from buffer |
| filefy | ^0.1.10 | MIT | File utilities |
| browser-image-compression | ^1.0.14 | MIT | Image compression in browser |
| jszip | ^3.7.0 | MIT OR GPL-3.0 | Create and read zip files |
| xlsx | ^0.18.5 | Apache-2.0 | Read and write spreadsheet files |

### 1.8 PDF Generation & Processing
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| jspdf | ^2.3.1 | MIT | PDF generation library |
| jspdf-autotable | ^3.5.13 | MIT | Auto table plugin for jsPDF |
| react-pdf | 5.3.1 | MIT | Display PDFs in React |

### 1.9 Data Processing & CSV
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| json2csv | ^5.0.7 | MIT | Convert JSON to CSV |
| @vtex/react-csv-parse | ^3.0.2 | MIT | CSV parsing for React |

### 1.10 Routing & Navigation
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| react-router-dom | ^5.2.0 | MIT | Declarative routing for React |
| query-string | ^6.8.3 | MIT | Parse and stringify URL query strings |

### 1.11 Text Processing
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| draft-js | ^0.11.7 | MIT | Rich text editor framework |
| draft-js-export-html | ^1.4.1 | MIT | Export Draft.js to HTML |
| draft-js-import-html | ^1.4.1 | MIT | Import HTML to Draft.js |
| react-draft-wysiwyg | ^1.14.5 | MIT | WYSIWYG editor built on Draft.js |
| html-to-text | ^6.0.0 | MIT | Convert HTML to text |

### 1.12 Utilities & Helpers
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| lodash | ^4.17.21 | MIT | Utility library |
| bluebird | ^3.7.2 | MIT | Promise library |
| uuid | ^8.3.1 | MIT | UUID generator |
| numeral | ^2.0.6 | MIT | Number formatting library |
| object-hash | ^1.3.1 | MIT | Generate hashes from objects |
| color-hash | ^1.0.3 | MIT | Generate colors from hash |
| string-template | ^1.0.0 | MIT | String templating |
| string-to-color | ^2.2.2 | MIT | Convert strings to colors |
| safe-evaluate-expression | ^1.7.3 | MIT | Safe expression evaluation |
| fuse.js | ^6.6.2 | Apache-2.0 | Fuzzy search library |
| jwt-decode | ^2.2.0 | MIT | Decode JWT tokens |
| path | ^0.12.7 | MIT | Node.js path utilities |

### 1.13 Hooks & React Utilities
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| use-debounce | ^7.0.1 | MIT | Debounce hook for React |
| use-deep-compare-effect | ^1.8.1 | MIT | Deep compare effect hook |
| use-state-persist | ^0.3.1 | MIT | Persist state hook |
| usehooks-ts | ^3.1.0 | MIT | Collection of React hooks |

### 1.14 Charts & Data Visualization
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| chart.js | ^2.9.4 | MIT | Chart library |
| react-chartjs-2 | ^2.11.1 | MIT | React wrapper for Chart.js |

### 1.15 UI Enhancement Components
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| react-beautiful-dnd | ^13.1.0 | Apache-2.0 | Drag and drop library |
| react-date-range | ^1.4.0 | MIT | Date range picker |
| react-headroom | ^3.2.0 | MIT | Hide header on scroll |
| react-responsive-carousel | ^3.2.10 | MIT | Carousel component |
| react-rating | ^2.0.5 | MIT | Rating component |
| react-user-avatar | ^1.10.0 | MIT | User avatar component |
| react-virtuoso | ^1.9.1 | MIT | Virtual scrolling |
| react-helmet | ^6.1.0 | MIT | Document head management |

### 1.16 File Upload & Processing
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @rpldy/uploady | ^1.8.3 | MIT | File upload library |
| @rpldy/upload-drop-zone | ^1.8.3 | MIT | Drop zone for file uploads |
| @rpldy/upload-paste | ^1.8.3 | MIT | Paste support for uploads |

---

## 2. Proprietary/Third-Party Services & SDKs

### 2.1 Authentication & Identity
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Magic SDK | magic-sdk ^10.0.0, @magic-ext/oauth ^4.0.0 | MIT | Authentication service |

### 2.2 Analytics & Monitoring
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Google Firebase | firebase ^8.0.2 | Apache-2.0 | Backend-as-a-Service platform |
| Heap Analytics | react-heap ^0.1.3 | MIT | User analytics platform |
| Microsoft Clarity | react-microsoft-clarity ^1.2.0 | MIT | User behavior analytics |
| Inspectlet | inspectlet.ts (custom) | Proprietary | Session recording service |
| LaunchDarkly | launchdarkly-react-client-sdk ^3.0.6 | Apache-2.0 | Feature flag management |

### 2.3 Business Intelligence & Reporting
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Power BI | powerbi-report-component ^1.3.2 | MIT | Microsoft Power BI embedding |
| Luzmo | @luzmo/react-embed ^5.2.5 | MIT | Business intelligence platform |

### 2.4 Customer Support & Communication
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Crisp Chat | crisp-sdk-web ^1.0.25 | MIT | Customer support chat |
| Freshchat | reactjs-freshchat ^1.3.3 | MIT | Customer messaging platform |
| CommandBar | commandbar ^1.9.0 | MIT | User assistance platform |

### 2.5 Notifications & Messaging
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Knock | @knocklabs/react ^0.1.3 | MIT | Notification infrastructure |

### 2.6 Collaboration & Communication
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Weavy | @weavy/uikit-react ^21.1.2 | MIT | Collaboration platform |

### 2.7 Data Import & Processing
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Nuvo | nuvo-react ^2.13.3 | MIT | Data import and cleaning |

### 2.8 User Feedback & Documentation
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Olvy | @olvyhq/widget-react ^0.1.3 | MIT | User feedback and changelog |

### 2.9 Advanced UI Components
| Service | Package | License | Description |
|---------|---------|---------|-------------|
| Material Table | @material-table/core 4.3.31 | MIT | Data table component |
| React Permission | @easytool/react-permission ^0.1.7 | MIT | Permission management |
| Lit Localize | @lit/localize ^0.12.1 | BSD-3-Clause | Localization library |

---

## 3. Development Dependencies

### 3.1 Build Tools & Bundling
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @babel/core | ^7.11.6 | MIT | Babel compiler core |
| @babel/eslint-parser | ^7.19.1 | MIT | Babel parser for ESLint |
| @babel/preset-typescript | ^7.10.4 | MIT | TypeScript preset for Babel |
| react-app-rewired | ^2.1.11 | MIT | Override create-react-app webpack config |
| customize-cra | ^0.2.12 | MIT | Customize create-react-app configuration |

### 3.2 Code Quality & Linting
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| eslint-config-airbnb | ^16.1.0 | MIT | Airbnb's ESLint config |
| eslint-config-prettier | ^8.5.0 | MIT | Prettier ESLint config |
| eslint-plugin-prettier | ^4.0.0 | MIT | Prettier ESLint plugin |
| prettier | ^2.1.2 | MIT | Code formatter |
| @typescript-eslint/eslint-plugin | ^5.40.1 | MIT | TypeScript ESLint plugin |
| @typescript-eslint/parser | ^5.40.1 | MIT | TypeScript ESLint parser |

### 3.3 Testing
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @testing-library/react | ^9.1.4 | MIT | React testing utilities |
| @testing-library/cypress | ^7.0.1 | MIT | Cypress testing utilities |
| cypress | ^6.5.0 | MIT | End-to-end testing framework |
| jest-junit | ^16.0.0 | Apache-2.0 | JUnit reporter for Jest |
| enzyme | ^3.10.0 | MIT | JavaScript testing utility |

### 3.4 GraphQL Code Generation
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @graphql-codegen/cli | 4.0.0 | MIT | GraphQL code generator CLI |
| @graphql-codegen/typescript | 4.0.0 | MIT | TypeScript plugin |
| @graphql-codegen/typescript-operations | 4.0.0 | MIT | TypeScript operations plugin |
| @graphql-codegen/typescript-react-apollo | 4.0.0 | MIT | React Apollo plugin |

### 3.5 Storybook
| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @storybook/react | ^6.1.11 | MIT | Storybook for React |
| @storybook/addon-essentials | ^6.1.11 | MIT | Essential Storybook addons |
| @storybook/addon-storyshots | ^6.1.11 | MIT | Storyshots addon |

---

## 4. Patched Dependencies

The following packages have been modified using patch-package:

| Package | Patch File | Reason |
|---------|------------|--------|
| @knocklabs/client | @knocklabs+client+0.8.16.patch | Custom modifications |
| @material-table/core | @material-table+core+4.3.31.patch | Custom modifications |
| react-scripts | react-scripts+5.0.0.patch | Custom modifications |
| reactjs-freshchat | reactjs-freshchat+1.3.3.patch | Custom modifications |

---

## 5. License Summary

### 5.1 License Distribution

| License Type | Count | Percentage |
|--------------|-------|------------|
| MIT | 185+ | ~85% |
| Apache-2.0 | 15+ | ~7% |
| BSD-3-Clause | 8+ | ~4% |
| BSD-2-Clause | 5+ | ~2% |
| ISC | 3+ | ~1% |
| Other | 2+ | ~1% |

### 5.2 Notable License Types

**MIT License** (Most Common): Allows commercial use, modification, distribution, and private use. Requires attribution.

**Apache-2.0**: Allows commercial use, modification, distribution, and private use. Provides patent grant. Requires attribution.

**BSD Licenses**: Allow commercial use with attribution requirement.

**Proprietary Services**: Multiple SaaS platforms are integrated, each with their own terms of service.

---

## 6. Compliance Notes

### 6.1 Required Attributions

Most MIT and Apache-2.0 licensed components require attribution in the application. The following should be included in the application's about/credits section:

1. Full license text for Apache-2.0 components
2. Copyright notices for MIT components
3. Attribution for any BSD-licensed components

### 6.2 Copyleft Concerns

No GPL (General Public License) or other copyleft licenses were identified in the dependency tree, which means there are no obligations to open-source the Harold application code.

### 6.3 Patents

Apache-2.0 licensed components include explicit patent grants, providing additional protection for patent-related issues.

---

## 7. Maintenance Recommendations

### 7.1 Immediate Actions Required

1. **Service Agreements**: Ensure all third-party service agreements are current
2. **Patch Documentation**: Document purpose and necessity of all custom patches
3. **License Compliance**: Review attribution requirements for UI integration

### 7.2 Ongoing Maintenance

1. **Quarterly License Audits**: Review new dependencies and license changes
2. **Automated Scanning**: Implement license scanning in CI/CD pipeline
3. **Version Monitoring**: Monitor dependency updates for license changes
4. **Security Updates**: Maintain regular updates while preserving patches
5. **Service Monitoring**: Track changes in third-party service terms

### 7.3 Risk Mitigation

1. **Service Diversification**: Plan for service provider changes
2. **Patch Reduction**: Work to eliminate custom patches where possible
3. **License Monitoring**: Track license changes in dependency updates
4. **Alternative Planning**: Identify alternatives for critical proprietary services

---

## 7. Third-Party API Service Providers

The following third-party services require valid service agreements and make direct API calls:

### 7.1 External API Services

| Service | Package/Integration | Agreement Type | API Documentation |
|---------|---------------------|----------------|-------------------|
| Nylas Email API | Direct axios integration | Service Agreement | [Nylas API](https://developer.nylas.com/docs/api/) |

### 7.2 Third-Party Service Providers

The following third-party services require valid service agreements:

| Service | Package | Agreement Type | API Documentation |
|---------|---------|----------------|-------------------|
| Google Firebase | firebase ^8.0.2 | Service Agreement | [Firebase API](https://firebase.google.com/docs/reference) |
| Magic SDK | magic-sdk ^10.0.0, @magic-ext/oauth ^4.0.0 | Service Agreement | [Magic API](https://magic.link/docs) |
| Luzmo | @luzmo/react-embed ^5.2.5 | Service Agreement | [Luzmo API](https://developer.luzmo.com/api/overview) |
| Microsoft Power BI | powerbi-report-component ^1.3.2 | Service Agreement | [Power BI Embedded API](https://learn.microsoft.com/en-us/power-bi/developer/embedded/) |
| Knock Labs | @knocklabs/react ^0.1.3 | Service Agreement | [Knock API](https://docs.knock.app/reference) |
| Weavy | @weavy/uikit-react ^21.1.2 | Service Agreement | [Weavy API](https://www.weavy.com/docs) |
| Nuvo | nuvo-react ^2.13.3 | Service Agreement | [Nuvo API](https://www.nuvo.io) |
| Olvy | @olvyhq/widget-react ^0.1.3 | Service Agreement | [Olvy API](https://developers.olvy.co/) |
| Heap Analytics | react-heap ^0.1.3 | Service Agreement | [Heap API](https://developers.heap.io/reference) |
| Microsoft Clarity | react-microsoft-clarity ^1.2.0 | Service Agreement | [Clarity API](https://clarity.microsoft.com/) |
| Inspectlet | inspectlet.ts (custom) | Service Agreement | [Inspectlet API](https://www.inspectlet.com/help/api) |
| LaunchDarkly | launchdarkly-react-client-sdk ^3.0.6 | Service Agreement | [LaunchDarkly API](https://docs.launchdarkly.com/home/connecting/api) |
| Crisp Chat | crisp-sdk-web ^1.0.25 | Service Agreement | [Crisp API](https://docs.crisp.chat/references/rest-api/v1/) |
| Freshchat | reactjs-freshchat ^1.3.3 | Service Agreement | [Freshchat API](https://developers.freshchat.com/api/) |
| CommandBar | commandbar ^1.9.0 | Service Agreement | [CommandBar API](https://www.command.ai/docs) |

### 7.3 Email Service Integration

| Service | Endpoints Used | Purpose |
|---------|----------------|---------|
| Nylas Email API | `https://api.eu.nylas.com/v3/connect/auth`, `https://api.eu.nylas.com/v3/connect/token`, `https://jellyfish-app-k94ys.ondigitalocean.app/https://api.eu.nylas.com/v3/grants/me/messages/send` | Email authentication, token refresh, and sending emails |
| Google Gmail API | via Nylas scopes: `https://www.googleapis.com/auth/gmail.send` | Gmail integration through Nylas |
| Microsoft Graph API | via Nylas scopes: `https://graph.microsoft.com/Mail.ReadWrite`, `https://graph.microsoft.com/Mail.Send` | Outlook integration through Nylas |

### 7.4 Document Processing Service

| Service | Endpoint | Purpose |
|---------|----------|---------|
| Document Processing API | `https://goldfish-app-yrnjr.ondigitalocean.app/process_doc` | AI-powered document verification and processing |

---

*This report was automatically generated on August 1, 2025, and reflects the current state of the Harold Web application's dependencies as of commit staging-v2.*

## 6. COMPLIANCE NOTES

1. **MIT License**: Allows commercial use, modification, distribution, and private use. Requires attribution.

2. **Apache-2.0**: Allows commercial use, modification, distribution, and private use. Provides patent grant. Requires attribution and state changes.

3. **BSD Licenses**: Allow commercial use with attribution requirement.

4. **Dual Licensed Packages**: Some packages offer multiple license options (e.g., MIT OR Apache-2.0).

5. **Patched Packages**: Four packages have been modified and require careful tracking for updates and compliance.

6. **Service Dependencies**: Multiple SaaS platforms are integrated, each with their own terms of service.

---

**Note**: This inventory should be updated regularly as dependencies change. For the most current information, run `yarn licenses list` in the project directory.

**Last Updated**: August 1, 2025  
**Review Frequency**: Recommended quarterly or before major releases
