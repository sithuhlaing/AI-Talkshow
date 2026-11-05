CONTEXT & REPOSITORIES:

1. DATABASE SCHEMA (SQLite / Room):
CREATE TABLE expenses (
    id TEXT PRIMARY KEY,
    amount REAL NOT NULL,
    category TEXT NOT NULL,
    created_at INTEGER NOT NULL -- Unix timestamp
);

2. UTILITY HELPERS (`src/utils/formatters.ts`):
export const formatCurrency = (amount: number, currency = 'USD'): string => {
    return new Intl.NumberFormat('en-US', { style: 'currency', currency }).format(amount);
};

3. ARCHITECTURAL CONVENTIONS:
- All data access must go through the repository layer (`src/db/expenseRepository.ts`).
- Never perform database queries directly inside React UI components.
- Follow functional programming patterns and avoid global state mutations.

TASK:
Write the `getMonthlySummary(year: number, month: number)` method inside `expenseRepository.ts` following the schema and formatting helper provided above.