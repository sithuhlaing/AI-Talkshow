EXECUTION HARNESS & VERIFICATION INSTRUCTIONS:

TASK: Implement and verify the `calculateCategoryTotals` utility function.

AUTOMATED CHECKS & HARNESS STEPS:
1. IMPLEMENTATION: Write `calculateCategoryTotals(expenses: Expense[]): Map<string, number>`.
2. UNIT TESTING: Create a companion test file (`calculateCategoryTotals.test.ts`) using Vitest/Jest covering:
   - Valid inputs across multiple categories.
   - Empty expense arrays (should return empty map).
   - Precision handling for floating-point additions (e.g., 0.1 + 0.2).
3. TYPE CHECKING & LINTING: Enforce strict TypeScript compilation without using `any`.

EXECUTION COMMANDS:
Run `npm test` and `npm run lint`. If any test fails or lint rule is violated, analyze the error trace, revise the implementation, and rerun the test suite until all checks pass.

OUTPUT REQUIREMENT:
Show the exact test execution output proving all test cases passed successfully.