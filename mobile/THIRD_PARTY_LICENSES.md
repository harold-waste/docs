# Third-Party Components and Open Source Software License Report
## Harold Mobile Application

**Document Date:** August 1, 2025  
**Application Version:** 2.14.26  
**Repository:** harold-waste/harold-mobile  
**Branch:** staging-v2  

---

## Executive Summary

This document provides a comprehensive list of all third-party modules, proprietary components, and open ### 8.1 Immediate Actions Required

1. **Service Agreements**: Ensure all third-party service agreements are current
2. **API Key Security**: Regularly rotate Firebase API keys and validate access permissions
3. **Backend API Security**: Monitor and secure GraphQL endpoint access
4. **Patch Documentation**: Document purpose and necessity of all custom patches
5. **Native Dependencies**: Review native iOS/Android library compliance
6. **Custom Fork Maintenance**: Keep react-native-queue fork updated and documented

### 8.2 Ongoing Maintenance

1. **Quarterly License Audits**: Review new dependencies and license changestware incorporated into the Harold mobile application. The application is built using React Native framework and includes both JavaScript/TypeScript dependencies and native iOS/Android components.

---

## License Distribution Summary

| License Type | Count | Percentage |
|--------------|-------|------------|
| MIT | 120+ | ~80% |
| Apache-2.0 | 18+ | ~12% |
| BSD-3-Clause | 6+ | ~4% |
| BSD-2-Clause | 4+ | ~3% |
| ISC | 2+ | ~1% |

**Total Dependencies**: 150+ packages (including transitive dependencies, excluding native dependencies)

---

## 1. JavaScript/TypeScript Dependencies

### 1.1 Production Dependencies (75 packages)

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @apollo/client | ^3.11.8 | MIT | GraphQL client with caching |
| @easytool/react-permission | ^0.1.7 | MIT | React permission management |
| @firebase/app | 0.6.22 | Apache-2.0 | Firebase core SDK |
| @react-native-async-storage/async-storage | ^1.19.3 | MIT | Async storage for React Native |
| @react-native-camera-roll/camera-roll | 5.6.0 | MIT | Camera roll access |
| @react-native-community/checkbox | ^0.5.15 | MIT | Cross-platform checkbox component |
| @react-native-community/datetimepicker | ^7.1.0 | MIT | Date/time picker component |
| @react-native-community/netinfo | ^9.0.0 | MIT | Network information API |
| @react-native-community/push-notification-ios | ^1.10.1 | MIT | iOS push notifications |
| @react-native-firebase/app | ^16.5.0 | Apache-2.0 | React Native Firebase core |
| @react-native-firebase/messaging | ^16.5.0 | Apache-2.0 | Firebase Cloud Messaging |
| @react-native-masked-view/masked-view | ^0.3.0 | MIT | Masked view component |
| @react-native-picker/picker | ^2.4.1 | MIT | Picker component |
| @react-navigation/bottom-tabs | ^5.11.8 | MIT | Bottom tab navigation |
| @react-navigation/core | ^6.4.9 | MIT | Navigation core library |
| @react-navigation/drawer | ^5.12.4 | MIT | Drawer navigation |
| @react-navigation/native | ^6.0.8 | MIT | React Navigation for React Native |
| @react-navigation/stack | ^6.2.0 | MIT | Stack navigation |
| @sentry/react-native | ^6.16.0 | MIT | Error tracking and performance monitoring |
| @types/react-dom | 18.2.0 | MIT | TypeScript definitions for React DOM |
| @types/react-native-push-notification | ^8.1.1 | MIT | TypeScript definitions |
| @typescript-eslint/typescript-estree | ^5.47.1 | BSD-2-Clause | TypeScript AST parser |
| accordion-collapse-react-native | ^1.0.0 | MIT | Accordion component |
| apollo-link-persisted-queries | ^0.2.2 | MIT | GraphQL persisted queries |
| apollo-link-retry | ^2.2.16 | MIT | Apollo Link retry logic |
| apollo3-cache-persist | ^0.9.1 | MIT | Apollo cache persistence |
| appcenter | ^4.4.3 | MIT | Microsoft App Center SDK |
| appcenter-analytics | ^4.4.3 | MIT | App Center Analytics |
| appcenter-crashes | ^4.4.3 | MIT | App Center Crash Reporting |
| firebase | ^8.6.3 | Apache-2.0 | Firebase JavaScript SDK |
| flatted | ^3.3.2 | ISC | Circular JSON parser |
| graphql | ^14.6.0 | MIT | GraphQL implementation |
| graphql-tag | ^2.10.1 | MIT | GraphQL query parser |
| html-to-text | ^9.0.5 | MIT | HTML to text converter |
| jwt-decode | ^2.2.0 | MIT | JWT token decoder |
| lodash | ^4.17.15 | MIT | Utility library |
| mime-types | ^2.1.31 | MIT | MIME type utilities |
| moment | ^2.24.0 | MIT | Date manipulation library |
| moment-timezone | ^0.5.28 | MIT | Timezone support for Moment.js |
| numeral | ^2.0.6 | MIT | Number formatting library |
| path | ^0.12.7 | MIT | Node.js path utilities |
| pouchdb-adapter-react-native-sqlite | ^2.0.0 | Apache-2.0 | PouchDB SQLite adapter |
| pouchdb-find | ^7.2.1 | Apache-2.0 | PouchDB query plugin |
| pouchdb-react-native | ^6.4.1 | Apache-2.0 | PouchDB for React Native |
| pouchdb-upsert | ^2.2.0 | Apache-2.0 | PouchDB upsert functionality |
| react | 18.2.0 | MIT | React library |
| react-dom | 18.2.0 | MIT | React DOM library |
| react-native | 0.72.4 | MIT | React Native framework |
| react-native-app-link | ^1.0.0 | MIT | Deep linking utilities |
| react-native-appstate-hook | ^1.0.6 | MIT | App state management hook |
| react-native-blob-util | ^0.15.0 | MIT | Blob/file utilities |
| react-native-check-version | ^1.0.5 | MIT | App version checking |
| react-native-code-push | ^8.1.0 | MIT | CodePush OTA updates |
| react-native-config | ^1.5.1 | MIT | Environment configuration |
| react-native-contacts | ^6.0.3 | MIT | Contacts access |
| react-native-device-info | ^5.6.1 | MIT | Device information |
| react-native-dotenv | ^0.2.0 | MIT | Environment variables |
| react-native-fast-image | ^8.3.4 | MIT AND Apache-2.0 | Fast image component |
| react-native-fetch-api | ^3.0.0 | MIT | Fetch API polyfill |
| react-native-fs | ^2.18.0 | MIT | File system access |
| react-native-geolocation-service | ^5.3.0-beta.1 | MIT | Geolocation services |
| react-native-gesture-handler | ^2.12.0 | MIT | Gesture recognition |
| react-native-get-random-values | ^1.5.0 | MIT | Random value generation |
| react-native-global-props | ^1.1.5 | MIT | Global props management |
| react-native-google-places-autocomplete | ^1.8.1 | MIT | Google Places autocomplete |
| react-native-image-picker | ^7.0.0 | MIT | Image selection |
| react-native-image-resizer | ^1.4.4 | MIT | Image resizing |
| react-native-image-zoom-viewer | ^3.0.1 | MIT | Image zoom viewer |
| react-native-indicators | ^0.17.0 | MIT | Loading indicators |
| react-native-keyboard-manager | ^4.0.13-17 | MIT | Keyboard management |
| react-native-material-menu | ^1.1.3 | MIT | Material design menu |
| react-native-mmkv-storage | ^0.9.1 | MIT | High-performance storage |
| react-native-modal | ^13.0.0 | MIT | Modal component |
| react-native-pager-view | ^6.2.1 | MIT | Pager view component |
| react-native-pdf | 6.7.4 | MIT | PDF viewer component |
| react-native-pell-rich-editor | ^1.9.0 | MIT | Rich text editor |
| react-native-polyfill-globals | ^3.1.0 | MIT | Global polyfills |
| react-native-progress | ^4.1.2 | MIT | Progress indicators |
| react-native-push-notification | ^8.1.1 | MIT | Push notification handling |
| react-native-queue | Custom Fork | MIT | Background task queue (Custom Harold fork) |
| react-native-range-datepicker | ^1.9.1 | MIT | Date range picker |
| react-native-reanimated | ^3.3.0 | MIT | Animation library |
| react-native-render-html | ^6.1.0 | MIT | HTML rendering |
| react-native-safe-area-context | ^4.5.3 | MIT | Safe area utilities |
| react-native-scalable-image | ^1.1.0 | MIT | Scalable image component |
| react-native-screens | ^3.21.0 | MIT | Native screen components |
| react-native-share | ^12.0.3 | MIT | Native sharing |
| react-native-splash-screen | ^3.3.0 | MIT | Splash screen management |
| react-native-sqlite-2 | ^3.5.2 | Apache-2.0 | SQLite database |
| react-native-svg | ^13.9.0 | MIT | SVG support |
| react-native-tab-view | ^3.5.2 | MIT | Tab view component |
| react-native-toast-message | ^2.1.6 | MIT | Toast notifications |
| react-native-user-avatar | ^1.0.8 | MIT | User avatar component |
| react-native-ux-cam | ^5.4.11 | MIT | UX analytics |
| react-native-vector-icons | ^10.0.0 | MIT | Vector icon library |
| react-native-webview | ^13.2.2 | MIT | WebView component |
| react-redux | 7.2.1 | MIT | React Redux bindings |
| redux | ^4.0.5 | MIT | State management |
| redux-persist | ^6.0.0 | MIT | Redux persistence |
| redux-saga | ^1.1.3 | MIT | Redux side effect management |
| reselect | ^4.0.0 | MIT | Selector library |
| string-template | ^1.0.0 | MIT | String templating |
| text-encoding | ^0.7.0 | Unlicense OR Apache-2.0 | Text encoding polyfill |
| use-debounce | ^7.0.1 | MIT | Debounce hook |
| use-deep-compare-effect | ^1.3.1 | MIT | Deep comparison hook |
| uuid | ^8.3.1 | MIT | UUID generation |
| web-streams-polyfill | 3.3.3 | MIT | Web Streams API polyfill |

### 1.2 Development Dependencies (67 packages)

| Package | Version | License | Description |
|---------|---------|---------|-------------|
| @babel/core | ^7.20.0 | MIT | Babel compiler core |
| @babel/plugin-proposal-export-default-from | ^7.10.4 | MIT | Babel plugin |
| @babel/plugin-proposal-export-namespace-from | ^7.10.4 | MIT | Babel plugin |
| @babel/plugin-proposal-object-rest-spread | ^7.11.0 | MIT | Babel plugin |
| @babel/plugin-syntax-async-generators | ^7.8.4 | MIT | Babel plugin |
| @babel/plugin-transform-async-to-generator | ^7.10.4 | MIT | Babel plugin |
| @babel/preset-env | ^7.20.0 | MIT | Babel preset |
| @babel/preset-typescript | ^7.10.4 | MIT | Babel TypeScript preset |
| @babel/runtime | ^7.20.0 | MIT | Babel runtime |
| @graphql-codegen/cli | ^5.0.3 | MIT | GraphQL code generation CLI |
| @graphql-codegen/fragment-matcher | ^5.0.2 | MIT | GraphQL fragment matcher |
| @graphql-codegen/introspection | ^4.0.3 | MIT | GraphQL introspection |
| @graphql-codegen/typescript | ^4.1.0 | MIT | TypeScript code generation |
| @graphql-codegen/typescript-operations | ^4.3.0 | MIT | TypeScript operations |
| @graphql-codegen/typescript-react-apollo | ^4.3.2 | MIT | React Apollo code generation |
| @graphql-toolkit/relay-operation-optimizer | ^0.10.7 | MIT | Relay operation optimizer |
| @react-native-community/eslint-config | ^3.0.0 | MIT | ESLint configuration |
| @react-native/eslint-config | ^0.72.2 | MIT | React Native ESLint config |
| @react-native/metro-config | ^0.72.0 | MIT | Metro bundler configuration |
| @rnx-kit/align-deps | ^2.2.4 | MIT | Dependency alignment tool |
| @tsconfig/react-native | ^3.0.0 | MIT | TypeScript configuration |
| @types/html-to-text | ^6.0.0 | MIT | TypeScript definitions |
| @types/jest | ^29.2.1 | MIT | Jest TypeScript definitions |
| @types/jwt-decode | ^2.2.1 | MIT | TypeScript definitions |
| @types/lodash | ^4.14.161 | MIT | Lodash TypeScript definitions |
| @types/mime-types | ^2.1.0 | MIT | TypeScript definitions |
| @types/moment-timezone | ^0.5.30 | MIT | TypeScript definitions |
| @types/numeral | ^0.0.28 | MIT | TypeScript definitions |
| @types/pouchdb | ^6.4.0 | MIT | PouchDB TypeScript definitions |
| @types/pouchdb-core | ^7.0.6 | MIT | TypeScript definitions |
| @types/pouchdb-upsert | ^2.2.6 | MIT | TypeScript definitions |
| @types/react | 18.2.0 | MIT | React TypeScript definitions |
| @types/react-native | 0.72.3 | MIT | React Native TypeScript definitions |
| @types/react-native-material-menu | ^1.0.3 | MIT | TypeScript definitions |
| @types/react-native-vector-icons | ^6.4.15 | MIT | TypeScript definitions |
| @types/react-native-view-pdf | ^0.8.2 | MIT | TypeScript definitions |
| @types/react-redux | ^7.1.9 | MIT | TypeScript definitions |
| @types/react-test-renderer | ^18.0.0 | MIT | TypeScript definitions |
| @types/string-template | ^1.0.2 | MIT | TypeScript definitions |
| @types/uuid | ^8.3.0 | MIT | TypeScript definitions |
| @typescript-eslint/eslint-plugin | ^6.7.5 | MIT | TypeScript ESLint plugin |
| @typescript-eslint/parser | ^6.7.5 | BSD-2-Clause | TypeScript ESLint parser |
| apollo-link-logger | ^2.0.0 | MIT | Apollo Link logger |
| babel-eslint | ^10.1.0 | MIT | Babel ESLint parser |
| babel-jest | ^29.2.1 | MIT | Babel Jest transformer |
| babel-loader | ^8.0.6 | MIT | Babel webpack loader |
| babel-plugin-module-resolver | ^4.0.0 | MIT | Babel module resolver |
| eslint | ^8.51.0 | MIT | JavaScript linter |
| eslint-config-airbnb | ^18.1.0 | MIT | Airbnb ESLint configuration |
| eslint-config-prettier | ^6.11.0 | MIT | Prettier ESLint configuration |
| eslint-import-resolver-babel-module | ^5.1.2 | MIT | Babel module resolver for ESLint |
| eslint-import-resolver-typescript | 2.3.0 | ISC | TypeScript resolver for ESLint |
| eslint-plugin-graphql | ^3.1.1 | MIT | GraphQL ESLint plugin |
| eslint-plugin-import | ^2.28.1 | MIT | Import ESLint plugin |
| eslint-plugin-jsx-a11y | ^6.2.3 | MIT | Accessibility ESLint plugin |
| eslint-plugin-prettier | ^3.1.4 | MIT | Prettier ESLint plugin |
| eslint-plugin-react | ^7.20.0 | MIT | React ESLint plugin |
| eslint-plugin-react-hooks | ^2.3.0 | MIT | React Hooks ESLint plugin |
| eslint-plugin-sort-keys-fix | ^1.1.1 | MIT | Sort keys ESLint plugin |
| eslint-plugin-typescript | ^0.14.0 | MIT | TypeScript ESLint plugin |
| get-graphql-schema | ^2.1.2 | MIT | GraphQL schema fetcher |
| graphql-import | ^1.0.0-beta.2 | MIT | GraphQL import system |
| graphql-tools | ^4.0.7 | MIT | GraphQL tools |
| jest | ^29.2.1 | MIT | Testing framework |
| jest-fetch-mock | ^3.0.3 | MIT | Fetch mock for Jest |
| metro-react-native-babel-preset | ^0.76.5 | MIT | Metro Babel preset |
| patch-package | ^6.4.7 | MIT | Package patching tool |
| postinstall | ^0.7.0 | MIT | Postinstall script runner |
| postinstall-postinstall | ^2.1.0 | MIT | Postinstall helper |
| prettier | ^2.4.1 | MIT | Code formatter |
| react-hooks-testing-library | ^0.6.0 | MIT | React Hooks testing utilities |
| react-native-bundle-visualizer | ^2.2.1 | MIT | Bundle analyzer |
| react-native-flipper | ^0.142.0 | MIT | Flipper debugging |
| react-native-flipper-apollo-devtools | ^0.0.2 | MIT | Apollo Flipper plugin |
| react-native-version | ^4.0.0 | MIT | Version management |
| react-test-renderer | 18.2.0 | MIT | React test renderer |
| redux-devtools | ^3.5.0 | MIT | Redux development tools |
| redux-devtools-extension | ^2.13.8 | MIT | Redux DevTools extension |
| redux-flipper | ^1.4.2 | MIT | Redux Flipper plugin |
| rn-async-storage-flipper | ^0.0.9 | MIT | AsyncStorage Flipper plugin |
| timezone-mock | ^1.0.17 | MIT | Timezone mocking for tests |
| typescript | 4.6.3 | Apache-2.0 | TypeScript compiler |

### 1.3 Patched Dependencies

The following third-party packages have been modified using patch-package:

| Package | Version | Patch Description |
|---------|---------|-------------------|
| @firebase/app | 0.6.22 | Custom modifications |
| @react-navigation/core | 6.4.9 | Navigation fixes |
| @types/pouchdb-upsert | 2.2.6 | TypeScript definition fixes |
| htmlparser2 | 8.0.2 | HTML parsing modifications |
| react-native | 0.72.5 | Core React Native patches |
| react-native-reanimated | 3.5.4 | Animation library fixes |
| react-native-scalable-image | 1.1.0 | Image scaling modifications |

---

## 2. iOS Native Dependencies

### 2.1 CocoaPods Dependencies

| Pod | License | Description |
|-----|---------|-------------|
| GoogleUtilities | Apache-2.0 | Google utilities for iOS |
| FirebaseCore | Apache-2.0 | Firebase core iOS SDK |
| React-Native Framework | MIT | React Native iOS runtime |
| Hermes Engine | MIT | JavaScript engine |

*Note: Additional CocoaPods are managed automatically by React Native and may include other Firebase services, networking libraries, and native components.*

---

## 3. Android Native Dependencies

### 3.1 Gradle Dependencies

| Dependency | License | Description |
|------------|---------|-------------|
| com.facebook.react:react-android | MIT | React Native Android runtime |
| com.facebook.react:hermes-android | MIT | Hermes JavaScript engine |
| com.facebook.flipper:flipper | MIT | Flipper debugging (debug builds only) |
| com.facebook.flipper:flipper-network-plugin | MIT | Network debugging plugin |
| com.facebook.flipper:flipper-fresco-plugin | MIT | Image debugging plugin |
| org.jetbrains:annotations | Apache-2.0 | JetBrains annotations |

---

## 4. Proprietary/Custom Components

### 4.1 Harold-Specific Modifications

| Component | Source | License | Description |
|-----------|--------|---------|-------------|
| react-native-queue | https://github.com/harold-waste/react-native-queue-asyncstorage.git | MIT | Custom fork for AsyncStorage compatibility |

---

## 5. License Summary

### 5.1 License Distribution

| License Type | Count | Percentage |
|--------------|-------|------------|
| MIT | ~85% | Majority of dependencies |
| Apache-2.0 | ~8% | Firebase, Google, and related services |
| BSD-2-Clause | ~2% | TypeScript and related tools |
| ISC | ~2% | Various utilities |
| Unlicense | ~1% | Public domain software |
| Other | ~2% | WTFPL, Public Domain, etc. |

### 5.2 Notable License Types

- **MIT License**: The most permissive license used by the majority of JavaScript packages
- **Apache-2.0**: Used by Google/Firebase services and some React Native components
- **BSD-2-Clause**: Used by TypeScript and related Microsoft tools
- **ISC**: Similar to MIT, used by some Node.js utilities
- **Unlicense**: Public domain dedication
- **WTFPL**: "Do What The F*ck You Want To Public License" - very permissive

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

## 7. Third-Party Service Providers

The following third-party services require valid service agreements:

| Service | Package/Integration | Agreement Type | API Documentation |
|---------|-------------------|----------------|-------------------|
| Firebase/Google Cloud Platform | @react-native-firebase/app, @react-native-firebase/messaging, firebase | Service Agreement | [Firebase API](https://firebase.google.com/docs/reference), [Cloud Storage API](https://cloud.google.com/storage/docs/apis) |
| Sentry | @sentry/react-native | Service Agreement | [Sentry API](https://docs.sentry.io/api/) |
| UXCam | react-native-ux-cam | Service Agreement | [UXCam API](https://uxcam.com/docs/) |

### 7.1 Backend API Integration

The application connects to multiple backend API endpoints depending on the environment:

- **Development**: `http://localhost:5000/graphql`
- **Staging**: `https://staging.api.julesai.com/graphql`
- **Demo**: `https://demo.api.haroldwaste.com/graphql`
- **Production**: `https://api.haroldwaste.com/graphql` and `https://api.julesai.com/graphql`

### 7.2 Firebase Services

The application uses Firebase for:
- Cloud Storage (file uploads and image storage)
- Cloud Messaging (push notifications)
- Authentication and user management

### 7.3 Analytics and Monitoring

- **Sentry**: Error tracking and performance monitoring
- **App Center**: Crash reporting, analytics, and CodePush OTA updates
- **UXCam**: User experience analytics and session recording (production only)

---

## 8. Maintenance Recommendations

### 8.1 Immediate Actions Required

1. **Service Agreements**: Ensure all third-party service agreements are current
2. **Patch Documentation**: Document purpose and necessity of all custom patches
3. **Native Dependencies**: Review native iOS/Android library compliance
4. **Custom Fork Maintenance**: Keep react-native-queue fork updated and documented

### 7.2 Ongoing Maintenance

1. **Quarterly License Audits**: Review new dependencies and license changes
2. **Automated Scanning**: Implement license scanning in CI/CD pipeline for both JS and native dependencies
3. **Service Monitoring**: Monitor third-party service availability and performance
4. **API Rate Limiting**: Implement proper rate limiting for external service calls
5. **Version Monitoring**: Monitor dependency updates for license changes
6. **Security Updates**: Maintain regular updates while preserving patches
7. **Platform Compliance**: Monitor iOS App Store and Google Play policy changes

### 8.3 Risk Mitigation

1. **Service Diversification**: Plan for third-party service outages or policy changes
2. **API Fallbacks**: Implement fallback mechanisms for critical external services
3. **Data Privacy**: Ensure compliance with user data collection policies (UXCam, analytics)
4. **Platform Diversification**: Plan for mobile platform policy changes
5. **Patch Reduction**: Work to eliminate custom patches where possible
6. **License Monitoring**: Track license changes in dependency updates
7. **Alternative Planning**: Identify alternatives for critical native dependencies

### 8.4 Security Considerations

1. **Environment Variables**: Secure storage and rotation of API keys and tokens
2. **Network Security**: Implement certificate pinning for critical API endpoints
3. **Data Encryption**: Ensure proper encryption for data in transit and at rest
4. **User Privacy**: Review third-party data collection practices (UXCam, Sentry, App Center)

---

*This report was automatically generated on August 1, 2025, and reflects the current state of the Harold mobile application's dependencies as of commit staging-v2.*
