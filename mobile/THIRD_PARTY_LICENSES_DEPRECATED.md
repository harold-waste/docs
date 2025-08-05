# Deprecated and Unsupported Dependencies Report
## Harold Mobile Application

**Document Date:** August 4, 2025  
**Application Version:** 2.14.26  
**Repository:** harold-waste/harold  
**Branch:** staging-v2  

---

## Executive Summary

This document identifies deprecated libraries, unsupported dependencies, and packages with security or maintenance concerns in the Harold mobile application. These packages require attention for future upgrades or replacements to maintain application security and stability.

---

## 1. Deprecated JavaScript/TypeScript Dependencies

### 1.1 Critical - Deprecated Production Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **moment** | ^2.24.0 | **DEPRECATED** | Officially deprecated since 2020, in maintenance mode. Legacy mode. | Migrate to `date-fns` or `dayjs`. Consider `moment-timezone` replacement. |
| **moment-timezone** | ^0.5.28 | **DEPRECATED** | Depends on deprecated Moment.js | Migrate to `date-fns-tz` or `dayjs` with timezone plugin |
| **graphql** | ^14.6.0 | **OUTDATED** | Very old version (current: 16.x), multiple security vulnerabilities | Upgrade to GraphQL 16.x+ |
| **firebase** | ^8.6.3 | **OUTDATED** | V8 SDK is legacy, V9+ modular SDK recommended | Migrate to Firebase v9+ modular SDK |
| **react-redux** | 7.2.1 | **OUTDATED** | Missing React 18 optimizations | Upgrade to 8.x+ for React 18 support |
| **jwt-decode** | ^2.2.0 | **OUTDATED** | Very old version, potential security issues | Upgrade to 3.x+ or 4.x |
| **uuid** | ^8.3.1 | **OUTDATED** | Missing newer security features | Upgrade to 9.x+ |

### 1.2 Maintenance Mode Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **apollo-link-persisted-queries** | ^0.2.2 | **MAINTENANCE** | Part of deprecated Apollo Link ecosystem | Migrate to Apollo Client 3.x built-in features |
| **apollo-link-retry** | ^2.2.16 | **MAINTENANCE** | Part of deprecated Apollo Link ecosystem | Use Apollo Client 3.x error link |
| **react-native-device-info** | ^5.6.1 | **OUTDATED** | Major versions behind (current: 10.x) | Upgrade to 10.x+ for latest device support |
| **text-encoding** | ^0.7.0 | **DEPRECATED** | Web standard polyfill no longer needed | Remove, use native TextEncoder/TextDecoder |
| **path** | ^0.12.7 | **BROWSER POLYFILL** | Node.js path polyfill for browsers | Consider removing if not needed in RN context |

### 1.3 React Navigation V5 Dependencies (Deprecated)

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@react-navigation/bottom-tabs** | ^5.11.8 | **DEPRECATED** | V5 is deprecated, V6+ recommended | Migrate to V6+ |
| **@react-navigation/drawer** | ^5.12.4 | **DEPRECATED** | V5 is deprecated, V6+ recommended | Migrate to V6+ |
| **@react-navigation/stack** | ^6.2.0 | **MIXED** | V6 but mixed with V5 dependencies | Ensure all navigation deps are V6+ |

### 1.4 Security Concerns

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **lodash** | ^4.17.15 | **SECURITY RISK** | Known prototype pollution vulnerabilities | Upgrade to 4.17.21+ or replace with modern alternatives |
| **@sentry/react-native** | ^6.16.0 | **OUTDATED** | Multiple versions behind (current: 5.x+) | Upgrade for latest security fixes |

---

## 2. Deprecated Development Dependencies

### 2.1 Critical Development Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **babel-eslint** | ^10.1.0 | **DEPRECATED** | Replaced by @babel/eslint-parser | Replace with @babel/eslint-parser |
| **eslint-plugin-typescript** | ^0.14.0 | **DEPRECATED** | Replaced by @typescript-eslint packages | Remove, use @typescript-eslint/* |
| **typescript** | 4.6.3 | **OUTDATED** | Multiple major versions behind (current: 5.x) | Upgrade to TypeScript 5.x |
| **prettier** | ^2.4.1 | **OUTDATED** | Missing important formatting improvements | Upgrade to 3.x |

### 2.2 Testing Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **react-hooks-testing-library** | ^0.6.0 | **DEPRECATED** | Merged into @testing-library/react | Use @testing-library/react-hooks or React 18 testing |

---

## 3. React Native Specific Deprecated Packages

### 3.1 Community Packages (Potential Issues)

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **react-native-splash-screen** | ^3.3.0 | **UNMAINTAINED** | No updates for 2+ years, React Native 0.70+ issues | Consider react-native-bootsplash |
| **react-native-sqlite-2** | ^3.5.2 | **UNMAINTAINED** | Limited maintenance, consider alternatives | Migrate to react-native-sqlite-storage or Watermelon DB |
| **react-native-mmkv-storage** | ^0.9.1 | **OUTDATED** | Superseded by react-native-mmkv | Migrate to react-native-mmkv |

### 3.2 Version Compatibility Issues

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **react-native** | 0.72.4 | **OUTDATED** | Missing latest security patches | Upgrade to 0.72.latest or 0.73+ |
| **@react-native-firebase/app** | ^16.5.0 | **COMPATIBILITY** | May have issues with RN 0.72+ | Verify compatibility, upgrade if needed |

---

## 4. Apollo/GraphQL Ecosystem Issues

### 4.1 Apollo Link Deprecations

The application uses several deprecated Apollo Link packages that have been superseded by Apollo Client 3.x built-in functionality:

| Package | Replacement | Action Required |
|---------|-------------|-----------------|
| apollo-link-persisted-queries | Built-in persisted queries | Refactor to use Apollo Client 3.x API |
| apollo-link-retry | Built-in retry link | Use Apollo Client 3.x error handling |
| apollo-link-logger | Built-in logging | Use Apollo Client 3.x dev tools |

---

## 5. Firebase Migration Requirements

### 5.1 Firebase V8 to V9+ Migration

The application uses Firebase v8 SDK which is in maintenance mode:

| Current Package | Version | New Package | Action |
|----------------|---------|-------------|--------|
| firebase | ^8.6.3 | Firebase v9+ modular | Full refactor required |
| @firebase/app | 0.6.22 | @firebase/app v9+ | Update imports and initialization |

**Impact:** This requires significant code changes due to the modular SDK architecture change.

---

## 6. Immediate Action Required

### 6.1 High Priority (Security/Stability)

1. **lodash** - Security vulnerabilities
2. **moment/moment-timezone** - Deprecated, large bundle size
3. **graphql** - Multiple versions behind
4. **jwt-decode** - Potential security issues

### 6.2 Medium Priority (Maintenance)

1. **React Navigation V5** components - Migrate to V6+
2. **Firebase V8** - Plan migration to V9+
3. **babel-eslint** - Replace with modern alternative
4. **TypeScript** - Upgrade for better React 18 support

### 6.3 Low Priority (Optimization)

1. **react-native-mmkv-storage** - Better performance with react-native-mmkv
2. **uuid** - Newer versions have better performance
3. **text-encoding** - Remove unnecessary polyfill

---

## 7. Migration Roadmap

### Phase 1: Security Fixes (Immediate)
- [ ] Upgrade lodash to latest secure version
- [ ] Replace babel-eslint with @babel/eslint-parser
- [ ] Upgrade jwt-decode to v3+

### Phase 2: Core Updates (Next 2-4 weeks)
- [ ] Migrate from Moment.js to date-fns or dayjs
- [ ] Upgrade TypeScript to 5.x
- [ ] Update React Navigation to V6+

### Phase 3: Major Migrations (1-3 months)
- [ ] Firebase V8 to V9+ migration
- [ ] Apollo Link deprecation cleanup
- [ ] React Native version update

### Phase 4: Optimization (3-6 months)
- [ ] Storage layer optimization (MMKV)
- [ ] Bundle size optimization
- [ ] Performance improvements

---

## 8. Replacement Recommendations

### 8.1 Date/Time Libraries
```bash
# Remove
moment, moment-timezone

# Add
date-fns, date-fns-tz
# OR
dayjs, dayjs-plugin-timezone
```

### 8.2 State Management
```bash
# Upgrade
react-redux@8.x
redux-toolkit (if not using)
```

### 8.3 Development Tools
```bash
# Replace
babel-eslint → @babel/eslint-parser
eslint-plugin-typescript → @typescript-eslint/eslint-plugin
```

---

## 9. Compatibility Matrix

| React Native | TypeScript | React | Node.js | Status |
|--------------|------------|-------|---------|---------|
| 0.72.4 | 4.6.3 | 18.2.0 | >=16 | ⚠️ Needs updates |
| 0.72.latest | 5.x | 18.2.0 | >=16 | ✅ Recommended |
| 0.73.x | 5.x | 18.2.0 | >=18 | 🎯 Target |

---

## 10. Risk Assessment

### High Risk
- **Security vulnerabilities** in lodash, old GraphQL version
- **Bundle size impact** from deprecated Moment.js
- **Maintenance burden** from unmaintained packages

### Medium Risk
- **Future React Native compatibility** issues
- **Developer experience** degradation
- **Build time** increases from legacy tooling

### Low Risk
- **Performance** improvements available
- **Bundle optimization** opportunities
- **Developer productivity** enhancements

---

*This report was generated on August 4, 2025, based on current dependency analysis and community deprecation notices.*
