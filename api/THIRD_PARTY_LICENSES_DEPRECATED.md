# Deprecated and Unsupported Dependencies Report
## Harold API Server

**Document Date:** August 4, 2025  
**Application Version:** 1.0.0  
**Repository:** harold-waste/harold-api  
**Branch:** staging-v2  

---

## Executive Summary

This document identifies deprecated libraries, unsupported dependencies, and packages with security or maintenance concerns in the Harold API server. These packages require attention for future upgrades or replacements to maintain application security and stability.

---

## 1. Deprecated JavaScript/TypeScript Dependencies

### 1.1 Critical - Deprecated Production Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@babel/polyfill** | ^7.0.0 | **DEPRECATED** | Deprecated since Babel 7.4.0, no longer maintained | Replace with `core-js/stable` and `regenerator-runtime` |
| **moment** | ^2.24.0 | **DEPRECATED** | Officially deprecated since 2020, in maintenance mode. Legacy mode. | Migrate to `date-fns` or `dayjs`. Consider `moment-timezone` replacement. |
| **moment-business-days** | ^1.2.0 | **DEPRECATED** | Depends on deprecated Moment.js | Migrate to `date-fns` business days addons |
| **moment-timezone** | ^0.5.33 | **DEPRECATED** | Depends on deprecated Moment.js | Migrate to `date-fns-tz` or `dayjs` with timezone plugin |
| **axios** | ^0.19.0 | **SECURITY RISK** | Known security vulnerabilities (CVE-2021-3749, CVE-2020-28168) | Upgrade to axios v1.6.0+ |
| **node-fetch** | ^2.6.0 | **DEPRECATED** | Superseded by built-in fetch in Node.js 18+ | Use native fetch or upgrade to node-fetch v3+ |
| **graphql** | 17.0.0-alpha.2 | **UNSTABLE** | Using pre-release version in production | Use stable GraphQL v16.x |

### 1.2 Maintenance Mode Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@sentry/node** | 5.11.1 | **OUTDATED** | Multiple major versions behind (current: v8+) | Upgrade to @sentry/node v8.x+ for security fixes |
| **firebase** | ^7.14.6 | **OUTDATED** | V7 SDK is legacy, V10+ recommended | Migrate to Firebase v10+ SDK |
| **knex** | 0.95.6 | **OUTDATED** | Multiple major versions behind (current: v3+) | Upgrade to Knex v3.x (coordinate with patches) |
| **prisma** | ^4.9.0 | **OUTDATED** | Major version behind (current: v5+) | Upgrade to Prisma v5.x |

### 1.3 Security Concerns

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **uuid** | ^9.0.0 | **PATCHED** | May have custom modifications affecting security | Verify patches and upgrade to latest |
| **lodash** | ^4.17.15 | **SECURITY RISK** | Potential prototype pollution vulnerabilities | Upgrade to 4.17.21+ or replace with modern alternatives |

---

## 2. Deprecated Development Dependencies

### 2.1 Critical Development Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **babel-eslint** | ^10.1.0 | **DEPRECATED** | Replaced by @babel/eslint-parser | Replace with @babel/eslint-parser |
| **@babel/plugin-proposal-***** | Various | **DEPRECATED** | Most proposal plugins are now part of preset-env | Remove and use preset-env targets |
| **typescript** | 4.9.5 | **OUTDATED** | Multiple major versions behind (current: 5.x) | Upgrade to TypeScript 5.x |
| **eslint** | ^7.10.0 | **OUTDATED** | Multiple major versions behind (current: v8+) | Upgrade to ESLint v8.x |
| **eslint-config-airbnb** | ^16.1.0 | **OUTDATED** | Multiple major versions behind | Upgrade to latest eslint-config-airbnb |

### 2.2 Testing Dependencies

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **jest** | ^26.6.1 | **OUTDATED** | Multiple major versions behind (current: v29+) | Upgrade to Jest v29.x |
| **ts-jest** | ^26.4.2 | **OUTDATED** | Should match Jest version | Upgrade to ts-jest v29.x |

### 2.3 Build Tools

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **webpack** | ^5.64.2 | **OUTDATED** | Minor versions behind in v5 series | Update to latest webpack v5.x |

---

## 3. Third-Party Service Dependencies

### 3.1 Service Provider Packages (Potential Issues)

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@knocklabs/node** | 0.6.1 | **PATCHED** | Custom patch indicates compatibility issues | Coordinate with vendor for official fix |
| **@magic-sdk/admin** | ^1.8.0 | **SERVICE DEPENDENT** | Depends on Magic Labs service continuity | Monitor service status and alternatives |

### 3.2 Version Compatibility Issues

| Package | Version | Status | Issue | Recommended Action |
|---------|---------|---------|-------|-------------------|
| **@types/lodash** | 4.14.165 | **PATCHED** | Custom patch indicates type issues | Update types and remove patch |

---

## 4. Custom Patches Risk Assessment

### 4.1 Packages with Custom Patches

The application uses several packages with custom patches that have been modified with custom patches located in the `/patches` directory:

| Package | Patch File | Issue | Action Required |
|---------|------------|--------|-----------------|
| **@knocklabs/node** | @knocklabs+node+0.6.1.patch | Custom modifications for Harold integration | Coordinate with vendor for official support |
| **@types/lodash** | @types+lodash+4.14.165.patch | TypeScript compatibility issues | Update to latest types and resolve conflicts |
| **knex** | knex+0.95.6.patch | Custom database query modifications | Document patch purpose and plan migration |

**Impact:** Vendor updates may break custom modifications, requiring maintenance overhead.

---

## 5. Database and ORM Migration Requirements

### 5.1 Knex to Latest Version

The application uses Knex v0.95.6 which is significantly outdated:

| Current Package | Version | New Package | Action |
|----------------|---------|-------------|--------|
| knex | 0.95.6 | knex v3.x | Major refactor required due to API changes |
| @wwwouter/typed-knex | ^4.4.0 | Updated version | Verify compatibility with Knex v3.x |

**Impact:** This requires careful migration due to breaking changes and custom patches.

### 5.2 Prisma Migration

| Current Package | Version | New Package | Action |
|----------------|---------|-------------|--------|
| prisma | ^4.9.0 | prisma v5.x | Update schema and client generation |

---

## 6. GraphQL Ecosystem Issues

### 6.1 GraphQL Alpha Version

The application uses GraphQL alpha version which poses stability risks:

| Package | Current | Recommended | Action Required |
|---------|---------|-------------|-----------------|
| graphql | 17.0.0-alpha.2 | graphql v16.x | Downgrade to stable version |
| graphql-jit | ^0.7.1 | Latest compatible | Verify compatibility with stable GraphQL |

---

## 7. Immediate Action Required

### 7.1 High Priority (Security/Stability)

1. **axios@0.19.0** - Security vulnerabilities (CVE-2021-3749, CVE-2020-28168)
2. **@babel/polyfill** - Deprecated, causing build issues
3. **graphql** - Alpha version in production
4. **@sentry/node** - Multiple versions behind with security issues

### 7.2 Medium Priority (Maintenance)

1. **moment/moment-timezone** - Deprecated, large bundle size
2. **babel-eslint** - Replace with modern alternative
3. **TypeScript** - Upgrade for better performance and features
4. **Jest/ts-jest** - Upgrade for better test performance

### 7.3 Low Priority (Optimization)

1. **webpack** - Minor version updates
2. **node-fetch** - Replace with native fetch
3. **firebase** - Plan migration to v10+

---

## 8. Migration Roadmap

### Phase 1: Security Fixes (Immediate)
- [ ] Upgrade axios to v1.6.0+
- [ ] Replace @babel/polyfill with core-js/stable
- [ ] Downgrade graphql to stable v16.x
- [ ] Upgrade @sentry/node to v8.x

### Phase 2: Core Updates (Next 2-4 weeks)
- [ ] Migrate from Moment.js to date-fns or dayjs
- [ ] Replace babel-eslint with @babel/eslint-parser
- [ ] Upgrade TypeScript to 5.x
- [ ] Update Jest and ts-jest to v29.x

### Phase 3: Major Migrations (1-3 months)
- [ ] Knex upgrade to v3.x (coordinate with patches)
- [ ] Prisma upgrade to v5.x
- [ ] Firebase migration to v10+
- [ ] ESLint ecosystem upgrade

### Phase 4: Optimization (3-6 months)
- [ ] Remove deprecated Babel proposal plugins
- [ ] Replace node-fetch with native fetch
- [ ] Bundle size optimization
- [ ] Performance improvements

---

## 9. Replacement Recommendations

### 9.1 Date/Time Libraries
```bash
# Remove
moment, moment-timezone, moment-business-days

# Add
date-fns, date-fns-tz
# OR
dayjs, dayjs-plugin-timezone, dayjs-plugin-businessDays
```

### 9.2 Development Tools
```bash
# Replace
babel-eslint → @babel/eslint-parser
@babel/polyfill → core-js/stable + regenerator-runtime

# Upgrade
typescript@5.x
jest@29.x
ts-jest@29.x
eslint@8.x
```

### 9.3 HTTP Clients
```bash
# Upgrade
axios@1.6.0+

# Replace (Node.js 18+)
node-fetch → native fetch API
```

---

## 10. Compatibility Matrix

| Node.js | TypeScript | GraphQL | Knex | Prisma | Status |
|---------|------------|---------|------|--------|---------|
| 18.x | 4.9.5 | 17.0.0-alpha.2 | 0.95.6 | 4.9.0 | ⚠️ Needs updates |
| 18.x | 5.x | 16.x | 3.x | 5.x | ✅ Recommended |
| 20.x | 5.x | 16.x | 3.x | 5.x | 🎯 Target |

---

## 11. Risk Assessment

### High Risk
- **Security vulnerabilities** in axios, old Sentry version
- **Stability issues** from GraphQL alpha version
- **Bundle size impact** from deprecated Moment.js and @babel/polyfill
- **Custom patches** may break with updates

### Medium Risk
- **Future Node.js compatibility** issues
- **Developer experience** degradation from outdated tooling
- **Build performance** issues from legacy dependencies
- **Maintenance burden** from deprecated packages

### Low Risk
- **Performance** improvements available with newer versions
- **Bundle optimization** opportunities
- **Developer productivity** enhancements from modern tooling

---

## 12. Security Vulnerabilities Summary

### Critical CVEs

| Package | CVE | Severity | Description | Fix Version |
|---------|-----|----------|-------------|-------------|
| axios | CVE-2021-3749 | High | Regular expression denial of service | 1.6.0+ |
| axios | CVE-2020-28168 | High | SSRF vulnerability | 1.6.0+ |
| node-fetch | CVE-2022-0235 | Medium | Exposure of sensitive information | 3.0.0+ |

### Packages in Maintenance Mode

| Package | Last Major Update | Security Status | Action |
|---------|------------------|-----------------|--------|
| moment | 2020 | Limited patches | Replace immediately |
| @babel/polyfill | 2019 | No updates | Replace immediately |

---

*This report was generated on August 4, 2025, based on current dependency analysis and security advisory databases.*
