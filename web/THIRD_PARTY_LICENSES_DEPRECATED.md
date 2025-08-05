# Deprecated and Unsupported Dependencies Report
## Harold Web Application

**Document Date:** August 4, 2025  
**Application Version:** 1.0.8  
**Repository:** harold-waste/harold-web  
**Branch:** staging-v2  

---

## Executive Summary

This document identifies deprecated libraries, unsupported dependencies, and packages with security or maintenance concerns in the Harold web application. These packages require attention for future upgrades or replacements to maintain application security and stability.

---

## 1. Deprecated JavaScript/TypeScript Dependencies

### 1.1 Critical - Deprecated Production Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **moment** | ^2.29.1 | **DEPRECATED** | Officially deprecated since 2020, in maintenance mode. Legacy mode. | Migrate to `date-fns` or `dayjs`. Consider `moment-timezone` replacement. |
| **moment-timezone** | ^0.5.33 | **DEPRECATED** | Depends on deprecated Moment.js | Migrate to `date-fns-tz` or `dayjs` with timezone plugin |
| **@material-ui/core** | ^4.12.4 | **EOL** | Material-UI v4 is end-of-life, no security updates | Migrate to `@mui/material` v5+ |
| **@material-ui/lab** | ^4.0.0-alpha.57 | **EOL** | Material-UI v4 Lab is end-of-life | Migrate to `@mui/lab` v5+ |
| **@date-io/moment** | ^1.3.11 | **DEPRECATED** | Depends on deprecated Moment.js | Switch to `@date-io/date-fns` or similar |
| **graphql** | 17.0.0-alpha.2 | **PRE-RELEASE** | Using alpha version in production, stability concerns | Use stable v16.x or latest stable |
| **firebase** | ^8.0.2 | **LEGACY** | V8 SDK is legacy, V9+ modular SDK recommended | Migrate to Firebase v9+ modular SDK |
| **jwt-decode** | ^2.2.0 | **OUTDATED** | Very old version, potential security issues | Upgrade to 4.x+ |

### 1.2 Maintenance Mode Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **apollo-link-persisted-queries** | ^0.2.2 | **MAINTENANCE** | Part of deprecated Apollo Link ecosystem | Migrate to Apollo Client 3.x built-in features |
| **react-router-dom** | ^5.2.0 | **OUTDATED** | V5 is outdated, V6+ recommended for better TypeScript support | Migrate to V6+ |
| **chart.js** | ^2.9.4 | **OUTDATED** | V2 is severely outdated, V4 is current | Upgrade to Chart.js v4+ |
| **react-chartjs-2** | ^2.11.1 | **OUTDATED** | Incompatible with Chart.js v4 | Upgrade to compatible version |
| **styled-components** | ^5.3.5 | **OUTDATED** | Missing React 18 optimizations | Upgrade to 6.x+ for React 18 support |
| **react-pdf** | 5.3.1 | **OUTDATED** | Multiple versions behind (current: 7.x+) | Upgrade to 7.x+ for better features |
| **path** | ^0.12.7 | **BROWSER POLYFILL** | Node.js path polyfill for browsers | Consider removing if not needed in web context |

### 1.3 Testing Framework Dependencies (Deprecated)

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **enzyme** | ^3.10.0 | **DEPRECATED** | No longer actively maintained, React 18 compatibility issues | Migrate to `@testing-library/react` |
| **enzyme-adapter-react-16** | ^1.14.0 | **DEPRECATED** | Outdated React adapter, part of deprecated Enzyme ecosystem | Remove with Enzyme migration |
| **@testing-library/react** | ^9.1.4 | **OUTDATED** | Very old version, missing React 18 support | Upgrade to v16+ for React 18 support |

### 1.4 Security Concerns

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **cypress** | ^6.5.0 | **REMOVAL PLANNED** | No longer used, severely outdated with security vulnerabilities | Remove package and related dependencies |
| **react-scripts** | 5.0.0 | **PATCHED** | Using patched version, potential security issues | Consider migrating to Vite or upgrade |
| **framer-motion** | ^4.1.17 | **OUTDATED** | Multiple versions behind (current: 11.x+) | Upgrade for security and performance |

---

## 2. Deprecated Development Dependencies

### 2.1 Critical Development Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **babel-cli** | ^6.26.0 | **DEPRECATED** | Babel 6 is legacy, replaced by @babel/cli | Replace with @babel/cli |
| **typescript** | 4.6.3 | **OUTDATED** | Multiple major versions behind (current: 5.x) | Upgrade to TypeScript 5.x |
| **prettier** | ^2.1.2 | **OUTDATED** | Missing important formatting improvements | Upgrade to 3.x |
| **eslint-config-airbnb** | ^16.1.0 | **OUTDATED** | Very old version, missing modern rules | Upgrade to latest version |

### 2.2 Build Tools & Bundling

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@storybook/react** | ^6.1.11 | **OUTDATED** | V6 is outdated, V8 is current | Upgrade to Storybook v8+ |
| **@storybook/addon-essentials** | ^6.1.11 | **OUTDATED** | Part of outdated Storybook ecosystem | Upgrade with Storybook |
| **@storybook/addon-storyshots** | ^6.1.11 | **OUTDATED** | Part of outdated Storybook ecosystem | Upgrade with Storybook |

### 2.3 GraphQL Code Generation

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@graphql-codegen/cli** | 4.0.0 | **OUTDATED** | Missing latest features (current: 5.x) | Upgrade to latest version |
| **@graphql-codegen/typescript** | 4.0.0 | **OUTDATED** | Missing latest TypeScript support | Upgrade to latest version |

---

## 3. React/UI Framework Specific Deprecated Packages

### 3.1 Material-UI Migration Required

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@material-ui/core** | ^4.12.4 | **EOL** | End of life, no security updates | Complete migration to @mui/material v5+ |
| **@material-ui/lab** | ^4.0.0-alpha.57 | **EOL** | End of life, experimental components outdated | Migrate to @mui/lab v5+ |

### 3.2 Date/Time Library Migration

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **moment** | ^2.29.1 | **DEPRECATED** | Large bundle size, deprecated | Migrate to date-fns or dayjs |
| **moment-timezone** | ^0.5.33 | **DEPRECATED** | Depends on deprecated moment | Use date-fns-tz or dayjs timezone |
| **@date-io/moment** | ^1.3.11 | **DEPRECATED** | Moment.js adapter | Switch to @date-io/date-fns |

---

## 4. Apollo/GraphQL Ecosystem Issues

### 4.1 Apollo Link Deprecations

The application uses deprecated Apollo Link packages that have been superseded by Apollo Client 3.x built-in functionality:

| Package | Replacement | Action Required |
|---------|-------------|-----------------|
| apollo-link-persisted-queries | Built-in persisted queries | Refactor to use Apollo Client 3.x API |
| graphql (alpha) | Stable GraphQL version | Use GraphQL 16.x stable |

---

## 5. Firebase Migration Requirements

### 5.1 Firebase V8 to V9+ Migration

The application uses Firebase v8 SDK which is in maintenance mode:

| Current Package | Version | New Package | Action |
|----------------|---------|-------------|--------|
| firebase | ^8.0.2 | Firebase v9+ modular | Full refactor required |

**Impact:** This requires significant code changes due to the modular SDK architecture change.

---

## 6. Testing Framework Migration

### 6.1 Enzyme to Testing Library Migration

| Current Package | Version | Replacement | Action |
|----------------|---------|-------------|--------|
| enzyme | ^3.10.0 | @testing-library/react | Rewrite all Enzyme tests |
| enzyme-adapter-react-16 | ^1.14.0 | N/A | Remove after migration |

**Impact:** All existing Enzyme tests need to be rewritten using Testing Library patterns.

---

## 6.2 Cypress Removal Plan

| Current Package | Version | Status | Action |
|----------------|---------|---------|--------|
| cypress | ^6.5.0 | Remove | Uninstall completely |
| @testing-library/cypress | ^7.0.1 | Remove | No longer needed |
| cypress-* plugins | Various | Remove | Clean up all cypress-related packages |

**Impact:** Remove all Cypress-related dependencies and test files. Consider alternative E2E testing if needed.

---

## 7. Immediate Action Required

### 7.1 High Priority (Security/Stability)

1. **cypress** - Remove unused package with security vulnerabilities
2. **moment/moment-timezone** - Deprecated, large bundle size
3. **@material-ui/core** - End of life, no security updates
4. **babel-cli** - Legacy Babel 6 version

### 7.2 Medium Priority (Maintenance)

1. **Storybook v6** components - Migrate to V8+
2. **Firebase V8** - Plan migration to V9+
3. **TypeScript 4.6** - Upgrade for better React 18 support
4. **Enzyme testing** - Migrate to Testing Library

### 7.3 Low Priority (Optimization)

1. **react-pdf** - Better performance with newer versions
2. **chart.js** - Better features and performance in v4
3. **styled-components** - Better React 18 support

---

## 8. Migration Roadmap

### Phase 1: Security Fixes (Immediate)
- [ ] Remove Cypress and related testing dependencies
- [ ] Replace babel-cli with @babel/cli
- [ ] Upgrade react-scripts or migrate to Vite

### Phase 2: Core Updates (Next 2-4 weeks)
- [ ] Migrate from Moment.js to date-fns or dayjs
- [ ] Upgrade TypeScript to 5.x
- [ ] Migrate Enzyme tests to Testing Library

### Phase 3: Major Migrations (1-3 months)
- [ ] Material-UI v4 to MUI v5+ migration
- [ ] Firebase V8 to V9+ migration
- [ ] Storybook v6 to v8+ migration

### Phase 4: Optimization (3-6 months)
- [ ] Chart.js v2 to v4 migration
- [ ] React Router v5 to v6+ migration
- [ ] Bundle size optimization

---

## 9. Replacement Recommendations

### 9.1 Date/Time Libraries
```bash
# Remove
moment, moment-timezone, @date-io/moment

# Add
date-fns, date-fns-tz, @date-io/date-fns
# OR
dayjs, @date-io/dayjs
```

### 9.2 UI Framework
```bash
# Remove
@material-ui/core, @material-ui/lab

# Add
@mui/material, @mui/lab, @mui/icons-material
```

### 9.3 Testing Framework
```bash
# Remove
enzyme, enzyme-adapter-react-16

# Upgrade
@testing-library/react@16+, @testing-library/jest-dom
```

### 9.4 Development Tools
```bash
# Replace
babel-cli → @babel/cli
typescript@4.6.3 → typescript@5.x
prettier@2.x → prettier@3.x
```

---

## 10. Compatibility Matrix

| React | TypeScript | Material-UI/MUI | Node.js | Status |
|-------|------------|-----------------|---------|---------|
| 18.0.0 | 4.6.3 | v4 (EOL) | >=16 | ⚠️ Needs updates |
| 18.2.0+ | 5.x | v5+ | >=16 | ✅ Recommended |
| 18.3.x | 5.x | v6+ | >=18 | 🎯 Target |

---

## 11. Risk Assessment

### High Risk
- **Unused security vulnerabilities** in Cypress 6.x (removal required)
- **End-of-life dependencies** Material-UI v4, no security updates
- **Bundle size impact** from deprecated Moment.js
- **React 18 compatibility** issues with old dependencies

### Medium Risk
- **Future React compatibility** issues
- **Developer experience** degradation from outdated tooling
- **Build time** increases from legacy dependencies
- **Testing reliability** with deprecated Enzyme

### Low Risk
- **Performance** improvements available
- **Bundle optimization** opportunities
- **Developer productivity** enhancements
- **Modern feature** access

---

## 12. Estimated Migration Effort

| Migration | Effort | Duration | Risk | Priority |
|-----------|---------|----------|------|----------|
| Remove Cypress | Very Low | 1 day | Very Low | High |
| Moment.js → date-fns | High | 2-3 weeks | Medium | High |
| Material-UI v4 → v5 | Very High | 1-3 months | High | High |
| Enzyme → Testing Library | Medium | 2-4 weeks | Medium | Medium |
| Storybook v6 → v8 | Medium | 1-2 weeks | Low | Medium |
| Firebase v8 → v9 | High | 3-4 weeks | Medium | Medium |

---

*This report was generated on August 4, 2025, based on current dependency analysis and community deprecation notices.*
