LOOP ITERATION: Refinement & Bug Fix (Cycle #2)

CURRENT STATE:
The `getMonthlySummary` query completed, but unit test `test_edge_case_timezone_offset` failed.

ERROR TRACE FROM HARNESS:
AssertionError: Expected summary total for October to be $120.00, but got $150.00.
Reason: Expenses created near 00:00 UTC on November 1st are incorrectly aggregated into October due to local UTC conversion mismatch.

FEEDBACK & CORRECTION TASK:
1. PLAN: Identify where UTC timestamps are being converted to local date strings in `expenseRepository.ts`.
2. FIX: Adjust SQL timestamp query parameters to compare boundary timestamps using UTC offset explicitly (`startOfMonthUTC` to `endOfMonthUTC`).
3. CHECK: Rerun the Vitest test suite (`npm test -- -t timezone_offset`).
4. REPEAT: If edge cases persist for leap years or DST shifts, revise the query logic and report the output.