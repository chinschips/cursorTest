## Google Sheets template: employee daily tasks (CSV tabs)

This repo includes a simple Google Sheets template to **track and monitor employees’ daily tasks**.

### Files (import each CSV as its own sheet/tab)

- `templates/Daily Log.csv` (main tracker)
- `templates/Employees.csv` (employee lookup)
- `templates/Lists.csv` (dropdown values for status/priority/category)
- `templates/Summary.csv` (starter summary formulas)

### How to use in Google Sheets

1. Create a new Google Sheet.
2. For each CSV above: **File → Import → Upload → Insert new sheet(s)**.
3. Rename the sheets to exactly:
   - `Daily Log`
   - `Employees`
   - `Lists`
   - `Summary`

### Recommended dropdowns (Data validation)

In `Daily Log`:

- **Employee (col B)**: use `Employees!A2:A`
- **Status (col I)**: filter `Lists` to `Status` values
- **Priority (col H)**: filter `Lists` to `Priority` values
- **Category (col G)**: filter `Lists` to `Category` values
- **Blocked? (col P)**: filter `Lists` to `Blocked?` values

Tip: easiest is to create helper ranges in `Lists` (e.g., a `Status` column) and point validation at that range.

### Summary tab

`Summary.csv` includes ready-to-use `QUERY()` formulas that summarize:
- actual hours by employee
- done / in-progress / blocked task counts by employee

These formulas assume the `Daily Log` sheet name is exactly **Daily Log** and that **Actual Hours** is column **O**.
.
