# Security review — 2026-11-14

This is a partial remediation, not a certification that the repository is free of vulnerabilities. Changes remain in a draft pull request pending review.

## starter-code

npm findings before: {"info": 0, "low": 10, "moderate": 106, "high": 67, "critical": 38, "total": 221}. After remediation: {"info": 0, "low": 16, "moderate": 5, "high": 13, "critical": 0, "total": 34}.
Counts refer to dependency findings in this project, including development dependencies. Projects without a committed lockfile were first resolved to create an auditable baseline. Production builds were checked on Node.js 24 with CI=true, npm ci --ignore-scripts --legacy-peer-deps and NODE_OPTIONS=--openssl-legacy-provider for legacy Webpack compatibility; these builds are not browser end-to-end tests.

Production build/test result: `{   "project": "lab-wiki-countries/starter-code",   "manifest_sha256": "60eb4bd25d3ece078eb47a1f6ac3a74c4bef5d676d938f6fc3254f9df2374918",   "lock_sha256": "ad1f5acfc6cec1ed3a71648590d439e2acda0aa0622e852b34555a3b81c6fcf4",   "install_exit": 0,   "build_exit": 0 }`.

### Remaining advisories

- `react-scripts`: moderate; requires dependency migration. 

Do not treat compatible lockfile updates as completion of the framework migrations above.
