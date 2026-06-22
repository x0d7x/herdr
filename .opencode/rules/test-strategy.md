---
agentic:
  generated_by: agentic
  source: "areas/software/qa/rules/test-strategy.md"
  repository: "https://github.com/sawrus/agent-guides"
  created_by: "v0.4.0"
  updated_by: "v0.4.0"
---
# Rule: Test Strategy

**Priority**: P0 — Untested code cannot be promoted to production.

1. **Test pyramid proportions**: For every 1 E2E test → ~5 integration tests → ~20 unit tests.
2. **Tests ship with code**: New features and bug fixes include tests in the same PR.
3. **Coverage baselines**: Coverage may not decrease on merge. New code meets minimum threshold (default: 80% for business logic).
4. **No production hotfixes without tests**: Emergency fixes must include a regression test before the fix is considered complete.
5. **Test naming convention**: `[component] [scenario] [expected outcome]`
   - ✅ `"checkout with expired card shows error message"`
   - ❌ `"test_checkout_2"`
