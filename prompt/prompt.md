ROLE: Senior Full-Stack Engineer
GOAL: Build an interactive, mobile-responsive Expense Tracker feature in React & SQLite.

TARGET USERS: Individual users tracking monthly household budgets on mobile devices.

FUNCTIONAL REQUIREMENTS:
1. Allow users to add, edit, delete, and categorize expenses (e.g., Food, Transport, Utilities).
2. Display real-time monthly spending totals and category breakdowns.
3. Validate user inputs (flag missing amounts, zero/negative values, or future dates).

CONSTRAINTS:
- Do NOT introduce external UI frameworks (use pure CSS/Tailwind).
- Use local SQLite storage via offline-first hooks; do NOT rely on external web APIs.
- Ensure all input state changes are fully typed in TypeScript.

SUCCESS CRITERIA:
- The form validates invalid inputs before submission and displays inline error messages.
- Total sums update instantly without requiring a full page refresh.